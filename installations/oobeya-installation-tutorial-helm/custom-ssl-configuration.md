---
description: Add Custom SSL with Helm files
icon: lock
---

# Custom SSL Configuration

### Add new secret object

```
$ vi example-ssl-secret.yml
```

If necessary, you can add multiple SSL files as follows.

```
apiVersion: v1
kind: Secret
metadata:
  name: oobeya-addons-ssl
  namespace: oobeya
type: Opaque
stringData:
  ssl.crt: |
    -----BEGIN CERTIFICATE-----
    -----END CERTIFICATE-----


  tls.key: |
    -----BEGIN CERTIFICATE-----
    -----END CERTIFICATE-----

    
  another-custom-ssl.crt: |
    -----BEGIN CERTIFICATE-----
    -----END CERTIFICATE-----
```

### Edit values.yaml

```
$ vi values.yaml
```

### Find customSSL step

```
customSSL:
    secretSSL:
      enabled: false                # Set false -> true
      name: ""                      # The secret name where SSL files are generated
      mountPath: "/srv/certs"
      certFileNames:
          - ""                      # Write SSL file name, example: "ssl-gitlab.crt"
          - ""                      # If there is one, the name of the other SSL file added
          - ""                      # If there is one, the name of the other SSL file added
```

To confirm that SSLs are actually deployed to the Pod:

```
$ kubectl logs oobeya-addons-xxx-xxx -n oobeya
```

Expected output example:

```
SSL Conf enabled: true
SSL Cert Alias:
SSL Cert Files: ssl.crt tls.key another-custom-ssl.crt
****************************************************************
Copying certificate file with command: cp /srv/certs/ssl.crt /opt/java/openjdk/lib/security/ssl.crt
Certificate was added to keystore

Copying certificate file with command: cp /srv/certs/tls.key /opt/java/openjdk/lib/security/tls.key
Certificate was added to keystore

Copying certificate file with command: cp /srv/certs/another-custom-ssl.crt /opt/java/openjdk/lib/security/another-custom-ssl.crt
Certificate was added to keystore
```
