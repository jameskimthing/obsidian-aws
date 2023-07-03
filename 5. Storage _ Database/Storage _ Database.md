#organize 
# Storage && Database
- Check [[Backup]]

![[Storage.png]]
## Storage
- *EFS* vs *FSx*
	- [[EFS]] --> Cheaper, some services only support this (like [[Lambda]], Linux [[ECS]] containers)
	- [[FSx]] --> Some services only support this (like Windows [[ECS]] containers)

| Icon | Name | Description |
| --- | --- | --- |
| ![[Backup.png]] | [[Backup]] | Centralized backput management |
| ![[EBS.png]] | [[EBS]] | Block storage |
| ![[S3.png]] | [[S3]] | Object storage |
| ![[EFS.png]] | [[EFS]] | File system |
| ![[FSx.png]] | [[FSx]] | Similar to [[EFS]], without some tradeoffs |
| ![[Storage Gateway.png]] | [[Storage Gateway]] | Connect on-prem storage to AWS |

#### Comparison in between

|  | [[EBS]] | [[EFS]] | [[S3]] |
| --- | --- | --- | --- |
| About | Attachable hard drives | Attachable file systems | Independent object storage |
| Format | Unformatted hard drive | Pre-formatted file system | Store application, user, business, or personal files |
| Scaling | Less auto-scaling, more manual work | Scales automatically | Unlimited scaling built-in |
| Usage | EC2-exclusive | Can be used with multiple services | Access with or without other services |
| Multi-attach | Is possible, but not the focus | Is a core feature |  |


![[Database.png]]
## Database
- Database Types
	- **SQL** --> Relational, data normalized and split across tables. (ex: MySQL, PostgreSQL, [[RDS]])
	- **NoSQL** --> Not relational, data may nor may not be split acrosstables (ex: MongoDB, Firestore, [[DynamoDB]], [[Neptune]])
- More AWS Services
	- **MemoryDB** = Persistent in-memory storage
	- **DocumentDB** = Document (nested data structure) database
	- **Keyspaces** = Wide column database (flexible column formats)
	- **Timestream** =Time series databse
	- **Quantum Ledger Database** = Immutable log of data changes
- Hosting options
	- **Managed** --> Less control, less responsibility
		- Define rules, but AWS does the heavy lifting
		- ex: [[RDS]], [[DynamoDB]]
	- **Self Hosted** --> Full control, more responsibility
		- Keep software patched and manage backups
		- ex: [[EC2]]
- With the internet:
	- ![[VPCs and Databases.png|750]]

| Icon | Name | Description |
| --- | --- | --- |
| ![[ElastiCache.png]] | [[ElastiCache]] | Caching. AWS version of redis |
| ![[DMS.png]] | [[DMS]] | Database migration service |
| ![[Neptune.png]] | [[Neptune]] | Serverless graph database |


