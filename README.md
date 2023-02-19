# TerraScapeX
a Terraform workspace project for creating different environments on AWS is a powerful tool for managing infrastructure in a scalable and efficient way.

first launch an ec2 instance then install awscli and terraform on it.
create a iam role and attach admintrationaccess policy to it.
we will create resouces and keep them variablized, defining the variables in variables.tf and for different environment we will create a file which store the values for those variables, for e.g qa.tfvars for the qa environment.
Basically workspace in terraform refers to maintining a different tfstate file for each environment.
Using Terraform workspaces, you can keep your infrastructure configuration organized and maintain separate environments for development, testing, and production, all within the same codebase. This makes it easy to manage changes and roll out updates to different environments without affecting others.
This project allows you to define the resources for each environment in a modular and reusable way, so you can easily create new environments or make changes to existing ones. With Terraform, you can also use version control to track changes to your infrastructure configuration, which helps with collaboration and accountability.
**terraform workspace command**
- terraform workspace list ( it will give you list of all the workspaces)
- terraform workspace new ( will create a new workspace for you)
- terraform workspace select ( it will select a particular environment )
- terraform terraform apply -var-file="qa.tfvars" (to make the current state = desired state for a particular state)
-  or to run any terraform command we just need to pass on the variable file.
