---
title: "What is Terraform? A Deep Dive into IaC, APIs, and Multi-Cloud Automation"
datePublished: Sat Nov 15 2025 15:02:48 GMT+0000 (Coordinated Universal Time)
cuid: cmi0f1r8p000102jj4wxicg32
slug: what-is-terraform-a-deep-dive-into-iac-apis-and-multi-cloud-automation
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1763218940840/6e8e6843-4952-462d-927a-b5714cf90c47.png
tags: aws, azure, automation, devops, terraform, infrastructure-as-code, gcp, devops-articles, terraform-cloud, devops-journey, devopscommunity

---

## What is Infrastructure as Code (IaC)?

**Infrastructure as Code (IaC)** is the practice of managing and provisioning cloud resources (like servers, networks, databases, and storage) using **code** instead of manually clicking through cloud dashboards.

In simple words:  
👉 *“IaC allows you to build your entire cloud setup using code files.”*

### Why IaC is important?

* ✅ **Automation** – Deploy infrastructure with one command
    
* ✅ **Consistency** – No human errors or missed settings
    
* ✅ **Version Control** – Track changes using Git
    
* ✅ **Reproducibility** – Same setup can be recreated anytime
    
* ✅ **Scalability** – Deploy to any cloud provider easily
    

## What is Terraform?

**Terraform** is an open-source Infrastructure as Code (IaC) tool created by HashiCorp.  
It allows you to define and manage infrastructure across **multiple cloud providers** like AWS, Azure, GCP, DigitalOcean, and many more — all using a single language called **HCL (HashiCorp Configuration Language).**

### What problem does Terraform solve?

Before Terraform:

* Infrastructure was created manually
    
* Settings differed from environment to environment
    
* Multi-cloud setups were difficult
    
* Teams couldn’t track changes
    

With Terraform:

* You write infrastructure in a `.tf` file
    
* Terraform talks to cloud APIs
    
* It creates, updates, or destroys your cloud resources automatically
    
* Everything is predictable and version-controlled
    

### Why Terraform is popular?

* ⚡ Multi-cloud support
    
* ⚡ Declarative configuration
    
* ⚡ Easy automation
    
* ⚡ State management
    
* ⚡ Large provider ecosystem
    

Terraform basically brings the power of **coding** to **cloud infrastructure**.

## What is API?

**API (Application Programming Interface)** is a way for two systems to communicate with each other.

In the cloud world, APIs are used by tools (like Terraform) to talk to cloud providers.

Example:

* When Terraform creates an EC2 instance, it sends a request to the **AWS API**
    
* When Terraform creates a VM in Azure, it talks to the **Azure API**
    

👉 *API is like a waiter in a restaurant — you tell your order, the waiter conveys it to the kitchen, and gets your food back.*

## **What We Can Do With Terraform**

Terraform is a powerful Infrastructure as Code (IaC) tool that helps teams build, manage, and automate cloud infrastructure with consistency and reliability. Here are the key things you can do with Terraform:

**1\. Manage Any Infrastructure**

Terraform works with multiple cloud providers and platforms through its provider system.  
You can manage:

* AWS, Azure, GCP
    
* Kubernetes clusters
    
* Databases
    
* DNS services
    
* On-premises systems
    
* SaaS platforms
    

Whether your infrastructure is simple or complex, Terraform can handle it.

**2\. Track Your Infrastructure**

Terraform keeps track of all the infrastructure it creates using a **state file**.  
This helps Terraform understand:

* What currently exists
    
* What needs to change
    
* What resources must be updated or destroyed
    

This tracking ensures consistency and prevents duplication or accidental changes.

**3\. Automate Changes**

Whenever you update your `.tf` configuration files, Terraform automatically figures out:

* What should be added
    
* What should be modified
    
* What should be removed
    

Running `terraform plan` and `terraform apply` automates the entire update process, saving time and reducing human error.

**4\. Standardize Configuration**

Terraform allows you to define reusable modules and templates.  
This helps teams enforce:

* Consistent naming
    
* Standard architecture patterns
    
* Security and compliance policies
    

By using the same configuration everywhere, you ensure uniform and predictable infrastructure across environments.

**5\. Collaborate as a Team**

Terraform makes team collaboration easy through:

* Remote state backends
    
* State locking
    
* Version control integration
    
* Shared modules
    

Multiple engineers can work on the same infrastructure safely without overwriting each other's changes.

## **Lifecycle of Terraform**

Terraform follows a clear and predictable lifecycle to create, update, and manage cloud infrastructure. Understanding this lifecycle helps you know exactly how Terraform works internally and what happens at each stage.

The Terraform lifecycle includes the following major steps:

---

### **1\. Write**

You start by writing the infrastructure configuration using `.tf` files.  
Here you define:

* Providers (AWS, Azure, GCP, etc.)
    
* Resources (EC2, VPC, S3, IAM roles, etc.)
    
* Variables, outputs, and modules
    

This step describes *what* your infrastructure should look like.

---

### **2\. Initialize (**`terraform init`)

Terraform downloads the required **providers** and sets up the working directory.  
This step prepares Terraform to interact with cloud platforms.

---

### **3\. Plan (**`terraform plan`)

Terraform checks your configuration and compares it with the existing infrastructure state.  
It then shows a detailed **execution plan**, including:

* What will be created
    
* What will be updated
    
* What will be destroyed
    

This stage ensures you know exactly what changes will happen *before* applying them basically its a dry test run for expected output.

---

### **4\. Apply (**`terraform apply`)

Terraform executes the plan and creates the actual infrastructure.  
It communicates with cloud provider APIs and provisions resources exactly as defined in your config files.

You can review the plan once again before approval.

---

### **5\. Manage & Update**

Whenever you change your `.tf` files, Terraform automatically identifies what needs to be updated.  
Then you run `plan` and `apply` again to safely modify resources.

This allows continuous, safe management of infrastructure.

---

### **6\. Destroy (**`terraform destroy`)

When you no longer need the infrastructure, Terraform can remove everything it created.  
This ensures clean teardown and prevents unused resources from generating cost.

Terraform lifecycle is:  
**Write → Init → Plan → Apply → Update → Destroy**  
This workflow ensures infrastructure is consistent, automated, and predictable.

## **Different Files in a Terraform Repository and Their Purpose**

A Terraform project usually follows a standard file structure. Each file in the repository has a specific purpose to keep your configuration clean, organized, and easy to manage. Here are the most commonly used Terraform files:

---

### **1.** [`main.tf`](http://main.tf)

This is the **core configuration file**.  
It usually contains:

* Provider configuration
    
* Resource definitions
    
* Modules (if used)
    

In simple words, [`main.tf`](http://main.tf) is where the main infrastructure code lives.

---

### **2.** [`variables.tf`](http://variables.tf)

This file is used to declare all the input variables that your Terraform code will use.  
You define:

* Variable names
    
* Types (string, number, list, map…)
    
* Default values (optional)
    
* Descriptions
    

This makes your configuration flexible and reusable.

---

### **3.** [`outputs.tf`](http://outputs.tf)

This file defines the **output values** that Terraform should display after the infrastructure is created.  
Common outputs:

* Public IP of EC2
    
* DNS of Load Balancer
    
* VPC IDs
    
* Bucket name
    

Outputs help share important details with other tools or team members.

---

### **4.** [`provider.tf`](http://provider.tf) (optional but common)

Some teams prefer keeping provider configuration in a separate file.  
This file may contain:

* AWS/Azure/GCP provider block
    
* Region information
    
* Version constraints
    

It keeps things cleaner when there are multiple providers.

---

### **5.** [`input.tf`](http://input.tf) (alternate name for variables)

Some projects use names like [`input.tf`](http://input.tf) instead of [`variables.tf`](http://variables.tf).  
Purpose remains the same:  
➡️ Define all input variables.

---

### **6.** `terraform.tfvars`

This file assigns actual values to the variables declared in [`variables.tf`](http://variables.tf).  
You store:

* AWS region
    
* Instance type
    
* Environment name (dev, test, prod)
    

This allows separation of configuration (code) from values (environment-specific data).

---

### **7.** `terraform.tfstate` (auto-generated)

This file stores the **current state** of your infrastructure.  
It tracks:

* All resources Terraform created
    
* Their IDs
    
* Their properties
    

**You should never edit this file manually.**  
Also, in production, you should keep it in **remote backends** (like S3) to avoid corruption and for team collaboration.

---

### **8.** `terraform.tfstate.backup` (auto-generated backup)

Terraform automatically creates a backup of the last state file when you run `apply`.  
This helps recover state in case something goes wrong.

---

### **9.** `modules/` folder (optional)

If you’re using modules, they live inside a `modules` directory.  
Modules help you reuse code and standardize your infrastructure.

Example modules:

* EC2 module
    
* VPC module
    
* S3 module
    

---

### **10.** [`versions.tf`](http://versions.tf) (optional but common)

This file pins the Terraform version and provider versions to avoid compatibility issues.

---

### **11.** [`README.md`](http://README.md)

Always recommended.  
Explains:

* What the Terraform project does
    
* How to run it
    
* Required variables
    

Helps teams understand and maintain the repo.

---

### **In Simple Terms**

A clean Terraform repo looks like this:

```bash
main.tf            → core infrastructure code  
variables.tf       → input variable definitions  
outputs.tf         → outputs after apply  
terraform.tfvars   → variable values  
provider.tf        → cloud provider configuration  
versions.tf        → Terraform & provider version  
terraform.tfstate  → state file (auto-generated)  
modules/           → reusable components
```

---

## Terraform flow with AWS

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1763456173195/b015cddf-05b5-4330-a574-2bcc15ef491d.jpeg align="center")

* DevOps Engineer creates a terraform script and stored in a GitHub so others can also contribute and use the script.
    
* Jenkins and any other CI tools tracks the Version control system like GitHub, bitbucket, GitLab and execute the terraform script.
    
* Never Push or store your terraform state file in GitHub repo because it contains some sensitive information related to infrastructure Always store terraform state file in remote backend like AWS s3 or Azure Storage container.
    
* State file tracks the infrastructure if any changes in made like upgradation of computer resource and any AWS azure services. so with state file terraform understand what was resources before and what changes is done like Git works
    

---

## Short Forms & Abbreviations

| Term | Full Form |
| --- | --- |
| IaC | Infrastructure as Code |
| API | Application Programming Interface |
| HCL | HashiCorp Configuration Language |
| AWS | Amazon Web Services |
| GCP | Google Cloud Platform |
| VM | Virtual Machine |
| VCS | Version Control System |

## 🎯 Conclusion

Infrastructure as Code (IaC) is transforming how companies manage cloud infrastructure by replacing manual processes with automation and consistency. Terraform stands out as one of the most powerful IaC tools, thanks to its provider ecosystem, multi-cloud support, and declarative approach.

Understanding APIs is also crucial because they enable Terraform to communicate with cloud platforms and perform actions automatically.

This foundational knowledge sets the stage for deeper concepts like Terraform state, providers, modules, and real-world automation workflows.

---

[Video Lecture Link 1](https://www.youtube.com/watch?v=G1BRnIHBBig)

[Video Lecture Link 2](https://youtu.be/CzdfdKWRDB8?si=-hU6Z7-Itp76FxMC)