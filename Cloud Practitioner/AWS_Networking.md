# AWS Networking

## AWS Virtual Private Cloud

- Private Network 
- Subnet : Chunks of IP Address in a VPC, that group resources together based on security or operational needs
- `Public Subnet`  : Resources put in this subnet are public facing
  - Need to attach an Interet Gateway in front of the VPC to allow public traffic to connect to this
  - Need to attach a Virtual Private Gateway in front of the VPC to restrict access to only specific group of people

- `Private Subnet` : Resources put in this are private, and not publically accessible
  - However, the bandwith used to connect to Private resources is the same as the one being used by the public
  - Can cause congestion due to large traffic

- Subnets can communicate with each other in a VPC

## AWS Direct Connect

- Helps provide a direct connection to the VPC that is not shared by the public.
- Dedicated to only the selected group which have been provided access


## Network Hardening

### Network ACL

![image](https://user-images.githubusercontent.com/103091956/217143349-668ffaba-7671-41f6-b38a-997a041431d0.png)

- `STATELESS`
- Every packet directed to the VPC is checked at the gateway against a `Network Access Control List (ACL)`
- Network ACL determine whether a packet has access to enter or leave VPC based on
  - who sent the packet
  - how the packet is trying to communicate
- Don't allow any packet to come in or go out

### Security Group

![image](https://user-images.githubusercontent.com/103091956/217144014-5a38a095-fe03-4966-9fab-2db19b13d45d.png)

- Virtual Firewall
- Controls inbound and outbound traffic for an EC2 instance
- By default they don't allow any packet to come in, and allow all packets to go out
- `STATEFUL` : Remember if a packet left an instance, and on its way back that packet is allowed to go in to an EC2 instance

## Global Networking

### Route 53

- AWS Domain Name Service
- Routing policies
  - Latency based routing
  - Geolocation / Geoproximity based DNS
  -  Weighted round robin
