CloudFormation Stack Deployment and Management 🚀

Welcome to my CloudFormation stack project! In this little adventure, I’ll walk you through using AWS CloudFormation to deploy, update, and delete resources—like an Amazon EC2 instance and security groups—while keeping it all as simple as possible. Think of it as my personal way of showing how to spin up infrastructure in the cloud without manually clicking buttons every five seconds. 🔧

Project Overview

Here’s what I’ll be doing (and what you can follow along with if you want to give this a shot):

✅ Deploy a network layer with a VPC and subnet. No fancy stuff here—just getting the foundation laid out.
✅ Deploy an application layer with an EC2 instance and security group, because every app needs somewhere to live and be protected, right?
✅ Update the stack to allow HTTPS traffic. It’s time for a little security—because no one likes HTTP-only sites. 🔒
✅ Explore AWS CloudFormation Designer. Yes, a fancy visual tool that makes templates look like art. Let’s check it out. 🎨
✅ Delete the stack but keep important things (like EBS volumes) safe with a snapshot. It’s like breaking up with a cloud resource but keeping the memories. 📸


Files Included

lab-application.yaml - My original CloudFormation template for the application.

lab-application2.yaml - The updated version that adds support for HTTPS (because why not?).


What I Do Here

I follow these steps to set everything up:


First, I deploy the network layer—VPC, subnet—nothing too wild.

Then, I set up the EC2 instance and the security group for the application layer.

I update the stack to make sure HTTPS is ready to roll. 🔐

I explore AWS CloudFormation Designer, just to make sure I’m not the only one who thinks this tool is cool. 😎

Finally, I delete the stack, but not before saving important data (in this case, the EBS volume) with a snapshot.







All of this should be manageable, and you’ll get a feel for managing infrastructure in the cloud without losing your mind. 😌
