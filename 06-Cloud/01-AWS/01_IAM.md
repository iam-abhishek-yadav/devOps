## IAM (AWS Identity and Access Management)

- Manages access to AWS account and resources.
- Centralized view of authentication (who/what is allowed) and authorization (permissions).
- Allows sharing access without sharing keys/passwords.

## IAM Features

  - Global
  - Integrated with AWS services
  - Shared access
  - Multi-factor authentication
  - Free to use

### IAM User

- Represents a person or service interacting with AWS.
- Billed to your account for any activity.
- IAM user credentials include access to the AWS Management Console and programmatic access to AWS CLI and API.

### IAM User Credentials

- Permanent credentials, stay with the user until forced rotation by admins.
- Types of access:
  - AWS Management Console (username and password)
  - Programmatic access (access keys for AWS CLI and API)

### IAM Groups

- Collection of users sharing inherited permissions.
- More convenient and scalable way of managing permissions.
- Best practice for organizing users in AWS accounts.

### IAM Policies

- IAM policies manage access and provide permissions.
- Attached to IAM identities (users, groups, roles).
- Evaluated when an IAM identity makes a request.

#### IAM Policy Examples

- Admin Access Policy (Allow all actions on all resources):

```json
{
  "Version": "2012-10-17",
  "Statement": [{
    "Effect": "Allow",
    "Action": "*",
    "Resource": "*"
  }]
}
```
-   Granular S3 Access Policy (Deny S3 access outside specified AWS account):


```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "DenyS3AccessOutsideMyBoundary",
      "Effect": "Deny",
      "Action": ["s3:*"],
      "Resource": "*",
      "Condition": {
        "StringNotEquals": {
          "aws:ResourceAccount": ["222222222222"]
        }
      }
    }
  ]
}
```

### IAM Roles

IAM roles play a crucial role in managing access to AWS resources, especially when dealing with entities like IAM users, groups, and policies. Below are key points related to IAM roles:

- IAM roles provide a secure way to grant permissions to trusted entities.
- Unlike IAM users, roles are not associated with specific users or groups but can be assumed by anyone who needs temporary access to AWS credentials.
- For applications running on Amazon EC2 instances, IAM roles come into play. These roles allow the application to gain access to temporary AWS credentials to sign API calls.
- IAM roles have associated AWS credentials used for signing requests. However, unlike IAM users, roles do not have login credentials like a username and password.
- IAM role credentials are programmatically acquired, temporary, and automatically rotated for enhanced security.
- In scenarios where an EC2 instance needs to sign requests to AWS services, assigning an IAM role to the instance is a common practice.
- IAM roles can be assumed by various identities, and they serve many use cases. It's important to note that the credentials provided by roles expire, and roles are assumed programmatically.
- IAM roles are often used for access between AWS services. They facilitate role-based access, allowing one AWS service to assume a role, gain temporary credentials, and send API calls to another AWS service.
- External identity providers can also assume IAM roles to gain access to AWS. This is useful for scenarios where existing enterprise user directories need to be leveraged to grant access to AWS resources.

### IAM Best Practices

- Lock down the AWS root user
- Follow the principle of least privilege
- Use IAM appropriately
- Use IAM roles when possible
- Consider using an identity provider
- Regularly review and remove unused users, roles, and other credentials
