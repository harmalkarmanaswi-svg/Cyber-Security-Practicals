# AWS CloudWatch Monitoring & Alerts Practical

## Objective
To monitor an Amazon EC2 instance using Amazon CloudWatch and create an alarm that can send an email notification through Amazon Simple Notification Service (SNS) when CPU utilization exceeds a defined threshold.

## AWS Services Used
- **Amazon EC2** — instance being monitored
- **Amazon CloudWatch** — metric monitoring and alarm
- **Amazon SNS** — email notification delivery

## Configuration
- **AWS Region:** Asia Pacific (Mumbai) `ap-south-1`
- **Metric namespace:** `AWS/EC2`
- **Metric:** `CPUUtilization`
- **Statistic:** Average
- **Period:** 5 minutes
- **Alarm name:** `High-CPU-Utilization-Alarm`
- **Condition:** CPU utilization greater than `70%`
- **Evaluation:** 1 datapoint within 5 minutes
- **SNS topic:** `Manaswi-CloudWatch-Alerts`
- **Notification protocol:** Email

## Procedure
1. Open the AWS Management Console and navigate to **CloudWatch** in the Mumbai region.
2. Open **Metrics → EC2 → Per-Instance Metrics**.
3. Find and select the EC2 instance's `CPUUtilization` metric.
4. Choose **Create alarm** and configure the statistic, period, and threshold.
5. Set the condition to trigger when CPU utilization is greater than 70%.
6. Under **Configure actions**, create or select the SNS topic `Manaswi-CloudWatch-Alerts` and set the alarm action to notify when the alarm is in the **In alarm** state.
7. Name the alarm `High-CPU-Utilization-Alarm` and create it.
8. Open the SNS confirmation email and click **Confirm subscription**.
9. Return to CloudWatch and SNS to verify the alarm and email subscription.

## Result
- The CloudWatch alarm `High-CPU-Utilization-Alarm` was created successfully.
- The SNS confirmation page displayed **Subscription confirmed!** for `Manaswi-CloudWatch-Alerts`.
- At the time of the captured screenshots, the alarm state was **Insufficient data** because CloudWatch had not yet received enough metric datapoints for evaluation. This does not mean the alarm failed to be created. Allow time for metric data to arrive, then refresh the alarm page to check its state.

## Screenshots
The `screenshots/` folder contains evidence captured during the practical:
1. CloudWatch overview
2. EC2 metrics list
3. CPUUtilization metric selected
4. Alarm metric and threshold configuration
5. SNS notification action configuration
6. Alarm review screen
7. Successful alarm creation
8. SNS subscription confirmation page

## Notes
- The SNS subscription list screenshot was captured before the email confirmation. The later confirmation page in this package shows that the `Manaswi-CloudWatch-Alerts` subscription was confirmed.
- A confirmed SNS subscription proves that the email endpoint was subscribed; it does not by itself prove that a threshold-triggered alarm email was delivered.
- Do not publish account identifiers, personal email addresses, or other sensitive console details publicly. Review screenshots before uploading them to a public repository.

## GitHub Upload Checklist
- [ ] Review screenshots for personal/account information before publishing.
- [ ] Create a GitHub repository named `AWS-CloudWatch-Monitoring-Alerts`.
- [ ] Upload `README.md` and the `screenshots/` folder.
- [ ] Verify that all images render correctly in the repository.
- [ ] Keep the repository description focused on EC2 CPU monitoring, CloudWatch alarms, and SNS email notifications.
