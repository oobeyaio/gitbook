---
description: >-
  Install Oobeya On-Premise Edition on a dedicated Linux server or virtual
  machine using Docker Compose.
icon: docker
---

# Oobeya Installation Tutorial & Requirements (Docker)

This deployment model is a good fit for organizations that want to run Oobeya inside infrastructure they control without operating a Kubernetes cluster.

For Kubernetes-based environments, use the [Helm](https://docs.oobeya.io/installations/oobeya-installation-tutorial-helm), [Kubernetes](https://docs.oobeya.io/installations/oobeya-installation-tutorial-kubernetes), or [OpenShift](https://docs.oobeya.io/installations/oobeya-installation-tutorial-openshift) installation guides instead.

***

### **PREREQUISITES**

If you want to run Oobeya on a server (VM, AWS, Azure, GCP, etc.) without any performance issues, you should set the minimum resources as follows:

#### **Minimum Hardware Requirements:**

* 16GB RAM _(The server requires at least 16GB of RAM to run efficiently for enterprises.)_
* 8 CPU / 4 Cores
* 100GB Disk Space

{% hint style="info" %}
For advanced infrastructure sizing guidance, see [Oobeya On-Premise Infrastructure Requirements](https://oobeya.io/on-premise/requirements).

For large enterprise deployments, validate sizing with the Oobeya team before production rollout.
{% endhint %}

#### **Container Runtime**

The Docker installation requires:

* Docker Engine
* Docker Compose

#### Supported External NoSQL Databases

* MongoDB Atlas, Azure CosmosDB, AWS DocumentDB, GCP Firestore, Custom MongoDB Server.

#### **Container Registry Access**

Allow outbound HTTPS access to the required Oobeya container registry:

```
oobeya.azurecr.io
```

If direct outbound registry access is not allowed, organizations can use an approved internal registry mirror or an offline image-transfer process.

{% hint style="info" %}
Coordinate offline or restricted-network installations with the Oobeya team before deployment.
{% endhint %}

#### **Request Oobeya Registry Credentials**

Oobeya application images are distributed through the Oobeya container registry. You will need registry credentials provided by the Oobeya team before starting the installation.

<a href="https://oobeya.io/contact" class="button primary" data-icon="paper-plane-top">Request Your Docker Credentials</a>

***

### **On-Premise Installation Video**

{% embed url="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FKIaYiYhgkesMJ5gtF3LE%2FEDIT-oobeya-installation-video.mp4?alt=media&token=bb3e770e-b742-442f-a354-798d66afede8" %}

### **Installing Oobeya Using Docker Compose**

Follow the steps below for the **quick** and **easy installation** of Oobeya to **work with your data**.

1- **Create** a new working directory.

```
mkdir oobeya
cd oobeya
```

2- **Download** the Oobeya installation package.

```
wget https://oobeya-app.s3.amazonaws.com/oobeya-configs.zip
```

3- **Unzip** the installation package.

```
unzip oobeya-configs.zip
```

4- **Edit&#x20;**_**`env.list`**_ file and enter your domain name or IP address (browse URL) for the following parameters:

{% code title="env.list" %}
```bash
CORS_ALLOWED_ORIGIN=https://oobeya.mycompany.com,http://<server-IP>
OOBEYA_GATEWAY_BASE_URL=https://oobeya.mycompany.com,http://<server-IP>
```
{% endcode %}

5- The mount volume directory uses the `/data-oobeya` directory by default. You can use the `.env` file to change it.

When the application is run, it automatically creates this directory; it is recommended to use a **user with the necessary permissions** to create the directory.

6- You need to log in to pull Oobeya images. **The Oobeya Team will provide Docker login credentials**. [Request your credentials](https://oobeya.io/contact).

```
docker login -u {{user_name}} -p {{password}} oobeya.azurecr.io
```

7- **Run** the application using _`docker-compose`_.

```
docker-compose up -d
```

8- **Navigate** to the Oobeya browse URL to launch the Oobeya registration page. Then, set a new password for the _root user_ of Oobeya.

9\. Log in with the _**root**_ user and explore Oobeya!

{% hint style="success" %}
Now you are ready to connect your data sources with Oobeya to get **complete visibility** of your **software's health**.
{% endhint %}

