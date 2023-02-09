# AWS Storage

## Block Level Storage

- EC2 instance by default provide local storage called `Instance Store Volumes`
  - Physically attached to the AWS Host on which the EC2 instance is running
  - On terminating instance, all data stored on these instances is lost
  - During stopping and re-starting the EC2 instance can start on another host, and hence data will be lost

## AWS Elastic Block Storage

- Can create virtual hard drives (EBS Volume)
- Can be attached to the EC2 instances
- Not attached to the AWS host
- Define `size`, `type` and `configuration`
- Provides a feature to create `snapshots` : Incremental backups of EBS Volume

## AWS Simple Storage Service (S3)

- Store any type of data
- Data is stored as an object
  - Object contains of `Data`, `Metadata` and `Key`
- Data is stored in a `bucket`
- Max size of a single file is 5 TB
- Can version objects


- S3 Storage Classes

## S3 Standard

- 11 9's of durability -> 99.999999999 % chance that it will remain intact in an S3 bucket after 1 year
- Data uploaded on S3 is stored across atleast 3 AWS facilities
- Can be used for uploading static websites

## S3 Standard Infrequent Access

- Data that is accessed less frequently
- Perfect to store data backups

## S3 Glacier

- For data that is to be stored for millions of years

### S3 Lifecycle Management

- Moves data automatically between tiers


> Object Storage vs Block Storage

### Object Storage

- Stores file as an object
- If some change occurs in an object, the entire object needs to be re-uploaded

### Block Storage

- Breaks down a file into smaller parts called `blocks`