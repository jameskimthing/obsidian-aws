#organize 
![[Networking Content Delivery.png]]
# Networking Content Delivery
- Check [[IP Addresses]]

## Management && Security
- Management of the cloud, can also check out [[Management Governance]]
- Security, can check out [[Security]]
	- [[NACL]] --> Controlling traffic at [[Subnets]] level
	- [[Security Group]] --> Controlling traffic at instnance level
	- For more info, check out [[VPC]]
- [[GovCloud]] --> For having incredibly secure data

| Icon | Name | Description |
| --- | --- | --- |
| ![[CloudMap.png]] | [[CloudMap]] | Define custom names for application resources |
| ![[VPC.png]] | [[VPC]] | To manage own network in the cloud |
| ![[ACM.png]] | [[ACM]] | For [[SSL]] certs |
| ![[Direct Connect.png]] | [[Direct Connect]] | Connect directly between services, NOT with the internet, but AWS's own provisioned connection |

## Delivery
- [[Edge Locations]] --> Locations around the world that cache content
- [[Regions, AZs, Data Centers]] --> Servers around the world
- [[Compute#More Compute Locations|More Locations]] --> More locations
- [[S3#S3TA|S3TA]] --> Accelerated delivery from *S3* buckets
- *CloudFront* vs *Global Accelerator*
	- [[CloudFront]] --> [[Edge Locations]] to *cache* content
	- [[Global Accelerator]] --> Find the *optimal pathway*
- Check out the [[Route Table]]

| Icon | Name | Description |
| --- | --- | --- |
| ![[Route 53.png]] | [[Route 53]] | AWS-managed *DNS* service |
| ![[ELB.png]] | [[ELB]] | Distribute load across available instances |
| ![[CloudFront.png]] | [[CloudFront]] | A content delivery network |
| ![[_icons/Global Accelerator.png]] | [[Global Accelerator]] | Improve traffic performance |
| ![[EC2 Auto Scaling.png]] | [[EC2 Auto Scaling]] | Automatic scaling of [[EC2]] instances |


#### Examples
![[networking example.png|500]]
	1. Client requests data
	2. [[Route 53]] --> Uses DNS change "company.com" to ab IP address, sent back to client
	3. [[Edge Locations]] --> Request sent here, through services such as [[CloudFront]]
	4. [[ELB]] --> Then sent here, to the matching [[EC2]] instance


#### Example 2:
![[VPC Networking Sample.png|500]]


