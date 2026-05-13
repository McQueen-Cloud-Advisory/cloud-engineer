# Project 01: Static Site on Azure

## Purpose

Build and deploy a simple static site on Azure so you practice object storage hosting, access control, and baseline monitoring.

## Architecture

```text
Source content
-> Deployment workflow
-> Azure Blob Storage static website hosting
-> Optional CDN or custom domain
-> Azure Monitor
```

## Services Used

- [Azure Blob Storage](../services/blob-storage.md)
- [Microsoft Entra ID](../services/entra-id.md)
- [Azure Role-Based Access Control](../services/role-based-access-control.md)
- [Azure Monitor](../services/monitor.md)

## What You Will Build

- A static site deployed to Blob Storage.
- A repeatable deployment path for updates.
- Basic monitoring and access review around the delivery path.

## Skills Practiced

- Static site hosting
- Azure access control basics
- Object storage delivery patterns

## Implementation Notes

Start with Blob Storage static website hosting and keep the first version simple. Focus on storage configuration, deployment repeatability, and clear access boundaries before adding extra delivery features.

## Security Considerations

Keep write access narrow, review any public site exposure carefully, and use RBAC so deployment rights are not broader than necessary.

## Cost Considerations

The base project should stay low cost, but data transfer and optional CDN or custom domain services can increase spend.

## How to Extend This Project

- Add a custom domain and CDN.
- Add deployment automation.
- Add access logs and change rollback steps.

## Portfolio Value

This project demonstrates that you can deliver public content on a cloud platform while still thinking about access control and operational hygiene.

## Official References

- [Azure Blob Storage documentation](https://learn.microsoft.com/en-us/azure/storage/blobs/)
- [Static website hosting in Azure Storage](https://learn.microsoft.com/en-us/azure/storage/blobs/storage-blob-static-website)
- [Azure Monitor documentation](https://learn.microsoft.com/en-us/azure/azure-monitor/)
