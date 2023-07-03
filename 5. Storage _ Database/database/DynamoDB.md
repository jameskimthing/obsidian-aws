![[DynamoDB.png]]
# DynamoDB
- Check [[Key-Value Stores]]
- A fully managed NoSQL key-value database
- **Create Tables**
	- Set names && key(s)
	- Set expected read / write capacities (or on-demand)
	- Choose encryption settings
- **Manage Data**
	- Write && read via AWS API / CLI / SDK
	- Congigure backups

#### Other Features
- **Streams**
	- ![[DynamoDB Streams.png]]
	- Time-ordered series of database item changes
	- Subscribe to process item changes
- **Global Tables**
	- Fully managed mult-region database
	- High availability thanks to automatic replication
	- Great performance thanks to global reach
- **DAX**
	- ![[DynamoDB DAX.png]]
	- *DynamoDB Accelerator*
	- Managed in-memory [[Caching]] for *DynamoDB*
	- Accelerates database queries


