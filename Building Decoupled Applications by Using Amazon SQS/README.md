Project Overview


This project involves building an image processing application that transforms images by applying a tint. The architecture transitions from a tightly coupled model to a decoupled architecture using Amazon SQS and Amazon SNS.




Start Architecture

At the beginning of this project, the architecture follows a tightly coupled model:



✅ The web application checks for images.

✅ The user uploads an image via the web application.

✅ The web server stores the image in an S3 bucket and updates its metadata in an Amazon DynamoDB table.

✅ The web server initiates synchronous processing on the application server and waits for the tinted image to be available.

✅ The processed image becomes available to the user.


![Start Architecture](https://github.com/LizaImmax/AWS-Cloud-Projects/blob/main/Building%20Decoupled%20Applications%20by%20Using%20Amazon%20SQS/images/Start%20Architecture.png)



![Phase 1 Architecture](https://github.com/LizaImmax/AWS-Cloud-Projects/blob/main/Building%20Decoupled%20Applications%20by%20Using%20Amazon%20SQS/images/Phase%201%20-Tightly%20Coupled.png)


Final Architecture (Decoupled Architecture)


By the end of this project, the architecture transitions to a decoupled model:



✅ The user starts the web application, which checks for images.

✅ The user uploads an image through the web application.

✅ The web application writes the image to an S3 bucket and updates its metadata in DynamoDB.

✅ Once the image is stored, an S3 event triggers a notification to an SNS topic.

✅ The SNS topic has two subscribers:

✅ It publishes a message to an SQS queue.

✅ It sends an email notification to subscribed users.

✅ The application server polls the SQS queue for new messages.

✅ Upon receiving a message, the application server retrieves the image from S3, processes it (tinting and resizing), and updates its status in DynamoDB.

✅ The processed image is displayed to the user.




![Final Architecture](https://github.com/LizaImmax/AWS-Cloud-Projects/blob/main/Building%20Decoupled%20Applications%20by%20Using%20Amazon%20SQS/images/Final%20Architecture-%20Loosely%20Coupled.png)





Technologies Used

✅ Amazon S3 (Storage for images)

✅ Amazon SNS (Notification service)

✅ Amazon SQS (Message queue for decoupling components)

✅ Amazon DynamoDB (Database for metadata storage)

✅ AWS Cloud9 (IDE for development)

✅ Node.js (Application runtime)

How to Run the Project

✅ Set up an AWS Cloud9 instance.

✅ Clone the project repository.

✅ Deploy the initial web application.

✅ Implement SNS and SQS for event-driven communication.

✅ Test image uploads and monitor processing.

This project demonstrates the power of event-driven architectures in cloud applications, ensuring better performance, reliability, and scalability.
