---
description: Install Oobeya On-Premise Edition Using Docker Compose
icon: docker
---

# Oobeya Installation Tutorial & Requirements (Docker)

### **PREREQUISITES**

If you want to run Oobeya on a server (VM, AWS, Azure, GCP, etc.) without any performance issues, you should set the minimum resources as below:

#### **Minimum Hardware Requirements:**

* 16GB RAM _(Server requires at least 16GB of RAM to run efficiently for enterprises.)_
* 8 CPU / 4 Core
* 100GB Disk Space

#### **Required Applications:**

* Docker
* docker-compose

#### Supported External NoSQL Databases

* MongoDB Atlas, Azure CosmosDB, AWS DocumentDB, GCP Firestore, Custom MongoDB Server.

#### **Access Requirements:**

* Access to Docker Hub.
* Access to Azure Container Registry (ACR): https://oobeya.azurecr.io
* Docker login credentials for ACR access (provided by the Oobeya Team).

<p align="center"><a href="https://oobeya.io/contact" class="button primary">Request Your Docker Credentials</a></p>

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

8- **Navigate** to the Oobeya browse URL to launch the Oobeya registration page. Then, set a new password for the _root user_ of the Oobeya.

9\. Log in with the _**root**_ user and explore Oobeya!

{% hint style="success" %}
Now you are ready to connect your data sources with Oobeya to get **complete visibility** of your **software's health**.
{% endhint %}

