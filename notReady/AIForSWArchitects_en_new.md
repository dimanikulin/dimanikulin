# Headline
GenAI Assistant for Solution Architects

# Table of contents

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

or ---

# Introduction

I worked as a *lead software developer* in big medical product and meanwhile I took part in mentorship in GL Architecture mentorship. During mentorship I got a business case to implement - service marketplace platform. You might know in Ukraine we have **Kabanchic** - it helps to connect people like plumbers, electric engineer and with other people like their customer so they connect each other to get provide/get the services with/in.
In Europe we have **UrbanSitter** and USA we have something similar

# Service marketplace platform

So *customer* wanted implementing this marketplace platform. They wanted from us to have **Visa cards** to integrate(payment using the cards), web money and bitcoins. Also they wanted to have **Google Analytics** and put some advertisement in their platform.
 
 <img src="./Images/AIForSWArchitects1.jpg"  />

# ChatGPT Solutions Architect Assistant

Fortunatly during implementation I got access to video recording from **DOU Days 2024**.
DOU is a big IT society in Ukraine and they have some conference in May 2024 year. There was an architect from other company and he shown us architecture assistant based on generative AI. So for example you are software developer and you can use GitHub Copilot to help to generate the code and this generative AI assitance can help you as an architect to generate Arhitecture Vision.
So it helped him a lot to increase speed and decrease time of spent by to create architecture vision in times. What he said exactly he had to spend days to implement architecture and now using this assistant he had to spend just hours.
Let simply say ChatGPT was customized to help architects so it's not usual flow for usual user and it will directly go to architect flow with inputs, outputs and another deviation.

<img src="./Images/AIForSWArchitects2.jpg"  />

He provided example of simple solution to implement and he said before it it was 4 days and now using this assistant *It was able to make my architecture vision in four hours*. It was really challening for me. So I decided to check it to create Solution Architecture for my business case. It's based on **ChatGPT** so you prompt solution assistant, then you have response from it and so communication is done with this approach.
It accepts the input information in three forms we have usually for pre-sales so it's **RFP,** **RFI** and usual text (just plain text).
And what is good you can use some output from stage input for another stage. As the output it provides diagrams, tables and text description for everything. Also it migth provide the output in **Markdown** or **PlantUML** format.

This assistant was still in development, not sure about now.

## Preparation to use assistant

<img src="./Images/AIForSWArchitects3.png"  />

If you ask - *what about data leaks and data sharing with third party company like open AI?*
I will answer - *You need to have some preparation before using this assistant. So I had the usual RFI (request for information) and it had a lot of details from customer. And for sure I could not put everything from a RFI to my input to this assistance. So what I did I just removed everything from pictures, from text, from tables that could identify this RFI like request from that customer.*
So it is anonimization and you need to remove any **PI information**

And yes, you need to have input in form of **RFI**, **RFP** or another text for this assistante.

# Service marketplace platform - Success story
So it was success story and also there was not so success story but I will tell it a little bit a bit later.
I had five rounds of working with this assistant because when you have only one round information output can go in one wrong way and so on and had it in several rounds. Then I merged results and it was much more valuable and exact for me. By round I mean when you start working with assistant saying *hi let's start creation architecture vision* and until it tells *everything done so any clarification is welcome*. So from for *first* question to *the last* question it's one round for me.
Please notice when you work with several rounds you could have different answers on the same question.

## Service marketplace platform, Inputs

<img src="./Images/AIForSWArchitects4.png"  />

I used СhatGPT to help me create RFI. It had overview, some background information about marketplace platform, when I'm going to implement it. Also there was project scope and requirements - key features, functionality and so on technical requirements. And as usual there were terms and condition. I was able just to attach file so I had its input as a file and not in plain text copied from an editor. So it parsed it.

## Service marketplace platform, Outputs
This this assistant output is based on standard classic approach like descibed by Microsoft or Software Institute.
So it started from business goal and constrains. then it moved to discussion use cases and main features with quality attribute scenarios.
And then it made me happy when I got design with several views with operation plan, solution road map and team composition.
<img src="./Images/AIForSWArchitects5.png"  />

What was good with this assistant at communication -  I felt like I'm speaking with a human architect who quite is experienced in this area because I was not experienced. Still I was able to challenge it. For example I asked this assistant to prove that this point is acceptable for me. Why it choose for example Azure as a cloud platform and it explained it. So it was a kind of real communication with a kind of real architect.

As I said there were several diagrams and now you can see functional decomposition.
it's layered architecture with front end layer, backend services and databases layer.

<img src="./Images/AIForSWArchitects6.png"  />

 Also there is integration layer with third parties like **payment gateways**, **Ad API** and **Google Analytics**.

So it made three layer functional decomposition with description for each layer.

And here is another functional decomposition with less details from another round.
<img src="./Images/AIForSWArchitects7.png"  />

 I just meontioned it here so you see it outputs differently in different rounds of working with that.
 
 And as final step of working with resistant you will have architecture vision document. 
 There will fundamental text description for each area - for team composition, for diagrams etc.

# Final Deck

Based on output I had from five rounds working with architecture assistant I created final deck.

## Context View
It generated **Context View** so we see users like - *suppliers*, *customers* and *admins*
Also we have *core components* with some details inside of platform - *web services*, *admin panel*, *notification service*
And we have integration part - so *payment gateways*, *analytics* and *advertisement API*.
<img src="./Images/AIForSWArchitects8.png"  />

## Decomposition View
The next view is the Decomposition one - quite detailed view. And I was really happy to have it.
We have again *backend services* layer, we have *front end* layer, we have *integration* with *external* system and *database* layer. 

For *back end* we have several services - *Order management*, *Notification*, *Analytic*, *User*, *Integration* and *product* ones.  It communicates with *user data*, *product data*, *order data* and *ordering data* from *DB* layer.
In *front end* layer there are two interfaces - for admin and for another people - so for suppliers and for customers.
And again we have integration with *Payments gateways* and *Google API* as it was required by the customer.

<img src="./Images/AIForSWArchitects9.png"  />

## Deployment View
So moving to deployment view. It put here *backend and frontend clusters*, *payment gateways* like external systems and so on.
What wasn't good for me - we don't know anything about exactk services we need to use here - no service name *GCP platform* we can use and it's quite misleading for me.
<img src="./Images/AIForSWArchitects10.png"  />

Here you can comment: *So the diagram is let's say cloud agnostic I would say So that's just a very basic one.But personally I always struggling with the cloud services the existing on AWS or whatever and that's the main point for me because I'm not the back end let's say solution architect etc.* *So what if this solution might dive deeper and propose the exact solution based on the existing cloud services etc. And this diagram is I would say even primitive one like that's a very basic concept like giving the composition between services etc.*
*So I wouldn't use even that right because I can draw it on my own but from what I really would like to have a help of the s sort of assistance proposing the really existing services and maybe even the prompts give me the cheap best solution or… the fastest like the scale available solution etc. That would help building this solution out of the existing services and maybe some plan how to set up that on the infrastructure side to make it scalable etc etc*. *If we are talking about the exact AWS services I don't know and that would be one of the inputs right I need to build some AWS solution. Does this **GenAI accelerator** or what can provide the diagram mentioning the exact cloud services like this?*
*And based on that inputs that would give me the exact services maybe there is a way to extend this accelerator or something in that way that would be a really helpful instrument strument. Not this one I would say this diagram I would draw in several minutes for instance, But what I will really struggle is finding the right services*?

## Core Team Composition
It suggested this *core team composition*. So there is 12 people working with this product.
So it has one *project manager*, *business analyst*, *solution architect*, five *software developers*, two *DevOps* and two *QA engineers* with their required skills and responsibilities.

<img src="./Images/AIForSWArchitects11.jpg"  />

## Roadmap
It provided road map so it has about one half an year to implement this project from *project initialization* until *post deployment support* so when it is already on production.
<img src="./Images/AIForSWArchitects12.jpg"  />

# Conclusion
## Timing
So for this particular quite simple use case business case I spent a half a day to get everything from *requirement definition* and *business case description* until *team composition*. I think if it was real life without help of assistant I would spend about three or even four days to create the those artifacts. So for me it decreased time four times I spent on architecture.
<img src="./Images/AIForSWArchitects13.jpg"  />

## What was good and what was not good 
It provides all diagrams in **plant UML** so you can insert this **Plant UML** for example **into Draw.IO** and it will generate htose diagrams.
But all diagrams were portrait oriented and they didn't fit usual presentation page.
Probably it can be changed it but I didn't ask it to change orientation to be not portrayed but album so all diagrams fit usual presentation.
<img src="./Images/AIForSWArchitects14.png"  />
The *context diagram* based on **plant UML** was quite good but keep too much details as for me inside of.
And what I already said *deployment view* wasn't good in detail so it didn't provide cloud terms, cloud service names and so on.
And it provided *CI views* and they were for me fully useless.
Also As I said you can challenge it so retry asking question from another PoV.
And it did not fit with our GL styles but it might be a kind of automatic applying of styles for any diagram.

# Data Platform - Not success case
 and so again there was good case with this platform
 So I had everything I wanted from assistant every diagram skill set road and so on.  But there was another business case big data data plat platform and this assistant didn't help me. 
## Data Platform
TBD

# References

| # | Name                 | Source                | Release date           |  Author                 | Description   |
| - | ---------------------|---------------------- |----------------------- | ----------------------- |:-------------:|
