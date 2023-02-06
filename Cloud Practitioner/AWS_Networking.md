# AWS Networking

## AWS Virtual Private Cloud

- Private Network 
- Subnet : Chunks of IP Address, that group resources together
- `Public Subnet`  : Resources put in this subnet are public facing
  - Need to attach an Interet Gateway in front of the VPC to allow public traffic to connect to this
  - Need to attach a Virtual Private Gateway in front of the VPC to restrict access to only specific group of people

- `Private Subnet` : Resources put in this are private, and not publically accessible
  - However, the bandwith used to connect to Private resources is the same as the one being used by the public
  - Can cause congestion due to large traffic


## AWS Direct Connect

- Helps provide a direct connection to the VPC that is not shared by the public.
- Dedicated to only the selected group which have been provided access

