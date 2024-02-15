
# Cloud Storage

- **Object Storage:**
  - Manages data as "objects," not as a file and folder hierarchy or chunks of a disk.
  - Objects include binary data, associated metadata, and a globally unique identifier (URL).

- **Google Cloud's Cloud Storage:**
  - Object storage service for durable and highly available storage.
  - Fully managed scalable service with various use cases:
    - Serving website content.
    - Storing data for archival and disaster recovery.
    - Distributing large data objects to end-users via Direct Download.
    
- **Primary Use Cases:**
  - Binary Large-Object Storage (BLOB) for online content (videos, photos).
  - Backup and archival data storage.
  - Storage of intermediate results in processing workflows.

- **Organization of Files:**
  - Files are organized into buckets.
  - Buckets require a globally unique name and a specific geographic location for storage.

- **Immutability of Storage Objects:**
  - Objects are immutable, and each change creates a new version.
  - Option to overwrite older versions or enable versioning to keep a detailed history of modifications.

- **Access Control:**
  - Controlled through IAM roles and access control lists (ACLs).
  - IAM roles for most purposes, ACLs for finer control.
  - Roles are inherited from project to bucket to object.

- **Lifecycle Management Policies:**
  - Helps manage costs by defining rules for object lifecycle.
  - Examples include deleting objects older than a specified date or keeping a certain number of object versions.

- **Security Best Practices:**
  - IAM roles and ACLs help adhere to security best practices.
  - Users granted access and permissions only for the resources needed for their tasks.

- **Privacy Considerations:**
  - Personally identifiable information may be present in data objects.
  - Controlling access is crucial for maintaining security and privacy.

- **Cost Management:**
  - Lifecycle management policies help control costs by ensuring users pay only for what is needed.
 
### Cloud Storage Classes


1. **Standard Storage:**
   - Best for frequently accessed or hot data.
   - Suitable for data stored for brief periods.
   
2. **Nearline Storage:**
   - Ideal for infrequently accessed data, such as reading or modifying once a month or less.
   - Used for data backups, long-term multimedia content, and data archiving.

3. **Coldline Storage:**
   - A low-cost option for infrequently accessed data.
   - Meant for reading or modifying data at most once every 90 days.

4. **Archive Storage:**
   - The lowest cost option, used for data archiving, online backup, and disaster recovery.
   - Best for data accessed less than once a year, with higher costs for access and operations.

**Common Characteristics Across Storage Classes:**
- Unlimited storage with no minimum object size requirement.
- Worldwide accessibility and locations.
- Low latency and high durability.
- Uniform experience, extending to security tools and APIs.
- Geo-redundancy in multi-region or dual-region storage.

**Auto-Class Feature:**
- Automatically transitions objects to appropriate storage classes based on access patterns.
- Moves less-accessed data to colder storage classes to reduce costs.
- Optimizes future accesses by moving frequently accessed data to standard storage.

**Cost Management:**
- No minimum fee; pay only for what you use.
- No prior provisioning of capacity required.

**Security Features:**
- Data always encrypted on the server side before being written to disk at no additional charge.
- Data traveling between a customer's device and Google is encrypted by default using HTTPS/TLS (transport layer security).

**Data Upload Options:**
- Online transfer using Cloud Storage commands from Cloud SDK.
- Drag-and-drop option in Cloud Console (Google Chrome browser).
- Storage Transfer Service for quick and cost-effective import of large amounts of online data.
- Transfer Appliance for uploading large datasets by leasing a high-capacity storage server from Google Cloud.

**Integration with Other Google Cloud Products:**
- Imprt and export tables to and from BigQuery and Cloud SQL.
- Store App Engine logs, files for backups, and objects used by App Engine applications.
- Store instance startup scripts, Compute Engine images, and objects used by Compute Engine applications.
o
