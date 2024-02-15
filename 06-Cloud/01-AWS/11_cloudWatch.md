
## Visibility using CloudWatch
- AWS resources generate data for monitoring (metrics, logs, network traffic, events, etc.).
- CloudWatch is a centralized service for collecting and analyzing resource data.
- Enables monitoring system-wide performance changes, optimizing resource usage, and providing a unified view of operational health.

### CloudWatch Features
- Detect anomalous behavior.
- Set alarms for alerting.
- Visualize logs and metrics.
- Take automated actions like scaling.
- Troubleshoot issues.
- Discover insights for application health.

### How CloudWatch Works
- Managed service; no need to manage underlying infrastructure.
- Provides a centralized place for metrics analysis.
- AWS services automatically send metrics to CloudWatch (basic monitoring).
- Detailed monitoring (every minute) incurs a fee.
  
### CloudWatch Concepts
- Metrics: Time-ordered set of data points representing variable values over time.
- Dimensions: Name and value pairs attached to metrics for filtering.
- AWS services provide default metrics for resources (e.g., EC2 instances) at no charge.
- Custom metrics for application-specific monitoring.

### CloudWatch Dashboards
- Customizable home pages for data visualization.
- Configurable for one or more metrics through widgets (e.g., graphs).
- Aggregates statistics based on specified time periods.
- Allows external tools to ingest and analyze metrics.

### CloudWatch Logs
- Centralized storage and analysis for log files.
- Monitors, stores, and accesses log files from various sources (EC2 instances, Lambda functions, etc.).
- Enables querying and filtering of log data.
- Metric filters turn log data into numerical CloudWatch metrics.
- Security managed through AWS IAM policies.

### CloudWatch Alarms
- Initiates actions based on sustained state changes of metrics.
- Configured with metrics, thresholds, and time periods.
- Three possible states: OK, ALARM, INSUFFICIENT_DATA.
- Actions can be Amazon EC2, automatic scaling, or Amazon SNS notifications.
- Used for preventing and troubleshooting issues.

### Prevent and Troubleshoot Issues with CloudWatch Alarms
- CloudWatch Logs uses metric filters to turn log data into metrics.
- Steps:
  1. Set up a metric filter.
  2. Define an alarm based on the metric filter.
  3. Define an action for the alarm (e.g., email or text alert).
- Different alarms for different scenarios to prevent or troubleshoot operational issues.
- Alarms can invoke actions automatically (e.g., reboot EC2 instance, scale services, invoke Lambda functions).

