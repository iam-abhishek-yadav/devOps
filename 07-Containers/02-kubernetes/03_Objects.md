## Kubernetes Objects

- Kubernetes objects are persistent entities representing the state of your cluster.
- These entities describe:
  - Running containerized applications and their locations.
  - Available resources for applications.
  - Policies for application behavior (e.g., restart policies, upgrades, fault-tolerance).

- A Kubernetes object is a "record of intent," specifying the desired state of your cluster.

### Working with Kubernetes Objects

- To create, modify, or delete Kubernetes objects, you use the [Kubernetes API](https://kubernetes.io/docs/reference/kubernetes-api/)
- `kubectl` command-line interface automates API calls; you can also use the API directly with [client libraries](https://kubernetes.io/docs/reference/using-api/client-libraries/)

### Object Spec and Status

- Almost every Kubernetes object includes two nested object fields governing the object's configuration: the object spec and the object status.
- The object spec is set during creation, describing the desired state.
- The object status reflects the current state, actively managed by the Kubernetes control plane to match the desired state.

### Example: Deployment

```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: nginx-deployment
spec:
  selector:
    matchLabels:
      app: nginx
  replicas: 2
  template:
    metadata:
      labels:
        app: nginx
    spec:
      containers:
      - name: nginx
        image: nginx:1.14.2
        ports:
        - containerPort: 80
```
-   Use `kubectl apply` to create a Deployment from a manifest file:
``` bash
kubectl apply -f https://k8s.io/examples/application/deployment.yaml
```

### Required Fields

In the manifest (YAML or JSON file) for the Kubernetes object you want to create, you'll need to set values for the following fields:

-   `apiVersion`: Specifies the version of the Kubernetes API you're using.
-   `kind`: Defines the type or kind of object you want to create.
-   `metadata`: Contains data to uniquely identify the object (e.g., name, UID, namespace).
-   `spec`: Describes the desired state for the object.

The precise format of the object spec is different for every Kubernetes object, and contains nested fields specific to that object.
