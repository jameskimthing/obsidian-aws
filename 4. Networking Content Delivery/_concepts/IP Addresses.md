#concept 
## (CIDR) Classless Inter-Domain Routing
- A notation used to specify a range of IP addresses in a VPC or subnet
- For specifying the IP addresses that are allowed to access your resources and your VPC or subnet
- Consists of an IP address, followed by a slash (/), followed by the number of bits that make up the routing prefix
	- Example: 10.0.0.0/16 specifies a range of IP addresses that starts at 10.0.0.0 and includes all the addresses up to 10.0.255.255.
- *Note:* Typically, addresses starting with **172** mean they are private

## Private, Public, Elastic IP Address
#### Public IP Address
- For internet communication
- Automatically assigned IPs (by [[Subnets]]) will change when instances are stopped / restarted
- Can't control which *Public IP Address* gets assigned to an instance
#### Private IP Address
- For Internal communication

#### Elastic IP Address
- Managed and assigned by the user
- Don't change and can be re-assigned
- **Scarce:** Only have a few Elastic IPs per region & account
- Unused Elastic IPs incur charges
- Instead, can use things like a **DNS** or application integration services like [[SQS]]
