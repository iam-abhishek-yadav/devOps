## AWS Fargate
AWS Fargate is a purpose-built serverless compute engine for containers, providing a seamless experience for developers by abstracting the underlying EC2 instances. This allows developers to focus on application development without the burden of managing infrastructure. Fargate integrates natively with various AWS services and concepts, such as IAM and Amazon VPC.

### Key Features
- **Abstraction of EC2 Instances:** Fargate eliminates the need to manage and choose specific EC2 instances, streamlining the deployment process.
- **Integration with Amazon ECS:** Fargate seamlessly integrates with Amazon ECS, allowing for a consistent experience with ECS concepts, APIs, and AWS integrations.
- **Native Integration with Amazon VPC:** Leveraging the native integration with Amazon VPC, Fargate enables the launch of containers within your network, providing control over application connectivity.

### AWS Fargate Architecture

#### Workload Isolation and Security
Fargate ensures improved security by design, offering workload isolation and abstracting the complexities of managing EC2 instances. This allows developers to deploy containers in a secure and scalable manner.

#### Scalability and Infrastructure Management
One of the primary advantages of Fargate is its ability to scale and manage infrastructure dynamically. Developers no longer need to worry about cluster capacity, scaling, or choosing specific EC2 instances, as Fargate handles these aspects automatically.

### Use Cases
AWS Fargate is suitable for a variety of use cases, including but not limited to:
- **Application Development:** Developers can focus solely on building and improving applications, leaving the infrastructure management to Fargate.
- **Flexible Deployment:** Fargate supports both Amazon ECS and Amazon EKS architectures, providing flexibility in choosing the right container orchestration platform.


## AWS Lambda
AWS Lambda provides a serverless computing service that allows you to deploy workloads and applications without the need to manage EC2 instances or containers. It enables you to run code for various types of applications or backend services, including data processing, real-time stream processing, machine learning, WebSockets, IoT backends, mobile backends, and web applications.

### Key Features
- **Serverless Execution:** Lambda allows you to run code without provisioning or managing servers.
- **Broad Application Scope:** Suitable for a wide range of applications and backend services.
- **Language Support:** Lambda supports multiple languages for writing your source code.

### How Lambda Works
AWS Lambda operates based on the concept of Lambda functions. You can configure these functions using the Lambda console, Lambda API, AWS CloudFormation, or AWS Serverless Application Model (AWS SAM). Invoking a function can be done directly using the Lambda API or by configuring an AWS service or resource to trigger the function in response to an event.

#### Lambda Concepts
1. **Function:** The foundational principle of AWS Lambda where you define and execute your code.
2. **Trigger:** The event or source that initiates the execution of your Lambda function.
3. **Event:** The occurrence that triggers the execution of your Lambda function.
4. **Application Environment:** Configuration settings and variables for your Lambda function.
5. **Deployment Package:** The source code and its dependencies packaged for deployment.
6. **Runtime:** The programming language and version used for your Lambda function.
7. **Lambda Function Handler:** The method in your code that Lambda calls to start execution.

### Billing Granularity
Lambda offers a pay-as-you-go pricing model where you are charged for the number of invocations (requests) and the duration your code runs. The billing is rounded up to the nearest 1 millisecond of duration, with no minimum runtime. This cost-effective pricing makes it suitable for functions with low execution times, such as those under 100 ms or low latency APIs.

