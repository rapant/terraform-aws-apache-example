Terraform Module to provision an EC2 Instance that is running Apache.

Not intended for production use. Juste showcasung how to cast a custom mudule on terraform registry

```hcl
terraform {

}

provider "aws" {
  region = "us-east-1"
}

module "apache" {
  source = ".//terraform-aws-apache-example"
  vpc_id          = "vpc-00000000"
  my_ip_with_cidr = "MY_OWN_IP_ADDRESS/32"
  public_key      = "ssh-rsa AAAAB..."
  instance_type   = "t2.micro"
  server_name     = "Apache Example Server"
}

output "public_ip" {
  value = module.apache.public_ip
}
```
