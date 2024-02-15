
## Cloud Load Balancing in Google Cloud

  - Cloud Load Balancing is a distributed, software-defined, managed service for distributing user traffic across multiple instances of an application.
  - Reduces the risk of performance issues by efficiently spreading the load.
  - Fully managed service, eliminating the need for users to manage or scale load balancers.

- **Supported Traffic:**
  - Cloud Load Balancing supports various types of traffic, including HTTP, HTTPS, TCP, SSL, and UDP.
  - Provides cross-region load balancing with automatic multi-region failover.

- **Dynamic Scalability:**
  - Reacts quickly to changes in users, traffic, network conditions, backend health, and other related factors.
  - No "pre-warming" required, making it suitable for handling unexpected spikes in demand.

- **Load Balancing Options:**
  - `Global HTTP(S) Load Balancing`: Cross-regional load balancing for web applications.
  - `Global SSL Proxy Load Balancer`: For non-HTTP SSL traffic.
  - `Global TCP Proxy Load Balancer`: For other non-SSL TCP traffic.
  - `Regional External Passthrough Network Load Balancer`: Load balancing UDP traffic and traffic on any port number within a Google Cloud region.
  - `Regional External Application Load Balancer and Proxy Network Load Balancer`: Designed for incoming internet traffic.
  - `Regional Internal Load Balancer`: Load balancing traffic inside a project, suitable for communication between different layers of an application. Supports Proxy Network Load Balancer, Passthrough Network Load Balancer, and Application Load Balancer. Accepts traffic on a Google Cloud internal IP address and balances it across Compute Engine VMs.
  - `Cross-region Internal Load Balancer`: Layer 7 load balancer for load balancing traffic to globally distributed backend services. Provides traffic management to ensure routing to the closest backend.
