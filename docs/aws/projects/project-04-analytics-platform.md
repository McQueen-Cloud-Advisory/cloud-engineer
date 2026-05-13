# Project 04: Analytics Platform on AWS

## Purpose

Build a small analytics platform so you practice batch ingestion, layered data storage, query access, and operational oversight.

## Architecture

```text
Scheduled or event-driven ingestion
-> Amazon S3 landing zone
-> Transformation and cataloging
-> Query layer and reporting
-> Amazon CloudWatch
```

## Services Used

- [Amazon S3](../services/s3.md)
- [Amazon EventBridge](../services/eventbridge.md)
- [AWS Lambda](../services/lambda.md)
- [Amazon CloudWatch](../services/cloudwatch.md)
- AWS Glue
- Amazon Athena

## What You Will Build

- A raw and curated data layout in object storage.
- A simple transformation or cataloging flow.
- A queryable analytics layer for reporting or inspection.

## Skills Practiced

- Analytics data flow design
- Data lake organization
- Scheduled transformation
- Monitoring data platform operations

## Implementation Notes

Start with a small dataset and a simple raw-to-curated layout in S3. Add cataloging and querying only after the ingestion path and data shape are understandable.

## Security Considerations

Review who can access raw versus curated data, how credentials are handled, and whether any sensitive data needs masking or partitioned access.

## Cost Considerations

Storage growth, repeated queries, and transformation frequency can all increase cost. Keep the dataset and query scope intentionally small at first.

## How to Extend This Project

- Add partitioning and lifecycle rules.
- Add a dashboarding layer.
- Add data quality and freshness checks.

## Portfolio Value

This project demonstrates that you can think beyond application hosting and explain the data handling, transformation, and operational concerns of an analytics workload.

## Official References

- [Amazon S3 documentation](https://docs.aws.amazon.com/s3/)
- [AWS Glue documentation](https://docs.aws.amazon.com/glue/)
- [Amazon Athena documentation](https://docs.aws.amazon.com/athena/)
- [Amazon CloudWatch documentation](https://docs.aws.amazon.com/cloudwatch/)
