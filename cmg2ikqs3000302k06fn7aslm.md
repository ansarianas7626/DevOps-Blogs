---
title: "Virtual Machine Basics: Learn How VMs Work"
datePublished: Sat Sep 27 2025 16:57:40 GMT+0000 (Coordinated Universal Time)
cuid: cmg2ikqs3000302k06fn7aslm
slug: virtual-machine
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1758983720140/03c01399-9ce0-4d32-b8ba-a3e614806e49.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1758992239502/8cb650e1-4673-4e04-91b5-f46572872bb7.png
tags: virtual-machine, devops, virtualization, devops-articles, devops-journey, devopscommunity, abhishek-veeramalla

---

---

## What is a server?

Server is a computer system that provides resources, data, services or program to other computer called clients, over a network, server can be physical and virtual.

Examples of servers:

* 🌐 **Web Server** → Hosts websites (e.g., Apache, Nginx).
    
* 💾 **Database Server** → Stores and manages data (e.g., MySQL, MongoDB)
    
* ⚙️ **Application Server** → Runs business applications.
    

## What is Virtual Machine?

A **Virtual Machine (VM)** is a software-based computer system that runs inside a physical machine. It behaves just like a real computer it has its own CPU, memory, storage, and operating system. The main advantage of a VM is that you can run multiple operating systems on the same hardware, such as running Linux and Windows on one powerful server.

## Physical server Vs Virtual server

**1\. Physical Server**: A dedicated hardware machine with one operating system. If you want to run 3 different apps with different OS requirements, you’ll need 3 separate physical servers.

**2\. Virtual Server**: A virtualized environment created inside a physical server. Here, one physical server can host multiple virtual machines. This saves cost, power, and space while improving efficiency.

**Example:** Instead of buying 5 different computers for 5 developers, you can set up 5 VMs inside a single physical machine.

## What is a Hypervisor in Virtual Machines?

Hypervisor is software that can install virtual machines(VM) on our physical server what actually we are doing we are creating let say five difference virtual server on a single physical server each virtual server has its own CPU, Memory and storage. We can install different OS on different virtual machine.

There are two types of hypervisors:

* **Type 1 (Bare Metal Hypervisor)** – Installed directly on hardware (e.g., VMware ESXi, Microsoft Hyper-V).
    
* **Type 2 (Hosted Hypervisor)** – Installed on top of an operating system (e.g., VirtualBox, VMware Workstation).
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1758991667030/7806f7ab-5574-4e4e-aa5f-d57190012787.png align="center")

---

## How to create virtual machine

Creating a VM is simple using tools like VirtualBox, VMware, or cloud providers like AWS, Azure, or GCP. The general steps are:

1. Install a hypervisor (e.g., VirtualBox).
    
2. Allocate resources (CPU cores, RAM, storage).
    
3. 📀 Select an ISO image of the operating system (Linux, Windows, etc.).
    
4. ▶️ Boot the VM and install the OS.
    
5. 🖥️ Start using your virtual environment just like a physical machine.
    

## Real world example

Imagine a DevOps team working on multiple applications:

One app requires **Ubuntu Linux**🐧.

Another app requires **Windows Server**.

A third app needs **CentOS** 📦.

Instead of buying 3 separate servers, the team can create 3 VMs on a single powerful physical server. This setup allows them to:

1. Test different environments.
    
2. Roll back easily if something breaks.
    
3. Scale quickly without high costs.
    
4. This is exactly how companies reduce infrastructure costs and speed up development using virtualization.
    

## Why Virtualization is important in DevOps

* Saves cost by avoiding extra hardware.
    
* Faster testing and deployment.
    
* Easy rollback and recovery.
    
* Helps in creating staging & production environments quickly.
    

---

## **Short Forms & Abbreviations**

VM - Virtual Machines

OS - Operating System

## Conclusion

Virtual Machines let you run multiple “computers” on a single physical server. They save cost, space, and time while making testing and deployment easy. For beginners and DevOps teams alike, VMs are a simple way to work efficiently without needing extra hardware. 🚀

[Video Lecture Link](https://www.youtube.com/watch?v=lgUwYwBozow&list=PLdpzxOOAlwvIKMhk8WhzN1pYoJ1YU8Csa&index=4&pp=iAQB0gcJCQYKAYcqIYzv)