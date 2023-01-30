# EC2 - Elastic Cloud Compute

- Multi-tenancy : Sharing hardware between virtual machines
  - Runs on top of **Physical Host Machines** managed by AWS using virtualization technology
  - A user, using the AWS instance is sharing the host with other EC2 Users
  - A Hypervisor on the host machine is responsible for sharing resources with the connected computers

- While provision an EC2 instance, can configure:
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

## Pricing

Available plans
- On-Demand : No long term commitment. Used for short term, irregular workloads
- Savings Plan : Requires 1 year or 3 year term committment and offers low prices.
- Reserved Instances : Reserve an instance for 1 year or 3 year term
- Spot Instances : Use unused EC2 computing capacity, AWS can reclaim these any time (By giving a 2 min warning)
- Dedicated Hosts : Physical hosts dedicated for an account (Generally used for meeting compliance requirements)
