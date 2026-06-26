---
icon: docker
---

# Oobeya Version Upgrade For the docker-compose Installations

## **Access Requirements**

* Access to [Azure Container Registry (ACR)](https://oobeya.azurecr.io)
* Docker login credentials for ACR access (provided by the Oobeya Team if you don't have one).

***

## **Upgrading Oobeya version**&#x20;

Follow the steps below for the **quick** and **easy version upgrade** of Oobeya.

1- Navigate to the directory where the docker-compose file is located.

2- Pull the latest Oobeya docker images by running the below command.

```
docker-compose pull
```

3- Restart the application using the docker-compose command below.

```
docker-compose down && docker-compose up -d
```
