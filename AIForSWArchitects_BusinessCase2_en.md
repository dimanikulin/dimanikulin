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

 ---

# 1. Company

*Company Name*: HealthTech Solutions Inc.

*Industry*: Healthcare Technology

*Mission Statement*: Our mission is to revolutionize patient care by providing cutting-edge digital health solutions that enable personalized, data-driven healthcare. Through our advanced Internet of Things (IoT) platforms, we connect patients, doctors, and healthcare providers to optimize treatment outcomes and improve patient well-being.

*Overview:* HealthTech Solutions is a leader in developing IoT-enabled healthcare solutions aimed at providing real-time monitoring, predictive analytics, and early intervention for chronic disease management. With a strong portfolio of AI-driven health products, we aim to transform traditional healthcare systems into data-driven, proactive models.

# 2. Project

*Project Name*: MedConnect IoT Platform

*Project Objective*: The MedConnect IoT platform aims to collect, monitor, and analyze data from patients with chronic diseases such as diabetes, hypertension, and cardiovascular diseases. By leveraging smart medical devices and wearable technology, the platform will enable continuous patient monitoring, reduce hospital admissions, and support remote diagnosis and treatment plans.

*Problem Statement*:
Currently there are two platforms under data platform umbrella - one on Azure (Patient and Usage Data) and another on AWS (Sleep Data). AWS receive the data from IoT sensors, performs aggregation of that data and exposes it for the client apps. Patient and Usage Data is hosted on Azure cloud, it is derived from Patient Data and its main focus is product & company-wide analytics, ML models learning and future product development cases. Having two Clouds is too costly for us. It also reduce data managibility, security and collaboration.

*Solution*:
We would like to leverage numerous advantages from data consolidation in a single cloud, including improved data management, enhanced analytics capabilities, cost efficiencies, better data security, and streamlined collaboration within an organization.

# 3. Decision Makers

*Key Stakeholders*:

- *CEO & Founder*: Oversees strategic decisions and high-level vision for MedConnect.
- *Chief Medical Officer (CMO)*: Ensures the platform aligns with clinical requirements and enhances patient outcomes.
- *Chief Technology Officer (CTO)*: Responsible for technological infrastructure, security, and data analytics.
- *Chief Financial Officer (CFO)*: Manages the financial viability of the project and budget allocation.
- *Product Manager:* Oversees the platform's development, ensuring timely feature releases and customer alignment.
- *Healthcare Providers*: Input from doctors, specialists, and nurses to guide product features based on clinical needs.
- *Health Applications*: Input from devices.
- *Patients*: As end-users, they contribute through feedback and real-world testing.

# 4. Product History

*Initial Concept*: The concept of the MedConnect platform was born out of the growing need for real-time, continuous patient monitoring, especially for chronic disease management. Early prototypes were based on existing wearable devices but quickly evolved to include connected home-based medical devices like glucose monitors, blood pressure cuffs, and smart scales.

*Milestones:*

- *2019*: Initial research and development; prototype launched for internal testing.
- *2020*: Early-stage trials conducted with select hospitals and healthcare institutions.
- *2021*: Public beta released; partnerships established with device manufacturers.
- *2023*: Official product launch; integrated AI analytics platform goes live with healthcare provider integration.
- *2024*: Migration to unified Data Platform.

# 5. Schedule

Project Timeline:

- *Q1 2024*: Requirements gathering and stakeholder alignment.
- *Q2 2024*: Platform development kickoff with core feature integration.
- *Q3 2024*: Alpha testing with healthcare professionals and selected patients.
- *Q4 2024*: Beta release and validation, including feedback and iteration phase.
- *Q1 2025*: Full-scale product launch, including marketing and sales rollout.
- *Q2 2025*: Post-launch support, user training, and feature enhancement based on feedback.

# 6. Features

Core Features of MedConnect IoT Platform:

- *Real-Time Data Collection*: Integration with wearable and not wearable devices (smartwatches, glucose monitors, blood pressure monitors). Captures heart rate, glucose levels, blood pressure, and other vital signs.
- *Predictive Analytics & AI*: Uses machine learning to analyze data trends and predict potential health risks. Provides alerts for healthcare providers if intervention is required.
- *Remote Patient Monitoring (RPM)*: Enables healthcare providers to monitor patients remotely.
- *Data Dashboard for Providers:* A centralized dashboard for clinicians to monitor patient health. Provides historical data, trend analysis, and personalized health insights.
- *Patient Mobile App*: Allows patients to view their health data in real-time, receive medication reminders, and get proactive health tips.
- *Device Interoperability*: Supports integration with multiple medical devices, ensuring flexibility for patients and healthcare providers.

# 7. Actors

*Primary Actors*:

- *Patients*: Chronic disease patients who use the IoT platform for continuous monitoring. Primary beneficiaries of personalized health insights and real-time data tracking.
- *Healthcare Providers*: Doctors, nurses, and specialists who use the platform to monitor and treat patients remotely. They receive alerts on potential health risks and can adjust treatment plans accordingly.
- *Healthcare Institutions (Hospitals/Clinics)*: Institutions benefit by reducing hospital admissions, improving patient outcomes, and lowering healthcare costs.
- *Medical Device Manufacturers*: Providers of smart medical devices that integrate with the platform, enabling data capture from patients.
- *Insurance Companies*: Can leverage the platform’s data to optimize healthcare costs, adjust premiums, and offer wellness programs to policyholders.

# 8. Solution advisory objective

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

*Constraints*:

| # | Description | Priority (Hard/Soft) |
|---|-------------|:---------------------:|
| | As target cloud only AWS or MS Azure shall be used | Hard |
| | Big data lake(s) with clear boundaries shall be defined | Soft  |
| | The data lake(s) should have the capability to ingest the data in batch mode and real time pipeline with appropriate frequency/rate - 120 000 IoT sensors; each IoT sensor sends the data each 20-60 seconds| Hard |

*Main Use Cases*:

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

*Quality Attribute Scenarios*:

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

# 9. Current technical state

Now size of AWS is ~20TB, Azure is ~5TB. Data includes among other - patient data, sensor data, click stream, and data like order data, supply chain data from the IT data platform.

We have Java, .Net, NodeJS and Python in our technology portfolio.

# 10. Future technical state

Today we have < 10 external partners but going to grow 5x times in next 3 years.

We're looking forward to introduce SLAs.

At the end of the day we would like to make our AI/ML teams to work in isolated environments to not interfer with each other. Data access policies should be supported in such case (e.g. we should be able to configure what kind of information should be available and what is not).
The future plan is to reuse environments feature to expose the data for external partners.

<img src="./Images/TBD.jpg" alt="TBD" />

# References

| # | Name                 | Source                | Release date           |  Author                 | Description   |
| - | ---------------------|---------------------- |----------------------- | ----------------------- |:-------------:|
