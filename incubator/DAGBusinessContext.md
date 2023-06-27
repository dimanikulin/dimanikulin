# Headline
TBD

# Article description
TBD 

# Tags
TBD

# Definitions, Acronyms, Abbreviations
TBD

# Content
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

The graphic format is used to show the software architecture in the form of 
- holistic application architecture, 
- diagram of all services, 
- data flows etc. 

Offline and Online UML diagramming tools are used to save extracted Software Architecture.
Using graphic format users shall be able to tag any component, an item from inventory by any user-defined key words.


<img src="./Images/TBD.jpg" alt="TBD" />

# References
| # | Name                 | Source                | Release date           |  Author                 | Description   |
| - | ---------------------|---------------------- |----------------------- | ----------------------- |:-------------:|
