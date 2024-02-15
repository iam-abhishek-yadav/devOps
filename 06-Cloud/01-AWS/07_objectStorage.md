## Amazon S3 - Simple Storage Service

Amazon Simple Storage Service (Amazon S3) is a standalone object storage solution, decoupled from compute instances. It provides a flat structure for storing data and is widely used for its flexibility, scalability, and accessibility.

### Concepts

#### 1. Amazon S3 Objects
   - Stored in containers called buckets.
   - Object: A file combined with metadata.
   - Identified by a unique combination of bucket name, key, and version ID.

#### 2. Amazon S3 Bucket Names
   - Global uniqueness across all AWS accounts and regions.
   - Naming rules include length limits, allowed characters, and starting/ending with a letter or number.
   - Global buckets categorized into Standard Regions, China Regions, and AWS GovCloud (US).

#### 3. Amazon S3 Object Key Names
   - Uniquely identifies an object in a bucket.
   - Object keys imply a logical hierarchy through prefixes and delimiters, presenting a folder structure.

### Use Cases

Amazon S3 caters to various use cases, including:
1. Backup and Storage
2. Media Hosting
3. Software Delivery
4. Data Lakes
5. Static Websites
6. Static Content

## Security

- **Default Privacy:** All S3 resources are private by default.
- **Access Control:** Granular access provided through IAM policies, S3 bucket policies, and encryption.
- **IAM Policies:** Applied to resources or IAM users/groups/roles for defining allowed actions.
- **S3 Bucket Policies:** JSON-defined policies attached to S3 buckets for specifying allowed/denied actions.
- **Encryption:** Automatic encryption at rest and in transit, supporting server-side encryption with S3-managed keys.

## Storage Classes

Amazon S3 offers diverse storage classes to adapt to changing data characteristics:
- **S3 Standard:** General-purpose storage for various applications.
- **S3 Intelligent-Tiering:** Adapts to unknown/changing access patterns.
- **S3 Standard-Infrequent Access (S3 Standard-IA):** High durability, throughput, and low latency for infrequent access.
- **S3 One Zone-Infrequent Access (S3 One Zone-IA):** Lower-cost option with storage in a single Availability Zone.
- **S3 Glacier Instant Retrieval:** Fast retrieval for rarely accessed data.
- **S3 Glacier Flexible Retrieval:** Low-cost storage with expedited retrieval options.
- **S3 Glacier Deep Archive:** Lowest-cost storage for long-term retention, ideal for regulatory compliance.
- **S3 on Outposts:** Object storage for on-premises AWS Outposts environment.

## Versioning

- **Object Identification:** Uses unique version IDs to differentiate between object versions.
- **Benefits:** Preserves old versions, aids recovery from accidental deletions/overwrites.
- **Use Cases:** Common names, version preservation, and recovery from accidental actions.

## Managing Storage Lifecycle

Automate object transitions and expirations through lifecycle configuration:
- **Transition Actions:** Define when objects move to another storage class.
- **Expiration Actions:** Define when objects expire and should be permanently deleted.
- **Use Cases:** Periodic logs, data with changing access frequency.
