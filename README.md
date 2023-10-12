# AWS CDK Stack
This AWS CDK stack deploys an environment for hosting a .NET API, a React frontend, and an RDS PostgreSQL database. It sets up the necessary infrastructure and configurations to run these components on AWS Elastic Beanstalk.

## Prerequisites

Before deploying this stack, ensure that you have the following:

- AWS CDK installed and configured. If not, follow the [AWS CDK Getting Started](https://docs.aws.amazon.com/cdk/latest/guide/getting_started.html) guide.

## Getting Started

1. Clone this repository and navigate to the project directory:

   ```bash
   git clone https://github.com/hahmad748/cdk-beanstalk-postgres.git


2. Open the lib/CdkBeanstalkPostgresStack.cs file and update the following placeholders:

<path_to_api_artifact>: Replace with the local path to the build/deployment artifact of your .NET API.
<path_to_frontend_artifact>: Replace with the local path to the build/deployment artifact of your React frontend.
<your_api_base_url>: Replace with the base URL of your .NET API.
Review and customize other configuration settings such as RDS instance size, storage, database credentials, etc., as needed.

3. Build and deploy the AWS CDK stack:
```cdk deploy CdkBeanstalkPostgresStack```
4. After the deployment is complete, AWS CDK will provide you with a URL for the Elastic Beanstalk environment.
# Architecture
This stack deploys the following components:

- Elastic Beanstalk Application and Environment for hosting your .NET API and React frontend.
- RDS PostgreSQL database for storing data.
- Security group rules to allow communication between the Elastic Beanstalk environment and the RDS instance.
- Environment variables to pass RDS connection details to the Elastic Beanstalk environment.


# Contributing
Feel free to contribute to this project or report issues by creating a GitHub issue.

# License
This project is licensed under the MIT License. See the LICENSE file for details.

# Acknowledgments
[AWS CDK Documentation](https://docs.aws.amazon.com/cdk/)
[AWS Elastic Beanstalk Documentation](https://github.com/aws-samples/aws-cdk-examples/tree/master/csharp/elasticbeanstalk)
[Amazon RDS Documentation](https://github.com/aws-samples/aws-cdk-examples/tree/master/csharp/)


## Useful commands

* `dotnet build src` compile this app
* `cdk deploy`       deploy this stack to your default AWS account/region
* `cdk diff`         compare deployed stack with current state
* `cdk synth`        emits the synthesized CloudFormation template

@hahmad748 @devsfort