Café Web Application - Scalable and Highly Available Architecture



Overview

This project involves building a scalable and highly available architecture for the café's web application. The café’s website is expected to experience a significant increase in traffic after being featured on a popular TV food show. To ensure a smooth user experience, the architecture will be designed to handle fluctuating traffic, remain responsive, and distribute customer orders across multiple servers.

The architecture will be built on AWS using Elastic Load Balancing (ELB) and Amazon EC2 Auto Scaling to automatically adjust resources based on demand.



Objectives


Inspect the existing Virtual Private Cloud (VPC) and update it to work across multiple Availability Zones.

Set up an Application Load Balancer (ALB) to distribute incoming traffic across multiple EC2 instances.

Create a Launch Template to automate EC2 instance deployment.

Implement an Auto Scaling Group to scale resources dynamically based on traffic.

Set up alarms to trigger scaling actions based on system metrics.

Test the architecture for load balancing and automatic scaling functionality.


Architecture



Initial Architecture


At the start of the project, the architecture consists of the following:

A single EC2 instance running the café’s web server.

The web server is deployed in one Availability Zone (AZ).

Elastic Load Balancer (ELB) is not yet in use.

This basic setup can handle some traffic, but it won't scale well with the expected surge in visitors.


![Image Description](https://github.com/LizaImmax/AWS-Cloud-Projects/blob/main/Creating%20a%20Scalable%20and%20Highly%20Available%20Environment%20for%20the%20cafe/images/starting-architecture.png)




Final Architecture


The final architecture includes the following:

Multiple Availability Zones (AZs): The network is updated to span across two or more AZs, ensuring high availability.

Elastic Load Balancer (ELB): An Application Load Balancer (ALB) is used to distribute incoming traffic across multiple EC2 instances in different AZs.

EC2 Instances: The web application is deployed on EC2 instances across multiple AZs, ensuring redundancy.

Auto Scaling Group: An Auto Scaling group is configured to add or remove EC2 instances based on incoming traffic, ensuring that resources are always adequate to meet demand.

Alarms: Alarms are set on key system metrics (e.g., CPU usage) to trigger scaling actions.



![Image Description](https://github.com/LizaImmax/AWS-Cloud-Projects/blob/main/Creating%20a%20Scalable%20and%20Highly%20Available%20Environment%20for%20the%20cafe/images/final-architecture.png)



This architecture ensures that the café’s website can scale up or down based on real-time demand, providing a reliable and responsive experience for users.



Steps to Implement

Inspect and Update the VPC: Review the current VPC and configure it to work across multiple Availability Zones.

Set Up the Application Load Balancer (ALB): Create an ALB to distribute incoming traffic across the EC2 instances.

Create Launch Template: Configure a Launch Template that defines the settings for the EC2 instances.

Create an Auto Scaling Group: Set up an Auto Scaling group to automatically scale EC2 instances based on traffic.

Set Alarms: Configure CloudWatch alarms to trigger scaling actions based on CPU usage or other system metrics.

Test Load Balancing and Scaling: Simulate high traffic and verify that the system scales correctly and balances the load across instances.



Testing and Validation

Once the architecture is set up, the following tests should be conducted:


Traffic Simulation: Simulate heavy traffic to test the load balancing and auto-scaling functionality.

System Metrics Monitoring: Monitor the system to ensure that the Auto Scaling group is scaling correctly in response to traffic changes.

High Availability Verification: Test that the application remains available even if one of the Availability Zones goes down.


Conclusion


By implementing this scalable and highly available architecture, the café’s web application will be able to handle a significant increase in traffic, ensuring a smooth and reliable user experience. The architecture can also be scaled down when traffic decreases, optimizing costs while maintaining availability.


