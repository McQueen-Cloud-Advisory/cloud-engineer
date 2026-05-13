# Amazon Bedrock

## Purpose

Amazon Bedrock provides managed access to foundation models and generative AI building blocks on AWS.

## What Problem It Solves

It gives teams a managed way to integrate models without standing up their own model-serving infrastructure.

## When to Use It

- Use it when an application needs managed foundation model access on AWS.
- Use it when you want to integrate prompts, model calls, and AI application features into existing AWS systems.
- Use it as the base model layer for retrieval, guardrails, or agent workflows.

## When Not to Use It

- Do not treat model access as the whole architecture when the workload also needs retrieval, tools, and governance.
- Do not move sensitive prompts or data into production without access review and output validation.

## Cloud Engineering Considerations

### Identity and Access

Control which roles can call models and separate application runtime permissions from operator access.

### Networking

Review how Bedrock is reached from application runtimes and how those runtimes reach protected data or downstream tools.

### Security

Plan for data classification, prompt safety, output review, and guardrails around model behavior.

### Observability

Track model usage, latency, failures, and downstream application quality together.

### Cost

Model invocation patterns, tokens, and repeated experimentation can quickly affect cost.

## Related Projects

- [Project 05: Agentic RAG Assistant](../projects/project-05-agentic-rag-assistant.md)

## Related Patterns

- [Agentic RAG Assistant](../patterns/agentic-rag-assistant.md)

## Official References

- [Amazon Bedrock documentation](https://docs.aws.amazon.com/bedrock/)
- [Amazon Bedrock user guide](https://docs.aws.amazon.com/bedrock/latest/userguide/what-is-bedrock.html)
