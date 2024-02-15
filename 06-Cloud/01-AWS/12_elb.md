
## Load Balancers

- Load balancing distributes tasks across a set of resources.
- Resources: EC2 instances hosting the application.
- Tasks: Requests sent to the application.
- Load balancer redirects traffic based on algorithms (e.g., round-robin).

### Elastic Load Balancer (ELB)
- AWS provides ELB service for load balancing.
- ELB is directly in the path of traffic.

### ELB Features
- Automatically scales to handle incoming traffic demand.
- Supports hybrid mode, high availability, and scalability.
  
### Health Checks
- ELB ensures routing to healthy EC2 instances.
- Health checks: Establishing connections or making HTTP/HTTPS requests.
- Define appropriate health checks to verify all necessary elements.

### ELB Components
- Three main components: rules, listeners, and target groups.

### Types of Load Balancers
- Application Load Balancer (ALB)
  - Layer 7 (OSI model).
  - Ideal for HTTP and HTTPS traffic.
  - Routes traffic based on request content.

- Network Load Balancer (NLB)
  - Layer 4 (OSI model).
  - Ideal for TCP and UDP traffic.
  - Preserves client-side source IP address.

- Gateway Load Balancer (GLB)
  - For third-party virtual appliances.
  - Helps deploy, scale, and manage virtual appliances.

### ALB Features
- Routes traffic based on request data.
- Sends responses directly to the client.
- Uses TLS offloading, authenticates users, secures traffic, and supports sticky sessions.

### NLB Features
- Sticky sessions, low latency, source IP address preservation.
- Static IP support, elastic IP address support, DNS failover.

### GLB Features
- High availability, monitoring, streamlined deployments, private connectivity.

### Selecting Between ELB Types
- Choose based on application requirements.
- Major features include load balancer type, target type, protocol listeners, static IP, and more.

| Feature                     | ALB                 | NLB                  | GLB                                            |
|-----------------------------|---------------------|----------------------|-------------------------------------------------|
| Load Balancer Type           | Layer 7             | Layer 4              | Layer 3 gateway and Layer 4 load balancing      |
| Target Type                 | IP, instance, Lambda| IP, instance, ALB   | IP, instance                                    |
| Protocol Listeners          | HTTP, HTTPS         | TCP, UDP, TLS        | IP                                              |
| Static IP and Elastic IP    |                  | Yes                  |                                              |
| Preserve Source IP Address  | Yes                 | Yes                  | Yes                                             |
| Fixed Response              | Yes                 |                     |                                                 |
| User Authentication         | Yes                 |                   |                                                 |

