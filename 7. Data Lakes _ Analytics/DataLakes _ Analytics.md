#organize 
![[Pasted image 20230405132342.png]]
# DataLakes && Analytics
- Modern businesses generate huge amounts of data, structuring && analyzing such data efficiently can be a competitive advantage
- Check [here](https://aws.amazon.com/big-data/datalakes-and-analytics/)
- Key data lake aws service: [[S3]] (with [[Lake Formation]])
- Key data warehouse aws service: [[Redshift]]

## Analytics && Data Warehousing
- Example use case:
	- Use [[Kinesis]] to ingest and collect data streams from various sources
	- Use [[Glue DataBrew]] to perform the initial data preparation tasks like filtering, pivoting, and data type conversion
	- Use [[EMR]] to process the data streams, perform ETL (extract, transform, and load) and store the processed data in [[Redshift]]
	- Use [[OpenSearch Service]] to create search indexes and provide search functionality on the data
	- Use [[Athena]] to run SQL queries on the data stored in [[Redshift]]
	- Use [[QuickSight]] to create interactive visualizations and dashboards to gain insights from the data


## Data Movement
- Example use case:
	- Use [[Kinesis]] *Streams* to collect data streams in real-time from various sources
	- Use [[Kinesis]] *Firehose* to automatically transform, enrich, and load the data streams into Amazon [[MSK]] (Managed Streaming for Kafka)
	- Use [[Glue]] to create and schedule ETL jobs that process the data streams and prepare them for loading into a data warehouse like [[Redshift]] or a data lake like [[S3]]
	- Use [[DMS]] (Database Migration Service) to migrate the data from [[MSK]] to [[Redshift]] or [[S3]]
	- Use [[Glue]] to create a Data Catalog and register the data in the data lake or data warehouse

#### Between Glue and Glue Databrew:
- Use [[Glue Databrew]] to clean and prepare data, and then use AWS [[Glue]] to orchestrate the ETL jobs that move the data from the source data store to the destination data store
- Use AWS [[Glue]] to perform the ETL jobs, and then use [[Glue Databrew]] to perform additional data cleaning and normalization before the data is used for analytics or machine learning
- Use [[Glue Databrew]] to prepare data for use in other AWS services like Amazon [[SageMaker]] or Amazon [[QuickSight]], without using AWS [[Glue]]

## Data Lake
- [[S3]], [[Lake Formation]] --> Object storage
- [[S3 Glacier]], [[Backup]] --> Archive && backup
- [[Glue]], [[Lake Formation]] --> Data catalog
- [[Data Exchange]] --> Third-party data

## Predictive Analytics && Machine Learning
- [[Deep Learning AMIs]] --> Frameworks and interfaces
- [[SageMaker]] --> Platform services


