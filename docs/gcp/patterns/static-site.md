# Static Site on Google Cloud

## Purpose

This pattern explains how to host and deliver static content on Google Cloud with a simple, low-operations architecture.

## Pattern Summary

A static site pattern on Google Cloud commonly starts with Cloud Storage website hosting and may later add a load balancer, CDN, or custom domain. The design separates content delivery from server-side application logic and is a useful first production pattern.

This pattern matters because it introduces public content delivery, deployment discipline, and access control without requiring an application server.

## Common Use Cases

- Documentation sites
- Portfolio sites
- Simple public pages

## Reference Architecture

```text
Client
-> Optional load balancer or CDN
-> Cloud Storage static website hosting
-> Monitoring
```

## Provider Services

- Cloud Storage
- IAM and Service Accounts
- Cloud Monitoring

## Design Considerations

### Security

Keep write access narrow, review public content exposure carefully, and treat bucket permissions as part of the architecture.

### Reliability

Static site delivery is reliable when deployment is simple and rollback is easy.

### Observability

Use monitoring and access insights so delivery problems and unusual traffic are visible.

### Cost

This pattern is usually inexpensive, but data transfer and optional edge services can increase cost.

### Deployment

Deploy content through a repeatable workflow rather than ad hoc manual uploads wherever possible.

## Related Projects

- [Project 01: Static Site](../projects/project-01-static-site.md)

## Official References

- [Static website hosting on Cloud Storage](https://cloud.google.com/storage/docs/hosting-static-website)
- [Cloud Storage documentation](https://cloud.google.com/storage/docs)
