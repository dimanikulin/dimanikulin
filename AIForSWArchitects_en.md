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

Becacause I did not have any from those documents for my *Sample Case* I used *ChatGPT* (not Assistant meontioned previpsly) to help me to create [business case](./AIForSWArchitects_BusinessCase1_en.md) from anonymizated input doc (*Sample case anonymizated.docx*).

# Assistance

The assitante is located [here](https://chatgpt.com/g/g-J6uBbvDrm-solutions-architect-assistent) and the communication with it is in a form like with **ChatGPT** - Prompt from **User** and Response from **AI**.

Cause the [Assistance model](https://chatgpt.com/g/g-J6uBbvDrm-solutions-architect-assistent) has been updating (in dev state) I have had to update my business case description and assitance output in progress of assitance.

## Round 1

Business case description kept such chapters as

- Company
- Project
- Decision Makers
- Product History
- Schedule
- Features
- Actors

First I just wanted to try it out and just went from start to the end of assistance in way in suggested and without any clarification from my side. The result I have put into [Round 1](./AIForSWArchitects_Assistance1_en.md).

This is what we started from:

**Me** - Hi, Can you help me in solution architect advisory?

**AI** - What type of help do you need?

**Me** - To advise a customer on how to create unified data platform.

**AI** - Great! For advising on a unified data platform, we need to create an architecture vision document. Could you provide additional information like: Request for Proposal (RFP), Request for Information (RFI), Text of the customer request. Let me know which one you have.

**Me** - RFP

**AI** - Please share the Request for Proposal (RFP) document or key details from it so I can assist you in defining the architecture vision for the unified data platform.

**Me** - Sent [business case](./AIForSWArchitects_BusinessCase1_en.md).

**AI** - Thank you for sharing the details. Based on the RFP, we will proceed with defining the architecture vision for the MedConnect IoT Platform's Unified Data Platform. The first step is to define Architecture Drivers, which include business goals, constraints, and use cases. Let's begin with defining the main business goals.

At each step it suggested to clarify current step response or go to next step.

## Round 2

So It did provide first a lot of output but output was not aligned well with real Business Case. And I thought the reason of being output too common and not aligned eith Business Case - the Business Case itself as it also was too common.

And new version of [business case](./AIForSWArchitects_BusinessCase2_en.md) appeared with more details and much more targeted.

The result I have put into [Round 2](./AIForSWArchitects_Assistance2_en.md).

## Round 3

As it still did not provide the assitance I need I decided to have one more round with it.

And new version of [business case](./AIForSWArchitects_BusinessCase3_en.md) appeared with more details and much more targeted.

The result I have put into [Round 2](./AIForSWArchitects_Assistance3_en.md).

# Conclusion

For each work I performed I noticed the time I spent and here a full table to describe that.

TODO to put a links to documets

| # | Name                 | Time Spent | Description   |
| - | ---------------------|------------|:-------------:|
| 1 | Anonymization        | 120 (before me) +15 minutes | |
| 2 | Input doc prepation, round 1 | 90 mins | |
| 3 | Assitance, round 1 | 60 mins  | |
| 4 | Input doc prepation, round 2 | 30 + 30 | |
| 5 | Assitance, round 2 | 15 mins  | |
| 6 | Input doc prepation, round 3 | TBD | |
| 7 | Assitance, round 3 | TBD | |

<img src="./Images/TBD.jpg" alt="TBD" />

# References

| # | Name                 | Source                | Release date           |  Author                 | Description   |
| - | ---------------------|---------------------- |----------------------- | ----------------------- |:-------------:|
|   | DOU Day 2024         | [DOU](https://dou.ua/dou-day-2024/) |  | DOU | |
|   | ChatGPT Solutions Architect Assistent | [ChatGPT](https://chatgpt.com/g/g-J6uBbvDrm-solutions-architect-assistent) | | Probably SoftServe | |
|   | How to create architecture vision using AI | [gihub](https://github.com/dovchar/architecture-vision-GPTs) | | | |
