# Lab 6 – Scale and Load Balance Your Architecture

## Title

Scale and Load Balance Your Architecture

## Author

* **Name**: Santhose Arockiaraj J
* **Register Number**: 212224230248
* **Date of Submission**: 28/08/2026


---

## Objective

The objective of this lab is to understand how to design a scalable and highly available architecture on AWS using Auto Scaling and Elastic Load Balancing. This experiment focuses on distributing incoming traffic across multiple EC2 instances, automatically scaling resources based on demand, and validating fault tolerance.

---

## Prerequisites

* Basic knowledge of Amazon EC2 and VPC
* Completion of previous labs (IAM, EC2, EBS, Database Server)
* AWS Academy Lab access
* Stable internet connection

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Elastic Load Balancer (ELB / ALB)
* Auto Scaling Groups (ASG)
* Amazon CloudWatch

---

## Tasks Performed

### Task 1: Review Existing Architecture

Students review the existing EC2-based application architecture created in previous experiments.

### Task 2: Create a Launch Template

Students create a launch template that defines the EC2 instance configuration including AMI, instance type, security group, and user data.

### Task 3: Create an Auto Scaling Group

Students create an Auto Scaling Group using the launch template and configure minimum, maximum, and desired instance capacity.

### Task 4: Configure an Application Load Balancer

Students create an Application Load Balancer and configure target groups for routing traffic to EC2 instances.

### Task 5: Register Auto Scaling Group with Load Balancer

Students attach the Auto Scaling Group to the target group of the load balancer.

### Task 6: Configure Scaling Policies

Students configure scaling policies based on CPU utilization using Amazon CloudWatch alarms.

### Task 7: Test Load Balancing and Scaling

Students test the setup by generating traffic and observing automatic scaling and load distribution.

---

## Workflow (To be filled by Student)

First, I reviewed the existing EC2 architecture that was created in previous experiments to understand how the application was deployed and how instances were configured.

Next, I created a Launch Template by selecting the required AMI, instance type, key pair, and security group. I also added user data to automatically install and run the application when the instance starts.

After that, I created an Auto Scaling Group using the launch template. I configured the minimum, maximum, and desired number of instances to ensure the application can scale automatically based on demand.

Then, I set up an Application Load Balancer (ALB) to distribute incoming traffic across multiple EC2 instances. I also created a target group and configured health checks to monitor instance status.

Next, I attached the Auto Scaling Group to the target group so that all instances created by the scaling group can receive traffic through the load balancer.

After that, I configured scaling policies using Amazon CloudWatch. I set rules to automatically increase or decrease the number of instances based on CPU utilization.

Finally, I tested the setup by generating traffic to the application and observed how the load balancer distributed traffic and how the Auto Scaling Group automatically added or removed instances based on demand.


---

## Output Screenshots 
<img width="1365" height="639" alt="Screenshot 2026-08-24 132845" src="https://github.com/user-attachments/assets/d497c812-415a-4104-989b-642b26cf5365" />

<img width="1365" height="647" alt="Screenshot 2026-08-24 133900" src="https://github.com/user-attachments/assets/66e6d64a-c89e-4b57-923e-542e09881be3" />

<img width="1365" height="642" alt="Screenshot 2026-08-24 134241" src="https://github.com/user-attachments/assets/1852fd5e-13ff-44ae-a59a-c69dbd262c45" />

<img width="1365" height="643" alt="Screenshot 2026-08-24 134653" src="https://github.com/user-attachments/assets/2191a45b-2efd-4482-8624-8a28ae17e317" />

<img width="888" height="379" alt="Screenshot 2026-08-24 142028" src="https://github.com/user-attachments/assets/497a5d80-6bbf-45cb-aef0-7d8d999c0dff" />

<img width="1365" height="654" alt="Screenshot 2026-08-24 142634" src="https://github.com/user-attachments/assets/90b63c4f-e917-4361-bdfe-58dcbdede7e2" />

<img width="1362" height="654" alt="Screenshot 2026-08-24 143136" src="https://github.com/user-attachments/assets/a0b40708-3c13-403b-bf80-8dcc6a708efb" />

---


## Result

This experiment demonstrated how to build a scalable and fault-tolerant cloud architecture using Auto Scaling Groups and Elastic Load Balancing. The system automatically adjusted resources based on workload and ensured continuous service availability by distributing traffic across multiple instances.
