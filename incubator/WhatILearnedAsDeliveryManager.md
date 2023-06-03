# Headline
TBD
What I learned as a Delivery Manager while creating my product

# Article description
TBD 
, and uncover the significance of tracking implementation status for better requirement coverage

# Tags
TBD

# Content

First I started thinking how to get more engagement with my open source project. Why? Beacause: 
- Developers play a crucial role in adopting and integrating your product into their projects.
- Engaged developers who have a positive experience with your product can become powerful advocates.
- They are more likely to explore the extensibility options and customization capabilities of your product. 
- Also Engaged developers can provide valuable feedback, suggestions, and bug reports.
- Finally they may actively participate in your product's open-source community, contribute code, report issues, and collaborate on its development. 

Their contributions can accelerate the pace of innovation, foster a sense of ownership and community, and create a network effect that attracts more developers to get involved.

## Create a Good Readme
[It](https://github.com/dimanikulin/fva#readme) is the first thing that a visitor to your repository sees.
And good README serves as a comprehensive and accessible starting point for users and developers to engage with your project.

It should be able to convey what your project is able to do, how to instakk and work with the project, how to contribute, etc.
It also keeps structured information for product and its implementation details. 

My readme start with product logo. 

### Bages
Than it moves to bage chapters that are helpful for developers. There are following sections:
- Common (Repo stars, contributors, followers, sponsors and twitter URL)
- Release (last release version, last release date and numbers of downloads)
- Code statistic (status of build flow,GitHub commit activity,GitHub last commit and www.codefactor.io status)
- Issues and Pull requests (GitHub issues, GitHub closed issues, GitHub pull requests and GitHub closed pull requests)
- Repository statictis (GitHub top language, GitHub language count and GitHub repo size) 
- Documentation(Roadmap, Discussions, License and Main Readme)

<img src="FvaReadme.png" alt="FvaReadme"/>

There are 3 different types of badges in terms of their way of implementation
- Implememented by GitHub like [this](https://github.com/dimanikulin/fva/actions/workflows/main.yml/badge.svg?branch=master) 
- Implememented by img.shields.io like [this](https://img.shields.io/github/last-commit/dimanikulin/fva)
- Implememented by www.codefactor.io like [this](https://www.codefactor.io/repository/github/dimanikulin/fva)

# Quick Links
After it switches to Quick Links chapter. 
Quick links in a README file are important because they provide easy and convenient access to key sections, resources, or external references related to a project. 
They serve as navigational aids, allowing readers to quickly jump to specific parts of the README without having to scroll or search extensively.

So I add the Quick Links for each main chpter in [readme](https://github.com/dimanikulin/fva#readme)


not to overlod main reamd there were some child files created to keep details:
- 
-
-
TODO IN the root folder there are also all md file kept 

## Implementation status
Before diving into the coding phase, I considered how I could effectively track the coverage of requirements. 
I needed a way to implement tracing and determine which requirements were covered and which ones were not. 
To address this, I devised a table with the following columns:

**Implemented**: Indicates whether the requirement has been implemented, marked as either "yes" or "no."
**Feature ID**: An identifier sourced from the features.
**Component**: Specifies the name of the component.
**File names**: Lists the file names where the implementation for the requirement can be found.
**Description**: Provides a description of the functional requirement.

TODO link to Implementation status 

2. Focus on Documentation
How to install/deploy the project
Contributing guide
Tutorials and code examples
Architecture reference

3 Be active in developer communities
Trending repositories on GitHub
 4.Ask for feedback from relevant communities
Respond to feedback
Open-source communities are usually very helpful and give a lot of feedback. Respond to all this feedback, as the person has taken their valuable time to help you improve your project.

Grow a community around your project
Start a community on Discord or Slack where your users and contributors can hang out.


Add a public roadmap

Add relevant labels for contributors
Adding labels such as "good first issue" and "up for grabs" can attract more contributors to your repository.


## Releasing the code and the docs
&nbsp;&nbsp;&nbsp; The release of product shall be on demand as soon as peace of product functionality is ready for release.
Thus the release branch is being created or updated to keep added/updated product functionality.

&nbsp;&nbsp;&nbsp; Regardless of incremental approach to add or update product functions, the artifacts shall accumulate whole product installation packages and not increments even really small piece of functions is released.

The following artifacts shall be created:
- The documentation for code (based on doxy comments);
- The installation packages for Windows, Mac and Linux latest version. 



to speak main readm file sttucute, git hubm bages
and How to get more engagement with your open source project

&nbsp;&nbsp;&nbsp; Honestly, I didn't learn much as a Delivery Manager. Still, here are some points to consider...

## Project Status tracking
&nbsp;&nbsp;&nbsp; Tracking project status is quite an important activity of Delivery Manager.

### GitHub projects
&nbsp;&nbsp;&nbsp; **GitHub Projects** is tool for tracking project status online integrated into your GitHub profile.
It is quite easy to use, and it doesn't have a lot of functions. 
Here it [is](https://github.com/dimanikulin/fva/projects/3)

### ProjectLibre
&nbsp;&nbsp;&nbsp; In spite of all the above-mentioned, a more compex solution was required. 
My choice was [ProjectLibre](https://www.projectlibre.com/product/1-alternative-microsoft-project-open-source).
ProjectLibre desktop is a free and open-source project management software system, intended ultimately as a standalone replacement for Microsoft Project.
Despite being a free and small app, it gave me everything I needed.

TBD openproject

# References
| # | Name                 | Source           | Release date           |  Author                 | Description |
| - | ---------------------|---------------------- |----------------------- | ----------------------- |:-------------:|
| 1 | Getting started with project planning on GitHub| [Web](https://github.blog/2022-02-11-getting-started-with-project-planning-on-github/) |2022-02-11 | GitHub | |
| 2 | How to get more engagement with your open source project| [freecodecamp](https://www.freecodecamp.org/news/how-to-get-more-engagement-with-your-open-source-project/) | JANUARY 26, 2022 | navaneeth pk |Best practices to get more stars on your GitHub repos|