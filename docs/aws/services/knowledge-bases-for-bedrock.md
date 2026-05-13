# Knowledge Bases for Amazon Bedrock

## Purpose

Knowledge Bases for Amazon Bedrock connects foundation models and agent workflows to enterprise content so retrieval can be handled as part of the managed Bedrock stack.

## What Problem It Solves

It reduces the amount of custom retrieval plumbing a team has to build when an AI application needs grounded answers from approved documents or data sources.

## When to Use It

- Use it when a Bedrock-based application needs retrieval-augmented generation over internal content.
- Use it when you want a managed retrieval layer instead of stitching together multiple custom search components.
- Use it when you need to connect knowledge retrieval to Bedrock agents or model prompts.

## When Not to Use It

- Do not use it when the workload does not need retrieval or document grounding.
- Do not use it as a substitute for reviewing source quality, access controls, and document lifecycle.

## Cloud Engineering Considerations

### Identity and Access

Grant Bedrock and any supporting services only the permissions they need to read approved data sources and execute retrieval flows.

### Networking

Plan how the knowledge base reaches source content, embedding infrastructure, and any application entry points that depend on retrieval results.

### Security

Treat indexed content as sensitive application data. Review source boundaries, document-level access assumptions, and prompt injection risks.

### Observability

Monitor retrieval quality, failed ingestion jobs, and downstream application behavior so poor context quality is visible during testing and operation.

### Cost

Costs can grow through ingestion, storage, embeddings, and repeated retrieval traffic, so keep source scope and refresh schedules intentional.

## Related Projects

- [Project 05: Agentic RAG Assistant](../projects/project-05-agentic-rag-assistant.md)

## Related Patterns

- [Agentic RAG Assistant](../patterns/agentic-rag-assistant.md)

## Official References

- [Knowledge Bases for Amazon Bedrock documentation](https://docs.aws.amazon.com/bedrock/latest/userguide/knowledge-base.html)
- [Amazon Bedrock documentation](https://docs.aws.amazon.com/bedrock/)
