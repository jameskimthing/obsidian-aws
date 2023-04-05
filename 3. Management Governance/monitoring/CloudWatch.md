# CloudWatch
![[Pasted image 20230405131154.png]]
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

#### CloudWatch Logs
<svg class="w-6 h-6" height="48" width="48" xmlns="http://www.w3.org/2000/svg"><path d="M29.5 17c-3.258 0-6.03 2.092-7.062 5h2.169a5.503 5.503 0 014.893-3c3.032 0 5.5 2.467 5.5 5.5 0 3.032-2.468 5.5-5.5 5.5a5.49 5.49 0 01-4.24-2h-2.388a7.505 7.505 0 006.628 4c4.136 0 7.5-3.364 7.5-7.5S33.636 17 29.5 17zM2 33h13v-2H2v2zm0-15h13v-2H2v2zm0 8h27v-2H2v2zm41.843 9.738l-5.025-4.525a11.486 11.486 0 01-1.403 1.608l4.997 4.508a1.073 1.073 0 001.51-.08 1.075 1.075 0 00-.08-1.51zm1.566 2.85a3.068 3.068 0 01-2.284 1.012 3.06 3.06 0 01-2.051-.785l-5.24-4.726A11.432 11.432 0 0129.5 36c-5.12 0-9.467-3.366-10.951-8h2.128c1.397 3.51 4.822 6 8.823 6 5.238 0 9.5-4.262 9.5-9.5S34.738 15 29.5 15c-4.372 0-8.054 2.973-9.155 7h-2.063c1.146-5.143 5.737-9 11.218-9C35.84 13 41 18.158 41 24.5c0 1.777-.417 3.455-1.141 4.96l5.324 4.794a3.078 3.078 0 01.226 4.334zM1.999 41h19v-2H2v2zm0-31h21V8H2v2z" fill="#B0084D" fill-rule="evenodd"></path></svg>
- Lets you monitor and troubleshoot your systems and applications using your existing system, application, and custom log files
- Can be used for real time application and system monitoring as well as long term log retention
- [[CloudTrail]] logs can be sent to *CloudWatch Logs* for real-time monitoring

#### CloudWatch Alarm
<svg class="w-6 h-6" height="48" width="48" xmlns="http://www.w3.org/2000/svg"><path d="M41.425 40.667h-6.788V19.83c2.185.697 4.602.697 6.788 0v20.837zm.57-23.208a9.267 9.267 0 01-7.928 0 1 1 0 00-1.43.902v23.306a1 1 0 001 1h8.788a1 1 0 001-1V18.361a1 1 0 00-1.43-.902zM38.03 4a5.157 5.157 0 015.152 5.152 5.158 5.158 0 01-5.152 5.152 5.157 5.157 0 01-5.151-5.152A5.157 5.157 0 0138.03 4zm0 12.303a7.16 7.16 0 007.152-7.152c0-3.942-3.208-7.15-7.152-7.15-3.943 0-7.151 3.208-7.151 7.15 0 3.944 3.208 7.152 7.15 7.152zM2 46.183h43.94v-2H2v2zm18.575-5.516h6.788V27.728h-6.788v12.94zm-1 2h8.788a1 1 0 001-1V26.728a1 1 0 00-1-1h-8.788a1 1 0 00-1 1v14.94a1 1 0 001 1zm-13.06-2h6.788V23.334H6.516v17.333zm-1 2h8.788a1 1 0 001-1V22.334a1 1 0 00-1-1H5.516a1 1 0 00-1 1v19.333a1 1 0 001 1z" fill="#B0084D" fill-rule="evenodd"></path></svg>
- Can be used to monitor any Amazon CloudWatch metric in your account
- **Select a Metric**
	- e.g. avg. bytes stored in a bucket in 1 day
	- e.g. avg. cpu utilization on an [[EC2]] instance in 5 minutes
- **Define Alert Conditions**
	- e.g. > 5 kb
	- e.g. > 80%
- **Define Alarm Action**
	- e.g. Send notification via [[SNS]]
	- e.g. Trigger [[EC2 Auto Scaling]]
