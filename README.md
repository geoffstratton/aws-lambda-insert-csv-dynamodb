Repo Name
=========
aws-lambda-insert-csv-dynamodb

Description
---------------
AWS Lambda script for inserting CSV data into DynamoDB on S3 upload. Uses Python (tested with 3.7), Amazon's boto3 SDK, and a Lambda trigger.

Prerequisites
---------------
* The [boto3 SDK](https://aws.amazon.com/sdk-for-python/).
* Ensure that the IAM Role attached to the Lambda function has policies for S3 and DynamoDB access. AmazonS3FullAccess and AmazonDynamoDBFullAccess will certainly work.
* Ensure that the Lambda function is triggered by uploads to your S3 bucket.

### To set up boto3 for development (Amazon Linux and similar):
```
sudo yum install -y python3 python3-pip python3-setuptools
pip3 install boto3 --user
aws configure [enter your AWS access key and secret key]

python3
>>> import boto3
>>> ec2 = boto3.client('ec2')
>>> response = ec2.run_instances(ImageId='ami-00dc79254d0461090',InstanceType='t2.micro',KeyName='MY KEY',MinCount=1,MaxCount=1)
```
