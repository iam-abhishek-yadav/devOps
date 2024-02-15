
## Azure Virtual Machines (VMs) Overview
- Cloud-based service providing scalable and on-demand virtualized computing resources.
- Infrastructure as a Service (IaaS) offering.

### Capabilities
- **Total Control:** Over the operating system (OS) and custom software.
- **Customization:** Use custom hosting configurations.

### Management Options
- Azure Portal
- Azure CLI
- Azure PowerShell
- Automation tools
- Infrastructure as Code (ARM Templates)

### VM Creation
- Customization of software on VM.
- Flexibility of virtualization without physical hardware management.

### Image Provisioning
- Rapid VM creation using preconfigured VM images.
- Images may include OS and additional software.

### Scale in Azure
- Single VMs for testing, development, or minor tasks.
- Group VMs for high availability, scalability, and redundancy.

### Virtual Machine Scale Sets
- Group of identical, load-balanced VMs.
- Automated management, configuration, and updates.
- Auto-scaling based on demand or defined schedule.
- Suitable for large-scale services like compute, big data, and container workloads.

### Virtual Machine Availability Sets
- Ensures VMs stagger updates and have varied power and network connectivity.
- Groups VMs into update and fault domains.
- No additional cost for configuring availability sets.
- Ensures high availability and resilience.

### Use Cases
- Testing and development: Quick creation and deletion of VMs for various configurations.
- Running applications in the cloud: Economic benefits, resource usage based on demand.
- Extending datacenter to the cloud: Virtual network creation, application deployment.
- Disaster recovery: Cost-effective approach using IaaS in case of primary datacenter failure.
- Move to the cloud (Lift and Shift): Migration from physical servers to VMs with minimal changes.

### Resource Configuration
- VM size, storage disks, networking (virtual network, public IP address, port configuration).


## Azure Virtual Desktop Overview

- Desktop and application virtualization service running on the cloud.

### Capabilities
- Cloud-hosted version of Windows accessible from any location.
- Compatible with various devices, operating systems, and browsers.

### Security Features
- Centralized security management with Microsoft Entra ID.
- Multifactor authentication for user sign-ins.
- Granular Role-Based Access Controls (RBACs) for secure data access.

### Data and App Separation
- Desktop and apps run in the cloud, reducing the risk of data on personal devices.
- User sessions are isolated in both single and multi-session environments.

### Multi-Session Windows Deployment
- Utilizes Windows 10 or Windows 11 Enterprise multi-session.
- Enables multiple concurrent users on a single VM.
- Offers a consistent experience and broader application support compared to Windows Server-based operating systems.


## Azure Containers Overview

- Virtualization environment for running multiple instances of an application on a single host machine.

### Characteristics
- Lightweight, dynamic, and designed for creating, scaling, and stopping dynamically.
- Do not manage the operating system within the container.

### Container Engine
- Docker is a popular container engine, and Azure supports Docker.

### Azure Container Services

1. **Azure Container Instances (ACI)**
	- Fastest and simplest way to run a container in Azure.
	- Platform as a Service (PaaS) offering.
	- No need to manage virtual machines; service runs containers.

2. **Azure Container Apps**
	- Similar to Container Instances but with additional benefits.
	- PaaS offering with features like load balancing and scaling.
	- Enhances elasticity in design.

3. **Azure Kubernetes Service (AKS)**
	- Container orchestration service managing the lifecycle of containers.
	- Simplifies fleet management when deploying multiple containers.

### Container Usage in Solutions
- Microservice architecture: Break solutions into smaller, independent containers.
- Example: Separate a website into front end, back end, and storage containers.
- Enables maintenance,scaling, and updates independently for logical sections of the application.
 
