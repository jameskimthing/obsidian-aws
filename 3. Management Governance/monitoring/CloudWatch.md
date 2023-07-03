![[CloudWatch.png]]
# CloudWatch
- Managed monitoring service
- Gain system-wide visibility into resource utilization

## Usage
- **Collect Data**
	- Application logs (e.g. web server logs)
	- Service metrics && information
	- Detailed data collection via API or *CloudWatch Agent*
- **Analyze Data**
	- Log insights and *ServiceLens*
	- Charts && metric calculation
	- [[Containers]] and [[Lambda]] insights
- **Act**
	- Forward metrics or logs (e.g. to [[S3]] or external)
	- *Alarms*

#### CloudWatch ServiceLens
- Enhances the observability of your services and applications by enabling you to integrate:
	- Traces
	- Metrics
	- Logs
	- Alarms
	- And other resource health information
- Into one place
- Integrates CloudWatch with [[XRay]] to provide an end-to-end view of your application to help you more efficiently pinpoint performance bottlenecks and identify impacted users

#### CloudWatch Agent
- A software package that autonomously and continuously runs on your servers
- Can collect metrics and logs from [[EC2]], hybrid, and on-premises servers running both Linux and Windows

#### CloudWatch Dashboards
- Allow you to create, customize, interact with, and save graphs of AWS resources and custom metrics

![[CloudWatch Logs.png]]
#### CloudWatch Logs
- Lets you monitor and troubleshoot your systems and applications using your existing system, application, and custom log files
- Can be used for real time application and system monitoring as well as long term log retention
- [[CloudTrail]] logs can be sent to *CloudWatch Logs* for real-time monitoring

![[CloudWatch Alarms.png]]
#### CloudWatch Alarm
- Can be used to monitor any Amazon CloudWatch metric in your account
- Can be used to set *billing alarms*
- **Select a Metric**
	- e.g. avg. bytes stored in a bucket in 1 day
	- e.g. avg. cpu utilization on an [[EC2]] instance in 5 minutes
- **Define Alert Conditions**
	- e.g. > 5 kb
	- e.g. > 80%
- **Define Alarm Action**
	- e.g. Send notification via [[SNS]]
	- e.g. Trigger [[EC2 Auto Scaling]]
-