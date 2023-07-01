#organize 
![[Networking Content Delivery.png]]
# Networking Content Delivery
- [[Route 53]] --> AWS-managed *DNS* service
- [[ACM]] --> For [[SSL]] certificates
- [[CloudMap]] --> Define custom names for your application resources, and it maintains the updated location of these dynamically changing resources

#### Example:
![[networking example.png|500]]
Suppose application is running on several [[EC2]], in an [[EC2 Auto Scaling]], attached to [[ELB]] 
	1. Customer requests data from the application by going to AnyCompany’s website. 
	2. [[Route 53]] uses DNS resolution to identify AnyCompany.com’s corresponding IP address, 192.0.2.0. This information is sent back to the customer. 
	3. The customer’s request is sent to the nearest [[Edge Locations]] through [[CloudFront]]
	4. [[CloudFront]] connects to the [[ELB]], which sends the incoming packet to an [[EC2]]

## Content Delivery Network
- Systems of distributed servers that work together to deliver content to users in a fast and efficient manner
- [[S3TA]] --> Accelerated delivery from *S3* buckets
- For more places other than *Edge Locations*, check [[Local Zones, Outposts, Wavelength Zones]]

*Differences:*

|         | [[CloudFront]]                                      | [[Global Accelerator]]                                                                                                                          |
| ------- | --------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| Uses    | Uses [[Edge Locations]] to *cache* content          | Uses [[Edge Locations]] to *find an optimal pathway* to the nearest regional endpoint                                                           |
| Handles | *HTTP Protocol*                                     | Both *HTTP Protocol* and non-HTTP Protocols like *TCP* and *UDP*                                                                                |
| IP      | Multiple sets of dynamically changing IP addresses  | Set of static IP addresses as a fixed entry point                                                                                               |
| Pricing | Mainly based on data transfer out and HTTP requests | Fixed hourly fee + incremental charge over your standard Data Transfer rates ([DT-Premium](https://aws.amazon.com/global-accelerator/pricing/)) |
|         |                                                     |                                                                                                                                                 |




## Management
- Check [[IP Addresses]]
- [[VPC]] --> Gives you full control over your virtual networking environment, including resource placement, connectivity, and security

## Dynamic Scaling && Load Balancing
- [[EC2 Auto Scaling]] --> Automatic scaling of [[EC2]] instances
- [[ELB]] --> Service to distribute load (e.g. incoming requests) evenly across available instances
