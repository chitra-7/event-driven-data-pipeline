# event-driven-data-pipeline
1. **Data Sources**: APIs, user inputs, or other services generate events.
2. **Event Trigger**: AWS **S3 Event Notifications** or **EventBridge** trigger Lambda functions.
3. **Processing**:
   - `capture_event_data` Lambda function captures incoming events and stores raw data in **S3**.
   - `daily_report_generator` Lambda function generates daily summary reports and uploads them to **S3**.
4. **Monitoring**: **CloudWatch Logs** capture function execution details.
5. **CI/CD Pipeline**: GitHub Actions or Jenkins automates deployment of Lambda functions.
6. **Optional Notifications**: SNS/email notifications for monitoring or alerts.
