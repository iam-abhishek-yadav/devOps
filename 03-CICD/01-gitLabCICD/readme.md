## GitLab Overview:
- GitLab is a comprehensive DevOps platform that facilitates the entire software development lifecycle.
- GitLab executes pipelines to release new code changes to end-users.
- Self-hosted runners can be used to execute CI/CD jobs.
- Pipeline configuration is part of the application code.

## GitLab Architecture:
- **Instance/Server:**
  - Hosts application code and pipeline configuration.
  - Manages pipeline execution.
- **GitLab Runners:**
  - Agents responsible for running CI/CD jobs.

## .gitlab-ci.yml File:
- **Filename:** `.gitlab-ci.yml`
- **Syntax:**
  ```yaml
  stages:
    - stage1
    - stage2
  
  nameOfJob:
    stage: stage1
    variables:
      key: value
    services:
      - service container
    image: docker-image name
    before_script:
      - commands to run before script
    script:
      - command1
      - command2
    after_scripts:
      - commands after main script
  ```
  
## Viewing CI/CD Execution:

-   Access CI/CD in GitLab.
-   Navigate to Jobs, click on jobName to view job logs.

## Creating Variables:

-   Go to Settings => CI/CD => Variables.
-   Mask variables for sensitive information.

## SSH to Container:

```bash
ssh -o StrictHostKeyChecking=no -i keyFile user@IP
```
