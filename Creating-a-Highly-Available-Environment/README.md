High Availability in AWS



Project Overview



Critical business systems must remain operational even when some components fail. In AWS, to achieve high availability, applications should be deployed across multiple Availability Zones. Many AWS services, such as Load Balancers, are inherently highly available, while others, like Amazon EC2 instances, can be configured for high availability.

In this lab, we start with an application running on a single EC2 instance and enhance it to become highly available by deploying it across multiple Availability Zones. The goal is to ensure that even if some parts of the system fail, the application will continue to operate.




Objectives



After completing this lab, I should be able to:

Inspect a provided Virtual Private Cloud (VPC).
Create an Application Load Balancer.
Create an Auto Scaling group.
Test the application for high availability.




At the end of this lab, the architecture will look like the following example:
