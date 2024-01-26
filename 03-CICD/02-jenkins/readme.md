## Running Jenkins in Docker Container

To run Jenkins in a Docker container, execute the following command:

```bash
docker run -p 8080:8080 -p 50000:50000 -d -v jenkins_home:/var/jenkins_home jenkins/jenkins:lts
```
Access the initial admin password from the logs.

## Creating Multibranch Pipelines

1.  Navigate to `New Item` in Jenkins.
2.  Select `Multibranch Pipeline`.

## Creating Credentials

1.  Go to `Manage Jenkins`.
2.  Select `Manage Credentials`.
3.  Add or manage credentials as per requirement.

### Credentials Scope

-   **System**: Available only on the Jenkins server, not for Jenkins jobs.
-   **Global**: Accessible everywhere.

## Jenkinsfile

There are two types of Jenkinsfile:

-   **Scripted**: Uses the Groovy engine, offering advanced scripting capabilities and high flexibility.
-   **Declarative**: Follows a predefined structure.

### Requirements for Jenkinsfile

-   Must be at the top level.
-   Should define where to execute (`agent`).
-   Should have stages where the actual work happens.
    -   Each stage consists of steps.

Example Jenkinsfile:
```groovy
pipeline {
    agent any
    stages {
        stage("build") {
            steps {
                script {
                    // Your build steps here
                }
            }
        }
    }
}
```
## Triggering Builds

Builds can be triggered using either push notification or polling:

### Push Notification

-   Version control notifies Jenkins on new commits.
-   Configure push notification:
    -   Go to `Manage Jenkins` > `System` > `GitHub Server`.
    -   In your GitHub repository settings, navigate to `Webhooks` and add a webhook.

### Polling

-   Jenkins polls at regular intervals.
-   Configure polling:
    -   Go to your pipeline configuration.
    -   Under `Scan Multibranch Pipeline Triggers`, set up polling.
