# Project 02: Serverless Contact Form on Google Cloud

## Purpose

Build a serverless contact form so you practice managed container hosting, application data handling, secrets, and observability on Google Cloud.

## Architecture

```text
User request
-> Cloud Run
-> Firestore or another application data store
-> Secret Manager
-> Cloud Monitoring
```

## Services Used

- [Cloud Run](../services/cloud-run.md)
- [Secret Manager](../services/secret-manager.md)
- [Cloud Monitoring](../services/cloud-monitoring.md)
- [IAM and Service Accounts](../services/iam-and-service-accounts.md)
- Firestore

## What You Will Build

- A user-facing contact form endpoint.
- A backend service that validates and stores submissions.
- Basic monitoring, secret handling, and deployment controls.

## Skills Practiced

- Serverless application delivery
- Service account design
- Runtime secret handling
- Basic application data integration

## Implementation Notes

Use Cloud Run for the first-pass service and keep the application surface small. Focus on runtime identity, request validation, and a data flow you can explain clearly.

## Security Considerations

Use service accounts and Secret Manager, validate form input carefully, and keep data store permissions scoped to the application runtime.

## Cost Considerations

Cloud Run and supporting services should remain low cost at small scale, but repeated testing, verbose logging, and data store growth can increase spend.

## How to Extend This Project

- Add spam controls or moderation.
- Add a notification workflow.
- Add an admin review view for submissions.

## Portfolio Value

This project demonstrates that you can connect a public endpoint, a managed runtime, secrets, and operational telemetry into one application path.

## Official References

- [Cloud Run documentation](https://cloud.google.com/run/docs)
- [Secret Manager documentation](https://cloud.google.com/secret-manager/docs)
- [Firestore documentation](https://cloud.google.com/firestore/docs)
- [Cloud Monitoring documentation](https://cloud.google.com/monitoring/docs)
