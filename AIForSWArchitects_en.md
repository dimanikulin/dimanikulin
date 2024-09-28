# Headline

Artifical Intelengency For Software Architects

# Alternative headline

TBD

# Table of contents

- [Tags](./AIForSWArchitects_en.md#tags)
- [Definitions, Acronyms, Abbreviations](./AIForSWArchitects_en.md#definitions-acronyms-abbreviations)
- [Introduction](./AIForSWArchitects_en.md#introduction)
TBD
- [References](./AIForSWArchitects_en.md#references)

# Tags

TBD

# Definitions, Acronyms, Abbreviations

| # | Abbreviation or Acronym | Definition     |
| - | ------------------------|:--------------:|
| 1 |

# Introduction

At [DOU Day 2024](https://dou.ua/dou-day-2024/) I found quite interesting the [ChatGPT Solutions Architect Assistent](https://chatgpt.com/g/g-J6uBbvDrm-solutions-architect-assistent)

It gave me undersnading on how I can use AI to [create architecture vision](https://github.com/dovchar/architecture-vision-GPTs?tab=readme-ov-file) from scratch spending hours but not days.  

So I decided to try it on my project to start.

# Preparation

## Anonymization

Here we need to write sabout business case anonymization, so **AI** that you use for assitance will not find out the details for commercial project if any.

What you need to do at least is to remove any **PII** (*Personally Identifiable Information*) from input documentation.

So I created *Sample case anonymizated.docx* from *Sample case.docx*.

## Preparation for input docs

As input documentation for creation architecture vision the following artifacts might be considered:

- RFP (Request for Proposal)
- RFI (Request for Information)
- Text of customer request

Becacause I did not have any from those documents for my *Sample Case* I used *ChatGPT* (not Assistant meontioned previpsly) to help me to create [business case](./AIForSWArchitects_BusinessCase_en.md) from anonymizated input doc (*Sample case anonymizated.docx*).
Business case description kept such chapters as

- Company
- Project
- Decision Makers
- Product History
- Schedule
- Features
- Actors

TBD to use all the docs from initial case

# Assitance

The assitante is located [here](https://chatgpt.com/g/g-J6uBbvDrm-solutions-architect-assistent) and the communication with it is in a form like with **ChatGPT** - Prompt from **User** and Response from **AI**. So I put in a table form.

First I just wanted to try it out and just went from start to the end of assistance in way in suggested and without any clarification from my side. The result a put into [Round 1](./AIForSWArchitects_Round1.md)

## Business goals

First it suggested to define **Essential business goals**.

| # | My Prompt            | AI Response  |
| - | ---------------------|:------------:|
|   | Hi, Can you help me in solution architect advisory? | What type of help do you need? |
|   | To advise a customer on how to create unified data platform.| Great! For advising on a unified data platform, we need to create an architecture vision document. Could you provide additional information like: Request for Proposal (RFP), Request for Information (RFI), Text of the customer request. Let me know which one you have. |
|   | 1 | Please share the Request for Proposal (RFP) document or key details from it so I can assist you in defining the architecture vision for the unified data platform. |
|   | I sent [business case](./AIForSWArchitects_BusinessCase_en.md) | Thank you for sharing the details. Based on the RFP, we will proceed with defining the architecture vision for the MedConnect IoT Platform's Unified Data Platform. The first step is to define Architecture Drivers, which include business goals, constraints, and use cases. Let's begin with defining the main business goals. + Description Priority in form of a Table below. Would you like to proceed with defining constraints, or should we continue working on business goals?|

### Essential business goals for the solution

Description and its Priority

- Create a unified data platform to support real-time and batch data ingestion. - **Hard**
- Enable scalable data storage optimized for healthcare data (vital signs, historical records). - **Hard**
- Provide seamless data access for healthcare providers, patients, and analytics teams. - **Soft**
- Ensure compliance with healthcare standards (e.g., HIPAA) for data security and privacy. - **Hard**
- Support predictive analytics to enable proactive healthcare decision-making. - **Soft**
- Optimize data storage and minimize the need for cross-environment data copying. - **Soft**

## Risks

| # | My Prompt            | AI Response  |
| - | ---------------------|:------------:|
|   | What are key risks?  |The key risks associated with the MedConnect IoT Platform's Unified Data Platform project can stem from various technical, operational, and business challenges. Below are potential risks based on the RFP: See table below. Would you like to continue with defining constraints, or should we explore further details on these risks? |

### The section outlines key design risks for the solution

| # | Risk Description     | Mitigation Strategy  |
| - | ---------------------|:------------:|
|   | *Data Security & Privacy Compliance*: Ensuring the platform adheres to HIPAA and other healthcare data standards. | Implement end-to-end encryption, audit trails, and regular compliance checks. Engage security experts.|
|   | *Integration with Multiple Devices*: Difficulty in ensuring compatibility with diverse IoT devices and healthcare systems.| Establish strong partnerships with device manufacturers. Use open standards for device interoperability.|
|   | *Scalability for Real-Time Data Processing*: The system might struggle to handle large volumes of data in real-time from numerous devices.| Design a scalable, distributed architecture using cloud-native solutions (e.g., auto-scaling, load balancing).|
|   | *Data Quality & Accuracy*: Risk of low-quality or incorrect data affecting predictive analytics and healthcare decisions. | Implement rigorous data validation, monitoring tools, and introduce feedback loops to correct inaccuracies.|
|   | *High Initial Costs*: Setting up a cloud-based platform with real-time and batch data ingestion capabilities may have high upfront costs. | Develop a phased implementation plan and optimize cloud resource usage to lower costs.|
|   | *Third-Party Dependency: Reliance on third-party devices and cloud services, leading to potential service disruptions. | Include backup service providers and design failover strategies for critical services.|
|   | *Cross-Environment Data Consistency: Potential issues with data consistency across multiple environments. | Design robust data synchronization mechanisms and minimize data copying through efficient storage solutions.|

# Conclusion

For each work I performed I noticed the time I spent and here a full table to describe that.

| # | Name                 | Time Spent | Description   |
| - | ---------------------|------------|:-------------:|
|   | Anonymization        | 120 (before me) +15 minutes | |
|   | Input doc prepation  | 90 mins | |
|   | Business goals | 15 mins  | |
|   | Risks | 15 mins | |

<img src="./Images/TBD.jpg" alt="TBD" />

# References

| # | Name                 | Source                | Release date           |  Author                 | Description   |
| - | ---------------------|---------------------- |----------------------- | ----------------------- |:-------------:|
|   | DOU Day 2024         | [DOU](https://dou.ua/dou-day-2024/) |  | DOU | |
|   | ChatGPT Solutions Architect Assistent | [ChatGPT](https://chatgpt.com/g/g-J6uBbvDrm-solutions-architect-assistent) | | Probably SoftServe | |
|   | How to create architecture vision using AI | [gihub](https://github.com/dovchar/architecture-vision-GPTs) | | | |
