---
description: Install Oobeya On-Premise Edition Using Kubernetes.
icon: dharmachakra
---

# Oobeya Installation Tutorial (Kubernetes)

This guide explains how to install **Oobeya** on your Kubernetes cluster.

#### **Minimum Hardware Requirements:**

* 16GB RAM _(Server requires at least 16GB of RAM to run efficiently for enterprises.)_
* 8 CPU / 4 Core
* 100GB Disk Space

#### Supported External NoSQL Databases

* MongoDB Atlas, Azure CosmosDB, AWS DocumentDB, GCP Firestore, Custom MongoDB Server.

{% hint style="warning" %}
**Warning**: Installation requires a valid StorageClass.&#x20;

Before you begin, please ensure that your cluster has a configured **StorageClass**, as persistent volumes are required.
{% endhint %}

{% hint style="info" %}
**Note**: Oobeya uses an Ingress object to expose the application interface. The default configuration is provided in `ingresses.yml`. If you are using **Traefik**, you can use `traefik-route.yml` instead.
{% endhint %}

***

Follow the steps below for the **quick** and **easy installation** of Oobeya to **work with your data**.

### 1. Create a Namespace

Create a dedicated namespace for Oobeya:

```bash
kubectl create namespace oobeya
```

***

### 2. Request Access Credentials

You will need a registry access token from the Oobeya team. Once received, create a Kubernetes secret:

```bash
kubectl create secret docker-registry oobeya-secret \
  --docker-server=https://oobeya.azurecr.io \
  --docker-username=<CREDENTIALS-NAME> \
  --docker-password=<YOUR-CREDENTIALS> \
  --namespace=oobeya
```

***

### 3. Download Manifest Files

Download and extract the Oobeya installation manifests:

```bash
wget https://oobeya-app.s3.us-east-1.amazonaws.com/oobeya-cluster-install.tar
tar -xvf oobeya-cluster-install.tar && cd oobeya
```

***

### 4. Configure Persistent Volumes

Persistent Volume Claims (PVCs) are defined in the following files:

* `oobeya-mongo.yml` and `oobeya-rabbitmq.yml`     &#x20;

Edit each file to set the correct **StorageClass** name for your environment.

***

### 5. Configure Domain or IP

To access Oobeya in a browser, configure your **domain name** or **machine IP**.

Edit the `configmaps.yml` file:

```bash
vi $(pwd)/configmaps.yml
```

Update the following fields:

**1. dashboard-configmap**

```yaml
CORS_ALLOWED_ORIGIN: "http://your-IP-or-Domain"
```

**2. gateway-configmap**

```yaml
CORS_ALLOWED_ORIGIN: "http://your-IP-or-Domain"
OOBEYA_GATEWAY_BASE_URL: "http://your-IP-or-Domain"
```

***

### 6. Deploy Oobeya

Apply all manifests to your Kubernetes cluster:

```bash
kubectl apply -f .
```

***

### 7. Access Oobeya

* By default, Oobeya runs on **port 80**.
* Once all services show `1/1 Running`, you can access the Oobeya interface from your browser at:

```
http://your-IP-or-Domain
```

***

### **Next Steps**

After installation, you can proceed with:

* Creating the first user
* [Entering the License Key](../../administration/license-management/)
* [Connecting Integrations](../../integrations/all-integrations/)
