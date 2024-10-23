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

##############################################################################

#####################################################################

# Business case and business goals

*Goal*: Create unified data platform.

*Business Goals/Drivers*:

| # | Description | Priority (Hard/Soft) |
|---|-------------|:---------------------:|
| | Data consolidation in a single cloud | Hard |
| | Improved data management | Hard |
| | Enhanced analytics capabilities | Hard |
| | Cost efficiencies | Soft |
| | Better data security | Soft |
| | Streamlined collaboration within an organization | Soft|

# Constraints (business, technical, legal, etc.)

| # | Description | Priority (Hard/Soft) |
|---|-------------|:---------------------:|
| | As target cloud only AWS or MS Azure shall be used | Hard |
| | Big data lake(s) with clear boundaries shall be defined | Soft  |
| | The data lake(s) should have the capability to ingest the data in batch mode and real time pipeline with appropriate frequency/rate - 120 000 IoT sensors; each IoT sensor sends the data each 20-60 seconds| Hard |

# Main use cases

| # | Use Case Name     | Description | Actor     |
| - | ------------------|-------------|:------------:|
| 1 |Patient Data Ingestion | Capture real-time health data (e.g., glucose levels, blood pressure) from wearable and home devices.| Patients, Medical Devices |
| 2 | Real-Time Data Monitoring | Healthcare providers monitor patient vitals in real-time, receiving alerts for critical changes.| Healthcare Providers |
| 3 | Predictive Analytics & Alerts | Use AI algorithms to predict potential health risks and trigger alerts to doctors for interventions.| Healthcare Providers |
| 4 | Data Access & Analytics Dashboard | Enable healthcare providers to access patient history, trends, and analytics through a dashboard.| Healthcare Providers |
| 5 | Patient Data Access | Patients can view their own health data, trends, and receive personalized insights via a mobile app.| Patients |
| 6 | Data Export to Third-Party Systems | Export patient data to external healthcare systems or insurance companies for further analysis. | Insurance Companies |
| 7 | Data Storage & Archiving | Store and archive patient health data, ensuring compliance with healthcare regulations like HIPAA.| Data Platform |
| 8 | Data Sharing Across Environments | Synchronize and share data across cloud environments without duplicating or losing information.| Data Platform, Cloud Providers |

# Quality attribute scenarios

| # | Quality Attribute   | Scenario |  Business Priority  | Related To |
| - | ------------------|-------------|-------------|:------------:|
| 1 | Security | Patient health data must be encrypted during transmission and storage, ensuring compliance with HIPAA. | High |  Data Storage, Access |
| 2 | Availability | The system must maintain 99.9% uptime to ensure healthcare providers can access patient data at all times. |  High |  Data Access, Monitoring |
| 3 | Performance |  Real-time patient monitoring must process data within 2 seconds of ingestion from IoT devices. |  High |  Real-Time Monitoring |
| 4 | Scalability |  The platform should scale to support up to 50 external partners in next 3 years |  High |  Data Consuming |
| 5 | Scalability |  The platform should scale to support up to 4 000 devices with 120 000 IoT sensors(each IoT sensor sends the data each 20-60 seconds) without degrading performance. |  High |  Data Ingestion |
| 6 | Availability |  To be able to perform cross-location analytics together with ability of ML team to leverage from the cross-location data. |  High |  Predictive Analytics |
| 7 | Maintainability |  The platform must allow updates to AI models without affecting the real-time data pipeline. |  Medium |  Predictive Analytics |
| 8 | Reliability |  Data synchronization between cloud environments must ensure no data loss even during network disruptions. |  High | Data Sharing |

# Other information

The data lake(s) should store the data in the right format which is ideal for the relevant use cases
This also includes consolidation of data per cloud and per environment. There is a need to explore solutions and architecture of the future state platform(s) in which the need to copy data from one platform to another, one environment to another, is effectively managed, minimized and potentially eliminated.

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

# Current technical state

Now size of AWS is ~20TB, Azure is ~5TB. Data includes among other - patient data, sensor data, click stream, and data like order data, supply chain data from the IT data platform.

We have Java, .Net, NodeJS and Python in our technology portfolio.

# Future technical state

Today we have < 10 external partners but going to grow 5x times in next 3 years.

We're looking forward to introduce SLAs.

At the end of the day we would like to make our AI/ML teams to work in isolated environments to not interfer with each other. Data access policies should be supported in such case (e.g. we should be able to configure what kind of information should be available and what is not).
The future plan is to reuse environments feature to expose the data for external partners.

<img src="./Images/TBD.jpg" alt="TBD" />

# References

| # | Name                 | Source                | Release date           |  Author                 | Description   |
| - | ---------------------|---------------------- |----------------------- | ----------------------- |:-------------:|
