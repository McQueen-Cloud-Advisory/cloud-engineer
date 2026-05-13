# AI and Agentic Workloads on AWS

## Purpose

This page frames modern AI and agentic systems on AWS as cloud engineering workloads that need security, deployment, observability, and governance decisions.

## What Problem It Solves

It helps teams connect model capabilities, retrieval, tools, guardrails, and runtime integration instead of treating AI as a separate experimental track.

## When to Use It

- Use it when planning how Bedrock-based applications fit into existing cloud systems.
- Use it when a workload needs model access, retrieval, tools, or multi-step agent behavior.
- Use it when you need a clear operating model for AI security, monitoring, and cost control.

## When Not to Use It

- Do not start with agent orchestration if a simple prompt workflow is enough.
- Do not treat model access as separate from IAM, secrets, data access, and logging design.

## Cloud Engineering Considerations

### Identity and Access

Review which roles can call models, retrieve source data, and operate any surrounding application runtime or pipeline.

### Networking

Plan how AI runtimes, data sources, and user-facing APIs communicate, especially when private connectivity or VPC controls are required.

### Security

Address prompt injection, sensitive data exposure, model output review, and guardrail requirements before production rollout.

### Observability

Track latency, model failures, retrieval quality, and application-level outcomes so the workload is measurable end to end.

### Cost

Costs can increase quickly through token usage, retrieval, orchestration, and repeated experimentation, so budgets and usage reviews matter.

## Related Projects

- [Project 05: Agentic RAG Assistant](../projects/project-05-agentic-rag-assistant.md)

## Related Patterns

- [Agentic RAG Assistant](../patterns/agentic-rag-assistant.md)

## Official References

- [AWS generative AI overview](https://aws.amazon.com/generative-ai/)
- [Amazon Bedrock documentation](https://docs.aws.amazon.com/bedrock/)
