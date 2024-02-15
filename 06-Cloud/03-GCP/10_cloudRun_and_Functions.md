
## Application Development in the Cloud


### Cloud Run

- **Cloud Run:**
  - Managed compute platform for stateless containers via web requests or Pub/Sub events.
  - Serverless, built on Knative and can be managed on Google Cloud or anywhere Knative runs.
  - Fast, scales instantly, charges based on actual resource usage with 100-millisecond granularity.

- **Developer Workflow:**
  1. Write the application in your preferred language.
  2. Build and package into a container image.
  3. Push the container image to Artifact Registry, where Cloud Run deploys it.
  - Cloud Run provides a unique HTTPS URL for the deployed container.
  - Serverless nature allows developers to focus on application development.

- **Container and Source-Based Workflows:**
  - Support both container-based and source-based workflows.
  - Source-based approach deploys source code, and Cloud Run builds it into a container image using Buildpacks.
  - Cloud Run handles HTTPS serving, and developers focus on handling web requests.

- **Pricing Model:**
  - Unique model charges for system resources used during web requests, with 100-millisecond granularity.
  - No charges when the container is idle.
  - Additional small fee for every one million requests served.
  - Container time cost increases with CPU and memory.

- **Language Support:**
  - Supports any binary compiled for Linux 64-bit.
  - Popular languages include Java, Python, Node.js, PHP, Go, and C++.
  - Also supports less common languages like Cobol, Haskell, and Perl.

### Cloud Functions

- **Event-Driven Applications:**
  - Many applications have event-driven parts (e.g., image uploads).
  - Cloud Functions for lightweight, event-based, asynchronous compute.
  - Write single-purpose functions responding to cloud events without managing a server.

- **Key Features:**
  - Small, single-purpose functions for specific tasks.
  - Responds to cloud events (e.g., Cloud Storage, PubSub) asynchronously.
  - Supports HTTP invocation for synchronous execution.
  - Executes business logic tasks with event-driven workflows.

- **Language Support:**
  - Supports various programming languages: Node.js, Python, Go, Java, .Net Core, Ruby, PHP.
  - Refer to runtime documentation for specific versions.

- **Execution Model:**
  - Charges based on resource usage, billed to the nearest 100 milliseconds while the code is running.
  - Integrates and extends Cloud Services.

