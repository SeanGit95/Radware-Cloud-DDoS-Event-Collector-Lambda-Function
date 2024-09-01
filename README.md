# Radware-Cloud-DDoS-Event-Collector-Lambda-Function

This AWS Lambda function fetches Cloud DDoS (CDDoS) logs from Radware's API and uploads them to an S3 bucket. It handles pagination, error retries, and saves the last execution time to continue from where it left off in subsequent executions.

## Features

- **Fetch Logs:** Retrieve CDDoS logs within a specific time range.
- **Paginated Requests:** Handle paginated API responses.
- **Error Handling:** Includes retries and logging for better debugging.
- **Upload to S3:** Save fetched logs to an S3 bucket in JSON format.

## Setup

### Prerequisites

- AWS Account with S3 permissions
- Radware API Key and Account ID

### Environment Variables

Set the following environment variables in your Lambda function:

- `BUCKET_NAME`: Name of the S3 bucket.
- `RADWARE_API_KEY`: API key for Radware.
- `RADWARE_ACCOUNT_ID`: Account ID for Radware.

### Deployment

1. Upload the Lambda function to AWS.
2. Set the necessary environment variables in the Lambda console.
3. Schedule the Lambda function using CloudWatch Events to run at desired intervals.

### Logging

The function uses Python’s built-in `logging` module to log information, warnings, and errors.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
