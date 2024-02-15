
## Kubernetes and Google Kubernetes Engine (GKE)

### Kubernetes Overview

- **Kubernetes (K8s):**
  - Open source platform for managing containerized workloads and services.
  - Facilitates orchestration of containers on multiple hosts, enabling easy scaling, deployment, rollouts, and rollbacks.
  - Consists of APIs for deploying containers on a set of nodes called a cluster.

- **Kubernetes Components:**
  - Control Plane: Primary components managing the cluster.
  - Nodes: Computing instances representing machines.
  - Pod: Smallest deployable unit, representing a running process.

- **Pods and Deployments:**
  - Pods encapsulate containers with shared networking and storage resources.
  - Deployments represent groups of replicas of the same pod, ensuring high availability.
  - Pods are accessed through services that provide fixed IP addresses.

- **Scaling and Declarative Approach:**
  - Scaling with `kubectl scale` command or autoscaling based on parameters.
  - Strength in working declaratively using configuration files, defining desired states.

- **Updating Applications:**
  - Use `kubectl rollout` or modify deployment configuration files.
  - Example: Create new version pods individually, ensuring safety during updates.

### Google Kubernetes Engine (GKE)

- **Introduction:**
  - GKE is a hosted managed Kubernetes service in Google Cloud.
  - Environment consists of compute engine instances forming a cluster.

- **Cluster Customization:**
  - Create clusters with different machine types, node counts, and network settings.
  - Kubernetes commands and resources used for application deployment, administration, policy setting, and monitoring.

- **Advanced Cluster Management:**
  - Features provided by Google Cloud:
    - Load balancing for compute engine instances.
    - Node pools for subset designation within a cluster.
    - Automatic scaling of node instances.
    - Automatic upgrades and auto-repair for node health.
    - Logging and monitoring with Google Cloud's operation suite.

- **Starting GKE Cluster:**
  - Use the command: `gcloud container clusters create k1`.

