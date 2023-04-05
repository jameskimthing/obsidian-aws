#organize 
# Storage && Database
- Check [[Backup]]

## Storage
![[Pasted image 20230405132008.png]]
1. [[EBS]] for block storage
2. [[S3]] for object storage
3. [[EFS, FSx]] for a file system

#### Comparison
|              | EBS                                 | EFS                                | S3                                                   |
| ------------ | ----------------------------------- | ---------------------------------- | ---------------------------------------------------- |
| About        | Attachable hard drives              | Attachable file systems            | Independent object storage                                                     |
| Format       | Unformatted hard drive              | Pre-formatted file system          | Store application, user, business, or personal files |
| Scaling     | Less auto-scaling, more manual work | Scales automatically               | Unlimited scaling built-in                     |
| Usage        | EC2-exclusive                       | Can be used with multiple services | Access with or without other services                  |
| Multi-attach | Is possible, but not the focus      | Is a core feature                  |                                                      |


## Database
![[Pasted image 20230405132017.png]]
- [[ElastiCache]] --> For caching
- Also check [[Other Database Services]]
- Check [[DMS]] --> Database migration service
- Check [[Neptune]] --> Serverless graph database

#### Database types
|                   | SQL                                      | NoSQL                                                 |
| ----------------- | ---------------------------------------- | ----------------------------------------------------- |
| About             | Relational                               | Not relational                                        |
| Schema            | Fixed                                    | None                                                  |
| Normalized, Table | Normalized, split across multiple tables | Not normalized, may or may not be split across tables |
| *Examples*        | MySQL, PostreSQL, [[RDS]]                | MongoDB, [[DynamoDB]], Firestore, [[Neptune]]         |

- Different data / workload requirements favor different types

#### Hosting Options
|          | Self Hosted                                   | Managed                             |
| -------- | --------------------------------------------- | ----------------------------------- |
| Software | Install && operate database software manually | Let AWS manage                      |
| Used on  | e.g. [[EC2]]                                  | Key services: [[RDS]], [[DynamoDB]] |
| Control  | Full control, more responsibility             | Less control, less responsibility   |
| Manage   | Keep software patched, manage backups         | Define rules, but AWS does the heavy liftin                                    |
 
#### Database && VPCs
- Connection between internet requests and [[VPC]]s
- ![[VPCs and Databases.png|750]]