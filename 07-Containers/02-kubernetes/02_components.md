## Control Plane Components

### kube-apiserver
- Exposes the Kubernetes API and serves as the front end for the control plane.
- Scales horizontally by deploying multiple instances.

### etcd
- Consistent and highly-available key-value store for all cluster data.
- Used as Kubernetes' backing store.
- Ensure backup plans for etcd data.

### kube-scheduler
- Watches for newly created Pods with no assigned node and selects a node for them to run on.
- Scheduling decisions consider factors like resource requirements, constraints, affinity, anti-affinity, data locality, and deadlines.

### kube-controller-manager
- Manages controller processes, each responsible for specific tasks.
- Examples include Node controller (responds to node failures), Job controller (handles one-off tasks), and more.
- Logically separate controllers are compiled into a single binary for simplicity.

### cloud-controller-manager
- Embeds cloud-specific control logic into the Kubernetes control plane.
- Links the cluster to the cloud provider's API and manages cloud-specific components.
- Only runs controllers relevant to the cloud provider.
- Scales horizontally to improve performance or tolerate failures.

## Node Components

### kubelet
- Agent running on each node that ensures containers in a Pod are running and healthy.
- Manages containers specified in PodSpecs, provided through various mechanisms.

### kube-proxy
- Network proxy on each node, implementing part of the Kubernetes Service concept.
- Maintains network rules allowing communication to Pods from inside or outside the cluster.
- Uses the operating system packet filtering layer or forwards traffic itself.

### Container runtime
- Fundamental component enabling Kubernetes to run containers effectively.
- Manages the execution and lifecycle of containers in the Kubernetes environment.
- Supports container runtimes like containerd, CRI-O, and implementations of the Kubernetes CRI (Container Runtime Interface).

![Kubernetes Cluster Architecture](https://kubernetes.io/images/docs/kubernetes-cluster-architecture.svg)
