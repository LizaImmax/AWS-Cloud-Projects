
Breaking a Monolithic Node.js Application into Microservices


Project Overview

This project involves migrating a monolithic Node.js application into a microservices-based architecture. The application is a message board where users can create threads and post messages. By adopting microservices, I improved scalability, resilience, and maintainability.


Architecture


Monolithic vs. Microservices



Monolithic Architecture:

All application logic is in a single codebase.

A failure in one function can crash the entire application.

Scaling requires replicating the entire application.



Microservices Architecture:

Each function (thread creation, message posting, user management) is a separate service.

Services communicate via APIs and can be independently deployed and scaled.

More fault-tolerant—failure in one service doesn’t affect others.



![Alt Text](https://github.com/LizaImmax/AWS-Cloud-Projects/blob/main/Breaking%20a%20Monolithic%20Node.js%20Application%20into%20Microservices/Images/Application-design-monolith-to-microservices.png)



Technologies Used

Node.js – Backend framework

Docker – Containerization

Amazon ECS – Container orchestration

API Gateway – Managing API traffic

Load Balancer – Traffic distribution

MongoDB / PostgreSQL – Database (optional based on preference)


