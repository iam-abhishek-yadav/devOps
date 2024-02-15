
## Cloud SQL

Google Cloud's Cloud SQL is a fully managed relational database service, providing support for MySQL, PostgreSQL, and SQL Server. Here are key features and details:

- **Managed Service:**
  - Fully managed, allowing developers to focus on building applications rather than mundane tasks.
  - Google handles tasks such as applying patches, managing backups, and configuring replications.

- **Scalability:**
  - Can scale up to 128 processor cores, 864 GB of RAM, and 64 TB of storage.

- **Automatic Replication:**
  - Supports automatic replication scenarios, including Cloud SQL primary instance, external primary instance, and external MySQL instances.

- **Managed Backups:**
  - Cloud SQL supports managed backups, ensuring securely stored and accessible data for potential restores.
  - The cost of an instance covers seven backups.

- **Security Features:**
  - Encrypts customer data on Google's internal networks and when stored in database tables, temporary files, and backups.
  - Includes a network firewall for controlling network access to each database instance.

- **Accessibility:**
  - Cloud SQL instances are accessible by other Google Cloud services and external services.

- **Compatibility:**
  - Compatible with App Engine using standard drivers like Connector/J for Java or MySQLdb for Python.
  - Compute Engine instances can be authorized to access Cloud SQL instances.

- **Support for External Applications:**
  - Supports other applications and tools like SQL Workbench, Toad, and external applications using standard MySQL drivers.

## Cloud Spanner

Google Cloud's Cloud Spanner is a fully managed relational database service with unique features. 

- **Horizontally Scalable:**
  - Scales horizontally to handle high-performance applications and services.
  - Suited for applications requiring high numbers of input and output operations per second.

- **Strong Consistency:**
  - Provides strong global consistency, ensuring reliable and predictable behavior.

- **SQL Compatibility:**
  - Uses SQL, making it easy for developers familiar with relational databases.
  - Supports features like joins and secondary indexes.

- **Battle-Tested:**
  - Battle-tested by Google in mission-critical applications and services.
  - Powers Google's $80 billion business, demonstrating its reliability and scalability.

- **Built-in High Availability:**
  - Designed with built-in high availability features for robust and resilient operations.

- **Performance:**
  - Capable of handling tens of thousands of reads and writes per second or more.

Cloud Spanner is especially well-suited for applications that demand a SQL relational database management system with strong global consistency, high availability, and significant input/output operations.

