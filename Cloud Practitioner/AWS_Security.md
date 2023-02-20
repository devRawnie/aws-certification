# AWS Security


## Shared Responsibility Model

- AWS is responsible for securing the cloud
- Customer is responsible for security of the services being used in the cloud

![image](https://user-images.githubusercontent.com/103091956/218302152-78cf5f69-294c-4aae-9aa8-b55712bbb68d.png)

### EC2

![image](https://user-images.githubusercontent.com/103091956/2
18302401-cf279179-37dd-438f-be45-d37992c35403.png)


## AWS User Permissions and Access

- When we register for an AWS Account we are essentially creating a `Root User`
- A Root User can access any resource in the account
  - Root user should `always` enable Multi Factor Authentication

## AWS Identity and Access Management

- Create an IAM User
- By default, these users have no permissions
- Permissions can be granted at a granular level
- Follow the `Principal of Least Privilege`
  - Only allow permissions to someone for something that they need
- Attach an IAM Policy to an IAM User
  - A JSON Document
  - Describes what API calls a user `can/can not` make
  - Contains of an Effect, Action and Resource
  - `Effect` : Allow/Deny
  - `Action` : API Call
  - `Resource` : Unique ID on which the effect is applied for the given action
- `IAM Group` : Can attach a policy to a group, and it will be applied to all the users in that group
- `IAM Roles`
  - Have associated permissions
  - These roles can be assigned to an IAM User temporarily
  - Can assign roles to external identities and federate users into AWS Account without creating an AWS IAM User for them 

## AWS Orgnaizations

- Central location to manage multiple accounts
- Consolidated Billing for all accounts
- Service Control Policies : To give permissions to member accounts
- `Organizational Units` : Multiple accounts can be grouped into organizational units to make it easier to manage accounts

## Compliances

- Consumer data used in EU -> General Data Protection Regulation (GDPR)
- Healthcare applications in US -> Health Insurance Portability and Accountability Act (HIPAA)

### AWS Artifact
- Whitepapers and Documentation regarding how AWS is following best practices related to required compliances
- Compliance reports done by third parties
- Consists of
  - AWS Artifact Agreements : Manage agreements between AWS and an organization
  - AWS Artifact Reports : Provide compliance reports about standards to be followed for a member of a company

## Distributed Denial of Service (D.D.O.S) Attack

### UDP Flood
-  Attacker will request an online service for some data
-  In return address, it will put the address of the targeted service
-  The targeted service is overwhelmed by the amount of data it received

### HTTP Level Attacks

- Multiple machines send request to a normal HTTP endpoint multiple times

### SLOWLORIS ATTACK

- Attacker pretends to have a slow internet connection and hogs the resources, during which regular people can't use those resources

## AWS WAF

- Web Application Firewall
- Filters incoming traffic containing the signature of bad actors

## AWS SHIELD
- Service that protects all AWS Customers at no cost
- Protects the systems from most common and frequently occuring DDOS Attacks

## Security

### Encryption

- `Encryption at rest` : Data at rest that is stored in some database is in encrypted form
- `Encryption in transit` : Data passing between clients and services or between multiple services is encrypted
  - SQS
  - RDS
  - S3

## AWS Inspector

- Helps improve security and compliance of the AWS Deployed application
- Runs an automated security assessment against our infrastructure
  - Network configuration reachability piece
  - Amazon agent
  - Security assessment service

## AWS Guard Duty

- Checks cloudwatch logs and other metadata to detect any possible threat

