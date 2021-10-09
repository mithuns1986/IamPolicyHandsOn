Lab 01: S3 read access
Introduction
During bootstrapping your EC2 instance needs to download several artifacts from S3. Therefore, you are using the AWS CLI to synchronize all objects from an S3 bucket with a local folder on your instance. Replace with the output S3Bucket of your CloudFormation stack.

Write an IAM policy that allows you to synchronize all objects from a specific S3 bucket.

aws s3 sync s3://<S3Bucket> ~/

Make sure, you don't allow access to any other S3 buckets.

Instructions
Open S3. Search for a bucket with a name equal to the S3Bucket output of your CloudFormation stack and upload a few files.
Open IAM.
Search an IAM role with a name equal to the IamRole output of your CloudFormation stack.
Add an inline policy to your IAM role.
Make sure you are logged into the SSH bastion host.
Now it is time to test weather the EC2 instance is allowed to list and download all objects from your S3 bucket.

aws s3 sync s3://<S3Bucket> ~/

Help
Actions, Resources, and Condition Keys for Amazon S3
policy.json includes a sample solution for the necessary IAM policy.
Clean up
Remove the inline policy from your IAM role.
