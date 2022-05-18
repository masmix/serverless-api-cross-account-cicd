# Build CI/CD Pipeline for Cross Account Deployment of Lambda API Using Serverless Framework

# Reference Architecture: Cross Account AWS CodePipeline 

This reference architecture demonstrates how to push code hosted in [AWS CodeCommit](https://aws.amazon.com/codecommit/) repository in Development Account,
use [AWS CodeBuild](https://aws.amazon.com/codebuild/) to do application build, store the output artifacts in S3Bucket and deploy these artifacts to a Test AWS account, validate your deployment then approve the changes to be deployed to the Production Account using [AWS CloudFormation](https://aws.amazon.com/cloudformation/). This orchestration of code movement from code checkin to deployment is securely handled by [AWS CodePipeline](https://aws.amazon.com/codepipeline/).

## Introduction

In this project we are going to be implementing cross account deployment strategy explained in [this](https://aws.amazon.com/blogs/devops/aws-building-a-secure-cross-account-continuous-delivery-pipeline/) blog to deployment of Lambda based API’s using third party [Serverless](https://www.serverless.com/) framework.

![](images/CrossAccountServerlessDeployment.png)

#### Pre-requisites 
1. Install the [AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-install.html).
2. Intall the [SAM CLI](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-cli-install.html).
3. Clone this repository.
4. Have the following AWS accounts (if using Control Tower, [this is useful](https://docs.aws.amazon.com/controltower/latest/userguide/account-factory.html#quick-account-provisioning)):
    * Tooling - Source 
    * Development - Target 
5. Create permissions for tools account (optional)

## License

This library is licensed under the MIT-0 License. See the LICENSE file.

