# Headline
TBD

# Alternative headline

TBD

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


# Preqrequstires

---
=======Session 1=========
# Inro 5 min

# Developer use cases for AI with GitHub Copilot 
TBD

# Introduction to GitHub Copilot 
TBD

# GitHub Copilot Across Environments: IDE, Chat, GitHub.com, and Command Line Techniques 
TBD

# QA 

---
=======Session 2=========

# Introduction to prompt engineering with GitHub Copilot - 10 mins
TBD

# Using GitHub Copilot with С++ - 40 mins
TBD

# QA - 10 mins

---
=======Session 3=========
# Develop unit tests using GitHub Copilot tools 30 mins
TBD

# Documentation 15 mins
TBD

 # QA - 15 mins
---
=======Session 4=========
# Leveling up code reviews and pull requests with GitHub Copilot 30 mins
TBD

# Fixing the issues with copilot 
TBD

# QA - 30 mins


=======Session 5-6=========
# Hands-on #2 hours
TBD

# Advanced - (recommended for production teams)

# Advanced Prompt Engineering for C++
## Topics
Writing effective prompts:
- “Act as a senior C++ architect…”
- “Follow SOLID principles…”

Reducing hallucinations
Using Copilot Chat for:
- Refactoring plans
- Architecture discussions
- Context control (selective code highlighting)

## Exercise

- Refactor legacy C-style code to modern C++
- Optimize performance-critical code
- Ask Copilot to explain undefined behavior risks

# Patterns

- Thread-safe queue
- Observer pattern
- Strategy pattern



Run /plan before large changes
As the session evolves, Copilot automatically compacts context to keep the plan coherent. When work spans multiple files, run /plan in Copilot CLI (or use Shift+Tab to enter plan mode) to generate a reviewable outline of what will change. Use /model to compare strategies across models. Automatic compaction keeps long-running sessions focused. Install Copilot CLI (npm install -g @github/copilot) to get started.

Explore Copilot CLI →

 
Standardize how agents behave
across your team
AGENTS.md, Agent Skills, and custom agents define shared instructions and tool access so Copilot behaves predictably across sessions, models, workflows, and contributors. This is useful when multiple engineers are delegating work into the same repo.

https://docs.github.com/en/copilot/reference/customization-cheat-sheet?utm_source=lcm-mpu-dev-pro-get-started-Pro_UK_Day1&utm_medium=email&utm_campaign=FY26MAR-WW-LCM-PL-Free-Pro-PP-AA-Dev-TX-MPU

 
/delegate work and review a draft PR
Use /delegate in the CLI to assign tasks, explore /fleet for parallel subagents, and across your preferred models (using /model), and review sessions in the Agents tab. This keeps delegated work visible instead of detached from your repository.

Learn more →

 
Embed Copilot’s agent runtime in
your own tools
Use the Copilot SDK to build on the same GitHub-aware runtime Copilot runs on, with model routing and identity handled for you.Install Copilot CLI (npm install -g @github/copilot) to begin building with the SDK.

Build with the Copilot SDK →

<img src="./Images/TBD.jpg" alt="TBD" />

# References

| # | Name                 | Source                | Release date           |  Author                 | Description   |
| - | ---------------------|---------------------- |----------------------- | ----------------------- |:-------------:|
