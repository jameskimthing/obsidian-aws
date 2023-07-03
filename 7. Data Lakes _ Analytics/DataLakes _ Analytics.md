#organize 
![[Analytics.png]]
# DataLakes && Analytics
- Modern businesses generate huge amounts of data, structuring && analyzing such data efficiently can be a competitive advantage
- Check [here](https://aws.amazon.com/big-data/datalakes-and-analytics/)
- Key data lake aws service: [[S3]] && [[Lake Formation]]
- Key data warehouse aws service: [[Redshift]]
- 

## Data

| Icon | Name | Description |
| --- | --- | --- |
| ![[S3.png]] ![[_icons/Lake Formation.png]] | [[S3]], [[Lake Formation]] | Object storage |
| ![[Glacier.png]] ![[Backup.png]] | [[S3#S3 Glacier\|Glacier]], [[Backup]] | Archive && backup |
| ![[Glue.png]] ![[_icons/Lake Formation.png]] | [[Glue]], [[Lake Formation]] | Data catalog |
| ![[Data Exchange.png]] | [[Data Exchange]] | Third party data |



## Analytics && Data Warehousing
- Below table is an *example use case* of how the process might work
- Check [here](https://stackoverflow.com/questions/62251139/what-is-the-difference-between-aws-glue-etl-job-and-aws-emr) for the difference between [[Glue]] and [[EMR]]

| Icon | Name | Description |
| --- | --- | --- |
| ![[Kinesis.png]] | [[Kinesis]] | Ingest and collect data streams from various sources |
| ![[Glue Databrew.png]] | [[Glue Databrew]] | Perform the initial data preparation tasks like filtering, pivoting, data type conversion |
| ![[EMR.png]] | [[EMR]] | Process the data streams, perform [[ETL]] and store data [[Redshift]] |
| ![[Redshift.png]] | [[Redshift]] | Data from [[EMR]] comes here (is a data warehouse) |
| ![[Athena.png]] | [[Athena]] | Run SQL queries on data stored in [[Redshift]] |
| ![[QuickSight.png]] | [[QuickSight]] | Create interactive visualizations to gain insight from the data |
| ![[OpenSearch Service.png]] | [[OpenSearch Service]] | Real time searching, monitoring, analysis of business and operational data |


## Data Movement
- Below is an *example use case* of how data movement might work

| Icon | Name | Description |
| --- | --- | --- |
| ![[Kinesis Data Streams.png]] | [[Kinesis\|Kinesis Streams]] | Collect dat streams in real time from various sources |
| ![[Kinesis Firehose.png]] | [[Kinesis\|Kinesis Firehose]] | Automatically transform, enrich, and load data streams to Amazon [[MSK]] |
| ![[MSK.png]] | [[MSK]] | Streaming Data |
| ![[Glue.png]] | [[Glue]] | - Create and schedule [[ETL]] jobs that process the streams and prepare them to load into places like [[Redshift]] and [[S3]] <br> - Create a data catalog and register the data in the data lake / warehouse |


#### Between Glue and Glue Databrew:
- Use [[Glue Databrew]] to clean and prepare data, and then use AWS [[Glue]] to orchestrate the ETL jobs that move the data from the source data store to the destination data store
- Use AWS [[Glue]] to perform the ETL jobs, and then use [[Glue Databrew]] to perform additional data cleaning and normalization before the data is used for analytics or machine learning
- Use [[Glue Databrew]] to prepare data for use in other AWS services like Amazon [[SageMaker]] or Amazon [[QuickSight]], without using AWS [[Glue]]


## Predictive Analytics && Machine Learning

| Icon | Name | Description |
| --- | --- | --- |
| ![[Deep Learning AMIs.png]] | [[Deep Learning AMIs]] | Frameworks and interfaces |
| ![[SageMaker.png]] | [[SageMaker]] | Platform services |

