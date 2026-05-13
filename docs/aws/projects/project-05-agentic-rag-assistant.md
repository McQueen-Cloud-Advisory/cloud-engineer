# Project 05: Agentic RAG Assistant on AWS

## Purpose

Build an agentic retrieval-augmented assistant so you practice AI runtime integration, retrieval, guardrails, and operational governance in one workload.

## Architecture

```text
User request
-> AWS App Runner or Amazon API Gateway
-> Amazon Bedrock or Agents for Amazon Bedrock
-> Knowledge Bases for Amazon Bedrock
-> Guardrails for Amazon Bedrock
-> Amazon CloudWatch and AWS Secrets Manager
```

## Services Used

- [AWS App Runner](../services/app-runner.md)
- [Amazon API Gateway](../services/api-gateway.md)
- [Amazon Bedrock](../services/bedrock.md)
- [Agents for Amazon Bedrock](../services/bedrock-agents.md)
- [Knowledge Bases for Amazon Bedrock](../services/knowledge-bases-for-bedrock.md)
- [Guardrails for Amazon Bedrock](../services/guardrails-for-bedrock.md)
- [AWS Secrets Manager](../services/secrets-manager.md)
- [Amazon CloudWatch](../services/cloudwatch.md)

## What You Will Build

- A user-facing application endpoint.
- A grounded AI workflow with retrieval over approved content.
- Guardrails, secret handling, and operational visibility for the AI path.

## Skills Practiced

- AI application integration
- Managed retrieval design
- Agent workflow planning
- AI safety and observability

## Implementation Notes

Keep the first version narrow. Use a small knowledge corpus, define the tool or agent boundaries clearly, and make logging, prompt review, and access boundaries part of the implementation from the start.

## Security Considerations

Review who can access the application, what content is indexed, how secrets are stored, and how the system should respond to unsafe or adversarial input.

## Cost Considerations

Model usage, retrieval, guardrails, and supporting runtime resources can add up quickly. Limit the scope of testing and monitor usage patterns closely.

## How to Extend This Project

- Add user authentication and tenant separation.
- Add feedback capture and evaluation workflows.
- Add deployment automation and model usage dashboards.

## Portfolio Value

This project shows that you can treat AI workloads as engineering systems with deployment, security, observability, and governance requirements rather than as a simple prompt demo.

## Official References

- [AWS App Runner documentation](https://docs.aws.amazon.com/apprunner/)
- [Amazon Bedrock documentation](https://docs.aws.amazon.com/bedrock/)
- [Agents for Amazon Bedrock documentation](https://docs.aws.amazon.com/bedrock/latest/userguide/agents.html)
- [Knowledge Bases for Amazon Bedrock documentation](https://docs.aws.amazon.com/bedrock/latest/userguide/knowledge-base.html)
- [Guardrails for Amazon Bedrock documentation](https://docs.aws.amazon.com/bedrock/latest/userguide/guardrails.html)
