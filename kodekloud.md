https://kodekloud.com/pages/community
## 1-Traditional IT & Challenges
-Slow Deployment 
-Expensive 
-Limited Automation 
-Human Error 
-Wasted Resources 
-Inconsistency

## 2-Introduction to IaC
### Types of IaC Tools: 
![image](https://github.com/user-attachments/assets/649cb22f-a4c5-4bf0-bf66-dbbaf5e5e9ea)
![image](https://github.com/user-attachments/assets/4ce73cc9-cccc-41b3-bba3-bb30dd62b330)
![image](https://github.com/user-attachments/assets/182c368b-bf13-4d51-9318-220ed55f0221)
![image](https://github.com/user-attachments/assets/23cd7161-f63a-43cb-9c8c-73c68adc0631)

## 3-Why Terraform?
![image](https://github.com/user-attachments/assets/193ede97-bfea-4a35-b4cc-050951c94f39)

 Declarative(HELP TOGO FROM CURRENT TO DESIRE STATE), HashiCorp Configuration Language
STATE=blueprint of the infrastruturedeployed by terraform
![image](https://github.com/user-attachments/assets/4d1fa7b3-456d-4aa0-be8b-731cee979c8d)
### -terraform Cloud and Enterprise
provide simple collaboration with team
managing infrastructure 
improved security
centralizedUI to manage Terraform deployments
## 4-HCL Basics:
![image](https://github.com/user-attachments/assets/f37cd26e-e86a-492f-9a9f-1991c74e8c61)
## Provision, Update and Destory
Immutable infrastruture because to update terraform will delete the older infrastructure and create a new one
use single provider called local
![image](https://github.com/user-attachments/assets/200411d4-bdc6-453c-a99e-a66fa156fb91)
terraform init | plan | apply | destroy
## 5-Providers 
plugins are in .terraform     hashicorp(organizational namespace)/local (type) 
hashicorp/local                  (hostname)  registry.terraform.io/hashicorp/local 
![image](https://github.com/user-attachments/assets/fcb931fe-4d16-4185-afa8-ed75eef99968)
### use many providers
![image](https://github.com/user-attachments/assets/1cf2ee2f-2097-44f5-a4d0-00830cfe9889)

## 6-Input Variables
 hardcoding values is not a good idea because it limits the reusability of the code which defeats the purpose of using IAC
We want to make sure that the same code can be used again and again to deploy resources based on a set of input variables
that can be provided during the execution.


![image](https://github.com/user-attachments/assets/3790d89d-47c9-4932-9211-b9895681adf1)
![image](https://github.com/user-attachments/assets/30e5a5eb-efa6-44af-8e95-416d95c7d18c)
![image](https://github.com/user-attachments/assets/b9cb3e3f-3480-4071-b43f-b0f5d29ff411)
==========
![image](https://github.com/user-attachments/assets/c0238802-2e34-4694-ae12-8fe0b8a575f2)
you can set default variable like this
![image](https://github.com/user-attachments/assets/947193e2-74ee-419a-9be4-674aad42b406)
or use environment variable
![image](https://github.com/user-attachments/assets/217ab601-0936-45e0-b400-6c505882a021)
or use terraform.tfvars or terraform.tfvars.json
![image](https://github.com/user-attachments/assets/a1c7cb44-f2ae-47fe-a12b-b0120ace966e)

![image](https://github.com/user-attachments/assets/e4c1e28f-ccab-4bc3-892e-864776d9580b)
to use another name instead of terraform 
![image](https://github.com/user-attachments/assets/4c535864-14de-4176-a83c-f795c98a3270)
![image](https://github.com/user-attachments/assets/e1cb4f30-7fdd-4f9f-becb-40e1f7361333)

## 7-Output variables
![image](https://github.com/user-attachments/assets/f68a12a9-07d2-445f-a56f-3944ecd93502)
![image](https://github.com/user-attachments/assets/3571e1a0-a2a1-4fb7-b613-fc7f61d52fb5)
![image](https://github.com/user-attachments/assets/4e41e443-0972-453c-a3c9-39e8ed3afa7d)

## Resource Attributes
![image](https://github.com/user-attachments/assets/b5689c24-205e-419a-9039-688cd227a5f0)

## 8-Resource Dependencies
![image](https://github.com/user-attachments/assets/e87af545-481f-4603-944a-fbe2f6201aca)
![image](https://github.com/user-attachments/assets/4661bcf8-5309-44ad-9c9f-24537b543f78)

## 9-Terraform State
used by terraform to match the  resource configuration to real world infrastructure
### purpose state: 
-collaboration (when working as a team save it in remote data store: S3/hashicorp consul/google cloud storage/terraform cloud )

-tracking metadata(know what to delete even with dependencies)

-performance(make terraform to refer to the satefile alone while running cmd and bypass having to refresh state every time)
![image](https://github.com/user-attachments/assets/8e8261d6-97d1-4db5-bdf2-9fa8386f6067)
###  terraform state considerations
-sensitive data

-no manually edit
## 10-TERRAFORM Commands 
CHECK IF THE SYNTAXE IS CORRECT WITH
![image](https://github.com/user-attachments/assets/d513a279-568f-4a66-ae96-76fb072dc0e3)
![image](https://github.com/user-attachments/assets/6424600d-2261-4929-b768-eac86bb53a73)
it should be file_permission not file_permissions
![image](https://github.com/user-attachments/assets/f527a5aa-6de2-4f4a-ae15-307b16e6f4de)
![image](https://github.com/user-attachments/assets/c4c282f2-ee7b-46fb-9f77-f7c9290d16a3)
![image](https://github.com/user-attachments/assets/fc9af258-e990-47e8-9485-ef975e5c33db)
![image](https://github.com/user-attachments/assets/da13011e-4e9a-4b54-b0b8-90312f1767b0)
![image](https://github.com/user-attachments/assets/dfe9162e-e662-4956-baa9-9a6f3d3f091b)

## 11-Mutable vs  Immutable

LifeCycle Rules
Datasources
Meta Arguments 
count
 for-each
 Version Constraints
 AWS Basics
Programmatic Access
IAM Basics 
IAM with Terraform
Introduction to S3
S3 with Terraform
Introduction to DynanoDB
DynamoDB with Terraform
 Remote State
  State Locking
Remote Backend with S3
 State Commands
  Introduction to EC2
AWS EC2 With Terraform
Provisioners
Terraform Taints
Debugging
Terraform Import
Modules
Functions
Conditional Expressions
Workspaces
Terraform Cloud
	
