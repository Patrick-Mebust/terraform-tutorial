# Terraform Tutorial Project

This repository contains a comprehensive tutorial and implementation of Terraform infrastructure as code (IaC) practices, focusing on AWS cloud infrastructure.

## Project Overview

This project demonstrates various aspects of Terraform and AWS infrastructure management, including:

- AWS EC2 instance provisioning
- Security group configurations
- IAM policies and roles
- Infrastructure state management
- Best practices for Terraform deployments

## Repository Structure

- `aws/` - AWS-specific configurations and resources
- `src/` - Source code for any associated applications
- `data/` - Data processing and management
- `docs/` - Documentation and guides
- `examples/` - Example Terraform configurations
- `tests/` - Infrastructure testing
- `.terraform/` - Terraform state and cache files

## Key Files

- `terraform-ec2-policy.json` - IAM policy for EC2 instance management
- `terraform-key.pem` - SSH key for EC2 instance access
- `requirements.txt` - Python dependencies for associated tools
- `.gitignore` - Comprehensive ignore rules for Terraform and development files

## Setup Instructions

1. Install Terraform:
```bash
# For Ubuntu/Debian
sudo apt-get update && sudo apt-get install -y gnupg software-properties-common
wget -O- https://apt.releases.hashicorp.com/gpg | gpg --dearmor | sudo tee /usr/share/keyrings/hashicorp-archive-keyring.gpg
echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list
sudo apt update && sudo apt-get install terraform
```

2. Configure AWS credentials:
```bash
aws configure
```

3. Initialize Terraform:
```bash
terraform init
```

## Usage

1. Review the planned changes:
```bash
terraform plan
```

2. Apply the infrastructure:
```bash
terraform apply
```

3. Destroy the infrastructure when done:
```bash
terraform destroy
```

## Security Notes

- Never commit sensitive information like AWS credentials or private keys
- Use environment variables or AWS credentials file for authentication
- Regularly rotate access keys and certificates
- Follow the principle of least privilege for IAM roles

## Contributing

Contributions are welcome! Please:
- Fork the repository
- Create a feature branch
- Submit a pull request with clear documentation

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- HashiCorp for creating Terraform
- AWS for their cloud infrastructure services
- The open-source community for their contributions to infrastructure as code
