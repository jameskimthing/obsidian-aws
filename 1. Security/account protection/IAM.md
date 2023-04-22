# Identity and Access Management
![[Pasted image 20230405130212.png]]
- Web service that helps securely control access to AWS resources, used to control *who* has permissions to *what*

## About
- Check [Role vs User](https://stackoverflow.com/questions/46199680/difference-between-iam-role-and-iam-user-in-aws)
- An AWS IAM user is like a person who has a specific set of permissions to do things in AWS. An IAM role is like a hat that has specific permissions attached to it. Anyone who wears the hat can do things in AWS according to the permissions attached to the hat. The difference is that an IAM user is associated with a specific person while an IAM role can be worn by anyone who needs it
- **Root Account** --> The base account, not to be used / shared, can create *IAM users*

- **IAM User** --> End user think about people
- **Groups** --> A set of users under one set of permissions (*policies*)
- **Roles** --> Used to grant specific permission to specific actors for a set of duration of time
	- These actors can be *authenticated by AWS or some trusted external system*

- User and roles use **policies** for authorization
	- JSON document that outlines permissions for users or groups

#### Role Types
-   **AWS service roles** --> (for example: [[EC2]], [[Lambda]], [[Redshift]], ...)
-   **Cross-Account Access** --> Granting permissions to users from other AWS account, whether you control those account or not.
-   **Identity Provider Access** --> Granting permissions to users authenticated by a trusted external system
	- AWS supports two kinds of identity federation
		1. Web-based identity such as Facebook, Google
		2. IAM support ingeration via OpenID Connect - SAML 2.0 idetity such as Active Directory, LDAP.

## Notes
- By default, no permissions are given
- In AWS you apply the least privilege principle: don’t give more permissions than a user needs
- When permissions *clash* = Explicit **denies always win** over any allows

![[IAM.png|600]]

![[General overview.png|600]]