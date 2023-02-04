# AWS Global Infrastructure

## AWS Regions

- Region is a strategic AWS locations around the world, selected based on proximity
- One region has multiple datacenters
- Each datacenter has all the AWS Services
- Regions are inter-connected via a High Speed Fiber Network
- Developer can select which region to run their services in
- Data is isolated to the selected region unless explicit permission is given to move data across regions

**Factors to consider before choosing a region**

1. Compliance Requirements
2. Proximity : How close your region is from your customers
3. Feature Availability : Some region might not have all the AWS services
4. Pricing : Some locations are more expensive than others

## AWS Availability Zones

- Single data center (physical building) in an AWS Region
- Multiple Availability Zones are located miles apart in a single AWS Region
- > It is advised to keep the required infrastructure in atleast two AZs in a single region 
- Some services are by-default scoped to a region i.e. they run in multiple AZs

## Content Delivery Network

- Helps deliver and cache content (Text, Image, Video etc) all around the world
- AWS Service : `Cloudfront`
- Uses `Edge Locations`
  - separate from regions
  - deliver and cache content
  - 
  - Runs Cloudfront
  - Runs Domain Name Service called `AWS Route 53`
- `AWS Outposts` : AWS will install a fully operational regional center in user's data center


## Interacting with AWS Services
- AWS Management console
- AWS CLI
- AWS SDK
- Other tools (Ex. AWS Cloudformation, AWS Elastic Beanstalk)

### AWS Elastic Beanstalk

- Helps provision EC2 based environments
  - Load balancing
  - Scaling
  - Health monitoring

### AWS Cloudformation

- Can provision multiple services based on a declarative syntax given in JSON/YAML format called `Cloudformation Template`
