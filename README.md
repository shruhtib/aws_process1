
# Deploying Cloudformation to create lambda which respective role

Cloudformation template to read parameter store and store the details in S3

### Services Used:

Services Used:
 
 * [AWS CloudFormation](https://aws.amazon.com/cloudformation/) for deploying infrastructure (Infrastructure-as-Code).
 * [AWS Lambda](https://aws.amazon.com/lambda/) to process the ec2 instances. 
 * [AWS S3](https://aws.amazon.com/s3/) to store the instance information. 

### Requirement:
Create a Cloudformation template which deploys a lambda function which reads the already stored parameter store values and stores the same in S3 bucket. 


### Infrastructure as code

[AWS CloudFormation](https://aws.amazon.com/cloudformation) will be used to deploy python application on AWS.


### Prerequisite

 * Create a parameter in parameter store with key and value
 * Have a S3 bucket created


### How it works :

After the creation of Parameter and S3 bucket, Clouformation template should be deployed in the console. This template deploys the lambda and respective role for it. Lambda is created as an inline function in this.

A cloudformation custom resource will be called in order to trigger the lambda.
