Create an AWS VPC, Subnet, Security Group, and Network ACL using Terraform on AWS
This Terraform code was built with Terraform 0.12.16 and consists of two Terraform:
- tf files vpc.tf which is the actual configuration file and
- and variables.tf in which the variables are declared.

Within the configuration directory that the two files are located issue:
$ terraform init
The init argument will initialize the environment.
$ terraform fmt
$ terraform validate

Then issue:
$ terraform plan -out vpc.plan
The plan argument will syntax check the files and prepare the deployment and output the blueprint of resources to be created.

Deploy the VPC:
$ terraform apply vpc.plan
This will deploy the AWS VPC. 

To view data about the VPC/Subnet/Security Group from your local Linux box execute:
$ terraform show

To destroy the VPC execute:
$terraform destroy

To test the VPC create a new instance with the newly defined security group and subnet.