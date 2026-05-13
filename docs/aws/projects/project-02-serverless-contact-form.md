# Project 02: Serverless Contact Form on AWS

## Purpose

Build a serverless API-backed contact form so you practice API design, compute integration, data persistence, secrets handling, and monitoring together.

## Architecture

```text
User request
-> Amazon API Gateway
-> AWS Lambda
-> Amazon DynamoDB
-> AWS Secrets Manager and Amazon CloudWatch
```

## Services Used

- [Amazon API Gateway](../services/api-gateway.md)
- [AWS Lambda](../services/lambda.md)
- [Amazon DynamoDB](../services/dynamodb.md)
- [AWS Secrets Manager](../services/secrets-manager.md)
- [Amazon CloudWatch](../services/cloudwatch.md)

## What You Will Build

- An API endpoint for form submission.
- A Lambda function that validates and stores submissions.
- A data store and monitoring path for operational review.

## Skills Practiced

- Serverless API design
- Function-based integration
- Application data modeling
- Secret handling and monitoring

## Implementation Notes

Keep the API small and focus on validation, least-privilege permissions, clear logging, and predictable error handling. The goal is to understand the moving parts of a production-style serverless API.

## Security Considerations

Validate request input, restrict API access as needed, keep any downstream credentials in Secrets Manager, and ensure each service role only has the permissions it needs.

## Cost Considerations

This project is usually low cost at small traffic levels, but repeated testing, high request volume, or verbose logging can increase spend.

## How to Extend This Project

- Add spam protection or approval workflow.
- Add notification delivery for new submissions.
- Add a small admin view for reviewing stored submissions.

## Portfolio Value

This project demonstrates that you can connect a public API, serverless compute, data storage, and operational controls into one coherent system.

## Official References

- [Amazon API Gateway documentation](https://docs.aws.amazon.com/apigateway/)
- [AWS Lambda documentation](https://docs.aws.amazon.com/lambda/)
- [Amazon DynamoDB documentation](https://docs.aws.amazon.com/dynamodb/)
- [AWS Secrets Manager documentation](https://docs.aws.amazon.com/secretsmanager/)
