## Terraform Interview Questions and Answers

#### 1. What is Terraform?

Answer.

#### 2. When you created the environment using Terraform? What are all the components that you have created using Terraform?
**Answer.** I have experience creating environments using Terraform in previous roles. I utilized Terraform to provision and manage infrastructure components such as EC2 instances, VPCs, security groups, IAM roles and policies, S3 buckets.

#### 3. How to do changes in the configurations of already created resources using Terraform?
**Answer.** To make changes to existing resources in Terraform, you can modify the Terraform configuration files and then apply those changes using the terraform apply command. Terraform will automatically detect the differences and update the resources accordingly, ensuring the desired state matches the configured state. 

But, existing resources that were not initially created by Terraform. You want to bring them under Terraform management, then use Terraform import command. It will bring all details to terraform state.
```
terraform import aws_instance.example i-0123456789abcdef0
```

#### 4. What is statefile? Where can we store it?
**Answer.** The statefile in Terraform is a crucial file that tracks the current state of your infrastructure. It contains information about the resources Terraform manages, their configurations, and relationships. This file is used to plan and apply changes. You can store the statefile locally or remotely. For collaboration and consistency, it's recommended to use remote backends like AWS S3 or HashiCorp Terraform Cloud to store and share the statefile among team members.

#### 5. What if we loose terraform statefile? How to resolve it?
**Answer.** If the Terraform statefile is lost, it can lead to issues in managing infrastructure. To recover, you can attempt to recreate the statefile by importing existing resources using 'terraform import'. However, for a more robust solution, it's advisable to maintain backups of the statefile and store it securely. Services like Terraform Cloud or using remote backends with version control systems can mitigate the risk of losing the statefile.
