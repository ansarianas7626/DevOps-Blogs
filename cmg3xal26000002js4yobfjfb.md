---
title: "How to create Virtual Machine AWS & Azure"
datePublished: Sun Sep 28 2025 16:37:27 GMT+0000 (Coordinated Universal Time)
cuid: cmg3xal26000002js4yobfjfb
slug: how-to-create-virtual-machine-aws-and-azure
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1759077258356/76b7a0a7-dbba-486b-88fb-4a3aeade8d9f.png
tags: virtual-machine, aws, devops, devops-articles, devops-journey, devopscommunity, abhishek-veeramalla

---

## 1\. How to Create a Virtual Machine (General Way)

Think of a **Virtual Machine (VM)** as a *computer inside your computer*.

👉 Example: Imagine you have one big room (your computer). Now, you put walls inside it to create smaller rooms. Each small room works like an independent house. That’s exactly what a VM does.

**Steps (general):**

1. Install a virtualization tool like **VMware**, **VirtualBox**, or **Hyper-V**.
    
2. Choose the operating system (Windows, Linux, etc.) you want in your VM.
    
3. Allocate resources (RAM, storage, CPU).
    
4. Start the VM → Boom! You now have a mini-computer running inside your real computer.
    

---

## 2\. How to Create a Virtual Machine in AWS (EC2 Instance)

In AWS, VMs are called **EC2 Instances**.

👉 Example: Imagine AWS as a giant hotel. Each room in the hotel is a VM (EC2 instance). You rent the room only when you need it.

**Steps to create an EC2 instance:**

1. Login to your AWS Console.
    
2. Go to **EC2 Dashboard** → Click **Launch Instance**.
    
3. Choose an operating system (Amazon Linux, Ubuntu, Windows).
    
4. Select the hardware size (t2.micro is free for beginners).
    
5. Configure network and storage.
    
6. Create/choose a key pair (for login security).
    
7. Launch instance → Your VM is ready in the cloud.
    

---

## 3\. How to Create a Virtual Machine in Azure

Azure is Microsoft’s cloud platform, and creating a VM here is very similar to AWS.

👉 Example: Think of Azure as another hotel chain, just like AWS. The concept is the same—you rent a “room” (VM) on demand.

**Steps to create VM in Azure:**

1. Login to Azure Portal.
    
2. Search **Virtual Machines** → Click **Create VM**.
    
3. Select OS (Windows/Linux).
    
4. Choose VM size (based on RAM/CPU).
    
5. Configure username, password, and networking.
    
6. Click **Review + Create** → Done! Your VM is live.
    

---

## 4\. What is an API? (with AWS Example)

**API = Application Programming Interface**

👉 Example: Imagine you go to a restaurant. You don’t go inside the kitchen to cook food yourself. Instead, you ask the waiter (API). The waiter takes your request, goes to the kitchen (server), and brings your food (response).

That’s exactly how an API works in software:

* You (user) → make a request.
    
* API → delivers the request to the system.
    
* System → sends back the result through API.
    

### AWS API Example

AWS provides its own set of APIs called **AWS SDK (Software Development Kit) and AWS CLI (Command Line Interface)**.

* Instead of clicking in the AWS Console, you can directly send commands via API.
    
* Example:
    
    ```plaintext
    aws ec2 run-instances --image-id ami-12345 --instance-type t2.micro
    ```
    
    This single line will launch a VM (EC2 instance) without even opening the AWS website!
    

So AWS API = **shortcut to talk to AWS services programmatically**.

---

## 5\. Different Ways to Create a Virtual Machine in AWS

AWS doesn’t limit you to only one method. You can create Virtual Machines in multiple ways:

1. **AWS Management Console (UI)** – Beginner-friendly, just click and create.
    
2. **AWS API / AWS CLI** – Use commands or scripts to launch instances.
    
3. **AWS CloudFormation (CFT)** – Write configuration in a template (YAML/JSON) to automatically create infrastructure.  
    👉 Example: Instead of manually creating 10 VMs, you can define it once in a file and AWS will create them all for you.
    
4. **Kubernetes** – If you’re running container workloads, Kubernetes can spin up nodes (VMs) in AWS automatically.
    
5. **AWS CDK (Cloud Development Kit)** – Recently introduced. With CDK, you can use programming languages (Python, JavaScript, etc.) to define infrastructure. It’s like coding your cloud setup.
    

👉 Simple Analogy:

* Console = Manual booking of a hotel room.
    
* API/CLI = Calling the hotel and booking via phone.
    
* CloudFormation = Sending a full guest list in advance and hotel auto-arranges rooms.
    
* Kubernetes = A travel agency booking hotel rooms for groups automatically.
    
* CDK = Writing a software program that books hotels for you in smart ways.
    

---

## 6\. Short Forms and Abbreviations

Here are all the abbreviations used in this blog with their full forms:

* **VM** → Virtual Machine
    
* **AWS** → Amazon Web Services
    
* **EC2** → Elastic Compute Cloud
    
* **UI** → User Interface
    
* **API** → Application Programming Interface
    
* **CLI** → Command Line Interface
    
* **SDK** → Software Development Kit
    
* **CFT** → CloudFormation Template
    
* **CDK** → Cloud Development Kit
    
* **OS** → Operating System
    
* **CPU** → Central Processing Unit
    
* **RAM** → Random Access Memory
    

---

# Final Thoughts

Virtual Machines are like **computers within computers**. You can create them on your laptop, or in the cloud with AWS and Azure.  
AWS gives you multiple ways to create VMs—from simple clicks in the console to advanced automation using APIs, CloudFormation, Kubernetes, and CDK.

And APIs? They’re just **messengers** that let you talk to services like AWS directly.