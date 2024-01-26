
## ArgoCD: Continuous Delivery for Kubernetes
ArgoCD is a continuous delivery tool designed specifically for Kubernetes (k8s). It simplifies and streamlines the deployment and management of applications on Kubernetes clusters.

## Challenges Without ArgoCD:

- **Installation and Setup:**
  - Need to install and set up tools like `kubectl`.
  
- **Configuration Access:**
  - Configuring access to Kubernetes clusters and cloud platforms can be complex.
  
- **Security Challenges:**
  - Ensuring secure access and permissions is a challenge.
  
- **Visibility:**
  - Lack of visibility into deployment status.

## Continuous Delivery Workflow with ArgoCD:

1. **Deploy ArgoCD in Kubernetes Cluster:**
   - Install ArgoCD within the Kubernetes cluster.

2. **Configure ArgoCD to Track Git Repository:**
   - Set up ArgoCD to monitor a Git repository for changes.

3. **Automatic Application of Changes:**
   - ArgoCD monitors the Git repository and automatically applies changes to the cluster.

## ArgoCD Supports:

- Kubernetes YAML files
- Helm charts
- Kustomize

## Benefits of ArgoCD:

- **Infrastructure as Code:**
  - The entire Kubernetes configuration is defined as code in a Git repository.

- **No Manual Application:**
  - Config files are not manually applied from local laptops.

- **Single Interface:**
  - ArgoCD provides a unified interface for managing deployments.

- **Version Controlled Changes:**
  - Changes are version controlled, providing a history of modifications.

- **Improved Collaboration:**
  - Facilitates better team collaboration.

## Operational Capabilities:

- **Monitoring Changes:**
  - ArgoCD watches both the Kubernetes cluster and Git repository for changes, ensuring alignment.

- **Easy Rollback:**
  - Provides an easy rollback mechanism to revert to the last working state.

- **Cluster Disaster Recovery:**
  - Assists in recovering the cluster from disasters.

## ArgoCD as a Kubernetes Extension:

- **Utilizing Kubernetes Functionalities:**
  - ArgoCD leverages existing Kubernetes functionalities, such as using etcd for data storage and Kubernetes controllers for monitoring and comparing states.

- **Real-time Updates:**
  - Real-time updates of application states are achieved seamlessly.

## Working with Multiple Clusters:

When managing multiple Kubernetes clusters, it becomes crucial to maintain consistency and flexibility across environments. ArgoCD offers support for working with multiple clusters through the use of overlays, with the assistance of a tool called Kustomize.

### Kustomize Overview:

[Kustomize](https://kustomize.io/) is a Kubernetes configuration management tool that enables customization of manifests without direct modification. It achieves this by using patches and overlays, allowing for environment-specific variations without duplicating entire configuration files.

### Overlay with Kustomize in ArgoCD:

1. **Overlay Concept:**
   - An overlay, in the context of ArgoCD and Kustomize, is a mechanism to apply specific configurations on top of a base configuration.
   
2. **Managing Multiple Clusters:**
   - ArgoCD leverages Kustomize overlays to manage configurations for multiple clusters.
   
3. **Customizing Configurations:**
   - Each overlay can contain customizations specific to a particular cluster, environment, or deployment scenario.
   
4. **Consistency Across Environments:**
   - Using overlays ensures that common configurations remain consistent across all clusters, while allowing flexibility for environment-specific adjustments.

### Example Scenario:

Suppose you have a base set of Kubernetes manifests defining a common application configuration. To deploy this application to different clusters, you can create overlays for each cluster using Kustomize. Each overlay may contain cluster-specific configurations, such as different resource limits, environment variables, or specific features enabled or disabled.

### Benefits of Overlays with Kustomize:

- **Configuration Modularity:**
  - Modifies configurations without changing the base files, enhancing modularity and maintainability.

- **Environment Specifics:**
  - Easily handles variations between environments, ensuring configurations are tailored to each cluster's requirements.

- **Simplified Maintenance:**
  - Reduces duplication by allowing changes to be made in a centralized manner without copying entire configurations.

- **Version Control:**
  - Enhances version control practices by keeping track of both base configurations and overlays separately.

By incorporating overlays with Kustomize, ArgoCD provides a robust solution for managing multiple clusters, offering a balance between consistency and flexibility in Kubernetes configurations.


## Setting Up ArgoCD:

- [Install ArgoCD](https://argo-cd.readthedocs.io/en/stable/getting_started/#1-install-argo-cd)
- Check the status of pods using `kubectl get pods`.
```bash
kubectl get pod -n argocd
```
- Identify the port with `kubectl get services`.
```bash
kubectl get svc -n argocd
```
- Forward the port to access the ArgoCD UI.
```bash
kubectl port-forward -n argocd svc/argocd-server 8080:443
```
- Log in using the provided credentials.
```bash
kubectl get secret argocd-initial-admin-secret -n argocd -o yaml
echo <password> | base64 --decode
```
- Write the configuration file to define the desired state.
```yml
//example
apiVersion:  argoproj.io/v1alpha1
kind:  Application
metadata:
 name:  myapp-argo-application
 namespace:  argocd
spec:
 project:  default
 source:
 repoURL: <gitURL>
 targetRevision:  HEAD
 path:  dev
 destination: 
 server:  https://kubernetes.default.svc
 namespace:  myapp
 syncPolicy:
 syncOptions:
 -  CreateNamespace=true
 automated:
 selfHeal:  true
 prune:  true
 ```

