# Project 05: Agentic RAG Assistant on Google Cloud

## Purpose

Build an agentic retrieval-augmented assistant so you practice AI runtime integration, retrieval, safety controls, and platform operations on Google Cloud.

## Architecture

```text
User request
-> Cloud Run
-> Vertex AI and Vertex AI Agent Builder
-> Model Garden and Model Armor
-> Secret Manager and Cloud Monitoring
```

## Services Used

- [Cloud Run](../services/cloud-run.md)
- [Vertex AI](../services/vertex-ai.md)
- [Vertex AI Agent Builder](../services/vertex-ai-agent-builder.md)
- [Agent Development Kit](../services/agent-development-kit.md)
- [Model Garden](../services/model-garden.md)
- [Model Armor](../services/model-armor.md)
- [Secret Manager](../services/secret-manager.md)
- [Cloud Monitoring](../services/cloud-monitoring.md)
- [IAM and Service Accounts](../services/iam-and-service-accounts.md)

## What You Will Build

- A user-facing assistant endpoint.
- A retrieval-backed AI workflow over approved content.
- Safety, secret, and monitoring controls around the AI path.

## Skills Practiced

- AI application integration
- Retrieval design
- Agent workflow planning
- AI safety and observability

## Implementation Notes

Keep the corpus and workflow narrow at first. Focus on service accounts, retrieval quality, logging, and how the application should behave when AI components fail or return poor results.

## Security Considerations

Review prompt injection, document governance, safety controls, and service account scope from the beginning of the build.

## Cost Considerations

Model usage, retrieval, safety controls, and runtime hosting can compound quickly, so limit scope and monitor usage patterns early.

## How to Extend This Project

- Add user authentication and role-based access.
- Add evaluation workflows and feedback capture.
- Add deployment automation and usage dashboards.

## Portfolio Value

This project shows that you can frame AI work as a cloud engineering system with deployment, identity, safety, and observability requirements rather than as a simple prompt demo.

## Official References

- [Vertex AI documentation](https://cloud.google.com/vertex-ai/docs)
- [Agent Builder documentation](https://docs.cloud.google.com/agent-builder)
- [Model Armor overview](https://cloud.google.com/security/products/model-armor)
- [Cloud Run documentation](https://cloud.google.com/run/docs)
