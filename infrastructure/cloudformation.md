# AWS CloudFormation Cheatsheet (Latest LTS)

AWS CloudFormation is an Amazon Web Services (AWS) service that helps you model and set up your Amazon Web Services resources so you can spend less time managing those resources and more time focusing on your applications that run in AWS.

## Terminology

- Stack: a collection of AWS resources created together
- Template: a JSON or YAML file that describes the AWS resources and how they are connected
- Resource: an AWS component that represents a single item, such as an EC2 instance or an S3 bucket
- Parameter: a value that is passed into a CloudFormation template when a stack is created
- Output: a value that is returned after a stack is created

## Basic Syntax

Here's an example of a basic CloudFormation template in YAML format:

```yaml
---
AWSTemplateFormatVersion: "2010-09-09"
Resources:
  S3Bucket:
    Type: "AWS::S3::Bucket"
    Properties:
      BucketName: my-bucket-name
```

## Resources

A resource section is required in every CloudFormation template. It describes all the AWS resources that you want to create.

```yaml
Resources:
  EC2Instance:
    Type: "AWS::EC2::Instance"
    Properties:
      ImageId: ami-0c55b159cbfafe1f0
      InstanceType: t2.micro
```

## Parameters

A parameter section is optional in a CloudFormation template, but allows you to pass values into the template when you create or update a stack.

```yaml
Parameters:
  KeyName:
    Type: String
  InstanceType:
    Type: String
    Default: t2.micro
```

## Outputs

An output section is optional in a CloudFormation template, but can be used to display data to the user after a stack has been created.

```yaml
Outputs:
  InstanceId:
    Description: The instance ID
    Value: !Ref EC2Instance
    Export:
      Name: InstanceId
```

## Conclusion

This is just a brief overview of the AWS CloudFormation service and its basic syntax. For more information, you can check out the [Official AWS Documentation.](https://aws.amazon.com/cloudformation/)
