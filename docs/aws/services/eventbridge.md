# Amazon EventBridge

## Purpose

Amazon EventBridge routes events between services and can also trigger workloads on a schedule.

## What Problem It Solves

It helps decouple producers from consumers and gives teams a managed way to build scheduled and event-driven workflows.

## When to Use It

- Use it for scheduled tasks, event routing, and service integration flows.
- Use it when multiple systems should react to the same event without direct coupling.
- Use it to trigger ingestion or maintenance workloads at controlled intervals.

## When Not to Use It

- Do not use it as a substitute for durable workflow design when the process requires stronger orchestration guarantees.
- Do not publish high-volume noisy events without a clear consumer and retention strategy.

## Cloud Engineering Considerations

### Identity and Access

Review which services can publish events, which rules can invoke targets, and what permissions those targets need.

### Networking

Understand how EventBridge triggers downstream services and whether those targets also depend on private connectivity.

### Security

Validate event sources and avoid rules that allow overly broad or unintended triggers.

### Observability

Monitor failed invocations, rule matches, and downstream workload behavior together.

### Cost

Event volume and downstream target usage determine cost, so filter aggressively and avoid unnecessary fan-out.

## Related Projects

- [Project 03: Scheduled API Ingestion](../projects/project-03-scheduled-api-ingestion.md)
- [Project 04: Analytics Platform](../projects/project-04-analytics-platform.md)

## Related Patterns

- [Scheduled Job](../patterns/scheduled-job.md)
- [Analytics Platform](../patterns/analytics-platform.md)

## Official References

- [Amazon EventBridge documentation](https://docs.aws.amazon.com/eventbridge/)
- [EventBridge user guide](https://docs.aws.amazon.com/eventbridge/latest/userguide/eb-what-is.html)
