---
description: >-
  This guide explains how to install Oobeya on your Kubernetes cluster with
  Helm.
icon: dharmachakra
---

# Oobeya Installation Tutorial (Helm)

To install using the Helm Artifact Repository, you can follow the steps on [ArtifactoryHub](https://artifacthub.io/packages/helm/oobeya/oobeya).

### Contents

* [Minimum Hardware Requirements](./#minimum-hardware-requirements)
* [Install Oobeya Helm Chart](./#install-oobeya-helm-chart)
* [Configure Persistent Volumes](./#configure-persistent-volumes)
* [Configure custom MongoDB without PVC](./#configure-custom-mongodb-without-pvc)
* [Configuration](./#configuration)
* [Installing Oobeya with Helm](./#installing-oobeya-with-helm)

**Warning**: If you are not using Custom MongoDB, a StorageClass and a PVC are required.

#### **Minimum Hardware Requirements:**

* 16GB RAM _(Server requires at least 16GB of RAM to run efficiently for enterprises.)_
* 8 CPU / 4 Core
* 100GB Disk Space

#### Supported External NoSQL Databases

* MongoDB Atlas, Azure CosmosDB, AWS DocumentDB, GCP Firestore, Custom MongoDB Server.

### Install Oobeya Helm Chart

Please create a namespace for Oobeya.

```
kubectl create namespace oobeya
```

Please request a token from the Oobeya team for registry access.

```
kubectl create secret docker-registry oobeya-secret \
     --docker-server=https://oobeya.azurecr.io \
     --docker-username=(Credentials-Name) \
     --docker-password=(Your-Credentials) \
     --namespace=oobeya
```

To install using the Helm Artifact Repository, you can follow the steps on [ArtifactoryHub](https://artifacthub.io/packages/helm/oobeya/oobeya).

You can download the chart package.

```
wget https://oobeya-app.s3.us-east-1.amazonaws.com/oobeya-helm-lts.tar

tar -xvf oobeya-helm-lts.tar && cd oobeya
```

You can push the Oobeya directory to the ArgoCD or Kustomize Git Repository.

### Configure Persistent Volumes

Persistent Volume Claim (PVCs) are defined in the following files:

```
vi (pwd)/values.yaml
```

```
storage:
    mongoStorage:
      pvcName: oobeya-mongo-pvc
      storageClassName: local-path                      # StorageClass Name
      size: 100Gi                                       # Storage Size

    gitwiserStorage:
      enabled: true
      pvcName: oobeya-gitwiser-pvc
      storageClassName: local-path                      # StorageClass Name
      size: 20Gi                                        # Storage Size
```

Edit file to set the correct StorageClass name for your environment.

### Configure custom MongoDB without PVC

If you enable External MongoDB, you will no longer need a Storage Class or a PVC.

Steps required to create a user and database for Oobeya:

```
> use admin
```

```
db.createUser({
  user: "mongodb",                        # Your USERNAME
  pwd: "mongodb",                         # Your PASSWORD
  roles: [
    { role: 'readWrite', db: 'addonsDB' },
    { role: 'readWrite', db: 'admin' },
    { role: 'readWrite', db: 'gatewayDB' },
    { role: 'readWrite', db: 'agilespaceDB' },
    { role: 'readWrite', db: 'config' },
    { role: 'readWrite', db: 'dashboardDB' },
    { role: 'readWrite', db: 'devteamDB' },
    { role: 'readWrite', db: 'gitwiserDB' },
    { role: 'readWrite', db: 'uaaDB' }
  ]
});
```

If you're connecting to your external MongoDB, you'll need to fill in the blanks here:

```
oobeyaExternalMongo:
  isExternal: false                                       # Set true
  host: "oobeya-mongo.oobeya.svc.cluster.local"           # Set your MongoDB domain or IP
  port: "27017"                                           # Set MongoDB Port
  user: ""
  pass: ""
  authSource: "admin"
  databases:
    dashboard: "dashboardDB"
    devteam: "devteamDB"
    gitwiser: "gitwiserDB"
    uaa: "uaaDB"
    agilespace: "agilespaceDB"
    addons: "addonsDB"
    gateway: "gatewayDB"
```

### Configuration

To access Oobeya from the browser, you need to add the domain name or machine IP to the configuration.

```
vi (pwd)/values.yaml
```

* Please edit this:

1. values.yaml.oobeyaDashboard

```
 - corsAllowedOrigin: "http://your-IP-or-Domain"
```

2. values.yaml.oobeyaGateway

```
 - corsAllowedOrigin: "http://your-IP-or-Domain"
 - gatewayBaseOrigin: "http://your-IP-or-Domain"
```

If you're using `Nginx Ingress` for access:

```
ingressNginx:
  enabled: false
  className: "nginx"
  host: "oobeya.local"
```

If you're using `Traefik Ingress`, similar definitions are included in the values.yaml file.

### Installing Oobeya with Helm

```
helm lint .
```

```
helm upgrade --install oobeya . \
  --namespace oobeya
```

If you want to deploy a specific version:

```
helm upgrade --install oobeya . \
  --namespace oobeya \
  --set beVersion=2.0.xxx \
  --set feVersion=2.0.xxx
```
