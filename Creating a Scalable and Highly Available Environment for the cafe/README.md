☕ Café Web Application - Scalable and Highly Available Architecture 🚀

📌 Overview
This project focuses on building a scalable and highly available architecture for the café's web application. With the café set to be featured on a popular TV food show, we expect a massive traffic spike. The solution ensures:

✅ Scalability – Automatically adjusts resources based on demand.
✅ High Availability – Remains operational across multiple Availability Zones.
✅ Load Distribution – Efficiently distributes customer requests across multiple servers.

This is achieved using AWS services like:

Elastic Load Balancing (ELB) to balance incoming traffic.
Amazon EC2 Auto Scaling to dynamically manage resources.


🎯 Objectives


✔️ Inspect & Update the VPC to span multiple Availability Zones.
✔️ Deploy an Application Load Balancer (ALB) for efficient traffic distribution.
✔️ Create a Launch Template for automated EC2 instance deployment.
✔️ Configure an Auto Scaling Group to scale up/down based on demand.
✔️ Set up CloudWatch Alarms to trigger scaling actions.
✔️ Perform Load Testing to validate auto-scaling & high availability.

🏗️ Architecture

🔹 Initial Architecture (Before Scaling)

🛑 Single EC2 instance running the café’s web server.
🛑 Hosted in only one Availability Zone (AZ) (single point of failure).
🛑 No Elastic Load Balancer (ELB) – unable to distribute traffic efficiently.

⛔ This setup struggles under heavy load and isn’t resilient!

![Image Description](https://github.com/LizaImmax/AWS-Cloud-Projects/blob/main/Creating%20a%20Scalable%20and%20Highly%20Available%20Environment%20for%20the%20cafe/images/starting-architecture.png)


✅ Final Scalable Architecture

✔️ Multi-AZ Deployment – Resources span across at least two Availability Zones.
✔️ Application Load Balancer (ALB) – Spreads traffic evenly across instances.
✔️ Auto Scaling Group (ASG) – Dynamically adjusts EC2 instances based on traffic.
✔️ CloudWatch Alarms – Triggers scaling based on CPU utilization & other metrics.
✔️ Improved Redundancy & High Availability – No single point of failure!

🖼️![Image Description](https://github.com/LizaImmax/AWS-Cloud-Projects/blob/main/Creating%20a%20Scalable%20and%20Highly%20Available%20Environment%20for%20the%20cafe/images/final-architecture.png) 


🛠️ Steps to Implement

🔲 Step 1: Inspect & Update the VPC

Ensure the VPC spans multiple Availability Zones for redundancy.

🔲 Step 2: Set Up the Application Load Balancer (ALB)

Create an ALB to distribute traffic across EC2 instances.

🔲 Step 3: Create a Launch Template

Define a Launch Template to standardize EC2 instance deployment.

🔲 Step 4: Configure an Auto Scaling Group

Set up Auto Scaling to maintain optimal performance under fluctuating traffic.

🔲 Step 5: Configure CloudWatch Alarms

Set up alarms based on CPU usage, request count, and latency to trigger scaling.

🔲 Step 6: Perform Load Testing

Simulate heavy traffic and observe automatic scaling in action!



✅ Testing & Validation

📌 Traffic Simulation: Generate artificial load to test scaling & load balancing.

📌 Monitor System Metrics: Use CloudWatch to observe scaling events.

📌 High Availability Test: Simulate an AZ failure and verify app uptime.


🏆 Conclusion

By implementing this scalable and highly available architecture:

✅ The café’s website is ready to handle high traffic volumes.
✅ The system automatically scales up during peak demand & scales down to save costs.
✅ Zero downtime & high availability ensure an uninterrupted customer experience.

🎉 Now, the café team can focus on preparing amazing coffee ☕ while AWS handles the scaling! 🚀




