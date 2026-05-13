# Project 04: Analytics Platform on Azure

## Purpose

Build a small analytics platform so you practice data landing, orchestration, transformation, and reporting concepts on Azure.

## Architecture

```text
Data sources
-> Azure Data Factory
-> Azure Blob Storage raw and curated layers
-> Microsoft Fabric
-> Azure Monitor
```

## Services Used

- [Azure Data Factory](../services/data-factory.md)
- [Azure Blob Storage](../services/blob-storage.md)
- [Microsoft Fabric](../services/microsoft-fabric.md)
- [Azure Monitor](../services/monitor.md)

## What You Will Build

- A small raw and curated data layout.
- A pipeline that moves or reshapes data.
- A query or reporting surface over curated data.

## Skills Practiced

- Analytics pipeline design
- Object storage data layout
- Platform monitoring
- Data governance thinking

## Implementation Notes

Start with a narrow dataset and a small reporting goal. Focus on the shape of the flow from source to curated data rather than trying to reproduce a full enterprise analytics platform.

## Security Considerations

Review who can access raw versus curated data, how identities reach storage and analytics services, and how any sensitive data is protected.

## Cost Considerations

Storage, orchestration activity, and Fabric capacity or usage can become significant if the scope grows too quickly.

## How to Extend This Project

- Add data quality checks.
- Add partitioning and lifecycle controls.
- Add a small dashboard or scheduled report refresh.

## Portfolio Value

This project shows that you can think in terms of data movement, storage design, transformation, and reporting rather than only application hosting.

## Official References

- [Azure Data Factory documentation](https://learn.microsoft.com/en-us/azure/data-factory/)
- [Azure Blob Storage documentation](https://learn.microsoft.com/en-us/azure/storage/blobs/)
- [Microsoft Fabric documentation](https://learn.microsoft.com/en-us/fabric/)
