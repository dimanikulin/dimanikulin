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

Becacause I did not have any from those documents for my *Sample Case* I used *ChatGPT* (not Assistant meontioned previpsly) to help me to create [business case](./AIForSWArchitects_BusinessCase_Round1_en.md) from anonymizated input doc (*Sample case anonymizated.docx*).
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

The assitante is located [here](https://chatgpt.com/g/g-J6uBbvDrm-solutions-architect-assistent) and the communication with it is in a form like with **ChatGPT** - Prompt from **User** and Response from **AI**.

First I just wanted to try it out and just went from start to the end of assistance in way in suggested and without any clarification from my side. The result a put into [Round 1](./AIForSWArchitects_Assistance_Round1.md)

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
