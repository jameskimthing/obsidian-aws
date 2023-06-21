#organize 
![[Pasted image 20230405130505.png]]
# Security
- Securing your AWS account, services && application
- [[Cognito]] --> Security for the application user
- [[Security Hub]] --> Consolidated security status management
- [[ACM]] --> Managing [[SSL]] certificates


## Account Protection
- Account must not get compromised
- Prevent malicious account / service usage
- Secure cross-account service usage
- [[IAM]] && [[SSO (Now Identity Center)]] --> Manage identities
- [[Managed Directory]] --> Advanced login
- [[CloudTrail]] --> Track API usage (which identities did what)
- [[GuardDuty]] --> Detect malicious patterns
- [[Organizations]] --> To combine multiple accounts
- [[RAM]] --> Share resources cross-account

- For differences between *User Groups* and *Organizations*, check [here](https://stackoverflow.com/questions/66525514/the-differences-between-iam-and-aws-organization)


## Compliance
- Enforce && prove compliance
- [[Config]] --> Define && track service configuration
- [[Artifact]] --> Prove AWS is compliant
- [[Audit Manager]] --> Prove your compliance


## Application Protection
- Detect application / software vulnerabilities
- Detect insecure configurations
- Investigate security issues & incidents
- [[GuardDuty]] --> Automatically monitors your account for suspicious activities, and findings are surfaced
- [[Detective]] --> Analyze and explore security incidents (not automatic)
- [[Inspector]] --> Alerts you of application / workload vulnerabilities
- Also check [[CloudTrail]], which keeps a log of past API calls


## Network Protection
- Detect malicious network traffic
- [[WAF]] --> Protects against a particular threat
- [[Network Firewall]] --> Defends against a wider range of traffic
- [[Shield]] --> Protects against DDoS attacks
- [[Firewall Manager]] --> For managing firewalls centrally

- [[Security Group]] && [[NACL]] --> Controls traffic at instance / [[Subnets]] level


## Data Protection
- Encrypt data at rest && transit
- Protect code secrets
- Prevent unintended data exposure

- Keys, for encryption of data / files

- [[KMS]] --> Data encryption, AWS-managed keys
- [[CloudHSM]] --> Data encryption, Custom key store
- [[Secrets Manager]] --> Securely store secret values
- [[Parameter Store]] --> Environment variables (use [[Secrets Manager]] for *more* security)
- [[ACM]] --> Encrypt network traffic
- [[Macie]] --> Discover data protection issues

- For differences between *KMS* and *CloudHSM*, check [here](https://stackoverflow.com/questions/67446389/what-are-the-differences-between-aws-cloud-hsm-and-kms)


