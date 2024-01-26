
## GitHub Actions

GitHub Actions is a platform designed to automate developer workflows by listening to events and triggering specified workflows. Workflows are defined in YAML files and are executed on GitHub servers.

## Creating a Workflow

1. Navigate to your repository.
2. Go to the `Actions` tab.
3. Choose a template or create a new workflow by selecting `Set up a workflow yourself`.

## Where Does the Code Run?

- Code runs on GitHub servers.
- Each job in a workflow runs in a fresh virtual environment.

## Secrets

- Manage secrets at `GitHub` > `Your Repository` > `Settings` > `Secrets and Variables` > `Actions` > `New Repository Secret`.

## Example Workflow File

```yaml
on:
  push:
    branches: [master]
  pull_request:
    branches: [master]

jobs:
  build:
    runs-on: ${{matrix.os}}
    strategy:
      matrix:
        os: [ubuntu-latest, windows-latest, macOS-latest]

    steps:
      - name: Checkout Code
        uses: actions/checkout@v2

      - name: Set up JDK 1.8
        uses: actions/setup-java@v1
        with:
          java-version: 1.8

      - name: Grant permission for gradlew
        run: chmod +x gradlew

      - name: Build with Gradle
        run: ./gradlew build

      - name: Build and Push Docker Image
        uses: mr-smithers-excellent/docker-build-push@v4
        with:
          image: docker-hub-repo/image-name
          registry: docker.io
          username: ${{secrets.DOCKER_USERNAME}}
          password: ${{secrets.DOCKER_PASSWORD}}
```

## Additional Resources

[GitHub Actions Repository](https://github.com/actions)

[GitHub Events Documentation](https://docs.github.com/en/actions/using-workflows/events-that-trigger-workflows)

[GitHub Marketplace - Actions](https://github.com/marketplace?type=actions)

