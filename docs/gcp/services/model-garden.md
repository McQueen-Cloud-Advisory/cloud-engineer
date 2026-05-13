# Model Garden

## Purpose

Model Garden is Google Cloud's catalog of models and related options available through Vertex AI.

## What Problem It Solves

It helps teams compare and choose model options without building a completely separate discovery path for each provider or runtime.

## When to Use It

- Use it when selecting models for a Google Cloud AI workload.
- Use it when evaluation needs to compare multiple model options for the same application.
- Use it when the team needs a clearer inventory of available models and capabilities.

## When Not to Use It

- Do not choose models only on brand or benchmark assumptions without workload-specific evaluation.
- Do not expand model choice faster than the team can test and govern it.

## Cloud Engineering Considerations

### Identity and Access

Review which teams or runtimes are allowed to use different models and how model access is governed.

### Networking

Plan how application runtimes reach the chosen models and how that affects latency and integration design.

### Security

Model choice influences data handling and safety controls, so governance should start before deployment.

### Observability

Track which models are used, how they perform, and whether outcomes meet the application need.

### Cost

Different models can have very different cost profiles, so evaluation should include spend as well as quality.

## Related Projects

- [Project 05: Agentic RAG Assistant](../projects/project-05-agentic-rag-assistant.md)

## Related Patterns

- [Agentic RAG Assistant](../patterns/agentic-rag-assistant.md)

## Official References

- [Model Garden overview](https://cloud.google.com/vertex-ai/generative-ai/docs/model-garden/overview)
- [Vertex AI documentation](https://cloud.google.com/vertex-ai/docs)
