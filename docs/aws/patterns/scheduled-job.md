# Scheduled Job on AWS

## Purpose

This pattern explains how to run recurring workloads on AWS without maintaining a dedicated scheduler host.

## Pattern Summary

A scheduled job pattern on AWS commonly uses Amazon EventBridge to trigger a Lambda function or another managed target on a schedule. The workload usually pulls data, performs routine maintenance, or generates periodic outputs.

This pattern matters because recurring workloads often look simple until teams need retries, secrets, observability, and idempotency. A managed scheduling pattern helps keep those concerns explicit from the beginning.

## Common Use Cases

- API ingestion
- Routine maintenance tasks
- Scheduled report generation

## Reference Architecture

```text
Schedule
-> Amazon EventBridge
-> AWS Lambda
-> Storage or downstream API
-> Logging and monitoring
```

## Provider Services

- Amazon EventBridge
- AWS Lambda
- Amazon S3
- AWS Secrets Manager
- Amazon CloudWatch

## Design Considerations

### Security

Protect any external credentials, scope the runtime role carefully, and review downstream write permissions.

### Reliability

Design the job so it can be retried safely and so partial failures are visible.

### Observability

Track scheduled invocations, failures, and downstream processing results rather than only trigger success.

### Cost

The scheduling layer is inexpensive, but repeated processing, storage, and logging can grow steadily over time.

### Deployment

Ship schedule definitions, runtime code, and monitoring together so the job is easy to reproduce.

## Related Projects

- [Project 03: Scheduled API Ingestion](../projects/project-03-scheduled-api-ingestion.md)

## Official References

- [Amazon EventBridge documentation](https://docs.aws.amazon.com/eventbridge/)
- [AWS Lambda documentation](https://docs.aws.amazon.com/lambda/)
