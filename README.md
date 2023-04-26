# MonitorCloudTrailLogsAWS
The script monitors AWS CloudTrail logs for suspicious activity using regular expressions to detect patterns like IP addresses and S3 bucket names. It sends email alerts if found, assuming CloudTrail and CloudWatch Logs are configured, and requires customization to fit specific security needs.


AWS CloudTrail Log Monitoring Script

This Python script uses the AWS SDK for Python (Boto3) to monitor CloudTrail logs for suspicious activity. It searches for patterns such as IP addresses and S3 bucket names using regular expressions and sends an email alert if any suspicious events are found.
Requirements

    Python 3.x
    AWS SDK for Python (Boto3)
    AWS credentials with access to the CloudTrail and CloudWatch Logs APIs

Usage

    Configure your AWS credentials using one of the methods described in the Boto3 documentation.
    Modify the script to suit your specific needs, including the CloudTrail trail name and the email alert function.
    Run the script using python3 cloudtrail_monitor.py.

Customization

    You can modify the regular expressions in the search_event() function to match other patterns.
    You can replace the email alert function with a function that sends alerts through your preferred method (e.g. AWS SNS or SES, a third-party email service, etc.).
    You can modify the start time for the log query in the get_latest_events() function to suit your needs.

Disclaimer

This script is provided as an example only and may not be suitable for use in all environments. You should thoroughly review and customize the script to meet the specific needs and security requirements of your organization before using it in a production environment.
