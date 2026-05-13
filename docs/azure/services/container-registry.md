# Azure Container Registry

## Purpose

Azure Container Registry stores and distributes container images for Azure workloads.

## What Problem It Solves

It gives teams a managed registry for versioned container artifacts and controlled image delivery.

## When to Use It

- Use it to store images for Container Apps and other Azure container runtimes.
- Use it when deployment workflows need a managed registry integrated with Azure access controls.
- Use it to support consistent image versioning and lifecycle policies.

## When Not to Use It

- Do not keep stale images indefinitely.
- Do not treat registry storage as a replacement for image review, patching, and supply-chain controls.

## Cloud Engineering Considerations

### Identity and Access

Control who can push and pull images and which runtimes have access to production repositories.

### Networking

Review how build agents and runtimes reach the registry, especially in private network designs.

### Security

Track image provenance, base image choices, and any registry exposure or replication decisions.

### Observability

Monitor image publishing and pull behavior so the deployment supply chain stays visible.

### Cost

Storage, geo-replication, and retained image volume drive cost.

## Related Projects

- [Project 05: Agentic RAG Assistant](../projects/project-05-agentic-rag-assistant.md)

## Related Patterns

- [Agentic RAG Assistant](../patterns/agentic-rag-assistant.md)

## Official References

- [Azure Container Registry documentation](https://learn.microsoft.com/en-us/azure/container-registry/)
- [Azure Container Registry overview](https://learn.microsoft.com/en-us/azure/container-registry/container-registry-intro)
