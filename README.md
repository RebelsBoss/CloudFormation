# CloudFormation
## Overview pipline :
### 1. Network :
a. Create VPC. 
b. Create 2 private and 2 public subnets in VPC.
c. Create Internet Gateway and attach to public subnets.
d. Create 2 NAT Gateway and attach to private subnets.
e. Create 2 ElasticIPs attach with 2 NAT Gateway.
f. Writte route tables.
g. Create Security groups.
h. Create Endpoints for CI/CD process and attach with service.
### 2. IAM :
      a. Create roles for CI/CD process and attach with services.
### 3. EC2 :
      a. Create public and private template for Auto Scaling Groups with custom user data scripts (For reCAPTCHA Enterprise to work, create it in GCP and enter the sitekey).
      b. Create public and private Auto Scaling Groups with CPU policy.
      c. Create ClassicLB attach with public subnets.
### 4. S3 :
      a. Create S3.
### 5. CI/CD process :
      a. Create CodeBuild.
      b. Create CodeDeploy.
      c. Create CodePipeline.
      
## Install [aws cli](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html) and write in terminal :
```
aws config
```
```
git clone https://github.com/RebelsBoss/CloudFormation.git
```
```
aws cloudformation create-stack --stack-name [enter name stack] --template-body file://[enter path file.yaml] --capabilities CAPABILITY_NAMED_IAM

```
