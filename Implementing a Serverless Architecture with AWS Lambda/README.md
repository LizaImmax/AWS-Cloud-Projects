Serverless Inventory Tracking System with AWS Lambda and SNS



Overview


This project demonstrates how to build a serverless inventory tracking system using AWS services. It uses AWS Lambda, Amazon S3, Amazon DynamoDB, and Amazon SNS to automate the process of tracking inventory. The system includes the following steps:


✅ A store uploads an inventory file to Amazon S3.

✅ An AWS Lambda function is triggered by the S3 upload event, which processes the inventory data and stores it in an Amazon DynamoDB table.

✅ Another Lambda function is triggered by changes in the DynamoDB table, checking inventory levels and sending a notification to an Amazon SNS topic if stock levels are low.

✅ Amazon SNS sends an SMS or email notification requesting additional inventory when an item is out of stock.

✅ A web-based dashboard displays inventory data from the DynamoDB table, with Amazon Cognito handling authentication.



Objectives

✅ Implement a serverless architecture on AWS.

✅ Integrate Lambda functions with Amazon S3 and DynamoDB to process and store inventory data.

✅ Set up Amazon SNS to send notifications when inventory is low.

✅ Build a web-based dashboard to view real-time inventory levels, using Amazon Cognito for authentication.


Steps to Set Up


Step 1: Setup S3 Bucket
✅ Create an S3 bucket to upload inventory files.

✅ Configure event notifications to trigger a Lambda function when a file is uploaded.


Step 2: Create Lambda Functions

✅ Create a Lambda function that is invoked by S3 upload events.

✅ Configure the function to process the inventory file and insert records into Amazon DynamoDB.


Step 3: DynamoDB Setup

✅ Create a DynamoDB table to store inventory data.

✅ Set up DynamoDB Streams to trigger a second Lambda function when a new item is inserted.


Step 4: Configure SNS for Notifications

✅ Set up an SNS topic for low inventory notifications.

✅ Create a Lambda function that monitors the DynamoDB table and sends a message to the SNS topic when inventory levels are low.


Step 5: Setup Dashboard

✅ Set up a web dashboard application to display inventory data.

✅ Use Amazon Cognito for authentication to restrict access to the dashboard.


Technologies Used

✅ AWS Lambda

✅ Amazon S3

✅ Amazon DynamoDB

✅ Amazon SNS

✅ Amazon Cognito

✅ AWS SDK


Architecture
This project follows a serverless architecture where each component works independently, and AWS services automatically scale with demand. The Lambda functions are triggered by S3 events and DynamoDB streams, ensuring that the application remains efficient and cost-effective.


![Final Architecture](https://github.com/LizaImmax/AWS-Cloud-Projects/blob/main/Implementing%20a%20Serverless%20Architecture%20with%20AWS%20Lambda/images/Final%20Architecture.png)


Conclusion

This system is a perfect example of how serverless technologies like AWS Lambda and Amazon S3 can be used to build scalable and cost-effective applications. It eliminates the need for managing physical infrastructure while providing a robust, fully automated solution for inventory management. The solution is designed to be highly available, fault-tolerant, and scalable, making it ideal for handling global inventory needs.
