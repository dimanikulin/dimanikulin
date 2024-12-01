# Headline

TBD

# Alternative headline

TBD

# Table of contents

TBD

- [Tags](./!Template.md#tags)
- [Definitions, Acronyms, Abbreviations](./!Template.md#definitions-acronyms-abbreviations)
- [Overview](./!Template.md#overview)
- [Introduction](./!Template.md#introduction)
- [References](./!Template.md#references)

# Tags

TBD

# Definitions, Acronyms, Abbreviations

| # | Abbreviation or Acronym | Definition     |
| - | ------------------------|:--------------:|
| 1 |

# Overview

TBD

# Current Environment Details

Cloud providers for the two source platforms - AWS and MS Azure.
Data types and formats - Raw data files, Structured data and Unstructured (e.g., relational databases, unstructured files)
Approximate data volume to migrate - Now size of AWS is ~20TB, Azure is ~5TB

Existing tools and resources in place for data handling:

## AWS

- KAFKA - Data ingestions and flow control
- Aurora - Device raw data
- S3 - Raw data files
- Cassandra - Device Sessions and Info
- Aurora RDS - User data, products, orders
- AWS Transfer for SFTP

## Azure

- SQL Servers and DB - Structured data for BI
- Azure Data factories - Unstructured data for BI
- Storage/batch - Flow control for batch processing
- Events Hubs/Streams - Flow control for stream processing

# Target Environment Details

Target cloud platform - AWS, or please motivate to use Azure
Technology preferences or restrictions - Kubernetes, but serverless is OK as well.
Security and compliance requirements - Patient health data must be encrypted during transmission and storage, ensuring compliance with HIPAA.

# Migration Requirements

Expected downtime tolerance - zero downtime.
Real-time vs. batch data transfer requirements - The platform should scale to support up to 4 000 devices with 120 000 IoT sensors(each IoT sensor sends the data each 20-60 seconds) without degrading performance. Real-time only for ingesting.

Timeline - one weak. Please suggest phases for migration.

<img src="./Images/TBD.jpg" alt="TBD" />

# References

| # | Name                 | Source                | Release date           |  Author                 | Description   |
| - | ---------------------|---------------------- |----------------------- | ----------------------- |:-------------:|
