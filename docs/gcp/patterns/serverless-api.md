# Serverless API on Google Cloud

## Purpose

This pattern explains how to expose an API on Google Cloud using managed runtimes and supporting platform services.

## Pattern Summary

A serverless API pattern on Google Cloud often uses Cloud Run as the main request-handling runtime, with Secret Manager, service accounts, and monitoring services supporting the application path. Cloud Functions can also support event-driven pieces around the API.

This pattern matters because it shows how to build a production-minded API path without operating servers directly. Identity, secret handling, validation, and telemetry still matter even when the platform is managed.

## Common Use Cases

- Contact forms
- Internal APIs
- Lightweight application backends

## Reference Architecture

```text
Client
-> Cloud Run
-> Application logic and secrets
-> Application data store
-> Monitoring
```

## Provider Services

- Cloud Run
- Secret Manager
- IAM and Service Accounts
- Cloud Monitoring
- Optional Firestore or another application data store

## Design Considerations

### Security

Validate inputs, scope service accounts carefully, and keep secrets out of code and deployment artifacts.

### Reliability

Design for retries, downstream failure handling, and predictable deployment rollouts.

### Observability

Capture request latency, errors, and dependency behavior so issues can be traced end to end.

### Cost

Runtime requests, scale behavior, and telemetry volume are the main cost drivers.

### Deployment

Ship the runtime, configuration, permissions, and monitoring together so environments stay consistent.

## Related Projects

- [Project 02: Serverless Contact Form](../projects/project-02-serverless-contact-form.md)

## Official References

- [Cloud Run documentation](https://cloud.google.com/run/docs)
- [Secret Manager documentation](https://cloud.google.com/secret-manager/docs)
- [Cloud Monitoring documentation](https://cloud.google.com/monitoring/docs)
