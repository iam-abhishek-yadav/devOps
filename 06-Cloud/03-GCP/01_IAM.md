
## IAM (Identity and Access Management)

  - Used for managing access to resources in a Google Cloud organization.
  - Administrators apply policies to define who can perform specific actions on which resources.

- **Principals and Roles:**
  - **Principals ("who"):**
    - Can be a Google account, a Google group, a service account, or a Cloud Identity domain.
    - Each principal has a unique identifier, usually an email address.

  - **Roles ("can do what"):**
    - Defined collection of permissions.
    - When a role is granted to a principal, all the permissions within that role are granted.
    - Resulting policies apply to the chosen element and all elements below it in the hierarchy.

- **Deny Policies:**
  - Deny rules can prevent specific principals from using certain permissions.
  - IAM checks deny policies before allow policies.
  - Deny policies, like allow policies, are inherited through the resource hierarchy.

- **Role Types:**
  - **Basic Roles:**
    - Broad in scope.
    - Owner, Editor, Viewer, and Billing Administrator.
    - Project viewers can access but not modify resources.
    - Project editors can access and modify resources.
    - Project owners can manage roles, permissions, and billing.

  - **Predefined Roles:**
    - Specific sets of roles offered by Google Cloud services.
    - Example: Compute Engine's "instanceAdmin" role for managing virtual machines.
    - Defines where roles can be applied (project, folder, organization).

  - **Custom Roles:**
    - Created for more specific permissions.
    - Follows a "least-privilege" model.
    - Example: Creating an "instanceOperator" role with specific actions.
    - Custom roles can only be applied at the project or organization level, not the folder level.

- **Considerations:**
  - Basic roles might be too broad for projects with sensitive data.
  - IAM provides more tailored permissions for specific job roles.
  - Custom roles require managing the permissions and can only be applied at certain levels.

### Service Accounts
- Used to give permissions to Compute Engine virtual machines or applications. - Authenticates VMs to access specific resources. - Named with an email address and use cryptographic keys instead of passwords. 
-  **Managing Service Accounts:**  - Service accounts are resources with their own IAM policies. - Example: Alice can have the editor role on a service account, and Bob can have the viewer role. - Service accounts need to be managed for permissions and access control.

### Cloud Identity
-  Allows organizations to define policies and manage users/groups using Google Admin Console. - Admins can log in using user names and passwords from Active Directory or LDAP systems. - Provides centralized management for user access to cloud resources. 
-  **Benefits**  - When someone leaves, administrators can use the Google Admin Console to disable accounts and remove them from groups. - Available in a free edition and a premium edition with additional mobile device management capabilities. 
-  **Integration with Google Workspace:**  - If a Google Cloud customer is also a Google Workspace customer, Cloud Identity functionality is available in the Google Admin Console.
