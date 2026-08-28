# Build Your VPC and Launch a Web Server (AWS)
## Author

* **Name**: Santhose Arockiaraj J
* **Register Number**: 212224230248
* **Date of Submission**: 17/08/2026

---

## Objective

The objective of this experiment is to understand how to design and configure a basic network infrastructure in AWS using a Virtual Private Cloud (VPC). This lab focuses on creating a VPC with a public subnet, configuring an Internet Gateway and route table, launching an EC2 instance, and hosting a simple web server that can be accessed over the internet.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* Web browser with internet connectivity

---

## Tools Used

* AWS Management Console
* Amazon VPC
* Amazon EC2
* Internet Gateway
* Route Table
* Security Groups

---

## Tasks Performed

### Task 1: Create a VPC

Create a new Virtual Private Cloud (VPC) with a private IP address range. The VPC acts as a logically isolated network in AWS where all other resources will be deployed.

Students should create a VPC with an appropriate CIDR block (for example, 10.0.0.0/16) and assign a meaningful name.


### Task 2: Create a Public Subnet

Create a subnet inside the VPC to host public resources. Enable auto-assign public IPv4 so that instances launched in this subnet receive a public IP address.

The subnet should use a smaller CIDR range (for example, 10.0.1.0/24).


### Task 3: Create and Attach Internet Gateway

Create an Internet Gateway (IGW) and attach it to the VPC. This allows communication between resources in the VPC and the internet.


### Task 4: Configure Route Table

Create a route table and add a default route (0.0.0.0/0) pointing to the Internet Gateway. Associate this route table with the public subnet.

This step ensures that traffic from the subnet can reach the internet.


### Task 5: Create Security Group

Create a security group to act as a virtual firewall for the EC2 instance. Configure inbound rules to allow:

SSH on port 22

HTTP on port 80


### Task 6: Launch EC2 Instance

Launch an EC2 instance inside the public subnet using Amazon Linux 2 AMI and a suitable instance type (t2.micro).

Attach the previously created security group and key pair.


### Task 7: Configure Web Server

Install and start a web server (Apache HTTPD) on the EC2 instance using user data or manual commands.

Create a simple HTML page and verify that it can be accessed from a web browser using the public IP address of the instance.---

## Workflow (Student Explanation)

First, I created a VPC in Amazon Web Services.
I gave it a CIDR block of 10.0.0.0/16. This VPC acts as my private network where all my resources will be created.

Next, I created a public subnet inside the VPC with CIDR 10.0.1.0/24. I enabled auto-assign public IP so that any instance launched in this subnet will automatically get a public IP address.

After that, I created an Internet Gateway and attached it to my VPC. This allows my VPC to communicate with the internet.

Then, I created a route table and added a default route (0.0.0.0/0) pointing to the Internet Gateway. I associated this route table with my public subnet. This step ensures that traffic from my subnet can reach the internet.

Next, I created a security group which acts as a virtual firewall. I allowed inbound traffic for SSH on port 22 and HTTP on port 80.

After completing the network setup, I launched an EC2 instance using Amazon Linux 2 AMI with instance type t2.micro. I selected my VPC, public subnet, created security group, and key pair.

Finally, I connected to the EC2 instance using SSH and installed the Apache web server. I started the service and created a simple HTML page. Then I copied the public IP address of the instance and opened it in a web browser. The webpage was displayed successfully.

So, this is how I created a VPC, launched an EC2 instance, and hosted a simple web server in AWS.

---

## Output Screenshots (Attach 3)

### Screenshot 1: VPC and Subnet Details

<img width="1357" height="641" alt="Screenshot 2026-08-08 093810" src="https://github.com/user-attachments/assets/7ae39716-1811-4207-85a4-6b32c3f720f3" /> 
<img width="1365" height="646" alt="Screenshot 2026-08-08 093944" src="https://github.com/user-attachments/assets/e2a3bfe1-d0c0-413e-bf4e-b1c55d982190" />


### Screenshot 2: EC2 Instance Running
<img width="1365" height="657" alt="Screenshot 2026-08-08 095029" src="https://github.com/user-attachments/assets/cef27553-7b1d-4854-822a-794ca4e6374a" />
<img width="1359" height="671" alt="Screenshot 2026-08-08 094726" src="https://github.com/user-attachments/assets/1c80da6c-48fd-484c-9c71-5c11184da258" />


### Screenshot 3: Web Server Output in Browser
<img width="1426" height="503" alt="image" src="https://github.com/user-attachments/assets/0c350bf0-974e-49a7-bfde-5d40ed80a92a" />


## Result 

This experiment successfully demonstrated the creation of a custom VPC and deployment of a public-facing web server in AWS. By configuring networking components such as subnets, route tables, and security groups, and by launching an EC2 instance with a web server, the basic architecture of a cloud-hosted application was understood.
