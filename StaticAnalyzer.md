# Headline
Comprehensive Comparison of C++ Static Analyzers: From Open Source to Enterprise Solutions

# Alternative headline

C++ Static Analysis Tools Compared: Cppcheck, SonarQube, Clang SA, Coverity, PVS-Studio, Infer, and CodeChecker

# Table of contents

- [Tags](./!Template.md#tags)
- [Definitions, Acronyms, Abbreviations](./!Template.md#definitions-acronyms-abbreviations)
- [Overview](./!Template.md#overview)
- [Introduction](./!Template.md#introduction)
- [References](./!Template.md#references)
TBD

# Tags

C++, Static Analysis, Cppcheck, SonarQube, Clang Static Analyzer, Coverity, PVS-Studio, Infer, CodeChecker

# Definitions, Acronyms, Abbreviations

| # | Abbreviation or Acronym | Definition     |
| - | ------------------------|:--------------:|
| 1 |

# Overview

Here's a comparison of 6 C++ static analyzers - *Cppcheck*, *SonarQube*, *Clang Static Analyzer*, *Coverity*, *PVS-Studio*, *CodeChecker*, and *Infer* - across several relevant criteria.


# C++ Static Analyzers Comparison

| Analyzer         | Cost                         | Complex Issue Detection (e.g., infinite loops) | Support & Updates           | Use in Complex Projects | Integration (CI/IDE/Build) | False Positive Rate | Notes/Remarks |
|------------------|------------------------------|------------------------------------------------|-----------------------------|--------------------------|-----------------------------|----------------------|----------------|
| **Cppcheck**     | Free & Open Source           | Limited (syntax, logic, some memory)           | Good community, regular     | Moderate                 | Good (CI, IDEs like VSCode) | Low to Medium        | Good for lightweight checks, MISRA configurable |
| **SonarQube**    | Free (Community) / Paid tiers| Moderate (depends on plugins/rules)            | Excellent (ongoing dev)     | High                     | Excellent (Jenkins, GitHub, GitLab) | Low to Medium   | Great for monitoring code health trends |
| **Clang SA**     | Free (LLVM)                  | Good (path-sensitive, flow-aware)              | Active LLVM community       | High                     | Excellent (CMake, Ninja, CI) | Medium            | Used widely with modern toolchains |
| **Coverity**     | Commercial (free for OSS)    | **Excellent** (deep, interprocedural)          | Enterprise-grade            | **Very High**            | First-class (IDE/CI integration) | Low               | Ideal for regulated/safety-critical projects |
| **PVS-Studio**   | Paid (Free for OSS)          | **Very Good** (concurrency, data races, etc.)  | Commercial, frequent updates| High                     | IDEs (VS, CLion), CI/CD     | Low to Medium        | Great diagnostics; supports many standards |
| **Infer**        | Free (Facebook OSS)          | Good (concurrency, null derefs)                | Moderate (slower updates)   | Medium                   | CI support (Linux-focused)  | Medium             | Optimized for mobile & server OSS projects |
| **CodeChecker**  | Free & Open Source (LGPL)    | Good (uses Clang Static Analyzer under hood)   | Good community              | Moderate to High         | Integrates with GitHub, GitLab CI | Medium          | UI to review findings, supports suppression |

## Legend:
- **Cost**: Indicates licensing model.
- **Complex Issue Detection**: Quality of detecting bugs like infinite loops, deadlocks, etc.
- **Support & Updates**: Community or commercial support availability.
- **Use in Complex Projects**: Suitability for large-scale, multicomponent codebases.
- **Integration**: Ability to plug into common IDEs, CI/CD pipelines, and build systems.
- **False Positive Rate**: Indicates how often incorrect issues are reported.

# Use - case recommendations

Here's an expanded version of the C++ static analyzer comparison,  with use-case recommendations depending on your project (embedded systems, real-time, etc.) and budget (no money, some money, unlimited budget).

## 🔧 Embedded Systems
- **Recommended:**  
  - **Coverity** – top-tier detection of low-level and concurrency issues, MISRA support.
  - **PVS-Studio** – detects many subtle issues relevant to hardware interaction.
  - **Cppcheck** – useful on a budget, supports MISRA rules (manual config needed).

## ⏱️ Real-Time Applications (e.g., robotics, audio/video, SCADA)
- **Recommended:**  
  - **Coverity** – great for concurrency, memory access, and responsiveness analysis.
  - **Clang Static Analyzer** – efficient and integrates with RTOS-targeting toolchains.
  - **PVS-Studio** – helpful for logic and concurrency bugs.

## 🧪 Safety-Critical Systems (e.g., automotive, aerospace, medical)
- **Recommended:**  
  - **Coverity** – certified for ISO 26262, DO-178C use cases.
  - **PVS-Studio** – customizable ruleset for standards like MISRA, CERT.
  - **Cppcheck** – good base-level check when integrated early in CI.

## 💰 Budget-based Recommendations

### 🆓 No Budget
- **Use**:  
  - **Cppcheck** – main tool.
  - **Clang Static Analyzer** – for deeper control flow analysis.
  - **Infer** – adds value for concurrency bugs (especially in Linux/Android).
  - **SonarQube Community** – if you want quality tracking over time.

### 💸 Limited Budget (~$500–$2,000/year)
- **Use**:  
  - **PVS-Studio** – great ROI for price, especially for teams or startups.
  - Combine with **Cppcheck** and **Clang SA** to fill any gaps.
  - Optional: **SonarQube Developer Edition** for more C++ rules.

### 💼 No Budget Limit (Enterprise / Mission-critical)
- **Use**:
  - **Coverity** – enterprise-grade detection, support, and compliance.
  - **PVS-Studio** – complements Coverity with explainable reports.
  - **SonarQube Enterprise** – for metrics, dashboards, and team health.
  - Combine all of the above in CI/CD for layered defense and compliance.

## Open Source vs Commercial Projects

| Project Type  | Recommended Tools | Why |
|---------------|-------------------|-----|
| **Open Source** | `Cppcheck`, `Clang Static Analyzer`, `CodeChecker`, `Infer` | Free, open-source friendly, some offer OSS-specific licenses (e.g., Coverity, PVS-Studio for OSS) |
| **Commercial** | `Coverity`, `PVS-Studio`, `SonarQube Developer/Enterprise`, optionally `Cppcheck` | Commercial tools provide deep analysis, compliance checks (MISRA, CERT), strong support and integrations |

- **Note:**  
  - **Coverity** and **PVS-Studio** are commonly used in **aerospace, automotive, medical**, and other **certified** environments.
  - **Cppcheck + Clang SA + CodeChecker** can be a strong **low-cost pipeline** even in commercial contexts, though lacking full standard compliance analysis or enterprise features.

## Summary

If you're dealing with **tight safety or real-time constraints**, tools like **Coverity** and **PVS-Studio** shine thanks to their deep semantic understanding. For **open-source or hobby projects**, **Cppcheck**, **Clang SA**, and **Infer** are excellent, cost-free choices with reasonable capabilities.


# 🧑‍💻 GitHub vs GitLab Tooling Advice

| Platform | Best Tooling Options | Notes |
|----------|----------------------|-------|
| **GitHub** | `SonarQube`, `CodeChecker`, `Infer`, `Clang SA`, `Cppcheck` | GitHub Actions + built-in integrations; SonarCloud has GitHub-first support |
| **GitLab** | `CodeChecker`, `SonarQube`, `Cppcheck`, `PVS-Studio`, `Clang SA` | GitLab CI YAML makes custom analyzers easy to wire in; SonarQube can plug in smoothly |
| **Both**   | All tools can be used effectively | Prefer tools that support **CLI and JSON output** for CI integration (all above do) |

## GitHub Highlights:
- **SonarCloud** (SaaS version of SonarQube) is deeply integrated.
- Marketplace actions exist for **Cppcheck**, **Infer**, etc.

## GitLab Highlights:
- Native support for **Code Quality Reports** (`codeclimate.json`) — e.g., **Cppcheck** and **CodeChecker** can be configured to emit this.
- Full control via `.gitlab-ci.yml`, ideal for chaining analyzers.

# TL;DR Recommendations

| Scenario | Recommended Stack |
|----------|-------------------|
| **Open-source contributor** | `Cppcheck + Clang SA + CodeChecker` |
| **Startup with limited budget** | `PVS-Studio (low-cost team license) + Clang SA` |
| **Enterprise with safety/security needs** | `Coverity + PVS-Studio + SonarQube Enterprise` |
| **GitHub-hosted repo** | `SonarCloud + Clang SA + Infer` |
| **GitLab-hosted repo** | `CodeChecker + SonarQube + Cppcheck` |


<img src="./Images/TBD.jpg" alt="TBD" />

# References

| # | Name                 | Source                | Release date           |  Author                 | Description   |
| - | ---------------------|---------------------- |----------------------- | ----------------------- |:-------------:|
