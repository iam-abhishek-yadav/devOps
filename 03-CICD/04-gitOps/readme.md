
# GitOps Workflow

GitOps is a methodology for managing and automating infrastructure and application deployments using Git repositories as the single source of truth. The typical GitOps flow involves the following steps:

1. **Create Pull Request (PR):**
   - Changes to the infrastructure or application are initiated by creating a pull request.

2. **Run CI Pipeline:**
   - Continuous Integration (CI) pipelines are triggered automatically upon creating a pull request.
   - CI pipelines ensure that the proposed changes pass tests and meet defined quality criteria.

3. **Approve Changes:**
   - After successful CI, changes are reviewed and approved within the pull request.

4. **Run CD Pipeline:**
   - Continuous Deployment (CD) pipelines are triggered upon approval.
   - CD pipelines automate the deployment of changes to the target environment.

## Two Ways of Implementing GitOps

### 1. Push Approach
   - CI/CD tools like Jenkins are used to push changes to the target environment.

### 2. Pull Approach
   - An agent is installed in the target environment (e.g., in a Kubernetes cluster).
   - The agent monitors and compares the desired state (defined in the Git repository) with the actual state.
   - It applies the necessary changes to align the actual state with the desired state.
   - Examples of GitOps tools using the pull approach include FluxCD and ArgoCD.

## Rollback

In GitOps, rolling back changes is typically achieved using the `git revert` command. This creates a new commit that undoes the previous changes.

## Single Source of Truth

The Git repository serves as the single source of truth for the entire infrastructure and application configuration.

## Increased Security

GitOps provides increased security benefits by:
   - Avoiding the need to give everyone direct access to the Kubernetes cluster.
   - Enforcing changes through the established GitOps flow, ensuring proper review and approval.
