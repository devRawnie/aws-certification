# AWS Global Infrastructure

## AWS Regions

- Region is a strategic AWS locations around the world
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
- Multiple Availability Zones in a single AWS Region
- > It is advised to keep the required infrastructure in atleast two AZs in a single region 
