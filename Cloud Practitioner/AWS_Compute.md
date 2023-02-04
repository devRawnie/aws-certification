# AWS Compute Services


## 1. EC2 - Elastic Cloud Compute

- Multi-tenancy : Sharing hardware between virtual machines
  - Runs on top of **Physical Host Machines** managed by AWS using virtualization technology
  - A user, using the AWS instance is sharing the host with other EC2 Users
  - A Hypervisor on the host machine is responsible for sharing resources with the connected computers

- While provisioning an EC2 instance, can configure:
  - Operating System
  - Software to run (DB, Third Party Software)
- Can vertically scale on-demand
- Can setup networking on-demand
- CaaS (Compute as a Service) model

- Types of EC2 instances
  - Each instance type is grouped under an instance family
  - General Purpose : Code Repo, Web Server
  - Compute optimized : Gaming Server, Scientific Modeling
  - Memory optimized : Graphics Processing, Utiliie
  - Accelerated Computing : Use hardware accelerators
  - Storage Optimized : When high frequency I/O is required

### Pricing

Available plans
- On-Demand : No long term commitment. Used for short term, irregular workloads
- Savings Plan : Requires 1 year or 3 year term committment and offers low prices.
- Reserved Instances : Reserve an instance for 1 year or 3 year term
- Spot Instances : Use unused EC2 computing capacity, AWS can reclaim these any time (By giving a 2 min warning)
- Dedicated Hosts : Physical hosts dedicated for an account (Generally used for meeting compliance requirements)

### Scaling
- Automatically responding to changing demand by scaling up or out physical resources
  - Scale Up : Increase the server configuration
  - Scale Out : Increase the number of servers
- Handled by `AWS EC2 AUTO SCALING`
- Types
  - Dynamic Scaling : Responds to **changing** demand
  - Predictive Scaling : Schedules the right no of EC2 instances based on **predicted** demand

### AWS EC2 AUTO SCALING
- Create an autoscaling group and provision the following
  - Minimum Capacity : Instances that launch immediately after creating the group
  - Desired Capacity : Default to minimum capacity if not set.
  - Maximum Capacity : Maximum no of instances that will be created in this group

### Load Balancing
- Required to distribute traffic among different resources in an auto-scaling group
- AWS Service : `Elastic Load Balancer`
  - Single point of contact for all incoming web traffic
  - Works in a particular region
  - Scales automatically

### Messaging and Queuing

- Required when one service needs to communicate with another service and get a response back
- When this scales, the performance will degrade as the services are communicating synchronously

### AWS Simple Notification Service

- Publish / Subscribe service
- Publish a message to SNS (topic) -> Sends it to all subscribers


### AWS Simple Queue Service

- Send, Store and Receive messages between multiple components
- Messages are placed here, until they are processed

## 2. AWS Lambda

- Serverless compute option
- Cannot see the underlying architecture
- AWS Handles provisioning, scaling and availability
- Lambda function runs on a registered trigger source

## 3. AWS Elastic Container Service
## 4. AWS Elastic Kubernetes Service

- Container orchestration tools
- Container (`Docker`) packages code with its dependencies
- These containers run on EC2 instances and can be managed by ECS / EKS instances
- Scaling and Availability will have to be handled by developers

## 5. AWS Fargate

- Serverless compute platform for ECS / EKS
- Containers can run on Fargate instead of EC2
- Scalability and Availability will be handled by AWS for Fargate
