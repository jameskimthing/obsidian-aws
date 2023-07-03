# AWS Organizations
![[Organizations.png]]
- Check [[Control Tower]] --> *organizations*, but pre-configured
- Lets you create new AWS accounts at no additional charge
- With accounts in an organization, you can easily:
	- Allocate resources
	- Group accounts
	- Apply governance policies to accounts or groups, called **SCP** --> Secure Control Policy
		- are like [[IAM]]'s policies, but for *organizations*

#### Can have Consolidated Billing
![[Consolidated Billing.png]]
- Can have *Volume Discounts*
- Can be seen with [[Cost Explorer]]

#### Group accounts into *Organization Units* and enforce policies
![[Organization Units.png]]

#### SCPs - Secure Control Policies
- An AWS Organizations feature that allows you to set permission guardrails for organization accounts. These guardrails set maximum access rights which can't be exceeded by permissions set inside of the affected organization accounts. Even if an identity (e.g., an [[IAM]] user) in an account would receive a policy that grants more access rights, the SCP would restrict the maximum access rights

![[Organizations Example.png]]