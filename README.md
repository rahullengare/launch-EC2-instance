![image](https://github.com/user-attachments/assets/902c6e76-23fd-4e81-8cd5-a34ba897ff78)# Launch EC2 instance (Linux)

EC2 → Elastic Compute Cloud

## About Project

This project involves launching a Linux-based EC2 instance on AWS to create a virtual server in the cloud. The main objective is to learn how to deploy, configure, and access a Linux virtual machine using Amazon EC2. 

It includes creating a key pair, setting up a security group, launching the instance, and connecting via SSH. Key features include flexible instance types, secure remote access, and scalability. This setup is useful for hosting web apps, running development environments, or practicing Linux server management.

## **Tools and Technologies:**

- **Amazon Web Services (AWS)** – Cloud platform to host and manage resources
- **Amazon EC2** – Service to launch and manage virtual servers
- **Linux (Amazon Linux/Ubuntu)** – Operating system for the EC2 instance
- **SSH (Secure Shell)** – Protocol to securely connect to the instance
- **Key Pair** – Used for secure login to the EC2 instance
- **Security Group** – Acts as a virtual firewall to control inbound/outbound traffic
- **AWS Management Console / AWS CLI** – Interfaces to create and manage EC2 resources

## **What is Amazon EC2?**

> **Amazon EC2** is a cloud service that provides virtual computers (called instances) so you can run applications without needing physical servers.
> 
> 
> It offers features like flexible instance types, auto scaling, and pay-as-you-go pricing.
> 
> You can use it to host websites, run applications, process data, or develop and test software.
>

### Step 1 : AWS Console

1. Go to AWS Console login it
2. Search EC2 instance in Search Box 
3. click on EC2 service

![Project Screenshot](/images/aws-console.jpg)

### Step 2: Creating EC2 instance

1. **Click on Launch instance**
2. **Name and tags** 
    - Write the name of your instance → demo_server
3. **Application and OS Images (Amazon Machine Image)**
    - Select AMI in Quick Start Option → Amazon Linux
4. **Instance type**
    - select instance size or capacity → t2.micro
5. **Key pair (login)**
    - you login to Linux terminal now you can be select .pem → pem-server-key
6. **Network settings**
    - Select existing security group → launch-wizard-1
7. **Advanced details** 
    - User data script - write here direct you want direct instance launch
8. **Summary**
    - you can how many same instance launch that are mentation here → 1

![Project Screenshot](/images/launch-instance.jpg)
![Project Screenshot](/images/launch-instance1.jpg)
![Project Screenshot](/images/launch-instance2.jpg)
![Project Screenshot](/images/launch-instance3.jpg)
![Project Screenshot](/images/run-instance.jpg)

### Step 3: **Connecting to an Instance via SSH**

1. Click on instance **tab**
2. Now Select Your instance
3. then Click on Connect Option 
4. Click on **SSH client**
5. see write here example that is you key

```bash
ssh -i "pem-server-key.pem" ec2-user@172.31.27.189
```

![Project Screenshot](/images/ssh-key.jpg)

6. key copy now
7. private key store in your local machine to open git bash here
8. now open terminal Linux 
9. paste your SSH key & Run it
10. Now done your instance launch

![Project Screenshot](/images/connect-instance.jpg)

### Step 4: Terminating Your instance

1. Your use are done then got to AWS console 
2. Click on EC2 → instance 
3. Select instance You want to terminated
4. Click on Instance state 
5. Choose **Terminate (delete) instance**
6. Now click delete

![Project Screenshot](/images/delete-instance.jpg)
