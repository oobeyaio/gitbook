---
icon: wifi
---

# Network Access Requirements

Requests are made using the HTTP protocol via REST API calls.

The Oobeya server must be able to reach the following addresses as **outbound** traffic during initial setup and ongoing operation.

### 1. Image and Configuration File Access

| Purpose                                     | Address                                   | Port | Protocol |
| ------------------------------------------- | ----------------------------------------- | ---- | -------- |
| Container images (Azure Container Registry) | oobeya.germanywestcentral.data.azurecr.io | 443  | HTTPS    |
| Container images (Azure Container Registry) | oobeya.azurecr.io                         | 443  | HTTPS    |
| File/configuration repository (AWS S3)      | oobeya-app.s3.amazonaws.com               | 443  | HTTPS    |

### 2. Addon Tool Access (Outbound)

The Oobeya server must be able to reach the API or service addresses of the addon tools in use as outbound traffic:

| Category               | Addon Name                          | Deployment Type          | Default Port (No DNS/HTTPS) | Port (with DNS/HTTPS) | Protocol     |
| ---------------------- | ----------------------------------- | ------------------------ | --------------------------- | --------------------- | ------------ |
| **Project Management** | Jira Cloud                          | Cloud                    | —                           | 443                   | HTTPS        |
| **Project Management** | Jira Server / Data Center           | Server, Data Center      | 8080                        | 443                   | HTTP/HTTPS   |
| **Documentation**      | Confluence                          | Server, Data Center      | 8090                        | 443                   | HTTP/HTTPS   |
| **SCM & CI/CD & PM**   | Azure DevOps Cloud                  | Cloud                    | —                           | 443                   | HTTPS        |
| **SCM & CI/CD & PM**   | Azure DevOps Server                 | Server                   | 8080                        | 443                   | HTTP/HTTPS   |
| **SCM & CI/CD**        | GitHub Cloud                        | Cloud, Enterprise Cloud  | —                           | 443                   | HTTPS        |
| **SCM & CI/CD**        | GitHub Enterprise Server            | Enterprise On-premise    | 443                         | 443                   | HTTPS        |
| **SCM & CI/CD**        | GitLab Cloud                        | Cloud                    | —                           | 443                   | HTTPS        |
| **SCM & CI/CD**        | GitLab Self-Managed                 | Self Managed, Enterprise | 80                          | 443                   | HTTP/HTTPS   |
| **SCM & CI/CD**        | Bitbucket Cloud                     | Cloud                    | —                           | 443                   | HTTPS        |
| **SCM & CI/CD**        | Bitbucket Server / Data Center      | Server, Data Center      | 7990                        | 443                   | HTTP/HTTPS   |
| **SCM & CI/CD**        | Gitea                               | Server                   | 3000                        | 443                   | HTTP/HTTPS   |
| **SCM & CI/CD**        | Gerrit Cloud                        | Cloud                    | —                           | 443                   | HTTPS        |
| **SCM & CI/CD**        | Gerrit Server                       | Server                   | 8080                        | 443                   | HTTP/HTTPS   |
| **SCM & CI/CD**        | ArgoCD                              | Server                   | 8080                        | 443                   | HTTP/HTTPS   |
| **SCM & CI/CD**        | Jenkins                             | Server                   | 8080                        | 443                   | HTTP/HTTPS   |
| **SCM & CI/CD**        | CloudBees                           | Server                   | 8080                        | 443                   | HTTP/HTTPS   |
| **SCM & CI/CD**        | TeamCity Cloud                      | Cloud                    | —                           | 443                   | HTTPS        |
| **SCM & CI/CD**        | TeamCity Server                     | Server                   | 8111                        | 443                   | HTTP/HTTPS   |
| **SCM & CI/CD**        | Octopus Deploy Cloud                | Cloud                    | —                           | 443                   | HTTPS        |
| **SCM & CI/CD**        | Octopus Deploy Server               | Server                   | 8080                        | 443                   | HTTP/HTTPS   |
| **Quality & Security** | SonarQube Server                    | Server                   | 9000                        | 443                   | HTTP/HTTPS   |
| **Quality & Security** | SonarQube Cloud                     | Cloud                    | —                           | 443                   | HTTPS        |
| **Quality & Security** | Fortify                             | Server                   | 8080                        | 443                   | HTTP/HTTPS   |
| **Quality & Security** | Veracode                            | Cloud                    | —                           | 443                   | HTTPS        |
| **Quality & Security** | Xray Cloud (Jira Cloud)             | Cloud                    | —                           | 443                   | HTTPS        |
| **Quality & Security** | Xray Server / DC (Jira Server / DC) | Server / DC              | 8080                        | 443                   | HTTP/HTTPS   |
| **Monitoring & APM**   | Azure Application Insights          | Cloud                    | —                           | 443                   | HTTPS        |
| **Monitoring & APM**   | New Relic                           | Cloud                    | —                           | 443                   | HTTPS        |
| **Monitoring & APM**   | Datadog                             | Cloud                    | —                           | 443                   | HTTPS        |
| **Authentication**     | Microsoft Entra (Azure AD)          | Cloud                    | —                           | 443                   | HTTPS        |
| **Authentication**     | Okta                                | Cloud                    | —                           | 443                   | HTTPS        |
| **Authentication**     | LDAP                                | Server                   | 389 / 636                   | —                     | LDAP / LDAPS |

> **Note:** If the addon is accessed via DNS/domain with HTTPS, port 443 is opened. If DNS/HTTPS is not configured, the application's default port must be used instead. For Server/Data Center addons, the organization may have changed the default port during installation; in that case, access must be opened on the actual configured port. For addons running in **public/cloud environments**, access must be defined through **IP/domain whitelisting** rather than opening broad access — this applies to both outbound (this section) and inbound (Section 3) rules. The specific IP ranges or domains should be obtained from each provider's official documentation.

### 3. Adding the Oobeya Server to Addon Inbound Rules

The Oobeya server's access must be defined in the inbound settings of the addon tools in use:

| Category               | Addon Name                          | Deployment Type          | Default Port (No DNS/HTTPS) | Port (with DNS/HTTPS) | Protocol     |
| ---------------------- | ----------------------------------- | ------------------------ | --------------------------- | --------------------- | ------------ |
| **Project Management** | Jira Cloud                          | Cloud                    | —                           | 443                   | HTTPS        |
| **Project Management** | Jira Server / Data Center           | Server, Data Center      | 8080                        | 443                   | HTTP/HTTPS   |
| **Documentation**      | Confluence                          | Server, Data Center      | 8090                        | 443                   | HTTP/HTTPS   |
| **SCM & CI/CD & PM**   | Azure DevOps Cloud                  | Cloud                    | —                           | 443                   | HTTPS        |
| **SCM & CI/CD & PM**   | Azure DevOps Server                 | Server                   | 8080                        | 443                   | HTTP/HTTPS   |
| **SCM & CI/CD**        | GitHub Cloud                        | Cloud, Enterprise Cloud  | —                           | 443                   | HTTPS        |
| **SCM & CI/CD**        | GitHub Enterprise Server            | Enterprise On-premise    | 443                         | 443                   | HTTPS        |
| **SCM & CI/CD**        | GitLab Cloud                        | Cloud                    | —                           | 443                   | HTTPS        |
| **SCM & CI/CD**        | GitLab Self-Managed                 | Self Managed, Enterprise | 80                          | 443                   | HTTP/HTTPS   |
| **SCM & CI/CD**        | Bitbucket Cloud                     | Cloud                    | —                           | 443                   | HTTPS        |
| **SCM & CI/CD**        | Bitbucket Server / Data Center      | Server, Data Center      | 7990                        | 443                   | HTTP/HTTPS   |
| **SCM & CI/CD**        | Gitea                               | Server                   | 3000                        | 443                   | HTTP/HTTPS   |
| **SCM & CI/CD**        | Gerrit Cloud                        | Cloud                    | —                           | 443                   | HTTPS        |
| **SCM & CI/CD**        | Gerrit Server                       | Server                   | 8080                        | 443                   | HTTP/HTTPS   |
| **SCM & CI/CD**        | ArgoCD                              | Server                   | 8080                        | 443                   | HTTP/HTTPS   |
| **SCM & CI/CD**        | Jenkins                             | Server                   | 8080                        | 443                   | HTTP/HTTPS   |
| **SCM & CI/CD**        | CloudBees                           | Server                   | 8080                        | 443                   | HTTP/HTTPS   |
| **SCM & CI/CD**        | TeamCity Cloud                      | Cloud                    | —                           | 443                   | HTTPS        |
| **SCM & CI/CD**        | TeamCity Server                     | Server                   | 8111                        | 443                   | HTTP/HTTPS   |
| **SCM & CI/CD**        | Octopus Deploy Cloud                | Cloud                    | —                           | 443                   | HTTPS        |
| **SCM & CI/CD**        | Octopus Deploy Server               | Server                   | 8080                        | 443                   | HTTP/HTTPS   |
| **Quality & Security** | SonarQube Server                    | Server                   | 9000                        | 443                   | HTTP/HTTPS   |
| **Quality & Security** | SonarQube Cloud                     | Cloud                    | —                           | 443                   | HTTPS        |
| **Quality & Security** | Fortify                             | Server                   | 8080                        | 443                   | HTTP/HTTPS   |
| **Quality & Security** | Veracode                            | Cloud                    | —                           | 443                   | HTTPS        |
| **Quality & Security** | Xray Cloud (Jira Cloud)             | Cloud                    | —                           | 443                   | HTTPS        |
| **Quality & Security** | Xray Server / DC (Jira Server / DC) | Server / DC              | 8080                        | 443                   | HTTP/HTTPS   |
| **Monitoring & APM**   | Azure Application Insights          | Cloud                    | —                           | 443                   | HTTPS        |
| **Monitoring & APM**   | New Relic                           | Cloud                    | —                           | 443                   | HTTPS        |
| **Monitoring & APM**   | Datadog                             | Cloud                    | —                           | 443                   | HTTPS        |
| **Authentication**     | Microsoft Entra (Azure AD)          | Cloud                    | —                           | 443                   | HTTPS        |
| **Authentication**     | Okta                                | Cloud                    | —                           | 443                   | HTTPS        |
| **Authentication**     | LDAP                                | Server                   | 389 / 636                   | —                     | LDAP / LDAPS |

> **Note:** Same default port and DNS/HTTPS principles apply here as in Section 2. The whitelisting requirement for public/cloud environments described above applies equally to inbound rules.
