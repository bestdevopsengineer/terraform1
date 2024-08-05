# Terraform Language Documentation
## 1-About the Terraform Language
### The main purpose of the Terraform language is : 
declaring resources, which represent infrastructure objects.
### A Terraform configuration :
is a complete document in the Terraform language that tells Terraform how to manage a given collection of infrastructure. A configuration can consist of multiple files and directories.
### The syntax of the Terraform language
![image](https://github.com/user-attachments/assets/226a549d-77a6-462e-b03d-2dafb85f6543)
### Code style
### Code formatting
Indent two spaces for each nesting level | align their equals signs:

![image](https://github.com/user-attachments/assets/9e96c43d-c2fa-41c6-81aa-54e52d75888d)
### Code validation
The validate command does not check if argument values are valid for a specific provider, but it will verify that they are the correct type. It does not evaluate any existing state.
### File names
* A backend.tf file that contains your backend configuration.
* A main.tf file that contains all resource and data source blocks.
* A outputs.tf file that contains all output blocks in alphabetical order.
* A providers.tf file that contains all provider blocks and configuration.
* A terraform.tf file that contains a single terraform block which defines your required_version and required_providers.
* A variables.tf file that contains all variable blocks in alphabetical order.
* A locals.tf file that contains local values.
* A override.tf file that contains override definitions for your configuration.
* A network.tf file that contains your VPC, subnets, load balancers, and all other networking resources.
* A storage.tf file that contains your object storage and related permissions configuration.
* A compute.tf file that contains your compute instances.
 ### Linting and static code analysis
 Terraform does not have a built-in linter, but many organizations rely on a third party linting tool such as **TFLint** to enforce code standards. A linter uses static code analysis to compare your Terraform code against a set of rules. 
 ### Comments
 Use # for both single- and multi-line comments. The // and /* */ comment syntaxes are not considered idiomatic, but Terraform supports them to remain backwards-compatible with earlier versions of HCL.
 ### Resource naming
 ![image](https://github.com/user-attachments/assets/237f8233-7474-427f-871d-06976002cd75)
 ### Resource order
 The order of the resources and data sources in your code does not affect how Terraform builds them, so organize your resources for readability. Terraform determines the creation order based on cross-resource dependencies.
### Variables
![image](https://github.com/user-attachments/assets/f17e5472-38bb-4def-8096-a6a89bd7eec1)
### Outputs
![image](https://github.com/user-attachments/assets/44c39e47-1b31-4a90-9b34-798f689ba9e9)
Output values let you expose data about your infrastructure on the command line
### Local values
![image](https://github.com/user-attachments/assets/18f4f45a-f429-4cb2-94a3-7420facebf0c)
### Provider aliasing
![image](https://github.com/user-attachments/assets/784161b2-c86a-4736-ad8b-ad6afb87c86b)
### Dynamic resource count
![image](https://github.com/user-attachments/assets/d805f89b-1b35-4a27-9520-4efb77565185)  ![image](https://github.com/user-attachments/assets/cf3088eb-c0e6-416b-b39f-01b854d45e4a)
### .gitignore
exclude files that you should not publish to version control, such as your state file.
Do not commit:
terraform.tfstate, terraform.tfstate.*
.terraform.tfstate.lock.info , .terraform
Any .tfvars files that contain sensitive information. ,

Always commit:
* All Terraform code files
* Your .terraform.lock.hcl dependency lock file
* A .gitignore file that excludes the files listed below
  ### Workflow style
  * Pin your Terraform, provider, and module versions.
  * Name your module repositories using this three-part name terraform-<PROVIDER>-<NAME> when using the HCP Terraform registry.
  * Store local modules at ./modules/<module_name>.
  * Use the tfe_outputs data source or provider-specific data sources to share state between two state files.
  * Protect credentials by using **dynamic provider credentials** or a **secrets manager such as HashiCorp Vault**.
  * Write tests for your modules.
  * Use policy enforcement on HCP Terraform to set guardrails for infrastructure operations.

### Version pinning
To prevent providers and modules upgrades from introducing unintentional changes to your infrastructure, use version pinning.
![image](https://github.com/user-attachments/assets/fb07a9a2-cd1a-4228-8a56-1340cb12fc3b)





