# Auto Shutdown AWS EC2 Using Lambda

## Introduction

Running EC2 instances for long hours can increase AWS costs, especially while practicing or working on test environments. Instead of stopping instances manually from the AWS console every time, this project shows a better and more practical approach.

In this project, I used AWS Lambda to stop running EC2 instances by triggering a Lambda function manually. This helps reduce unnecessary cloud costs and also demonstrates how serverless automation can be used for basic infrastructure management, which is commonly expected in DevOps and MNC environments.

## Requirements

AWS EC2

AWS Lambda (Python 3.10)

AWS IAM

Python (boto3)

Git & GitHub

## Steps of Deployment

### step1 - Launch EC2 Instance

Create an EC2 instance using Amazon Linux to test the shutdown automation.

![auto1](./images/auto%201.png)

### step2 - Create IAM Role

Create an IAM role for Lambda and attach the following policies:

    AmazonEC2FullAccess

This role allows Lambda to stop EC2 instances and write logs.

![auto2](./images/auto%202.png)

Here, we have attached a policy to the role.

![auto3](./images/auto%203.png)

![auto4](./images/auto%204.png)

Here, we have successfully created a role.

![auto5](./images/auto%205.png)

### step3 - Create Lambda Function

Create a Lambda function

Runtime: Python 3.10

Attach the IAM role created earlier

![auto6](./images/auto%206.png)

![auto7](./images/auto%207.png)

### step4 - Add Python Code

Add Python code in the Lambda function to:

Identify running EC2 instances

Stop those EC2 instances using AWS SDK (boto3)

![auto8](./images/auto%208.png)

### step5 - Deploy the Function

Deploy the Lambda function after adding the code.

![auto9](./images/auto%209.png)

### step6 - Test the Lambda Function

Run a test event from the Lambda console.

![auto10](./images/auto%2010.png)

Here, testing of code is succeed.

### step7 - Output

Here, our ec2 instance is stopping.

![auto11](./images/auto%2011.png)

And finally here ec2 instance is stopped by using aws lambda function.

![auto12](./images/auto%2012.png)

## Conclusion

This project helped me understand how AWS Lambda can be used to automate EC2 management tasks. By stopping EC2 instances using a Lambda function, I learned how serverless automation can reduce manual effort and help control cloud costs. This project reflects a practical and real-world approach to cloud cost optimization.