# Static Site on Azure

## Purpose

This pattern explains how to host and deliver static web content on Azure with a simple, low-operations architecture.

## Pattern Summary

A static site pattern on Azure commonly starts with Blob Storage static website hosting and may later add CDN and custom domain capabilities. The design separates content delivery from server-side compute and is a useful entry point into cloud delivery patterns.

This pattern matters because it introduces access control, public delivery boundaries, deployment workflows, and low-cost web hosting without requiring a full application runtime.

## Common Use Cases

- Documentation sites
- Portfolio sites
- Simple public information sites

## Reference Architecture

```text
Client
-> Optional CDN or custom domain
-> Azure Blob Storage static website hosting
-> Azure Monitor
```

## Provider Services

- Azure Blob Storage
- Microsoft Entra ID
- Azure RBAC
- Azure Monitor

## Design Considerations

### Security

Keep write access restricted, review public-read requirements carefully, and separate deployment permissions from broader resource administration.

### Reliability

Static site hosting is reliable when content deployment is simple and rollback paths are clear.

### Observability

Use baseline monitoring and storage diagnostics so delivery issues and traffic changes are visible.

### Cost

This pattern is usually inexpensive, but data transfer and optional edge services can increase cost.

### Deployment

Prefer a repeatable deployment path over manual file uploads so content changes are predictable.

## Related Projects

- [Project 01: Static Site](../projects/project-01-static-site.md)

## Official References

- [Static website hosting in Azure Storage](https://learn.microsoft.com/en-us/azure/storage/blobs/storage-blob-static-website)
- [Azure Blob Storage documentation](https://learn.microsoft.com/en-us/azure/storage/blobs/)
