# CloudTrail
![[CloudTrail.png]]
- Can monitor your AWS deployments in the cloud by getting a history of AWS API calls, including
	- API calls made via the AWS Management Console
	- The AWS SDKs
	- The command line tools
	- And higher-level AWS services
- Can also identify:
	- Which users and accounts called AWS APIs for services that support *CloudTrail*
	- The source IP address the calls were made from
	- When the calls occurred

#### Cloudtrail Insights
![[CloudTrail Insights.png]]
- This optional feature allows CloudTrail to automatically detect unusual API activities in your AWS account
	- *ex:* CloudTrail Insights might detect that a higher number of Amazon [[EC2]] instances than usual have recently launched in your account. You can then review the full event details to determine which actions you need to take next
	

![[Cloudtrail form.png]]