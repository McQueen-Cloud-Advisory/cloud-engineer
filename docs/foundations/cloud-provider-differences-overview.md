# Cloud Provider Differences Overview

## Purpose

This page explains how to compare cloud providers by underlying capability and operating model instead of getting stuck on service names.

## What Stays the Same Across Providers

Most cloud platforms expose similar building blocks. You will find identity systems, virtual networks, object storage, managed databases, containers, serverless runtimes, monitoring, and infrastructure tooling everywhere. The names, defaults, and feature boundaries change, but the architectural questions are often the same.

- How are environments separated?
- How is access granted to humans and workloads?
- How are public and private services connected?
- Which compute model best matches the workload?
- How are logs, metrics, costs, and policies surfaced?

If you learn the problem each service category solves, it becomes much easier to map one provider to another.

## What Changes in Practice

The important differences are usually operational, not cosmetic.

- The top-level governance boundary differs. Google Cloud centers around organizations, folders, and projects. AWS centers around organizations and accounts. Azure centers around tenants, management groups, subscriptions, and resource groups.
- Identity models differ in naming and integration patterns, especially for workload identity and enterprise directory integration.
- Networking defaults differ, including how virtual networks are created, segmented, peered, and connected to managed services.
- Managed services may expose different limits, scaling behavior, and deployment surfaces even when the product category looks similar.
- Pricing models vary, especially around data transfer, storage classes, reserved capacity, and bundled platform features.

Those differences affect how teams structure environments, automate deployments, handle permissions, and estimate cost. A design that is clean on one provider may need a different layout or governance model on another.

## How To Translate a Design Between Providers

Start with the architecture intent, not the service catalog. If a system needs private networking, object storage, scheduled jobs, and role-based access, define those requirements first. Then look for the provider-specific services and defaults that satisfy them. This avoids a common mistake where engineers try to recreate one provider's exact product lineup instead of rebuilding the design using the target provider's strengths.

## Common Mistakes

- Memorizing product names without understanding the capability they represent.
- Assuming a familiar service on one provider behaves the same way on another.
- Ignoring governance and account structure until after resources already exist.
- Overlooking regional availability, quotas, or data residency differences.
- Comparing providers only on headline feature lists instead of operational fit.

## How This Fits Into Cloud Engineering

Cloud engineers often have to evaluate provider choices, migrate workloads, or explain why a design looks different across platforms. Strong provider comparison skills let you translate architecture deliberately instead of copying patterns blindly.

## Official References

- [Google Cloud global infrastructure](https://cloud.google.com/about/locations)
- [AWS global infrastructure](https://aws.amazon.com/about-aws/global-infrastructure/)
- [Azure geographies](https://learn.microsoft.com/en-us/azure/reliability/regions-list)
