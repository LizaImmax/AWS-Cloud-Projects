Implementing a Serverless Architecture for the Café

Project Description

This project implements a serverless architecture to automate the generation of daily sales reports for a café. The solution uses AWS Lambda, Amazon RDS, and Amazon SNS to fetch, process, and email the reports.



Start Architecture 

![Starting Architecture](https://github.com/LizaImmax/AWS-Cloud-Projects/blob/main/Implementing%20a%20Serverless%20Architecture%20for%20the%20Caf%C3%A9/images/starting-architecture.png)





Finish Architecture
![Final Architecture](https://github.com/LizaImmax/AWS-Cloud-Projects/blob/main/Implementing%20a%20Serverless%20Architecture%20for%20the%20Caf%C3%A9/images/final-architecture.png)


Features

✅ AWS Lambda function to generate sales reports.
✅ Automated scheduling using Amazon CloudWatch.
✅ Secure database access within a VPC.
✅ Email report delivery via Amazon SNS.

Prerequisites

To run this project, ensure you have:
✅ An AWS account.
✅ An existing Amazon RDS instance containing the café's sales data.
✅ AWS CLI configured with appropriate IAM permissions.
✅ Python 3.x installed (for local development and testing of Lambda code).

Setup and Deployment

Create the AWS Lambda Function: ✅

Write a Python script to query the RDS database and generate the sales report.

Deploy the script as a Lambda function.

Attach the necessary IAM role with access to RDS and SNS.

Configure the VPC Access: ✅

Assign the Lambda function to the appropriate VPC.

Ensure the security group allows outbound access to the RDS instance.

Set Up Amazon SNS: ✅

Create an SNS topic.

Subscribe the stakeholders' email addresses to the topic.

Update the Lambda function to publish messages to SNS.

Schedule the Lambda Execution: ✅

Create a CloudWatch rule to trigger the Lambda function daily.

Ensure the rule is correctly linked to the Lambda function.

Testing

✅ Run the Lambda function manually to check if it correctly retrieves and formats the report.
✅ Verify the SNS email delivery.
✅ Inspect CloudWatch logs for any errors or performance issues.

Future Enhancements

✅ Store the generated reports in an Amazon S3 bucket for historical access.
✅ Implement a dashboard using Amazon QuickSight for real-time sales insights.
✅ Enhance error handling and monitoring with AWS X-Ray and custom CloudWatch alarms.

Author

This project was implemented by me as part of a hands-on challenge to optimize the café's reporting process using serverless technologies.

License

This project is open-source and available for further development and customization.
