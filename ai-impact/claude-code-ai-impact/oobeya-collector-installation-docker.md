---
description: >-
  Install the Oobeya Collector next to an Oobeya Docker installation to receive
  Claude Code OpenTelemetry data.
---

# Oobeya Collector Installation (Docker)

The **Oobeya Collector** receives the OpenTelemetry data that Claude Code sends from your developers' machines and hands it to Oobeya. It is needed only for the [Claude Code integration](./); install it if your organization uses Claude Code.

The collector runs from its own Docker Compose file, separate from the Oobeya services. It keeps accepting data while Oobeya is being upgraded or restarted, and the data waits in Oobeya's RabbitMQ until Oobeya processes it.

***

### How It Works

```
Claude Code ──HTTP──▶ Oobeya Collector :8097 ──▶ RabbitMQ ──▶ Oobeya
                              │
                              └── :58097 management (internal only)
```

| Port      | Purpose                                                                                      | Reachable from                                                     |
| --------- | -------------------------------------------------------------------------------------------- | ------------------------------------------------------------------ |
| **8097**  | Receives Claude Code data at `/claude/v1/metrics` and `/claude/v1/logs`                      | Developer machines                                                 |
| **58097** | Management: health, status shown in Oobeya, log download, reprocessing of set-aside messages | The Oobeya server only. **Never expose it to developer networks.** |

The collector does not open or interpret the data. For every request it checks the path, the content type, the size (up to 8 MB), the ingest token and a rate limit, writes the request to RabbitMQ, and answers Claude Code only after RabbitMQ has confirmed it. It learns which ingest tokens are valid from the Oobeya gateway, refreshes that list every minute, and keeps working with the last list it received if the gateway is unavailable.

***

### 1. Prerequisites

* An Oobeya Docker installation in which **MongoDB and RabbitMQ run from `docker-compose.infra.yml`**, separate from `docker-compose.yml`. The collector joins the `oobeya-network` network that this file creates.
* Network access from every network your developers work from (office, VPN, remote) to port `8097` of the collector host.
* Access to the Oobeya container registry (`oobeya.azurecr.io`), as for the other Oobeya images.
* Resources: about 1 GB of memory for the collector container. The Claude Code queue in RabbitMQ can grow up to 2 GB by default while Oobeya is not processing it, so keep that much free disk space on the RabbitMQ volume.

{% hint style="info" %}
For Helm, Kubernetes and OpenShift installations, contact the Oobeya team.
{% endhint %}

***

### 2. Start MongoDB and RabbitMQ

In the Oobeya installation directory, make sure the infrastructure services are running. This also creates the shared `oobeya-network` network:

```bash
docker compose -f docker-compose.infra.yml up -d
```

***

### 3. Configure the Collector

Edit `collector.env` in the Oobeya installation directory:

{% code title="collector.env" %}
```bash
# Image tag and the host port developers reach
OOBEYA_COLLECTOR_TAG=latest
OOBEYA_COLLECTOR_HOST_PORT=8097

# Host address of the management port. Keep 127.0.0.1 when Oobeya runs on this host;
# otherwise use the private IP the Oobeya host reaches.
OOBEYA_COLLECTOR_MANAGEMENT_BIND=127.0.0.1

# Oobeya's RabbitMQ, with the user the Oobeya services use
# (RABBITMQ_DEFAULT_USER / RABBITMQ_DEFAULT_PASS in env.list)
RABBITMQ_HOST=oobeya-rabbitmq
RABBITMQ_PORT=5672
RABBITMQ_USERNAME=<rabbitmq-user>
RABBITMQ_PASSWORD=<rabbitmq-password>

# Oobeya gateway, as reached from the collector container
OOBEYA_GATEWAY_INTERNAL_URL=http://oobeya-gateway:8099
```
{% endcode %}

If the collector runs on a different host than Oobeya, set `RABBITMQ_HOST` to the Oobeya host and `OOBEYA_GATEWAY_INTERNAL_URL` to `http://<oobeya-host>:8099`.

See the [configuration reference](oobeya-collector-installation-docker.md#configuration-reference) for all variables.

***

### 4. Connect Oobeya to the Collector

Edit `env.list` and uncomment the Claude Code section:

{% code title="env.list" %}
```bash
OOBEYA_GATEWAY_INTERNAL_URL=http://oobeya-gateway:8099
OOBEYA_COLLECTOR_INTERNAL_URL=http://oobeya-collector:58097
OOBEYA_COLLECTOR_PUBLIC_URL=http://<collector-host>:8097
```
{% endcode %}

| Variable                        | Purpose                                                                                                                                                                                                                                              |
| ------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `OOBEYA_GATEWAY_INTERNAL_URL`   | Lets Oobeya verify ingest tokens when a Claude Code data source is tested.                                                                                                                                                                           |
| `OOBEYA_COLLECTOR_INTERNAL_URL` | The collector's management port. Oobeya reads the Claude Code queue only while this is set, and shows the collector status and logs from it. If the collector runs on another host, use `http://<collector-host>:58097`.                             |
| `OOBEYA_COLLECTOR_PUBLIC_URL`   | The address developers' machines reach. Oobeya puts it into the Claude Code settings it generates. If you use a [load balancer](oobeya-collector-installation-docker.md#recommended-https-with-a-load-balancer), set its HTTPS address here instead. |

Recreate the addons service so it picks up the new variables:

```bash
docker compose up -d --force-recreate oobeya-addons
```

***

### 5. Start the Collector

```bash
docker compose -f docker-compose.collector.yml --env-file collector.env up -d
```

***

### 6. Verify the Installation

On the collector host, check that the collector is ready. It is ready once it is connected to RabbitMQ and has received the token list from the Oobeya gateway:

```bash
curl http://127.0.0.1:58097/actuator/health/readiness
```

Expected result: a JSON response that starts with `{"status":"UP"`. If it shows `DOWN` or `OUT_OF_SERVICE`, the response lists which check failed: `rabbit` (RabbitMQ connection) or `allowList` (token list from the Oobeya gateway).

From a developer machine, check that the collector is reachable:

```bash
curl -i -X POST http://<collector-host>:8097/claude/v1/metrics -H "Content-Type: application/x-protobuf"
```

Expected result: `HTTP/1.1 401`. The collector is reachable, and it rejected this test request only because it carries no token.

Then continue with the [Claude Code integration](./). The collector status also appears in Oobeya under the Claude Code data source → **Data status and Claude Code settings**.

***

### Recommended: HTTPS with a Load Balancer

The collector itself serves plain HTTP. Without HTTPS, the ingest token and the usage data travel unencrypted between your developers' machines and the collector. We recommend putting the collector behind your load balancer or reverse proxy with a DNS name and a TLS certificate, for example `https://oobeya-collector.mycompany.com`.

1. Forward `https://oobeya-collector.mycompany.com/claude/` to port `8097` of the collector host, keeping the path unchanged.
2. Allow request bodies of at least **8 MB**.
3. Set `OOBEYA_COLLECTOR_PUBLIC_URL=https://oobeya-collector.mycompany.com` in `env.list` and recreate the addons service, so the Claude Code settings Oobeya generates point to the HTTPS address.
4. If developers already use the settings with the HTTP address, distribute the new settings.

Example for NGINX:

{% code title="nginx.conf" %}
```nginx
server {
    listen              443 ssl;
    server_name         oobeya-collector.mycompany.com;
    ssl_certificate     /etc/nginx/collector.crt;
    ssl_certificate_key /etc/nginx/collector.key;

    location /claude/ {
        client_max_body_size 8m;
        proxy_pass http://<collector-host>:8097;
    }
}
```
{% endcode %}

{% hint style="warning" %}
Forward only `/claude/` to the collector. Do not expose port `58097`, RabbitMQ (`5672`, `15672`) or the Oobeya gateway port (`8099`) through the load balancer.
{% endhint %}

***

### Upgrades

* **Upgrading Oobeya** does not stop the collector or RabbitMQ. Claude Code data keeps arriving and is processed once the Oobeya services are back. Update the Oobeya services with `docker-compose.yml` only; leave `docker-compose.infra.yml` and `docker-compose.collector.yml` running.
* **Upgrading the collector:** set `OOBEYA_COLLECTOR_TAG` in `collector.env` and run the start command again. The collector stops gracefully; data accepted before the restart is already in RabbitMQ. While it restarts, Claude Code retries for a few seconds; a longer interruption loses the events sent in that period.

***

### Operations

**Logs.** Download them in Oobeya under **Admin → General Settings → System Logs → Oobeya Collector**, or on the host:

```bash
docker logs oobeya-collector
```

**Set-aside messages.** A message Oobeya cannot process is moved to a dead-letter queue and kept for 7 days, so it does not block the others. After the cause is fixed, move these messages back to the queue for processing:

```bash
curl -X POST http://127.0.0.1:58097/actuator/deadletters
```

**Scaling.** The collector keeps no data of its own. One instance is enough for most organizations; the rate limits below apply per instance.

***

### Configuration Reference

| Variable                                  | Default                      | Description                                                                                                                                            |
| ----------------------------------------- | ---------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `OOBEYA_COLLECTOR_TAG`                    | `latest`                     | Image tag of `oobeya.azurecr.io/oobeya-collector`.                                                                                                     |
| `OOBEYA_COLLECTOR_HOST_PORT`              | `8097`                       | Host port developers (or your load balancer) reach.                                                                                                    |
| `OOBEYA_COLLECTOR_MANAGEMENT_BIND`        | `127.0.0.1`                  | Host address the management port `58097` is published on.                                                                                              |
| `RABBITMQ_HOST` / `RABBITMQ_PORT`         | `oobeya-rabbitmq` / `5672`   | Oobeya's RabbitMQ.                                                                                                                                     |
| `RABBITMQ_USERNAME` / `RABBITMQ_PASSWORD` | —                            | The RabbitMQ user of the Oobeya services.                                                                                                              |
| `OOBEYA_GATEWAY_INTERNAL_URL`             | `http://oobeya-gateway:8099` | Oobeya gateway, the source of the valid ingest tokens.                                                                                                 |
| `OOBEYA_COLLECTOR_QUEUE_MAX_BYTES`        | `2147483648` (2 GB)          | Maximum size of the Claude Code queue. When it is full, the collector answers `503`. Applied when the queue is first created.                          |
| `OOBEYA_COLLECTOR_DEAD_RETENTION`         | `7d`                         | How long set-aside messages are kept.                                                                                                                  |
| `OOBEYA_COLLECTOR_RATE_LIMIT_PER_TOKEN`   | `3000`                       | Requests per minute per ingest token. All developers of a data source share one token; an open Claude Code session sends about one request per minute. |
| `OOBEYA_COLLECTOR_RATE_LIMIT_GLOBAL`      | `10000`                      | Requests per minute for all tokens together.                                                                                                           |
| `OOBEYA_COLLECTOR_RETRY_AFTER_SECONDS`    | `0`                          | `Retry-After` value on `429` and `503`. `0` sends none and lets Claude Code use its own retry timing.                                                  |
| `JAVA_OPTS`                               | `-Xms128m -Xmx512m`          | JVM memory settings.                                                                                                                                   |
| `SSL_ENABLED` / `SSL_CERT_FILE_NAMES`     | `false` / —                  | Company CA certificates for the collector's calls to Oobeya, as in the other Oobeya services.                                                          |
| `OOBEYA_COLLECTOR_LOGGING_LEVEL`          | `INFO`                       | Log level.                                                                                                                                             |

Restart the collector after changing a variable.

#### Responses to Claude Code

| Status | When                                                                     | Claude Code retries |
| ------ | ------------------------------------------------------------------------ | ------------------- |
| `200`  | The data is stored in RabbitMQ.                                          | —                   |
| `401`  | The ingest token is missing, unknown, revoked or expired.                | No                  |
| `404`  | The path is not `/claude/v1/metrics` or `/claude/v1/logs`.               | No                  |
| `413`  | The request is larger than 8 MB.                                         | No                  |
| `415`  | The content type or encoding is not supported.                           | No                  |
| `429`  | A rate limit was reached.                                                | Yes                 |
| `503`  | The collector has no token list yet, or RabbitMQ is unreachable or full. | Yes                 |
