# Project 01: Static Site on Google Cloud

## Purpose

Build and deploy a simple static site on Google Cloud so you practice object storage hosting, deployment discipline, and baseline monitoring.

## Architecture

```text
Source content
-> Deployment workflow
-> Cloud Storage static website hosting
-> Optional load balancer or CDN
-> Cloud Monitoring
```

## Services Used

- [Cloud Storage](../services/cloud-storage.md)
- [IAM and Service Accounts](../services/iam-and-service-accounts.md)
- [Cloud Monitoring](../services/cloud-monitoring.md)

## What You Will Build

- A static site deployed to a Cloud Storage bucket.
- A controlled deployment path for updates.
- Baseline monitoring and access review around the delivery path.

## Skills Practiced

- Static site delivery
- Google Cloud access control basics
- Object storage hosting

## Implementation Notes

Start with Cloud Storage website hosting and keep the first version narrow. Focus on access boundaries, deployment repeatability, and monitoring before adding more delivery layers.

## Security Considerations

Keep write access narrow, review public content exposure carefully, and use service accounts deliberately for deployment automation.

## Cost Considerations

This project should be low cost, but data transfer and optional edge services can increase spend as traffic grows.

## How to Extend This Project

- Add a custom domain and CDN.
- Add CI/CD deployment automation.
- Add access logs and rollback procedures.

## Portfolio Value

This project shows that you can deliver a simple web asset on Google Cloud while still thinking about access control, deployment, and operations.

## Official References

- [Cloud Storage documentation](https://cloud.google.com/storage/docs)
- [Static website hosting on Cloud Storage](https://cloud.google.com/storage/docs/hosting-static-website)
- [Cloud Monitoring documentation](https://cloud.google.com/monitoring/docs)
