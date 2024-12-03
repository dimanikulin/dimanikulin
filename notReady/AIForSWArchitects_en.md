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

# Architect Mentorship Case

Two data platforms in AWS and Azure Clouds
Create unified data platform and to migrate data from 2 Clouds into single one based on unified data platform
The unified data platform should store the data in the right format which is ideal for the relevant use cases
This also includes consolidation of data per cloud and per environment
Expected output - At least 3 diagrams - target data platform functional, target data platform deployment and migration one.

TBD images

# ChatGPT Solutions Architect Assistant

At [DOU Day 2024](https://dou.ua/dou-day-2024/) I found quite interesting the [ChatGPT Solutions Architect Assistent](https://chatgpt.com/g/g-J6uBbvDrm-solutions-architect-assistent)

The author is architect and created that assistant based on GPT LLM to speed up architecture work.

And it gave me undersnading on how I can use AI to [create architecture vision](https://github.com/dovchar/architecture-vision-GPTs?tab=readme-ov-file) from scratch spending hours but not days.

The assitante is located [here](https://chatgpt.com/g/g-J6uBbvDrm-solutions-architect-assistent) and the communication with it is in a form like with **ChatGPT** - Prompt from **User** and Response from **AI**.

So I decided to try it on my project to help.

# Preparation to use assistant

## Anonymization

Here we need to speak about input anonymization, so **AI** that you use for assitance will not find out the details for commercial project if any.

What you need to do at least is to remove any **PII** (*Personally Identifiable Information*) from input documentation.

So I created *Sample case anonymizated.docx* from *Sample case.docx*.

## Input docs preparation

As input documentation for creation architecture vision the following artifacts might be considered:

- RFP (Request for Proposal)
- RFI (Request for Information)
- Text of customer request

Becacause I did not have any from those documents for my *Sample Case* I used *ChatGPT* (not Assistant meontioned previpsly) to help me to create [Assistance input 1](./AIForSWArchitects_Input1_en.md) from anonymizated input doc (*Sample case anonymizated.docx*).

Business case description kept such chapters as

- Company
- Project
- Decision Makers
- Product History
- Schedule
- Features
- Actors

# Assistance

I had three rounds.

## Getting familiar with assistant or first look

First I just wanted to try it out and just went from start to the end of assistance in way in suggested and without any clarification from my side. The result I have put into [Round 1](./AIForSWArchitects_Assistance1_en.md).

Despite it provided all the Views in text description format, for Deployment view it provided Example in PlantUML.

TBD images

## First valuable output from the assistant or second round

I used Output from Round 1 for Round 2 input.

So It did provide first a lot of output but output was not aligned well with real Business Case. And I thought the reason of being output too common and not aligned eith Business Case - the Business Case itself as it also was too common.

And new version of [Assistance Input 2](./AIForSWArchitects_Input2_en.md) appeared with more details and much more targeted.

The result I have put into [Round 2](./AIForSWArchitects_Assistance2_en.md).

TBD images

## Final round - Third round

As it still did not provide the assitance I need I decided to have one more round with it.

And new version of [Assistance Input 3](./AIForSWArchitects_Input3_en.md) appeared with more details and much more targeted, but strcuture was the same as for round 2

The result I have put into [Round 3](./AIForSWArchitects_Assistance3_en.md).

Here it failed to generate proper PlantUML for Context View.

TBD images

## Final round - Fourth round

And new version of [Assistance Input 4](./AIForSWArchitects_Input4_en.md) appeared with more details and much more targeted

TBD images

# To be or not to be - to use or not to use

For each work I performed I noticed the time I spent and here a full table to describe that.

TBD to put a links to documets

| # | Name                 | Time Spent | Output   |
| - | ---------------------|------------|:-------------:|
| 1 | Anonymization        | 120 (before me) +15 minutes | Sample case anonymizated.docx |
| 2 | Input doc prepation, round 1 | 90 mins | [Assistance input 1](./AIForSWArchitects_Input1_en.md) |
| 3 | Assitance, round 1 | 60 mins  | [Round 1](./AIForSWArchitects_Assistance1_en.md) |
| 4 | Input doc prepation, round 2 | 30 + 30 | [Assistance Input 2](./AIForSWArchitects_Input2_en.md) |
| 5 | Assitance, round 2 | 30 mins  | [Round 2](./AIForSWArchitects_Assistance2_en.md) |
| 6 | Input doc prepation, round 3 | 30 + 15 | [Assistance Input 3](./AIForSWArchitects_Input3_en.md) |
| 7 | Assitance, round 3 | 15 | [Round 3](./AIForSWArchitects_Assistance3_en.md) |

# Observations

At each step it suggested to clarify current step response or go to next step.

Still in development state. So you might need to align your input before next assistance round. Also the outputs for different sessions might be different even for the same input
Cause the [Assistance model](https://chatgpt.com/g/g-J6uBbvDrm-solutions-architect-assistent) has been updating (in dev state) I have had to update my business case description and assitance output in progress of assitance.

TBD iterative process.

Can make mistakes as all AI and human. So you need to review the output

I used Draw.IO to draw diargams from PlantUML generated

<img src="./Images/TBD.jpg" alt="TBD" />

# New case to consider

The first case assistant output was not good enough to take into account, probably because of case complexity and i decided to take easier case:[Round 1](./AIForSWArchitects_Input1_yes_en.md)

in format of RFP and ChatGPT helped again to provide template

# References

| # | Name                 | Source                | Release date           |  Author                 | Description   |
| - | ---------------------|---------------------- |----------------------- | ----------------------- |:-------------:|
|   | DOU Day 2024         | [DOU](https://dou.ua/dou-day-2024/) |  | DOU | |
|   | ChatGPT Solutions Architect Assistent | [ChatGPT](https://chatgpt.com/g/g-J6uBbvDrm-solutions-architect-assistent) | | Probably SoftServe | |
|   | How to create architecture vision using AI | [gihub](https://github.com/dovchar/architecture-vision-GPTs) | | | |
