# AWS S3 File Gateway Project

## 📘 Overview

This project implements an Amazon S3 File Gateway to enable on-premises applications to store files in Amazon S3 via a Network File System (NFS) interface. It demonstrates how to integrate local storage infrastructure with AWS cloud storage for scalable, durable, and cost-effective file storage.






(https://github.com/LizaImmax/AWS-Cloud-Projects/blob/main/Configuring%20Hybrid%20Storage%20and%20Migrating%20Data%20with%20AWS%20Storage%20Gateway%20S3%20File%20Gateway/images/mod16-arc.png)
---

## 🚀 Goals

- Deploy S3 File Gateway as an EC2 instance.
- Configure cache storage and IAM permissions.
- Create and mount an NFS file share on a Linux instance.
- Migrate image data from the local server to S3.
- Verify data replication across S3 buckets using S3 replication.

---

## 🛠️ Components Used

- **Amazon EC2**: To host the S3 File Gateway appliance.
- **Amazon S3**: For storing and replicating files.
- **IAM**: To control access to the S3 bucket.
- **Amazon VPC & Security Groups**: For network and access management.
- **Amazon CloudWatch** *(optional)*: For monitoring (disabled in this lab).
- **AWS Systems Manager Session Manager**: To securely connect to the Linux instance.

---

## 🧩 Project Structure

### Step 1: Deploy the S3 File Gateway Appliance
- Launch EC2 instance with `aws-storage-gateway` AMI.
- Configure VPC, subnet, public IP, and security groups.
- Attach an additional 150 GiB volume for cache storage.

### Step 2: Activate the Gateway
- Access the EC2 public IP through Storage Gateway Console.
- Connect to AWS and activate the gateway.

### Step 3: Create and Configure the File Share
- Configure file share settings with the source S3 bucket.
- Use NFS protocol and existing IAM role with required policies.

### Step 4: Mount NFS on Linux Instance
- Use the provided `mount` command to mount the file share.
- Verify using `df -h`.

### Step 5: Migrate Data to S3
- Copy image files (`.png`) from local directory to mounted share.

### Step 6: Verify Data Migration and Replication
- Confirm data appears in source S3 bucket (Ohio).
- Validate replication to destination S3 bucket (N. Virginia).

---




