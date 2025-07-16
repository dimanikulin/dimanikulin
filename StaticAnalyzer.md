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

TBD


# C++ Static Analyzers Comparison (Extended)

| Analyzer         | Cost                         | Complex Issue Detection (e.g., infinite loops) | Support & Updates           | Use in Complex Projects | Integration (CI/IDE/Build) | False Positive Rate | Notes/Remarks |
|------------------|------------------------------|------------------------------------------------|-----------------------------|--------------------------|-----------------------------|----------------------|----------------|
| **Cppcheck**     | Free & Open Source           | Limited (syntax, logic, some memory)           | Good community, regular     | Moderate                 | Good (CI, IDEs like VSCode) | Low to Medium        | Good for lightweight checks, MISRA configurable |
| **SonarQube**    | Free (Community) / Paid tiers| Moderate (depends on plugins/rules)            | Excellent (ongoing dev)     | High                     | Excellent (Jenkins, GitHub, GitLab) | Low to Medium   | Great for monitoring code health trends |
| **Clang SA**     | Free (LLVM)                  | Good (path-sensitive, flow-aware)              | Active LLVM community       | High                     | Excellent (CMake, Ninja, CI) | Medium            | Used widely with modern toolchains |
| **Coverity**     | Commercial (free for OSS)    | **Excellent** (deep, interprocedural)          | Enterprise-grade            | **Very High**            | First-class (IDE/CI integration) | Low               | Ideal for regulated/safety-critical projects |
| **PVS-Studio**   | Paid (Free for OSS)          | **Very Good** (concurrency, data races, etc.)  | Commercial, frequent updates| High                     | IDEs (VS, CLion), CI/CD     | Low to Medium        | Great diagnostics; supports many standards |
| **Infer**        | Free (Facebook OSS)          | Good (concurrency, null derefs)                | Moderate (slower updates)   | Medium                   | CI support (Linux-focused)  | Medium             | Optimized for mobile & server OSS projects |
| **CodeChecker**  | Free & Open Source (LGPL)    | Good (uses Clang Static Analyzer under hood)   | Good community              | Moderate to High         | Integrates with GitHub, GitLab CI | Medium          | UI to review findings, supports suppression |

---

## 🔍 What to Use: Open Source vs Commercial Projects

| Project Type  | Recommended Tools | Why |
|---------------|-------------------|-----|
| **Open Source** | `Cppcheck`, `Clang Static Analyzer`, `CodeChecker`, `Infer` | Free, open-source friendly, some offer OSS-specific licenses (e.g., Coverity, PVS-Studio for OSS) |
| **Commercial** | `Coverity`, `PVS-Studio`, `SonarQube Developer/Enterprise`, optionally `Cppcheck` | Commercial tools provide deep analysis, compliance checks (MISRA, CERT), strong support and integrations |

- **Note:**  
  - **Coverity** and **PVS-Studio** are commonly used in **aerospace, automotive, medical**, and other **certified** environments.
  - **Cppcheck + Clang SA + CodeChecker** can be a strong **low-cost pipeline** even in commercial contexts, though lacking full standard compliance analysis or enterprise features.

---

## 🧑‍💻 GitHub vs GitLab Tooling Advice

| Platform | Best Tooling Options | Notes |
|----------|----------------------|-------|
| **GitHub** | `SonarQube`, `CodeChecker`, `Infer`, `Clang SA`, `Cppcheck` | GitHub Actions + built-in integrations; SonarCloud has GitHub-first support |
| **GitLab** | `CodeChecker`, `SonarQube`, `Cppcheck`, `PVS-Studio`, `Clang SA` | GitLab CI YAML makes custom analyzers easy to wire in; SonarQube can plug in smoothly |
| **Both**   | All tools can be used effectively | Prefer tools that support **CLI and JSON output** for CI integration (all above do) |

### GitHub Highlights:
- **SonarCloud** (SaaS version of SonarQube) is deeply integrated.
- Marketplace actions exist for **Cppcheck**, **Infer**, etc.

### GitLab Highlights:
- Native support for **Code Quality Reports** (`codeclimate.json`) — e.g., **Cppcheck** and **CodeChecker** can be configured to emit this.
- Full control via `.gitlab-ci.yml`, ideal for chaining analyzers.

## TL;DR Recommendations

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
