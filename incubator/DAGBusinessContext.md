# Headline
TBD

# Article description
TBD 

# Tags
TBD

# Definitions, Acronyms, Abbreviations
TBD
API	API is the acronym for Application Programming Interface, which is a software intermediary that allows two applications to talk to each other.
API gateways	An API gateway is an API management tool that sits between a client and a collection of backend services. An API gateway acts as a reverse proxy to accept all application programming interface (API) calls, aggregate the various services required to fulfill them, and return the appropriate result.
Architecture Governance		Architecture governance is an approach, a series of processes, a cultural orientation, and set of owned responsibilities that ensure the integrity and effectiveness of the organization's architectures.
CI/CD	CI/CD or CICD is the combined practices of continuous integration and continuous delivery or continuous deployment.
Cloud Model	There are three major cloud service models: software as a service (SaaS), infrastructure as a service (IaaS) and platform as a service (PaaS). Cloud service pricing models are categorized into pay per use, subscription-based and hybrid, which is a combination of pay-per-use and subscription pricing models.
Cloud Services	The term "cloud services" refers to a wide range of services delivered on demand to companies and customers over the internet. These services are designed to provide easy, affordable access to applications and resources, without the need for internal infrastructure or hardware.
Cluster 	A computer cluster is a set of computers that work together so that they can be viewed as a single system. Unlike grid computers, computer clusters have each node set to perform the same task, controlled and scheduled by software.

# Content
## Executive summary
In the modern software world, the rapidly changing environment requires the software architecture to be changeable fast as well.
Everything connected to the software as business and product requirements, architectural requirements might evolve to succeed in the high-tech world. 

Therefore, a software architecture as a product technical basement should evolve fast and be for the changes. 

Although the readiness for changes is a key point for a product to succeed, the uncontrolled architecture drifts and erosions may lead a product to fail even when it is already in a production state and has been successful for a while.

For example, the architecture drift can lead to lose the initially expected extensibility and new customers can fail to use a product in case the number of users increases.
Such drifts might be identified during architecture reviews. Usually, the process of architecture reviews is quite a complex process and takes much time to assess the software architecture because it requires experienced architects and this process is almost manual. 

In addition, because it is manual almost it might be intended as not so efficient and many architectural issues might not be discovered due to the influence of human factors.

## Detecting Architectural Gaps with Automation
Please read [this paper](https://www.globallogic.com/insights/white-papers/detecting-architectural-gaps-with-automation/) before going to the next chapters. 

You'll learn:

- What architecture drift and erosion are, and how they impact the business.
- How dependency analysis, peer reviews, and other manual inspections work.
- Why even though they catch issues not prevented through the application of best practice good architecture governance, manual reviews are not the ideal solution.
- Specific considerations to keep in mind around compliance, data security, DevOps, and more when evaluating architecture review solutions.
- What automating architecture checks may look like in a series of example use case scenarios.
 
## Solution requirements
This section describes the requirements to implement the solution. 
This set of requirements are not limited and might be extended based on real project needs.
First, it starts from description of the solution modes and inputs, and then it switches to the solution integration and user interaction. 
After it describes the solution output with such quality attributes like modifiability, extendibility and configurability.

### Solution modes
The following modes shall be supported to run the solution:
- Standalone application: because the solution is required to be executed on demand it should be possible to run as a usual application without any dependencies on the target environment;
- Separate step in CI/CD pipeline: Because the regular assessment of architecture might be required, it should be possible to run it as integrated into CI/CD pipeline step.

In the scope of CI/CD, there should be a possibility to set initial architecture as referenced one and any deviations from it should be reported as drifts. 
Once the drift is detected, there should be an option to approve or decline the changes with comments. 
The description for change shall be provided with impact analysis so the user can acknowledge the cost of change.
For any drift, there should be a possibility to save the document keeping the description of drifts or erosion to help it analyze later.
Widely used CI/CD tools like Jenkins, Bamboo, etc. have to be easily integrated with proposed solutions.

### Solution inputs 
The inputs for the proposed solution can be: 
- any code from the solution under review;
- any configuration from the solution under review;
- software design from UML designing tools;
- Database scripts and database configuration.

### Solution integration 
Based on required inputs the proposed solution can be integrated with offline UML designing tools like:
- OmniGraffle;
- Microsoft Visio.

In addition, proposed solution can be integrated with such online UML designing tools like:
- Enterprise Architect;
- LucidChart;
- Draw.IO;
- PlantUML;
- Gliffy.com.

To have access to code and configuration the proposed solution can be integrated with source control management system like:
- SVN;
- Git.

In this way, the proposed solution user shall understand the more input is provided the more efficient automatic review will be performed.
As an example of the input code could be the code written in C# using microservices architecture. 
The other example could be the code written in JavaScript for multi-tier applications. 
The example of configuration might be the description of nodes used in deployment.
Another example could be the configuration of VPN network and API gateways.
The example of input software design can be description of interfaces saved in Enterprise Architect.

### User interaction
The user can interact with the solution using a web interface from a desktop computer. No mobile device (like smartphones or tablets) is intended because the low screen size of mobile devices is not suitable for the content the proposed solution is going to provide. 
Two types of user shall be supported: administrators and architects. 
The administrators shall be able to configure the system for intended use.
The architects shall be able to run the proposed solution for analysis and to review the analysis results.
The dashboards can be available to show metrics and software architecture status like: components count, dependencies list etc.

### Solution output
There are two formats of output: the text (plain text or table) one and graphic one.

The table format is used to provide a user with 
- a level of issue, 
- the issue priority, 
- the issue description itself 
- and the suggested way to fix the issue.

In addition, it shall list
- all dependencies (frameworks, libraries);
- APIs, 
- databases, 
- technology stack (languages) 
- and application layers into separate documents. 

It shall be possible to request the inventories of the 
- languages, 
- frameworks, 
- libraries, 
and databases used in the application at any time.

An example of text output might be following
| # | Level                | Priority              | Issue                  | Suggestion   |
| - | ---------------------|---------------------- |----------------------- |:-------------:|
| 1 | Architecture | Medium | BackEnd For FrontEnd services are directly integrated with third party services (external services) | To add an abstraction level to decrease the level of dependency on third parties |
| 2 | DevOps |	High |	Endpoints configuration are not correct basing of their meta description |To fix configuration |
| 3 | Architecture| High | Communication in between microservices does not meet initially predefined communication | To update initially documented communication or to fix current communication |
| 4 | Architecture| Medium | BackEnd For FrontEnd services are directly integrated with domain Data Access/data stores engines | To add an abstraction level to decrease the level of dependency on domain Data Access/Data stores engines |
| 5 | Architecture| Low | BackEnd For FrontEnd and Domain services are mixed | To move domain logic out of BackEnd For FrontEnd services|
| 6 | Architecture| Medium | Domain services are aware of client (browsers, devices)|	To move awareness of client away from domain services|
| 7 | Architecture| Medium | Domain services are stateful | To move state management away from domain services|
| 8 | DevOps| Medium | The code does not use the selected cloud model | To check Cloud Model being used|
|9  | DevOps | Medium | The architecture of solution uses the Cloud services it was not expected to use | To check Cloud Services being used |
|10 | DevOps | Medium | A microservice became strictly depending on an environment | To make that service be deployable on any environment |
|11 | Code | High | Technology standards changed - the developers started using the library or programming language that is out of scope.| To replace that library with allowed one |
|12 | Code | Low | A microservice accesses local FS and provides access to internal data | To add an abstraction level to decrease the level of dependency on internal data |

The graphic format is used to show the software architecture in the form of 
- holistic application architecture, 
- diagram of all services, 
- data flows etc. 

Offline and Online UML diagramming tools are used to save extracted Software Architecture.
Using graphic format users shall be able to tag any component, an item from inventory by any user-defined key words.

An example of graphic output might be following

<img src="./DAGBusinessContext.png" alt="TBD" />

In the picture above four services and one database are defined in the software architecture.
From the output you can see the relationship between them and the direction of communication.

### Modifiability and extendibility
Because there is no limitation on the solution, scope defined above the solution itself shall be extensible enough to support adding new features such a new check or even a new level.
Because there might not be good software practices used on a project the default set of checks shall be used to verify target architecture.
In case of established architecture governance, a proposed solution user shall be provided a possibility for extension of the set of checks.
Because there are multiple Static Code tools like Coverity, SonarQube, etc. there is no sense to implement low-level checks like checking indentation, formatting etc.

### Configurability
The following configuration items can be supported:
- Solution mode (available for configuration at deployment stage);
- A path to read the architecture documents from offline UML design tools;
- An address of online UML design tool API to read and write the architecture documents;
- Source control management system configuration;
- The addresses of databases for observation the data layer;
- The integration with CI/CD tools like Jenkins or Bamboo;
- The report plugins configuration (format, storage etc)

# References
| # | Name                 | Source                | Release date           |  Author                 | Description   |
| - | ---------------------|---------------------- |----------------------- | ----------------------- |:-------------:|
