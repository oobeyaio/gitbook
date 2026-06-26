---
icon: dharmachakra
---

# Oobeya Version Upgrade for Helm Installations

### Access Requirements

Access to Azure Container Registry (ACR)

Docker login credentials for ACR access (provided by the Oobeya Team if you don't have one)

### Upgrading Oobeya version

Follow the steps below for the quick and easy version upgrade of Oobeya.

1- List the pods under the oobeya namespace.

```
kubectl get pods -n oobeya
```

It is given as `imagePullPolicy: Always` in the deployment.yml manifest files.

`oobeya-mongo` and `oobeya-rabbitmq` are static pods. They do not need to receive updates.

### Set new versions

If you are proceeding with the static version:

```
helm upgrade --install oobeya . \
  --namespace oobeya \
  --set beVersion=2.0.xxx \
  --set feVersion=2.0.xxx
```

***

If you are proceeding with the latest strategy:

$ vi values.yaml

```
uiVersion: latest
beVersion: latest
```

Without changing anything:

Deployments should be restarted as a rollout restart.

**Deployments List:**

* `oobeya-dashboard`
* `oobeya-uaa`

After those services are up and running:

* `oobeya-agilespace`
* `oobeya-addons`
* `oobeya-devteam`
* `oobeya-gateway`
* `oobeya-gitwiser`
* `oobeya-ui`

2- Run the update command with the deployment name

```
kubectl rollout restart deployment <deployment-name> -n oobeya
```

3- Check the condition of the pods again

```
kubectl get pods -n oobeya
```
