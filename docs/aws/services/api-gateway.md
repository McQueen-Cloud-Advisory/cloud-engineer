# Amazon API Gateway

## Purpose

Amazon API Gateway provides a managed front door for HTTP, REST, and WebSocket APIs on AWS.

## What Problem It Solves

It gives teams a way to expose application endpoints, apply policies, and manage API behavior without building gateway infrastructure from scratch.

## When to Use It

- Use it to expose serverless APIs backed by Lambda or other AWS services.
- Use it when you need request validation, authorization, throttling, or staged deployment behavior.
- Use it when an application needs a managed API entry point that integrates with AWS identity and monitoring tools.

## When Not to Use It

- Do not use it if a simpler direct integration already meets the requirement.
- Do not treat the gateway as a replacement for application-level validation and security checks.

## Cloud Engineering Considerations

### Identity and Access

Decide whether the API should use IAM, tokens, custom authorizers, or another front-door identity model.

### Networking

Review private versus public exposure, custom domains, and how downstream services are reached.

### Security

Validate inputs, enforce authentication, and rate-limit high-risk endpoints.

### Observability

Track request volume, status codes, latency, and downstream failure patterns.

### Cost

Request volume and data transfer drive cost, so chatty clients and overly fine-grained APIs can become expensive.

## Related Projects

- [Project 02: Serverless Contact Form](../projects/project-02-serverless-contact-form.md)
- [Project 05: Agentic RAG Assistant](../projects/project-05-agentic-rag-assistant.md)

## Related Patterns

- [Serverless API](../patterns/serverless-api.md)
- [Agentic RAG Assistant](../patterns/agentic-rag-assistant.md)

## Official References

- [Amazon API Gateway documentation](https://docs.aws.amazon.com/apigateway/)
- [API Gateway developer guide](https://docs.aws.amazon.com/apigateway/latest/developerguide/welcome.html)
