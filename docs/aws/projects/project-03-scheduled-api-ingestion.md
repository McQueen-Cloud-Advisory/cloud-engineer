# Project 03: Scheduled API Ingestion on AWS

## Purpose

Build a scheduled ingestion workflow so you practice event scheduling, external API handling, storage design, and operational visibility.

## Architecture

```text
Amazon EventBridge schedule
-> AWS Lambda
-> External API call
-> Amazon S3 or Amazon DynamoDB
-> Amazon CloudWatch
```

## Services Used

- [Amazon EventBridge](../services/eventbridge.md)
- [AWS Lambda](../services/lambda.md)
- [Amazon S3](../services/s3.md)
- [AWS Secrets Manager](../services/secrets-manager.md)
- [Amazon CloudWatch](../services/cloudwatch.md)

## What You Will Build

- A scheduled ingestion trigger.
- A function that pulls external data and stores results.
- Monitoring and failure visibility for the ingestion path.

## Skills Practiced

- Scheduled automation
- External API integration
- Data landing zone design
- Operational alerting

## Implementation Notes

Use EventBridge to trigger the workload on a predictable schedule. Focus on idempotency, secret handling, clear failure logging, and a storage shape that supports later analysis.

## Security Considerations

Store API credentials in Secrets Manager, restrict function permissions, and validate how external API responses are handled before writing data downstream.

## Cost Considerations

The core schedule is inexpensive, but external API usage, storage growth, and log retention can become meaningful over time.

## How to Extend This Project

- Add retry and dead-letter handling.
- Add data quality checks before storing records.
- Add a downstream transformation or summary report.

## Portfolio Value

This project shows event-driven automation, integration with external systems, and the operational thinking needed for recurring jobs.

## Official References

- [Amazon EventBridge documentation](https://docs.aws.amazon.com/eventbridge/)
- [AWS Lambda documentation](https://docs.aws.amazon.com/lambda/)
- [Amazon S3 documentation](https://docs.aws.amazon.com/s3/)
- [AWS Secrets Manager documentation](https://docs.aws.amazon.com/secretsmanager/)
