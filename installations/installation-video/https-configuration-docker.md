---
icon: expeditedssl
layout:
  width: default
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
  tags:
    visible: true
  actions:
    visible: true
---

# HTTPS Configuration For Docker Installations

1- Copy the SSL Key and SSL Crt pair to the "nginx" folder under the OOBEYA-DIRECTORY directory by changing their names to ssl.key and ssl.crt.

```bash
$ mv example.key /OOBEYA-DIRECTORY/nginx/ssl.key
$ mv example.crt /OOBEYA-DIRECTORY/nginx/ssl.crt
```

2- In the 'server\_name' section, write your domain for both port 80 and port 443.

* /OOBEYA-DIRECTORY/nginx/nginx.conf

```json
  server {
    listen       80;
    listen       [::]:80;
    server_name  ops.oobeya.io;                         # YOUR DOMAIN
    access_log /var/log/nginx/access.log compression;
```

```json
  server { # This new server will watch for traffic on 443
        listen              443 ssl;
        server_name         ops.oobeya.io;              # YOUR DOMAIN
        ssl_certificate     /etc/nginx/ssl.crt;
        ssl_certificate_key /etc/nginx/ssl.key;
```

3- Remove the comment lines under the Nginx service in docker-compose.yml.

* /OOBEYA-DIRECTORY/docker-compose.yml

```yaml
  oobeya-nginx:
    image: "oobeya.azurecr.io/oobeya-nginx-gateway:latest"
    restart: "always"
    ports:
      - "80:80"
#      - "443:443"
    container_name: "oobeya-nginx"
#    volumes:
#      - ./nginx/nginx.conf:/etc/nginx/nginx.conf
#      - ./nginx/ssl.crt:/etc/nginx/ssl.crt
#      - ./nginx/ssl.key:/etc/nginx/ssl.key
```

4- Add "https://your-domain" to the CORS\_ALLOWED\_ORIGIN variable to be accessed with HTTPS.

```bash
$ vi /OOBEYA-DIRECTORY/env.list

CORS_ALLOWED_ORIGIN=https://your-domain
```

5- Finally, you can restart the Oobeya app using docker-compose.

```bash
$ docker-compose down && docker-compose up -d
```
