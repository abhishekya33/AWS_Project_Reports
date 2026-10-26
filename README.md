# AWS Hands-On Projects

Practical labs where I designed, built and secured infrastructure on AWS using the Management Console and CLI. Each project folder contains a full write-up with the architecture, step-by-step implementation, verification results, and security notes on what I would harden for production.

## Projects

| # | Project | What it demonstrates | Key services |
|---|---|---|---|
| 1 | [Custom VPC with NACL Traffic Filtering](./01-vpc-ec2-nacl-lab/) | Network design from scratch, public/private subnets, NAT, jump-host access, and blocking ICMP/SSH with NACL deny rules | VPC, EC2, NAT Gateway, NACL |
| 2 | [Chatbot on Elastic Beanstalk with S3 Image Storage](./02-beanstalk-chatbot-s3/) | Deploying a Node.js app, IAM roles instead of access keys, S3 bucket policy and CORS | Elastic Beanstalk, IAM, S3 |
| 3 | [Secure Multi-Tier Web Architecture](./03-multi-tier-web-architecture/) | Tiered security groups, private RDS, S3 static hosting, event-driven Lambda image processing | VPC, RDS, S3, Lambda, Beanstalk |

## Skills demonstrated

- **Network security:** VPC design, route tables, security groups vs. NACLs (stateful vs. stateless), explicit IP deny rules, private subnets with NAT
- **Identity and access management:** IAM users, roles and policies, least-privilege thinking, MFA considerations
- **Data protection:** S3 bucket policies, CORS, private database placement, security group chaining
- **Deployment and automation:** Elastic Beanstalk, event-driven Lambda, Linux/CLI administration
- **Verification:** each control is tested before and after (ping results, `AccessDenied` vs. success, connectivity checks)

## Repository structure

```
aws-projects/
├── README.md
├── 01-vpc-ec2-nacl-lab/
│   ├── README.md
│   └── images/
├── 02-beanstalk-chatbot-s3/
│   ├── README.md
│   └── images/
└── 03-multi-tier-web-architecture/
    ├── README.md
    └── images/
```

## Notes

- Account IDs, public IP addresses, instance IDs and credentials have been redacted or replaced with placeholders such as `<my-public-ip>`.
- These are learning labs. Where a setting was deliberately permissive (for example, SSH open to the internet), the project README says so and lists the production-grade alternative.
- AWS resources used in these labs were removed after testing to avoid ongoing charges.
