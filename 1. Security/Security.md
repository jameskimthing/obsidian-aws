#organize 
![[Pasted image 20230405130505.png]]
# Security
- Securing your AWS account, services && application
- [[Security Hub]] --> Important!
- [[Trusted Advisor]] --> Can check for security
- [[Shared Responsibility]] --> Security is shared between the user and AWS
- [[GovCloud]] --> Regions for very sensitive data
- Managing traffic:
	- [[Security Group]] --> At instance level
	- [[NACL]] --> At [[Subnets]] level
	- (Security groups preferred. for more info, check out [[VPC]])

## Client side

| Icon | Name | Description |
| --- | --- | --- |
| ![[_icons/Security Hub.png]] | [[Security Hub]] | Consolidated security status management |
| ![[Cognito.png]] | [[Cognito]] | Security for the application user |
| ![[ACM.png]] | [[ACM]] | Managing [[SSL]] certs |



## Account Protection
- Account must not get compromised (do **MFA**)
- Prevent malicious account / service usage
- Secure cross-account service usage
- For differences between *User Groups* and *Organizations*, check [here](https://stackoverflow.com/questions/66525514/the-differences-between-iam-and-aws-organization)

| Icon | Name | Description |
| --- | --- | --- |
| ![[Identity Center.png]] | [[Identity Center]] | Managing accounts |
| ![[_icons/IAM.png]] | [[IAM]] | Managing identities (employees) |
| ![[_icons/RAM.png]] | [[RAM]] | Securely share resources across accounts |
| ![[Organizations.png]] | [[Organizations]] | Check multiple accounts at once |
| ![[CloudTrail.png]] | [[CloudTrail]] | Track API usage (which identities did what) |



## Compliance
- Enforce && prove compliance

| Icon | Name | Description |
| --- | --- | --- |
| ![[_icons/Config.png]] | [[Config]] | Define && Track service configuration |
| ![[Artifact.png]] | [[Artifact]] | Get compliance reports |
| ![[_icons/Audit Manager.png]] | [[Audit Manager]] | Prove one's compliance |




## Application Protection
- Detect (application / software vulnerabilities) / insecure configurations 
- Investigate security issues & incidents
- [[CloudTrail]] --> Keeps a log of past API calls

| Icon | Name | Description |
| --- | --- | --- |
| ![[GuardDuty.png]] | [[GuardDuty]] | Automatically monitors accounts for suspicious activities, findings then surfaced |
| ![[Detective.png]] | [[Detective]] | Analyze && explore security incidents (not automatic) |
| ![[Inspector.png]] | [[Inspector]] | Alerts u of application / workload vulnerabilities |



## Network Protection
- Detect malicious network traffic
- [[Security Group]] && [[NACL]] --> Controls traffic at instance / [[Subnets]] level

| Icon | Name | Description |
| --- | --- | --- |
| ![[_icons/WAF.png]] | [[WAF]] | Protect against common web exploits and bots |
| ![[_icons/Network Firewall.png]] | [[Network Firewall]] | Defends against a wider range of traffic |
| ![[Shield.png]] | [[Shield]] | Protection against DDoS attacks |
| ![[_icons/Firewall Manager.png]] | [[Firewall Manager]] | Centrally configure and manage firewall rules |



## Data Protection
- Encrypt data at rest && transit
- Keys used for encryption of data / files
- Protect code secrets
- Prevent unintended data exposure
- For differences between [[KMS]] and [[CloudHSM]], check [here](https://stackoverflow.com/questions/67446389/what-are-the-differences-between-aws-cloud-hsm-and-kms)

| Icon | Name | Description |
| --- | --- | --- |
| ![[_icons/KMS.png]] | [[KMS]] | Data encryption, AWS-managed keys |
| ![[_icons/CloudHSM.png]] | [[CloudHSM]] | Data encryption, custom key store |
| ![[ACM.png]] | [[ACM]] | Encrypt network traffic ([[SSL]]) |
| ![[Macie.png]] | [[Macie]] | Discover data protection issues |
| ![[Secrets Manager.png]] | [[Secrets Manager]] | Securely store secret values |
| ![[Parameter Store.png]] | [[Systems Manager#Parameter Store\|Parameter Store]] | Env variables (not as secure as [[Secrets Manager]])  |  |




