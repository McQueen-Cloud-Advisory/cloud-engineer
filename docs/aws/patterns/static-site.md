# Static Site on AWS

## Purpose

This pattern explains how to host and deliver static content on AWS with a simple, low-operations architecture.

## Pattern Summary

A static site pattern separates content delivery from server-side application execution. On AWS, the first-pass version often starts with Amazon S3 for storage and optionally adds a CDN and custom domain later.

This pattern matters because it introduces deployment discipline, content versioning, access control, and low-cost web delivery without requiring an application server. It is a good way to practice the basics of cloud delivery and public access boundaries.

## Common Use Cases

- Documentation sites
- Marketing pages
- Portfolio sites

## Reference Architecture

```text
Client
-> Optional CDN or custom domain
-> Amazon S3 static website hosting
-> Logging and monitoring
```

## Provider Services

- Amazon S3
- AWS IAM
- Amazon CloudWatch
- Optional CloudFront or Route 53

## Design Considerations

### Security

Keep write access tightly controlled, review any public-read requirement carefully, and treat bucket policy design as part of the architecture.

### Reliability

Static site architectures are reliable when content deployment is simple and versioned, and when rollback is easy.

### Observability

Use access logging and baseline monitoring so delivery issues and unexpected traffic are visible.

### Cost

This pattern is usually inexpensive, but data transfer and CDN usage can increase with traffic.

### Deployment

Deploy content through a repeatable workflow instead of manual console uploads whenever possible.

## Related Projects

- [Project 01: Static Site](../projects/project-01-static-site.md)

## Official References

- [Hosting a static website using Amazon S3](https://docs.aws.amazon.com/AmazonS3/latest/userguide/WebsiteHosting.html)
- [Amazon S3 documentation](https://docs.aws.amazon.com/s3/)
