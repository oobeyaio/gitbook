---
description: Install Oobeya On-Premise Edition Using Openshift.
icon: dharmachakra
---

# Oobeya Installation Tutorial (OpenShift)

**Minimum Hardware Requirements:**

* 16GB RAM _(Server requires at least 16GB of RAM to run efficiently for enterprises.)_
* 8 CPU / 4 Core
* 100GB Disk Space

#### Supported External NoSQL Databases

* MongoDB Atlas, Azure CosmosDB, AWS DocumentDB, GCP Firestore, Custom MongoDB Server.

{% hint style="warning" %}
**Warning**: the setup in this document is possible with `Storage Class`.
{% endhint %}

The `oobeya-ui` service and its `init containers` must be run using a dedicated `Service Account` within the OpenShift environment due to their operational requirements. The necessary security permissions must be assigned to this Service Account. These elevated permissions are restricted solely to the required components, while all other pods continue to operate under the default security policies.

{% hint style="info" %}
**Note**: The Ingress object is used to access the application interface and is specified in the `route.yml` file. You need to change your DNS settings.
{% endhint %}

***

### Installation Steps

* Please switch to the oobeya project.
* If it doesn't exist, please create a namespace for Oobeya.

```
$ oc create namespace oobeya
```

* Request a token from the Oobeya team for registry access.

```
$ oc secret docker-registry oobeya-secret \
      --docker-server=https://oobeya.azurecr.io \
      --docker-username=(Credentials-Name) \
      --docker-password=(Your-Credentials) --namespace=oobeya
```

* You can download the Manifest files.

```
$ wget https://oobeya-app.s3.us-east-1.amazonaws.com/oobeya-oc-install.tar
```

```
$ tar -xvf oobeya-oc-install.tar && cd oobeya
```

### Configuration

* PVCs are given in `oobeya-mongo.yml` Enter the StorageClass name.
* To access Oobeya from the browser, you need to add the domain name or machine IP to the configuration.

```
$ vi (pwd)/configmaps.yml
```

Please edit this:

1. dashboard-configmap

```
CORS_ALLOWED_ORIGIN: "http://your-IP-or-Domain"
```

2. gateway-configmap

```
CORS_ALLOWED_ORIGIN: "http://your-IP-or-Domain"
OOBEYA_GATEWAY_BASE_URL: "http://your-IP-or-Domain"
```

### Deployment

You can run this command.

```
$ oc apply -f .
```

* By default, Oobeya broadcasts on port 80.
* When all services are '1/1 Running,' you can access Oobeya through your browser at 'http://your-IP-or-Domain'.
