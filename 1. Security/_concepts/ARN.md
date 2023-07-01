### ARNs
- Amazon Resource Names (ARNs) uniquely identify AWS resources
- When you need to specify a resource unambiguously across all of AWS, such as in [[IAM]] policies, [[RDS]] tags, and API calls
*example:*
```
arn:partition:service:region:account-id:resource-id
arn:partition:service:region:account-id:resource-type/resource-id
arn:partition:service:region:account-id:resource-type:resource-id
```
