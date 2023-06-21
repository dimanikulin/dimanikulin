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


# References
| # | Name                 | Source                | Release date           |  Author                 | Description   |
| - | ---------------------|---------------------- |----------------------- | ----------------------- |:-------------:|
