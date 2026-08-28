# Lab 4 – Working with Amazon Elastic Block Store (EBS)

## Author

* **Name**: Santhose Arockiaraj J
* **Register Number**: 212224230248
* **Date of Submission**: 21/08/2026

---

## Objective

The objective of this experiment is to understand how Amazon Elastic Block Store (EBS) provides persistent block-level storage for EC2 instances. This lab focuses on creating and attaching an EBS volume, formatting and mounting it on an EC2 instance, storing data, and verifying data persistence after instance reboot.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* An existing EC2 instance (Amazon Linux 2 preferred)
* Basic knowledge of Linux commands

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Amazon EBS
* SSH Client (Terminal / PuTTY)

---

## Tasks Performed

### Task 1: Explore Amazon EBS

Explore the Amazon EBS service through the EC2 dashboard. Observe different volume types such as General Purpose SSD (gp2/gp3), Provisioned IOPS SSD, Throughput Optimized HDD, and Cold HDD.

---

### Task 2: Create an EBS Volume

Create a new EBS volume in the same Availability Zone as the EC2 instance. Choose an appropriate size and volume type.

---

### Task 3: Attach EBS Volume to EC2 Instance

Attach the created EBS volume to the running EC2 instance as an additional block device.

---

### Task 4: Format the EBS Volume

Connect to the EC2 instance using SSH and format the attached volume with a file system (for example, ext4).

---

### Task 5: Mount the EBS Volume

Mount the formatted volume to a directory in the EC2 instance (for example, /data or /mnt/ebs).

---

### Task 6: Store Data in EBS Volume

Create files and directories inside the mounted EBS volume and store sample data.

---

### Task 7: Verify Data Persistence

Reboot the EC2 instance and verify that the data stored in the EBS volume is still available after reboot.

---

## Workflow (Student Explanation)

First, I logged in to the AWS Management Console.

I navigated to the EC2 Dashboard.

I explored the Elastic Block Store (EBS) section under EC2.

I observed different volume types such as General Purpose SSD (gp2/gp3), Provisioned IOPS SSD, Throughput Optimized HDD, and Cold HDD.

I clicked on “Volumes” and selected “Create Volume.”

I chose the required volume type (General Purpose SSD – gp3).

I entered the desired storage size (for example, 8 GB).

I selected the same Availability Zone as my running EC2 instance.

I clicked on “Create Volume” to create the EBS volume.

After the volume was created, I selected the volume and clicked on “Attach Volume.”

I selected my running EC2 instance and attached the volume as a new device (for example, /dev/xvdf).

I connected to my EC2 instance using SSH from the terminal.

I checked the attached disk using the command lsblk to verify the new volume.

I formatted the attached volume using the command:
sudo mkfs -t ext4 /dev/xvdf

I created a directory to mount the volume using:
sudo mkdir /mnt/ebs

I mounted the volume to the directory using:
sudo mount /dev/xvdf /mnt/ebs

I verified that the volume was mounted successfully using the df -h command.

I created sample files inside the mounted directory using:
sudo touch /mnt/ebs/sample.txt

I stored some sample data inside the file.

I rebooted the EC2 instance from the AWS Console.

After rebooting, I reconnected to the instance using SSH.

I checked the mounted directory and verified that the stored data was still available.

This confirmed that the EBS volume provides persistent storage even after instance reboot.

---

## Output Screenshots (Attach 3)

### Screenshot 1: EBS Volume Created
<img width="1365" height="642" alt="Screenshot 2026-08-21 175311" src="https://github.com/user-attachments/assets/5ee9476d-e574-456a-b652-0dd4c6dac7b3" />


---

### Screenshot 2: EBS Volume Attached to EC2
<img width="1365" height="645" alt="Screenshot 2026-08-21 183455" src="https://github.com/user-attachments/assets/950fbabf-de2e-488a-b9f4-87f74ba256a9" />

<img width="600" height="417" alt="Screenshot 2026-08-21 180426" src="https://github.com/user-attachments/assets/8a117130-26be-43b1-a893-7984adbd628b" />
<img width="523" height="302" alt="Screenshot 2026-08-21 180446" src="https://github.com/user-attachments/assets/2d1782be-cbf4-4449-b7fa-7adba83cc867" />
<img width="673" height="193" alt="Screenshot 2026-08-21 181313" src="https://github.com/user-attachments/assets/5b68709b-9795-44d4-8370-19fa3d01c8f2" />

---

### Screenshot 3: Mounted Volume with Data
<img width="1365" height="648" alt="Screenshot 2026-08-21 184241" src="https://github.com/user-attachments/assets/8b33c23d-7187-484e-878d-d36da2333e44" />
<img width="1365" height="644" alt="Screenshot 2026-08-21 184442" src="https://github.com/user-attachments/assets/2cfe7d6a-53c2-4aa8-9399-3d0acb02a94c" />

<img width="1365" height="642" alt="Screenshot 2026-08-21 184536" src="https://github.com/user-attachments/assets/ff2da03a-6829-4d27-b1f8-d21c9f94db43" />


---

## Result / Conclusion

This experiment demonstrated how Amazon EBS provides persistent storage for EC2 instances. By creating, attaching, formatting, and mounting an EBS volume, and by verifying data after reboot, the concept of durable block storage in the cloud was clearly understood.
