# Project 01: Static Site on AWS

## Purpose

Build and deploy a simple static site on AWS so you practice object storage hosting, deployment discipline, and basic operational controls.

## Architecture

```text
Source content
-> Deployment workflow
-> Amazon S3 static website hosting
-> Optional CDN or custom domain
-> CloudWatch and access review
```

## Services Used

- [Amazon S3](../services/s3.md)
- [AWS Identity and Access Management (IAM)](../services/iam.md)
- [Amazon CloudWatch](../services/cloudwatch.md)

## What You Will Build

- A static site deployed to an S3 bucket.
- A controlled deployment path for updates.
- Basic monitoring and logging around the site delivery path.

## Skills Practiced

- Object storage hosting
- Least-privilege deployment access
- Basic monitoring and lifecycle control

## Implementation Notes

Start with S3 static website hosting and keep the first version small. Focus on a clear deployment path, bucket access boundaries, and observable updates before adding a CDN or custom domain.

## Security Considerations

Allow only the minimum public access required for serving site assets, keep write access restricted to the deployment path, and review bucket policies carefully.

## Cost Considerations

This project should be low cost, but data transfer and optional CDN usage can add up if the site receives meaningful traffic.

## How to Extend This Project

- Add a custom domain and CDN.
- Add CI/CD deployment automation.
- Add access logs and versioned content rollback.

## Portfolio Value

This project shows you can deploy a basic web asset, control access paths, and explain the difference between storage, delivery, and monitoring concerns.

## Official References

- [Hosting a static website using Amazon S3](https://docs.aws.amazon.com/AmazonS3/latest/userguide/WebsiteHosting.html)
- [AWS IAM documentation](https://docs.aws.amazon.com/iam/)
- [Amazon CloudWatch documentation](https://docs.aws.amazon.com/cloudwatch/)
