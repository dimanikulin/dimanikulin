# Headline
TBD

# Article description
TBD 

# Tags
TBD

# Definitions, Acronyms, Abbreviations
TBD

# Content
## Context view for standalone application

A context diagram (view) defines solution bounds and connection with third parties like external systems, users and data. 

As shown above on the context diagram there is an interaction between Users and Proposed Solution. 
Interactions shall be implemented using UI web interface. 

To get the input the solution interacts with Online and Offline UML tools using its API to get initial Software Architecture and to save extracted Software Architecture.

To get access to code, configuration and DB the interactions with the Version Control Systems and interaction with DB are used.

Finally, Report Storage is used to save the outputs extracted from Architecture under analysis. 

<img src="DAGProposedSolution1.png" alt="DAGProposedSolution.png" />

## Context view for separate step in CI/CD

The only difference between previous view and Context View for Separate step in CI/CD is integration of the proposed solution with existing CI/CD pipeline.

<img src="DAGProposedSolution2.png" alt="DAGProposedSolution.png" />

## Functional view

A functional diagram below shows the high-level function decomposition of the proposed solution.
An agenda below explains the coloring for functional decomposition diagram.

<img src="DAGProposedSolution3.png" alt="DAGProposedSolution.png" />

### Integration layer
The integration layer function is to abstract and segregate the system from external components to improve the system extensibility and modifiability.

Following are the components:
- Online UML tools integration point - component to integrate Online UML tools with Processor;
- Offline  UML tools integration point - component to integrate Offline UML tools with Processor;
- VSC integration point - component to integrate Version Control Systems with Processor;
- Databases integration point - component to integrate databases configuration with Processor;
- CI/CD integration point - component to integrate CI/CD tools (like Jenkins, Bamboo) with Processor;
- The Reports plugins - an engine to generate reports in a flexible way and to save them on external report storage.

### User Interface
The user interface function interacts with the user in two modes: architects and administrator mode. 
It is based on a web interface that supports desktop browsers. 

### Data layer
The data layer function keeps following types of data:
- Architecture baselines - it is a history of Architecture changes so users can see at any time which Architecture change took place, available for a view from the architects panel;
- System configuration - it is a set of check configurations for processing, it also keeps track of reports plugins configuration, available for a change from the architects panel;
- User configuration - user profiles and access rights, available for a change from administrator panel.

### Processing layer
The processing layer is a core function of systems to process the input to find architecture problems. 
It is configured from the architect panel to run the checks against input. 
It interacts with the reports plugins engine to store the reports. 
It also saves the extracted architecture to Architecture baselines so the architects can review it later. 
To improve the quality of reports, Machine Learning (ML) during processing might be used. ML and its interaction is described in this document later.  

## Deployment view

The deployment schemes show how a solution shall be deployed with its flows and supporting components.

## Deployment view - on premise

<img src="DAGProposedSolution4.png" alt="DAGProposedSolution.png" />

On premise, deployment assumes only one computing node for installation. 
The Data Base component shall be deployed first as other components depend on it.
Then, the Processor and ML component are being deployed after the Database component is in place.
The User interface component, reports plugins and integration points are deployed at the last stage. 
The Data Base component shall be deployed in the form of one DB instance with several schemes inside.
User interface component is represented as a web service.
Processor and ML are native processes built for the target platform.
Reports plugins and integration points shall be represented as dynamic libraries that can be easily added, removed and configured at run time.

<img src="DAGProposedSolution5.png" alt="DAGProposedSolution.png" />

On premise, deployment assumes two computing nodes for installation.
Because the Machine Learning process can utilize the CPU time a lot, it is suggested to have a separate machine for Machine Learning process for cloud pipeline.

# References
| # | Name                 | Source                | Release date           |  Author                 | Description   |
| - | ---------------------|---------------------- |----------------------- | ----------------------- |:-------------:|
