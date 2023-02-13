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

https://explore.skillbuilder.aws/learn/course/134/play/62437/aws-cloud-practitioner-essentials
