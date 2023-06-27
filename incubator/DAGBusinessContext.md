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

### Solution modes

<img src="./Images/TBD.jpg" alt="TBD" />

# References
| # | Name                 | Source                | Release date           |  Author                 | Description   |
| - | ---------------------|---------------------- |----------------------- | ----------------------- |:-------------:|
