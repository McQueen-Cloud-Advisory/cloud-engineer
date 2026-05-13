# Project 05: Agentic RAG Assistant on Azure

## Purpose

Build an agentic retrieval-augmented assistant so you practice AI application delivery, retrieval, safety controls, and platform operations on Azure.

## Architecture

```text
User request
-> Azure Container Apps or API Management
-> Azure OpenAI and Foundry Agent Service
-> Azure AI Search
-> Azure AI Content Safety
-> Application Insights, Key Vault, and managed identities
```

## Services Used

- [Azure Container Apps](../services/container-apps.md)
- [Azure API Management](../services/api-management.md)
- [Azure OpenAI](../services/azure-openai.md)
- [Foundry Agent Service](../services/foundry-agent-service.md)
- [Azure AI Search](../services/azure-ai-search.md)
- [Azure AI Content Safety](../services/content-safety.md)
- [Azure Key Vault](../services/key-vault.md)
- [Managed Identities](../services/managed-identities.md)
- [Application Insights](../services/application-insights.md)
- [Microsoft Foundry](../services/microsoft-foundry.md)

## What You Will Build

- A user-facing application endpoint.
- A retrieval-backed assistant over approved content.
- Safety, identity, and telemetry controls around the AI path.

## Skills Practiced

- AI application integration
- Retrieval design
- Agent workflow planning
- AI safety and observability

## Implementation Notes

Keep the knowledge corpus and runtime surface small at first. Focus on access control, retrieval quality, telemetry, and how the app should behave when AI components fail or return poor results.

## Security Considerations

Review prompt injection, document governance, runtime identities, secret storage, and content safety checks as part of the initial implementation.

## Cost Considerations

Model usage, search, safety checks, and container runtime costs can increase quickly, so keep testing scope controlled and monitor usage patterns early.

## How to Extend This Project

- Add user authentication and role-based access.
- Add evaluation and feedback capture.
- Add CI/CD and usage dashboards.

## Portfolio Value

This project shows that you can frame AI work as a cloud engineering system with security, identity, observability, and deployment concerns rather than as a simple prompt demo.

## Official References

- [Azure OpenAI documentation](https://learn.microsoft.com/en-us/azure/ai-services/openai/)
- [Azure AI Search documentation](https://learn.microsoft.com/en-us/azure/search/)
- [Azure AI Content Safety documentation](https://learn.microsoft.com/en-us/azure/ai-services/content-safety/)
- [Azure Container Apps documentation](https://learn.microsoft.com/en-us/azure/container-apps/)
- [Azure AI Foundry documentation](https://learn.microsoft.com/en-us/azure/ai-foundry/)
