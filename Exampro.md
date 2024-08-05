# <u>1- Introduction </u>

* IAC declaratie and cloud agnostic
* automating infrastructure writing scripts
* working with multiple cloud providers
* enjoy designing and iterating on end to end infrastructure lifecycles
![image](https://github.com/user-attachments/assets/f2c13d53-e833-4a84-af71-75ceb28ef36e)
![image](https://github.com/user-attachments/assets/7d2c90d7-f9bb-4044-804f-0a9ef5771d97)

# 2- IaC Concepts
### - The Problem with Manual Configuration
* Its easy to misconfigure a service through human error 
* Its hard to manage the expected state of configuration for compliance
* Its hard to transfer configuration knowledge to other team members
### - Infrastructure as Code (IaC)
You write a configuration script to automate creating, updating, or destroying cloud infrastructure.
* IaC is a blueprint of your infrastructure
* IaC allows you to easily share, version, or inventory your cloud infrastructure.
### - Popular Infrastructure as Code tools (IaC)
![image](https://github.com/user-attachments/assets/31199f1d-31f8-411c-84be-50bb5aff5189)

### - Declarative+
![image](https://github.com/user-attachments/assets/d814820f-7dd0-4696-a0af-c791b7600a6e)
### - Infrastructure Lifecycle
the idea of having clearly defined and distinct work phases which are used by DevOps Engineers to plan, design, build, test, and deliver, maintain and retire cloud infrastructure.
* Day 0 - Plan and Design
* Day 1 - Develop and Iterate
* Day 2 - Go live and maintain
### - How does IaC enhance the Infrastructure Lifecycle?
![image](https://github.com/user-attachments/assets/41e7af0d-1626-493f-b492-503b98a2bcb2)
### - Non-Idempotent vs Idempotent ​
![image](https://github.com/user-attachments/assets/842eeccc-581d-4284-acfd-f6d72d3412d4)
### - Provisioning vs Deployment vs Orchestration​
![image](https://github.com/user-attachments/assets/22d6f76f-3010-410d-a231-8c474dd3eba6)
### - Configuration Drift​
when provisioned infrastructure has an unexpected configuration change due to:​
* team members manually adjusting configuration options​
* malicious actors​
* side effects from APIs, SDK, or CLIs.​
eg. a junior developer turns on Delete on Termination for the production database.​
### - How to detect configuration drift?​
![image](https://github.com/user-attachments/assets/69f343b6-5490-4d34-a26c-0d9a9ed93865)
help correct configuration drift in terraform : terraform plan |  terraform refresh or terraform apply -refresh-only -auto-approve
### - Mutable vs Immutable Infrastructure​
![image](https://github.com/user-attachments/assets/2398e942-1bac-48fc-b19c-c2e335955f4f)
### - What is GitOps?​
![image](https://github.com/user-attachments/assets/155c913a-f0de-494f-8861-c8f76befbea0)
### - Immutable Infrastructure Guarantee​
![image](https://github.com/user-attachments/assets/5c874209-7fed-47ba-84af-530ad36f5590)

# 3- HashiCorp Introduction
![image](https://github.com/user-attachments/assets/412202f3-446a-46ad-b03d-7191f0286839)
### HashiCorp Products​
![image](https://github.com/user-attachments/assets/9322d199-5c3a-4269-939e-7d549dce0cf2)
![image](https://github.com/user-attachments/assets/3a6add30-b8c5-4fa5-a24c-b3e5c2d48b7d)

### - what is terraform ?
![image](https://github.com/user-attachments/assets/30a74ec5-5f20-440b-a9b2-b30b95b3be74)
### - What is Terraform Cloud?​
![image](https://github.com/user-attachments/assets/cf4b9a3b-3712-4a08-8e6d-da13d797be0b)
# 4-Terraform Basics
### -Terraform Lifecycle​
![image](https://github.com/user-attachments/assets/2ede4f59-cf2a-457c-8e02-c0453bb7f9ce)
### - What is Change Management?​ | What is Change Automation?​ | What is a ChangeSet?​
![image](https://github.com/user-attachments/assets/d8ae28fb-6e39-4144-8a73-d7e96aa97a43)
### -Terraform - Execution Plans​
![image](https://github.com/user-attachments/assets/d2c6abb5-796e-4b07-bd6e-7969b7af8994)
### -Terraform – Visualizing Execution Plans​
![image](https://github.com/user-attachments/assets/458bc635-8e8d-46d3-9157-63a6eb55d6f5)
### -Terraform – Resource Graph​
![image](https://github.com/user-attachments/assets/7df319e2-f98d-44ad-97b8-3cdf1243cd0d)
### -Terraform — Use Cases​
![image](https://github.com/user-attachments/assets/c71b5148-00d6-4587-9120-f5575b9183c2)
### -Terraform Core and Terraform Plugins​
![image](https://github.com/user-attachments/assets/575f05c6-5b1b-4ab2-90f9-6fac32d1089c)
### -Terraform Best Practices
* Terraform is an online open-book about Terraform Best Practices​
* https://www.terraform-best-practices.com/
* terraform init will create .terraform.lock.hcl file and .terraform directory
* ![image](https://github.com/user-attachments/assets/7f12cc39-3755-4b81-bfc8-dfe75ef69c43)
* terraform fmt | terraform validate | terraform plan | terraform apply | terraform apply update | 
* **plan and apply do the validate by default**
### -variables
![image](https://github.com/user-attachments/assets/5c1a0ee0-7f8f-416b-8463-89ccadf8c6b4)

* terraform plan -var-instance_type="t2.micro"
![image](https://github.com/user-attachments/assets/b98f72a2-7272-4cf6-a239-358c560324f3)
### -local values
![image](https://github.com/user-attachments/assets/97520030-4262-4123-b593-44da3b5f1878)
### -outputs

# 5-Provisioners
# 6-Terraform Providers
Terraform Language
Variables and Outputs
Resource Meta-Arguments
Expressions
Terraform State
Initializing Working Directories
Writing and Modifying Terraform Code
Plan and Apply
Drift
Troubleshooting
Terraform Modules
Terraform Workflows
Backends
Resources and Complex Types
Built-In Functions
Terraform Cloud
Terraform Enterprise
Workspaces
Sentinel with Terraform
HashiCorp Packer
Consul
Vault
Misc
Booking Your Exam
