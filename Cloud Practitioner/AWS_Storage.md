# AWS Storage

## Block Level Storage

- EC2 instance by default provide local storage called `Instance Store Volumes`
  - Physically attached to the AWS Host on which the EC2 instance is running
  - On terminating instance, all data stored on these instances is lost
  - During stopping and re-starting the EC2 instance can start on another host, and hence data will be lost

## AWS Elastic Block Storage

- Can create virtual hard drives (EBS Volume)
- Can be attached to a `single` EC2 instances
- Not attached to the AWS host
- Availability Zone level resource
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

## AWS Elastic File System (EFS)

- Multiple instances can access data in EFS at the `same time`
- Linux file system
- Regional resource
- Automatically Scales

![image](https://user-images.githubusercontent.com/103091956/217779131-b1602209-bd14-4700-88c9-2a4738657899.png)

## AWS Relational Database Service

- Relational Database as a Service
- Provide `Lift and Shift Migration`
- Provides automated patching, Backups, Disaster Recovery
- MySQL, PostgreSQL, Oracle, MariaDB, Microsoft SQL Server

## AWS Aurora

- MySQL and PostgreSQL
- Data replication: Upto 6 copies of data in 3 Availability Zones
- Read Replication: Upto 15 read replicas
- Continuous Backup to S3
 
## AWS DynamoDB

- NoSQL (Non relational)  Database
- Data is stored as items
- Item has attributes (Key Value pair)
- Scaling is handled automatically
- Copies data redundantly across availability zones

## AWS Redshift

- `Data Warehouse` : Used for storing historical data and performing historical analysis (instead of operational analysis)
- Data warehouse as a Service
- For running Business Intelligence queries on large sets of data

## AWS Database Migration Service

- Used to migrate data frmo a source database to a destination database
- Source database is active during the migration
- Source and Target databases don't necessarily have to be of the same type
- `Homogeneous Migration` : Migrating data between same types of database
- `Heterogeneous Migration` : Migrating data between different types of database
  - First need to convert schema of data from source table into the schema compatible with the destination table
- Database Consolidation : Merging multiple databases into a single database
