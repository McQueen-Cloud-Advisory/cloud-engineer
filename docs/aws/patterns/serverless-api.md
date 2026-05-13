# Serverless API on AWS

## Purpose

This pattern explains how to expose an API on AWS using managed services for the front door, compute, data, and operations layers.

## Pattern Summary

A serverless API pattern typically uses Amazon API Gateway as the entry point and AWS Lambda for request handling. Application data often sits in DynamoDB or another managed store, while secrets and telemetry are handled by supporting platform services.

This pattern matters because it shows how to connect public request handling, business logic, access control, and monitoring without running web servers. It is a common first production pattern for small APIs and event-driven applications.

## Common Use Cases

- Contact forms
- Internal tools
- Simple application backends

## Reference Architecture

```text
Client
-> Amazon API Gateway
-> AWS Lambda
-> Application data store
-> Logging and monitoring
```

## Provider Services

- Amazon API Gateway
- AWS Lambda
- Amazon DynamoDB
- AWS Secrets Manager
- Amazon CloudWatch

## Design Considerations

### Security

Validate inputs, control who can call the API, and keep downstream permissions scoped tightly to the function runtime.

### Reliability

Design for retries, idempotency, and downstream failure handling so the API behaves predictably under load or transient errors.

### Observability

Capture API status codes, function errors, latency, and data store behavior together.

### Cost

Request volume, function duration, and logging volume are the main cost drivers.

### Deployment

Deploy the gateway, function, permissions, and configuration together so environments stay consistent.

## Related Projects

- [Project 02: Serverless Contact Form](../projects/project-02-serverless-contact-form.md)

## Official References

- [Amazon API Gateway documentation](https://docs.aws.amazon.com/apigateway/)
- [AWS Lambda documentation](https://docs.aws.amazon.com/lambda/)
- [Amazon DynamoDB documentation](https://docs.aws.amazon.com/dynamodb/)
