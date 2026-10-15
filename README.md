# AWS CloudFormation VPC Infrastructure Project

## Project Overview

This project was part of my cloud engineering learning journey.

The aim was to use AWS CloudFormation to build infrastructure in AWS using Infrastructure as Code (IaC), rather than creating everything manually through the AWS Management Console.

Infrastructure as Code allows us to define the infrastructure we want to create using a template. This makes it easier to repeat deployments, make changes and troubleshoot problems.

For this project, I used a YAML template to create a VPC, public and private subnets, EC2 instances, security groups and a bastion host.

## AWS Services Used

- AWS CloudFormation
- Amazon VPC
- Amazon EC2
- AWS Security Groups
- Internet Gateway
- Route Tables
- Amazon S3

I also used the AWS CLI and Visual Studio Code to write, deploy and manage the infrastructure.

## What I Built

I created a custom VPC with six subnets spread across two Availability Zones.

These included:

- Two public subnets
- Two private application subnets
- Two private data subnets

I configured an Internet Gateway and public route tables to provide internet connectivity for resources in the public subnets.

I also deployed a bastion host and two EC2 application instances, App1 and App2, in separate private application subnets.

Security groups were configured to control network access between the instances.

## Testing

After deploying the infrastructure, I tested connectivity between the two application instances.

I successfully used the ping command to confirm that App1 and App2 could communicate across the private network.

This helped me understand how resources inside the same VPC can communicate using private IP addresses.

## Challenges and Troubleshooting

One of the biggest challenges during this project was troubleshooting errors.

I encountered several issues involving YAML syntax, indentation, CloudFormation stack updates and EC2 instance configurations.

One particular issue involved an EC2 instance type that was not eligible for the AWS Free Tier on my account.

I had to investigate the error, check which instance types were eligible and update my CloudFormation template.

There were moments when the troubleshooting became frustrating, particularly when one error led to another.

However, I continued working through the problems until I successfully deployed and tested the infrastructure.

This experience helped me understand that troubleshooting is an important part of cloud engineering.

## What I Learned

Through this project, I gained practical experience with:

- Using Infrastructure as Code to create AWS resources
- Writing CloudFormation templates using YAML
- Understanding how VPCs and subnets work
- Deploying resources across multiple Availability Zones
- Configuring internet gateways and route tables
- Understanding the purpose of a bastion host
- Using security groups to control network access
- Deploying EC2 instances into private subnets
- Testing communication between EC2 instances
- Troubleshooting CloudFormation deployment errors
- Using the AWS CLI to manage infrastructure

## Project Files

- `vpc-public.yaml` — CloudFormation template showing the infrastructure configuration.

**Note:** The public template uses example values for the SSH IP address and EC2 key pair name. These must be updated before deployment.

## Project Cleanup

After completing the project and testing the infrastructure, I deleted the CloudFormation stacks and verified that the EC2 instances had been terminated.

This was done to avoid leaving unnecessary AWS resources running.

## Next Steps

I plan to continue developing my understanding of AWS networking, CloudFormation and Infrastructure as Code through further hands-on projects.

