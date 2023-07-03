![[CloudFormation.png]]
# CloudFormation
- Speed up cloud provisioning with infrastructure as code
- Lets you model, provision, and manage AWS and third-party resources by treating infrastructure as code

## CDK - Cloud Development Kit
- Builds on top of *CloudFormation*
- Allows you to define your cloud infrastructure via code
- No templates and no CloudFormation template language
	- Can use languages like Python or TypeScript to define your infrastructure
- Under the hood, the CDK tool then creates CloudFormation templates again
- The templates can be stored in [[S3]] buckets
