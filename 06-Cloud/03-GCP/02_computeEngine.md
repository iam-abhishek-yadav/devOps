## Google Cloud Compute Engine

  - Allows users to create and run virtual machines on Google infrastructure.
  - No upfront investments required, providing the flexibility to run thousands of virtual CPUs with consistent performance.
  - Each virtual machine includes the power and functionality of a full-fledged operating system.

- **Configuration and Creation:**
  - Configure virtual machines similar to physical servers, specifying CPU power, memory, storage, and the operating system.
  - Instances can be created via Google Cloud Console, Google Cloud CLI, or Compute Engine API.
  - Supports Linux and Windows Server images provided by Google or custom versions of these images.
  - Cloud Marketplace offers solutions from Google and third-party vendors, simplifying the setup process.

- **Pricing and Billing Structure:**
  - Compute Engine bills by the second with a one-minute minimum, and sustained-use discounts apply automatically.
  - Committed-use discounts provide up to a 57% discount for stable and predictable workloads, based on a one or three-year commitment.
  - Preemptible and Spot VMs offer significant cost savings, up to 90%, for non-urgent workloads.
  - Preemptible VMs have a maximum runtime of 24 hours, while Spot VMs do not have a maximum runtime but have the same pricing.

- **Storage and Custom Machine Types:**
  - Compute Engine provides default high throughput between processing and persistent disks at no extra cost.
  - Custom machine types allow flexibility in choosing machine properties, such as the number of virtual CPUs and memory.
  - Pay only for the resources needed, making it a cost-effective solution.

- **Custom Machine Types:**
  - Choose machine properties for instances, including virtual CPUs and memory.
  - Options include predefined machine types or creating custom machine types based on specific requirements.

- **Autoscaling:**
  - Feature that allows VMs to be dynamically added or removed based on load metrics.
  - Ensures optimal resource utilization and performance scalability for applications.

- **Load Balancing with VPC:**
  - Google’s Virtual Private Cloud (VPC) supports various load balancing techniques.
  - Efficiently balances incoming traffic among VMs to maintain application availability.

- **Scaling Strategies:**
  - Compute Engine supports configuring large VMs suitable for specific workloads like in-memory databases and CPU-intensive analytics.
  - Emphasizes scaling out, adding more instances horizontally, rather than scaling up.

- **Resource Constraints:**
  - The maximum number of CPUs per VM is determined by the "machine family" and user-specific quotas, which are zone-dependent.
  - Users should be aware of and manage quotas effectively for resource allocation.
