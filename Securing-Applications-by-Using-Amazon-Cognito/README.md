Securing Applications with Amazon Cognito



Overview


User authentication and authorization can be complex in web applications. Amazon Cognito simplifies this process by providing seamless sign-up, sign-in, and access control mechanisms.

This project demonstrates how to integrate Amazon Cognito with a Node.js web application to manage user authentication and authorization.




Project Objectives
By the end of this project, you will:
✅ Create and configure an Amazon Cognito user pool for authentication.
✅ Add users to the user pool and enable sign-in.
✅ Integrate the user pool into the web application.
✅ Configure an Amazon Cognito identity pool for authorization.
✅ Allow authenticated users to interact with Amazon DynamoDB securely.



Architecture
Initial Setup:
The Birds Web Application is hosted using:
A Node.js server running on AWS Cloud9.
A static website hosted in Amazon S3.
The app tracks bird sightings and contains protected pages.




![Initial Architecture](https://github.com/LizaImmax/AWS-Cloud-Projects/blob/main/Securing-Applications-by-Using-Amazon-Cognito/images/Cognito-Start%20Architecture.png)

Adding Authentication with Cognito User Pool
Users sign in via Amazon Cognito’s managed UI.
Cognito validates credentials and returns an access token.
The app verifies the token before allowing access to protected pages.



![Intermediate Architecture](https://github.com/LizaImmax/AWS-Cloud-Projects/blob/main/Securing-Applications-by-Using-Amazon-Cognito/images/Cognito-Intermediate%20Architecture.png)



Final Architecture: Adding Authorization with Identity Pool
Cognito Identity Pools issue temporary AWS credentials to authenticated users.
These credentials allow users to securely access DynamoDB.




![Final Architecture](https://github.com/LizaImmax/AWS-Cloud-Projects/blob/main/Securing-Applications-by-Using-Amazon-Cognito/images/Cognito-Final%20Architecture.png)





Step-by-Step Guide
1️⃣ Set up an Amazon Cognito User Pool
2️⃣ Create an Identity Pool for Authorization
3️⃣ Modify the Web Application to Use Cognito for Authentication
4️⃣ Implement Identity Pool Authorization for DynamoDB Access
5️⃣ Test User Authentication & Access to Protected Pages





Technologies Used
AWS Cognito (User Authentication & Identity Management)
Amazon S3 (Static Website Hosting)
Node.js (Backend Server)
Amazon DynamoDB (Data Storage)
AWS Cloud9 (Development Environment)





Hands-on Experience & Benefits
✔️ Gain practical knowledge of AWS Cognito authentication & authorization.
✔️ Learn how to secure web applications effectively.
✔️ Understand token-based authentication in AWS.
