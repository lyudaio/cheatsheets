# Terraform Cheatsheet (Latest LTS: 0.18.3)

## Introduction

Terraform is an open-source infrastructure as code software tool created by HashiCorp. It allows users to define and provision infrastructure components, such as virtual machines, DNS entries, and databases, using a high-level configuration language. Terraform uses a state file to track and manage changes to infrastructure components over time.

### Installation

To install Terraform, download the appropriate package for your operating system from the [Terraform website](https://www.terraform.io/downloads.html).

### Basic Syntax

- Variables are declared using the "variable" keyword followed by the name and data type (string, number, boolean, etc.)
- Providers are defined using the "provider" keyword followed by the provider name and the appropriate configuration block
- Resources are defined using the "resource" keyword followed by the resource type, name, and configuration block
- Data sources are defined using the "data" keyword followed by the data source type and name
- Output values are declared using the "output" keyword followed by a name and an expression to be evaluated

```hcl
# Example Terraform code
variable "example_variable" {
  type = string
}

provider "aws" {
  region = "us-west-2"
}

resource "aws_instance" "example" {
  ami           = "ami-0c55b159cbfafe1f0"
  instance_type = "t2.micro"
}

data "aws_ami" "example" {
  most_recent = true

  filter {
    name   = "name"
    values = ["amzn-ami-hvm-*-x86_64-gp2"]
  }
}

output "example_output" {
  value = "${aws_instance.example.id}"
}
```

### Common Commands

- `terraform init` - initializes a Terraform configuration and downloads any required providers
- `terraform plan` - generates an execution plan for the Terraform configuration
- `terraform apply` - applies changes to infrastructure components defined in the Terraform configuration
- `terraform show` - displays the state file for a Terraform configuration
- `terraform destroy` - destroys all infrastructure components defined in a Terraform configuration

### Conclusion

Terraform is a powerful tool for automating the deployment and management of infrastructure components. The Terraform syntax is relatively straightforward, and the tool integrates well with a variety of providers and data sources. By using Terraform, infrastructure can be versioned and managed in a consistent, reproducible way.
