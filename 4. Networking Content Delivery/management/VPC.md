# Virtual Private Cloud
![[Pasted image 20230405131606.png]]
- Used to manage your own network in the cloud
- Resources are grouped and organized in customer-managed networks
- Has *at least*:
	- 2 [[Subnets]]
	- 1 [[Route Table]]
- Each has a separate *IP CIDR* block (chcek [[IP Addresses]])
	- [[Subnets]] get parts of the block assigned
	- Resources such as an [[EC2]] instance receive auto-assigned public and private IPs
	- *Elastic IP* can be used for a fixed IP address
- [[VPC Endpoint && AWS PrivateLink]] for connecting without the internet

#### Managing Traffic
- Firewalls -> checks incoming / outgoing requests and conditionally blocks / allows them
- Controlling traffic:
	- [[Security Group]] --> At instance level
	- [[NACL]] --> At subnet level
	- *(Security Groups are preferred)*
*Security Groups vs NACL*

| About        | Security Group | Network Access Control List |
| ------------ | ---------------------------------------------------------- | ----------------------------------------------------------------------------- |
| State        | Stateful: Responses are allowed (if the request is passed) | Stateless: Requests & Responses are separate, need to manually allow response |
| Rules        | Supports **allow** rules only                              | Supports **allow && deny** rules                                              |

#### Internet Connection
- for with internal / only with own services, check [[Direct Connect]]
![[Pasted image 20230405131614.png]]
- **Internet Gateway**
	- What makes public [[Subnets]] have access to the internet
![[Pasted image 20230405131622.png]]
	- **NAT Gateway**
	- A Network Address Translation (NAT) service
	- Instances in a private subnet can connect to the internet
	- External services cannot initiate a connection with those instances

#### Connection between VPCs
![[Pasted image 20230405131635.png]]
- **VPC Peering:** Connecting 2 *VPC*s
![[Pasted image 20230405131656.png]]
- **Transit Gateway:** Connecting more than 2 *VPC*s

#### VPC Endpoint && AWS Privatelink


![[Security Group, NACL.png]]

