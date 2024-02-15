
## Firestore - Google Cloud's NoSQL Cloud Database

Google Cloud's Firestore is a versatile, horizontally scalable NoSQL cloud database designed for mobile, web, and server development. Here are key features and aspects of Firestore:

- **Data Organization:**
  - Data is stored in documents and organized into collections.
  - Documents can contain complex nested objects and subcollections.
  - Each document consists of key-value pairs, representing various data attributes.

- **NoSQL Queries:**
  - Firestore supports NoSQL queries for retrieving individual documents or collections based on query parameters.
  - Queries can include multiple chained filters, sorting options, and are indexed by default for efficient performance.

- **Data Synchronization:**
  - Utilizes data synchronization to update data across connected devices.
  - Efficiently handles simple one-time fetch queries and caches actively used data, enabling offline functionality.

- **Infrastructure Benefits:**
  - Leverages Google Cloud’s infrastructure for automatic multi-region data replication.
  - Provides strong consistency guarantees, supports atomic batch operations, and real transaction support.

- **Pricing:**
  - Charged for document reads, writes, deletes, and storage consumption.
  - Query charges are based on one "document read" per query, regardless of the returned data.
  - Additional charges may apply for specific network bandwidth usage.
  - Free daily quota for 50,000 document reads, 20,000 document writes, 20,000 document deletes, and 1 GB of stored data.

- **Free Quotas:**
  - Firestore offers a free daily quota, allowing developers to get started with minimal or no costs.
  - Free quotas include 10 GiB of free network egress per month between US regions.

- **Billing Information:**
  - For detailed pricing information, users can refer to the Firestore pricing page or use Google’s Billing Calculator to estimate costs based on specific use cases.

## Cloud Bigtable - Google Cloud's NoSQL Big Data Database

Google Cloud's Cloud Bigtable is a robust NoSQL Big Data database service designed for massive workloads with consistent low latency and high throughput. Key features and use cases include:

- **Powerful Database Service:**
  - Powers core Google services such as search, analytics, maps, and Gmail.
  - Suited for both operational and analytical applications, including IoT, user analytics, and financial data analysis.

- **Ideal Use Cases:**
  - Best suited for handling more than one terabyte of semi-structured or structured data.
  - Efficient with high-throughput, rapidly changing, and NoSQL data.
  - Well-suited for scenarios with time-series or natural semantic ordering of data.
  - Effective for big data processing, whether asynchronous batch or synchronous real-time, and running machine learning algorithms.

- **Data Interaction:**
  - Interacts seamlessly with other Google Cloud services and third-party clients.
  - APIs enable reading from and writing to Cloud Bigtable through data service layers like Managed VMs, HBase REST server, or Java servers using the HBase client.
  - Commonly used to serve data to applications, dashboards, and data services.

- **Streaming and Batch Processing:**
  - Supports streaming data through popular frameworks like Dataflow Streaming, Spark Streaming, and Storm.
  - Allows data to be read from and written to Cloud Bigtable through batch processes such as Hadoop MapReduce, Dataflow, or Spark.
  - Summarized or newly calculated data can be written back to Cloud Bigtable or downstream databases.

- **Integration with Google Cloud Ecosystem:**
  - Seamless integration with various Google Cloud services, enhancing its versatility and usability.

- **Considerations:**
  - Customers often choose Cloud Bigtable for scenarios where relational semantics are not crucial, and data characteristics align with its strengths.

- **API Interactions:**
  - Data can be streamed or batch processed using APIs, making it adaptable to diverse data processing requirements.

- **Downstream Databases:**
  - Spports writing summarized or newly calculated data back to Cloud Bigtable or downstream databases.

- **Scalability and Performance:**
  - Designed to handle massive workloads with efficient scalability, making it a powerful choice for substantial data processing tasks.
u
