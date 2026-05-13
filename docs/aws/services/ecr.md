# Amazon Elastic Container Registry (ECR)

## Purpose

Amazon ECR stores and distributes container images for AWS workloads.

## What Problem It Solves

It provides a managed image registry so application deployments can use versioned, controlled container artifacts.

## When to Use It

- Use it to store images for containerized applications on AWS.
- Use it when deployment pipelines need a managed registry integrated with AWS permissions.
- Use it to control image lifecycle and image distribution inside AWS-centric delivery flows.

## When Not to Use It

- Do not keep unused or unscanned images indefinitely.
- Do not treat image publishing as complete supply-chain security by itself.

## Cloud Engineering Considerations

### Identity and Access

Limit who can push and pull images and which runtimes are allowed to use production repositories.

### Networking

Review how build systems and runtimes reach the registry, especially in restricted network environments.

### Security

Enable scanning and image lifecycle controls, and review how base images are chosen and maintained.

### Observability

Track image publishing activity and deployment usage so image provenance stays visible.

### Cost

Stored images and data transfer determine cost, so lifecycle cleanup matters.

## Related Projects

This section will be expanded as related projects are added.

## Related Patterns

This section will be expanded as related projects are added.

## Official References

- [Amazon ECR documentation](https://docs.aws.amazon.com/ecr/)
- [Amazon ECR user guide](https://docs.aws.amazon.com/AmazonECR/latest/userguide/what-is-ecr.html)
