---
description: >-
  This guide covers how to configure GitLab, Azure DevOps, and Jenkins pipelines
  to show Git author information in SonarQube analysis.
---

# Configuring Git Author Tracking in SonarQube

## Sonarqube Author Setup

### Sonarqube Server Settings

* Go to: **Administration > SCM**
* Ensure SCM is dis**abled**&#x20;

### 1. Git Installation Check

Ensure Git is installed on the Sonarqube server.

### 2. CI/CD Setup

#### GitLab

```yaml
stage: testAndSonar
image: oobeya.azurecr.io/...

variables:
  GIT_DEPTH: "0"

script:
  # ...
```

Alternatively:

```bash
-Dsonar.git.depth=0
-Dsonar.scm.provider=git
```

#### Azure DevOps

```yaml
steps:
- checkout: self
  fetchDepth: 0  # Important

- task: SonarQubePrepare@6
  displayName: 'Prepare analysis on SonarQube'
  inputs:
    SonarQube: 'Sonar'
    scannerMode: 'CLI'
    configMode: 'manual'
    cliProjectKey: 'name'
    cliProjectName: 'name'
    extraProperties: |
      sonar.sourceEncoding=UTF-8
      sonar.sources=components,layouts,pages,plugins,public
      sonar.language=js
      sonar.exclusions=node_modules/**,dist/**
      sonar.projectVersion=1.0
      sonar.scm.provider=git  # Important
```

#### Jenkins

**Checkout Stage (Optional)**

```groovy
stages {
  stage('Checkout') {
    steps {
      checkout([$class: 'GitSCM',
                branches: [[name: '*/master']],
                doGenerateSubmoduleConfigurations: false,
                extensions: [[$class: 'CloneOption', noTags: false, reference: '', shallow: false, depth: 0]],
                userRemoteConfigs: [[url: 'https://github.com/google/guava']]
               ])
    }
  }
```

**SonarQube Analysis Stage (Must Use)**

```groovy
  stage('SonarQube Analysis') {
    steps {
      withSonarQubeEnv('Oobeya-Sonarqube') {
        sh '''
          mvn sonar:sonar \
            -Dsonar.projectKey=guava \
            -Dsonar.projectName="Google Guava Author Analysis" \
            -Dsonar.projectVersion=1.0 \
            -Dsonar.scm.provider=git  # Important
        '''
      }
    }
  }
}
```
