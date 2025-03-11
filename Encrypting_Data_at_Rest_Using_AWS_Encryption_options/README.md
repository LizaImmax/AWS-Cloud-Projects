Encrypting Data at Rest Using AWS Encryption Options


Overview and Objectives

In this project, I explore how AWS provides encryption options to secure data at rest. I review the default encryption for Amazon S3 objects, create an AWS KMS customer-managed key to encrypt Amazon EBS volumes, and observe how AWS CloudTrail logs key usage for auditing.

After completing this project, I will be able to:
✅ Review the default encryption provided by Amazon S3.
✅ Access encrypted Amazon S3 objects.
✅ Create an AWS KMS customer-managed key to encrypt and decrypt data at rest.
✅ Create and attach an encrypted data volume to an EC2 instance.
✅ Disable and re-enable an AWS KMS key and observe its effects on data access.
✅ Monitor encryption key usage through CloudTrail event history.
✅ Review key rotation.



Duration
⏳This project took me 1 hour.



AWS Service Restrictions
In this project, access to AWS services may be restricted to only those necessary to complete the steps. Attempting to access other services or perform actions beyond those outlined here may result in errors.



Project Scenario

I start with the following architecture:

An S3 bucket to store images.
An EC2 instance for testing encryption.
An AWS KMS key for encrypting data.
By the end of the project, I will have:



Created an encrypted Amazon EBS volume and attached it to my EC2 instance.
Used AWS KMS to encrypt and decrypt data securely.
Observed CloudTrail logs capturing encryption key usage.
Architecture


Initial Setup
📌 Before starting, my environment includes an S3 bucket and an EC2 instance.
(Insert Image 1 here)

Final Architecture
📌 By the end, my EC2 instance will use an encrypted EBS volume, AWS KMS for key management, and CloudTrail for monitoring key access.
(Insert Image 2 here)

Steps
🔹 Step 1: Attach an encrypted EBS volume to my EC2 instance. The instance receives an encrypted data key from the volume.

🔹 Step 2: The EC2 instance sends a request to AWS KMS to decrypt the encrypted data key.

🔹 Step 3: AWS KMS validates my user and role permissions and returns the plain data key.

🔹 Step 4: My EC2 instance stores the key in memory and uses it for encryption and decryption.

Conclusion
By completing this project, I have successfully implemented encryption at rest using AWS services. I now understand how AWS KMS integrates with EC2 and S3, how encryption keys work, and how CloudTrail logs encryption activity for auditing.


