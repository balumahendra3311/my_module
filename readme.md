```
# Terraform Module: My Module

This module creates a sample EC2 instance in AWS.

## Usage


module "my_module" {
  source = "github.com/arwahab/my-terraform-module"

  aws_region     = "us-west-1"
  ami_id = "ami-08116b9957a259459"
  instance_type  = "t2.micro"
}

output "instance_id" {
  value = module.my_module.instance_id
}

output "instance_public_ip" {
  value = module.my_module.instance_public_ip
}
```