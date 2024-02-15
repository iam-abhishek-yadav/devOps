
## Google Cloud Resource Hierarchy

Google Cloud's functional structure follows a four-level resource hierarchy:

### 1. Resources
- Represent virtual machines, Cloud Storage buckets, and other entities.
  
### 2. Projects
- Basis for enabling and using Google Cloud services.
- Separate entities under the organization node.
- Identified by a project ID, name, and number.
- Managed independently with different owners and users.

### 3. Folders
- Allow assignment of policies at a chosen level of granularity.
- Inherited policies and permissions by resources within.
- Can contain projects, other folders, or a mix of both.
- Facilitate grouping resources based on departments or teams.
- Delegation of administrative rights for independent work.

### 4. Organization Node
- Top-level encompassing all projects, folders, and resources.
- Special roles like organization policy administrator and project creator.
- Creation depends on Google Workspace domain or use of Cloud Identity.

