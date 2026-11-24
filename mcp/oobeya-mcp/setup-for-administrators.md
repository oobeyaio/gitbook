---
description: >-
  Configuration guide for system administrators: what the Oobeya MCP server is,
  the network and reverse proxy requirements, how to verify the setup, and how
  access is controlled.
---

# Setup for Administrators

The Oobeya MCP server lets AI tools such as Claude Code, Cursor, VS Code and GitHub Copilot read and manage Oobeya through the Model Context Protocol (MCP). It is part of the Oobeya platform service, so there is nothing extra to install. Every user signs in with their own Oobeya account, and every request runs with that user's Oobeya permissions.

{% hint style="info" %}
Available from **Oobeya 2.1.0** (backend and UI). For the end-user guide, see [Using Oobeya from Your AI Tool](using-oobeya-from-your-ai-tool.md).
{% endhint %}

## How It Works

```
AI tool (user's computer) ──HTTPS──▶ https://<your-oobeya-address>/mcp ──▶ Oobeya platform service
```

* The AI tool runs on the user's computer and connects to `https://<your-oobeya-address>/mcp`.
* On the first connection the tool opens the Oobeya sign-in screen in the user's browser. The user signs in with their usual method (local account, LDAP or SSO) and approves the connection on a consent screen.
* The tool then calls Oobeya with a token that belongs to that user. Oobeya answers every call with that user's permissions.
* Sign-in uses OAuth 2.1 (authorization code with PKCE). The tool registers itself with Oobeya automatically; there is no client ID or secret to create.

Oobeya does not connect to any AI service. The AI tool is the client: it asks Oobeya for data, and it sends the answers to its own model provider. Review your organization's agreement with that provider before you roll the MCP server out.

## 1. Prerequisites

* **Oobeya version:** 2.1.0 or later, for both the backend and the UI. The consent screen is part of the UI, so both must be upgraded together.
* **HTTPS:** Oobeya must be served over HTTPS. AI tools refuse to connect to a remote MCP server over plain HTTP.
* **Reverse proxy access:** you can change the nginx, ingress or Apache configuration in front of Oobeya.

Network access:

| From                               | To                  | Port | Required                                        |
| ---------------------------------- | ------------------- | ---- | ----------------------------------------------- |
| User computers running the AI tool | Your Oobeya address | 443  | Yes                                             |
| Oobeya server                      | The internet        | -    | No; Oobeya makes no outbound connection for MCP |

The AI tool connects from the user's computer, so the MCP server also works when Oobeya is not reachable from the internet.

## 2. Route the MCP Paths

Add four paths to the reverse proxy in front of Oobeya. All four go to the Oobeya platform service (port 8080), the same service that serves `/api`.

| Path                                      | Match  | Purpose                                             |
| ----------------------------------------- | ------ | --------------------------------------------------- |
| `/mcp`                                    | Exact  | The MCP server                                      |
| `/.well-known/oauth-protected-resource`   | Prefix | Tells the AI tool where to sign in                  |
| `/.well-known/oauth-authorization-server` | Prefix | Lists the sign-in, token and registration addresses |
| `/oauth2/`                                | Prefix | Sign-in, token and tool registration                |

These paths are defined by the MCP and OAuth standards, and AI tools look for them at the root of your Oobeya address. Without these rules the requests fall through to the Oobeya UI and the tool cannot connect.

Requirements for these paths:

* Forward the `Host`, `X-Forwarded-Proto` and `X-Forwarded-Host` headers, and `X-Forwarded-Port` when HTTPS is not on port 443. Oobeya builds the addresses it gives to the AI tool from these headers.
* For `/mcp`, turn response buffering off and allow a read timeout of at least 120 seconds.

{% hint style="info" %}
The `nginx.conf` and ingress manifests that ship with Oobeya already contain these rules. If you maintain your own proxy configuration, add them as shown below.
{% endhint %}

{% hint style="info" %}
You can find the whole configuration files below:\
[Docker](https://oobeya-app.s3.amazonaws.com/oobeya-configs.zip)\
[Helm](https://oobeya-app.s3.us-east-1.amazonaws.com/oobeya-helm-lts.tar)
{% endhint %}

{% tabs %}
{% tab title="nginx" %}
Add the four blocks inside your `server { ... }` block. `oobeya-api` is the upstream of the Oobeya platform service.

```nginx
location = /mcp {
    set $target_api "oobeya-dashboard";

    proxy_pass http://$target_api:8080;
    proxy_redirect     off;
    proxy_http_version 1.1;
    proxy_buffering    off;
    proxy_read_timeout 300s;

    proxy_set_header   Host $host;
    proxy_set_header   X-Real-IP $remote_addr;
    proxy_set_header   X-Forwarded-For $proxy_add_x_forwarded_for;
    proxy_set_header   X-Forwarded-Host $host;
    proxy_set_header   X-Forwarded-Proto https;
    proxy_set_header   X-Forwarded-Port 443;
    proxy_set_header   X-Forwarded-Scheme https;
}

location /.well-known/oauth-protected-resource {
    set $target_api "oobeya-dashboard";

    proxy_pass http://$target_api:8080;
    proxy_redirect     off;

    proxy_set_header   Host $host;
    proxy_set_header   X-Real-IP $remote_addr;
    proxy_set_header   X-Forwarded-For $proxy_add_x_forwarded_for;
    proxy_set_header   X-Forwarded-Host $host;
    proxy_set_header   X-Forwarded-Proto https;
    proxy_set_header   X-Forwarded-Port 443;
    proxy_set_header   X-Forwarded-Scheme https;
}

location /.well-known/oauth-authorization-server {
    set $target_api "oobeya-dashboard";

    proxy_pass http://$target_api:8080;
    proxy_redirect     off;

    proxy_set_header   Host $host;
    proxy_set_header   X-Real-IP $remote_addr;
    proxy_set_header   X-Forwarded-For $proxy_add_x_forwarded_for;
    proxy_set_header   X-Forwarded-Host $host;
    proxy_set_header   X-Forwarded-Proto https;
    proxy_set_header   X-Forwarded-Port 443;
    proxy_set_header   X-Forwarded-Scheme https;
}

location /oauth2/ {
    set $target_api "oobeya-dashboard";

    proxy_pass http://$target_api:8080;
    proxy_redirect     off;

    proxy_set_header   Host $host;
    proxy_set_header   X-Real-IP $remote_addr;
    proxy_set_header   X-Forwarded-For $proxy_add_x_forwarded_for;
    proxy_set_header   X-Forwarded-Host $host;
    proxy_set_header   X-Forwarded-Proto https;
    proxy_set_header   X-Forwarded-Port 443;
    proxy_set_header   X-Forwarded-Scheme https;
}
```

{% hint style="warning" %}
If your other `location` blocks set security headers with `add_header`, repeat them in these blocks. nginx does not inherit `add_header` lines from the `server` level into a `location` that has its own.
{% endhint %}
{% endtab %}

{% tab title="Kubernetes ingress" %}
Add the four paths to the ingress of the platform service. With ingress-nginx the forwarded headers are set for you; raise the read timeout, because the default is 60 seconds.

```yaml
apiVersion: networking.k8s.io/v1
kind: Ingress
metadata:
  name: qa-dashboard-platform
  annotations:
    kubernetes.io/ingress.class: nginx
    nginx.ingress.kubernetes.io/proxy-read-timeout: "300"
    nginx.ingress.kubernetes.io/proxy-buffering: "off"
spec:
  rules:
  - http:
      paths:
      - path: /api
        pathType: Prefix
        backend:
          service:
            name: qa-dashboard-platform
            port:
              number: 8080
      - path: /mcp
        pathType: Exact
        backend:
          service:
            name: qa-dashboard-platform
            port:
              number: 8080
      - path: /.well-known/oauth-protected-resource
        pathType: Prefix
        backend:
          service:
            name: qa-dashboard-platform
            port:
              number: 8080
      - path: /.well-known/oauth-authorization-server
        pathType: Prefix
        backend:
          service:
            name: qa-dashboard-platform
            port:
              number: 8080
      - path: /oauth2
        pathType: Prefix
        backend:
          service:
            name: qa-dashboard-platform
            port:
              number: 8080
```
{% endtab %}

{% tab title="Apache" %}
```apache
ProxyPreserveHost on
ProxyTimeout 300
RequestHeader set X-Forwarded-Proto "https"

ProxyPass         /mcp  http://<platform-host>:8080/mcp  Keepalive=On
ProxyPassReverse  /mcp  http://<platform-host>:8080/mcp  Keepalive=On
ProxyPass         /.well-known/oauth-protected-resource  http://<platform-host>:8080/.well-known/oauth-protected-resource
ProxyPass         /.well-known/oauth-authorization-server  http://<platform-host>:8080/.well-known/oauth-authorization-server
ProxyPass         /oauth2  http://<platform-host>:8080/oauth2  Keepalive=On
ProxyPassReverse  /oauth2  http://<platform-host>:8080/oauth2  Keepalive=On
```
{% endtab %}
{% endtabs %}

## 3. Optional Settings

The MCP server works with the default settings. Change these environment variables only when you need to.

| Variable                                           | Service  | Default             | Purpose                                                                                                                        |
| -------------------------------------------------- | -------- | ------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| `OOBEYA_MCP_ENABLED`                               | Platform | `true`              | Turns the MCP server on or off                                                                                                 |
| `OOBEYA_MCP_REQUEST_TIMEOUT`                       | Platform | `120s`              | Time limit of a single MCP request                                                                                             |
| `PLATFORM_SERVER_URL`                              | Platform | empty               | The public address of Oobeya. When empty, Oobeya uses the server address saved in its settings, and then the forwarded headers |
| `UAA_PUBLIC_CLIENT_TOKEN_VALIDITY_SECONDS`         | UAA      | `3600`              | Lifetime of an AI tool's access token                                                                                          |
| `UAA_PUBLIC_CLIENT_REFRESH_TOKEN_VALIDITY_SECONDS` | UAA      | `2592000` (30 days) | How long an AI tool stays connected without a new sign-in                                                                      |

## 4. Verify the Setup

Run the four requests below against your Oobeya address. All four must answer with JSON.

```bash
curl -s https://<your-oobeya-address>/.well-known/oauth-protected-resource
curl -s https://<your-oobeya-address>/.well-known/oauth-authorization-server
curl -s https://<your-oobeya-address>/oauth2/jwks
curl -s -i https://<your-oobeya-address>/mcp
```

| Request                                   | Expected answer                                                                                     |
| ----------------------------------------- | --------------------------------------------------------------------------------------------------- |
| `/.well-known/oauth-protected-resource`   | `200`, JSON with `"resource": "https://<your-oobeya-address>/mcp"`                                  |
| `/.well-known/oauth-authorization-server` | `200`, JSON with `"issuer": "https://<your-oobeya-address>"`                                        |
| `/oauth2/jwks`                            | `200`, JSON with a `keys` list                                                                      |
| `/mcp`                                    | `401`, JSON, and a `WWW-Authenticate` header that points to `/.well-known/oauth-protected-resource` |

{% hint style="info" %}
A request that returns an HTML page instead of JSON is not routed: it reached the Oobeya UI. Check the rule of that path in step 2.
{% endhint %}

If the JSON contains addresses that start with `http://` or with an internal host name, the forwarded headers are missing. Fix the headers, or set `PLATFORM_SERVER_URL` to your public address.

As a final check, connect with an AI tool as described in the user guide.

## 5. Roll Out to Your Users

Users connect by themselves; there is nothing to distribute.

1. Each user opens **Profile → AI access (MCP)** in Oobeya. The tab shows the MCP address of your installation and the setup steps for each supported AI tool: Claude Code, Codex, Cursor, VS Code, Devin (Windsurf), GitHub Copilot, Gemini CLI, Grok Build and OpenCode.
2. The user adds the address to their AI tool and signs in on the Oobeya screen that opens.

The Oobeya home page also shows a **Connect your AI tool (MCP)** card that leads to the same steps. Share the user guide with your teams.

## 6. Manage Access

* **Permissions:** an AI tool can do exactly what its user can do in Oobeya. Roles, team membership and team lead rights apply to every request. There is no separate MCP role.
* **Connected apps:** each user sees the AI tools connected to their account under **Profile → AI access (MCP) → Connected apps**, with the connection date and the last use, and can remove one with **Revoke access**. The tool loses access within a minute.
* **Session length:** an AI tool stays connected for up to 30 days. After that the user signs in again.
* **Turn the MCP server off:** set `OOBEYA_MCP_ENABLED=false` on the platform service and restart it. The profile tab then tells users that the MCP server is turned off.

## 7. Data and Privacy

* Oobeya returns only data that the signed-in user is allowed to see.
* Oobeya receives the tool calls, not the conversation. The user's prompts and the AI tool's answers stay between the tool and its model provider.
* The data Oobeya returns is sent by the AI tool to its model provider. Which provider that is, and how it handles the data, depends on the AI tool and on your organization's agreement with the provider.
* Passwords, tokens and certificates never pass through the AI tool. A task that needs a secret, such as connecting a new integration, answers with a link to the Oobeya screen where the user enters it.
* Changes are made only after the user approves the tool call in their AI tool. Deletions also require an explicit confirmation.

## 8. Limitations

* Only AI tools that run on the user's computer are supported. Cloud connectors, which call Oobeya from the provider's servers, need an Oobeya address that is reachable from the internet and are not covered here.
* A report for a very large team or a long period can take longer than the AI tool waits. In that case Oobeya answers that the report is still being calculated, and the user asks again after about a minute.

## 9. Troubleshooting

| Symptom                                                            | Likely cause                                       | What to do                                                                       |
| ------------------------------------------------------------------ | -------------------------------------------------- | -------------------------------------------------------------------------------- |
| The AI tool cannot connect, or reports an invalid response         | A path from step 2 is not routed                   | Run the checks in step 4; a path that returns HTML is missing its rule           |
| The sign-in screen opens on a wrong or internal address            | Forwarded headers are missing                      | Forward `X-Forwarded-Proto` and `X-Forwarded-Host`, or set `PLATFORM_SERVER_URL` |
| The browser shows a blank or "not found" page after sign-in starts | The UI version does not include the consent screen | Upgrade the UI together with the backend                                         |
| The profile tab says the MCP server is turned off                  | `OOBEYA_MCP_ENABLED` is `false`                    | Set it to `true` and restart the platform service                                |
| Requests end with a gateway timeout                                | The proxy read timeout is too short                | Allow at least 120 seconds for `/mcp`                                            |
| A user gets a "forbidden" answer                                   | The user lacks the Oobeya permission               | Grant the role or team membership in Oobeya, as for the UI                       |

## FAQ

**Do users need a separate account or license for MCP?** No. Users sign in with their existing Oobeya account.

**Can an AI tool see more than its user?** No. Every request runs with the permissions of the user who connected the tool.

**Does Oobeya send our data to an AI provider?** No. Oobeya only answers requests from the AI tool. The tool sends the answers to its own model provider.

**Do we have to open Oobeya to the internet?** No. The supported AI tools connect from the user's computer, inside your network or over your VPN.

**How do we stop a single tool or user?** The user removes the tool under Connected apps. To stop MCP for everyone, turn the MCP server off as described in step 6.

## Next Steps

* Share the user guide, [Using Oobeya from Your AI Tool (MCP)](using-oobeya-from-your-ai-tool.md), with your teams.
* Review the roles and team leads in Oobeya, because they decide what each user can read and change through MCP.
