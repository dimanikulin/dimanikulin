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

# Project Overview

There are two data platforms in AWS and Azure Clouds.
The customer wants to create unified data platform and to migrate data from 2 Clouds into single one based on unified data platform.

The data lake should store the data in the right format which is ideal for the relevant use cases.
This also includes consolidation of data per cloud and per environment.
There is a need to explore solutions and architecture of the future state platform in which the need to copy data from one platform to another, one environment to another, is effectively managed, minimized and potentially eliminated.

# Business Goals

- to improve data management,
- to enhance analytics capabilities,
- to reduce the costs,
- to improve data security,
- to have streamlined collaboration within an organization

# Scope of Migration

*In Scope*:

- Identify required Enterprise Data Producing systems
- Data Producer Onboarding
- Data Ingestion (push/pull, batch/streaming/API)
- Archiving and Format Optimization
- Transformation and Enrichment
- Polyglot Storage
- Access Interfaces (API, Export, Analytics Tools, etc.)
- Identify Enterprise Data Consumer systems
- Data Consumer Onboarding
- Administration and Operational Tools
- Data Warehouse Capability
- Enterprise Data Governance
- Enabling Data Science and other internal teams to effectively access/consume the data
- Enabling various BI reports to effectively access/consume the data

*Out-Of-Scope*:

- Core Artificial Intelligence /Machine Learning/Data Science Capabilities
- Core Reporting Capabilities
- Surrounding Transactional Systems/Feature System/Teams’ Capabilities and Roadmaps
- Market Study/Business Value Analysis
- Data Producing/Consuming systems not identified as key/required systems

## Types of data involved

- Raw data files
- Structured data
- Unstructured

## Volume of data to be migrated

Now size of AWS is ~20TB, Azure is ~5TB. Data includes among other - patient data, sensor data, click stream, and data like order data, supply chain data from the IT data platform.

## Specific services or applications

Nothing special.

### AWS

- KAFKA - Data ingestions and flow control
- Aurora - Device raw data
- S3 - Raw data files
- Cassandra - Device Sessions and Info
- Aurora RDS - User data, products, orders
- AWS Transfer for SFTP

### Azure

- SQL Servers and DB - Structured data for BI
- Azure Data factories - Unstructured data for BI
- Storage/batch - Flow control for batch processing
- Events Hubs/Streams - Flow control for stream processing

# Current Cloud Infrastructure

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

## Integration

- Matlab Production Server (ML)
- Azure data platform is intergrated to AWS data platform
- Power BI
- Devices and their sensors
- Customer Portal
- Health and sport applications
- Notification services
- Ratings application
- Hockey application
- Customer feedfack application

Today we have < 10 external partners but going to grow 5x times in next 3 years.

# Target Cloud Platform

As target cloud only AWS or MS Azure shall be used. When any selected the motivation shall be provided.

Big data lake(s) with clear boundaries shall be defined. The data lake(s) should have the capability to ingest the data in batch mode and real time pipeline with appropriate frequency/rate - 120 000 IoT sensors (each IoT sensor sends the data each 20-60 seconds)

At the end of the day we would like to make our AI/ML teams to work in isolated environments to not interfer with each other. Data access policies should be supported in such case (e.g. we should be able to configure what kind of information should be available and what is not).
The future plan is to reuse environments feature to expose the data for external partners.

# Business or Technical Constraints

There is no limit for budget but project shall be done in 4 months.

| # | Description | Priority (Hard/Soft) |
|---|-------------|:---------------------:|
| | As target cloud only AWS or MS Azure shall be used | Hard |
| | Big data lake(s) with clear boundaries shall be defined | Soft  |
| | The data lake(s) should have the capability to ingest the data in batch mode and real time pipeline with appropriate frequency/rate - 120 000 IoT sensors; each IoT sensor sends the data each 20-60 seconds| Hard |
| | Data migration shall comply both GDPR and HIPAA | Hard |
| | Data shall be retained for 3 years | Hard |  

# Quality Requirements

| # | Quality Attribute   | Scenario |  Business Priority  | Related To |
| - | ------------------|-------------|-------------|:------------:|
| 1 | Security | Patient health data must be encrypted during transmission and storage, ensuring compliance with HIPAA. | High |  Data Storage, Access |
| 2 | Availability | The system must maintain 99.9% uptime to ensure healthcare providers can access patient data at all times. |  High |  Data Access, Monitoring |
| 3 | Performance |  Real-time patient monitoring must process data within 2 seconds of ingestion from IoT devices. |  High |  Real-Time Monitoring |
| 4 | Scalability |  The platform should scale to support up to 50 external partners in next 3 years |  High |  Data Consuming |
| 5 | Scalability |  The platform should scale to support up to 4 000 devices with 120 000 IoT sensors(each IoT sensor sends the data each 20-60 seconds) without degrading performance. | High |  Data Ingestion |
| 6 | Availability |  To be able to perform cross-location analytics together with ability of ML team to leverage from the cross-location data. |  High |  Predictive Analytics |
| 7 | Maintainability |  The platform must allow updates to AI models without affecting the real-time data pipeline. |  Medium |  Predictive Analytics |
| 8 | Reliability |  Data synchronization between cloud environments must ensure no data loss even during network disruptions. |  High | Data Sharing |
| 9 | Availability | No downtime is expected during migration | High | Migration |
| 10 | Security | Patient health data must be encrypted during migration and storage, ensuring compliance with HIPAA. | High | Migration |

# Key Stakeholders

- *CEO & Founder*: Oversees strategic decisions and high-level vision for MedConnect.
- *Chief Medical Officer (CMO)*: Ensures the platform aligns with clinical requirements and enhances patient outcomes.
- *Chief Technology Officer (CTO)*: Responsible for technological infrastructure, security, and data analytics.
- *Chief Financial Officer (CFO)*: Manages the financial viability of the project and budget allocation.
- *Product Manager:* Oversees the platform's development, ensuring timely feature releases and customer alignment.
- *Healthcare Providers*: Input from doctors, specialists, and nurses to guide product features based on clinical needs. They receive alerts on potential health risks and can adjust treatment plans accordingly.
- *Health Applications*: Input from devices.
- *Patients*: As end-users, they contribute through feedback and real-world testing. Primary beneficiaries of personalized health insights and real-time data tracking.
- *Medical Device Manufacturers*: Providers of smart medical devices that integrate with the platform, enabling data capture from patients.

#####################################################################

# Current technical state

We have Java, .Net, NodeJS and Python in our technology portfolio.

# Future technical state

We're looking forward to introduce SLAs.

<img src="./Images/TBD.jpg" alt="TBD" />

# References

| # | Name                 | Source                | Release date           |  Author                 | Description   |
| - | ---------------------|---------------------- |----------------------- | ----------------------- |:-------------:|
