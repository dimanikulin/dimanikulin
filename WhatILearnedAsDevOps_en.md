<img src="https://img.shields.io/badge/Maintained%3F-yes-green.svg"/>

# Headline

What I Learned As a DevOps

# Table of contents

- [Tags](./WhatILearnedAsDevOps_en.md#tags)
- [Definitions, Acronyms, Abbreviations](./WhatILearnedAsDevOps_en.md#definitions-acronyms-abbreviations)
- [Overview](./WhatILearnedAsDevOps_en.md#overview)
- [References](./WhatILearnedAsDevOps_en.md#references)

# Tags

TBD

# Definitions, Acronyms, Abbreviations

| # | Abbreviation or Acronym | Definition     |
| - | ------------------------|:--------------:|
| 1 | [Qt](https://en.wikipedia.org/wiki/Qt_(software))|is a [widget toolkit](https://en.wikipedia.org/wiki/Widget_toolkit) for creating [graphical user interfaces](https://en.wikipedia.org/wiki/Graphical_user_interfaces) as well as [cross-platform applications](https://en.wikipedia.org/wiki/Cross-platform) that run on various software and hardware platforms such as [Linux](https://en.wikipedia.org/wiki/Linux), [Windows](https://en.wikipedia.org/wiki/Windows), [macOS](https://en.wikipedia.org/wiki/MacOS), [Android](https://en.wikipedia.org/wiki/Android_(operating_system)) or [embedded systems](https://en.wikipedia.org/wiki/Embedded_system) with little or no change in the underlying codebase while still being a native application with native capabilities and speed. |
| 2 | [Cpplint](https://github.com/google/styleguide/blob/gh-pages/cpplint/cpplint.py)|is a C++ static code analysis tool which looks for programming errors, helps enforcing a coding standard, sniffs for code smells and offers simple refactoring suggestions. |
| 3 | [Pylint](https://pypi.org/project/pylint/)| is a Python static code analysis tool which looks for programming errors, helps enforcing a coding standard, sniffs for code smells and offers simple refactoring suggestions.|

# Overview

TBD

---

To ignore some temporary files, build results, and files generated by popular Visual Studio add-ons I used [.gitignore](.gitignore) from [here](https://github.com/github/gitignore)
I extended it with dirs with images as I did not want to commit them because of big size, autogenerated by doxygen files and not ready for commit content

./build-scripts/bamboo-build-mdlint.sh test/ait/tests/safety/local_fault
./build-scripts/bamboo-build-mdlinter.py test/ait/tests/safety/local_fault

# Automated code checks

&nbsp;&nbsp;&nbsp;  Currently there are following automated checks to verify if the code meets code quality requirements:
- [Code QL](.github/workflows/codeqlanalysis.yml) Please see [[38]](./REFERENCES.md) TBD what for
- [code Checks](.github/workflows/codeChecks.yml) TBD what for
- [code factor](https://www.codefactor.io/repository/github/dimanikulin/fva/issues) TBD what for
TBD - to add a bage for each code check

Please notice the installation packages for Windows is built using Wix;
Once a release happened the current [documentation generated from the code](https://dimanikulin.github.io/fva/) appeared.

# unit tests

cmake_minimum_required(VERSION 3.10)
project(MyProject)

 Enable testing for the project
enable_testing()

 Add GoogleTest as a subdirectory. You need to have gtest in your project directory.
add_subdirectory(googletest)

 Add your source files here
add_executable(MyProject main.cpp)

 Link GoogleTest to your project
target_link_libraries(MyProject gtest gtest_main)

 Add your tests source files here
add_executable(MyProjectTests test_main.cpp)

 Link GoogleTest to your tests
target_link_libraries(MyProjectTests gtest gtest_main)

 Add the tests to CTest's test runner
add_test(NAME MyProjectTests COMMAND MyProjectTests)

It sets the minimum required version of CMake and the name of the project.
It enables testing for the project.
It adds GoogleTest as a subdirectory, so CMake can find the GoogleTest libraries.
It creates an executable for the project from the source files.
It links the GoogleTest libraries to the project.
It creates an executable for the tests from the test source files.
It links the GoogleTest libraries to the tests.
It adds the tests to CTest's test runner, so you can run the tests with the ctest command.

# Building the code

I use CMake to build the project on different platform CMakeLists.txt

cmake_minimum_required (VERSION 3.0)

if (WIN32)
    set(CMAKE_CXX_STANDARD_LIBRARIES "-static-libgcc -static-libstdc++ ${CMAKE_CXX_STANDARD_LIBRARIES}")
    set(CMAKE_EXE_LINKER_FLAGS "${CMAKE_EXE_LINKER_FLAGS} -Wl,-Bstatic,--whole-archive -lwinpthread -Wl,--no-whole-archive")
endif (WIN32)

project(fva)

add_subdirectory(FVACommonLib)
add_subdirectory(FVAConfigurator)
add_subdirectory(FVADataProcessor)
add_subdirectory(FVADescriptionEditor)
add_subdirectory(FVADictionaryEditor)
add_subdirectory(FVAFlowController)
add_subdirectory(FVAOrganizer)
add_subdirectory(FVAOrganizerWizard)
add_subdirectory(FVAPlayer)
add_subdirectory(FVAViewer)

&nbsp;&nbsp;&nbsp; There are 2 environments to build � CI (git hub) and local developer one.
[CMake](https://gitlab.kitware.com/cmake/community/-/wikis/Home) is used as a tool to control build process.
It is selected as cross-platform [tool](https://cmake.org/) available on all target platforms to build the package.
[This link](https://doc.qt.io/qt-5/cmake-get-started.html) was used to make a build of QT code with a help of [CMake](https://gitlab.kitware.com/cmake/community/-/wikis/Home).

# Building the code using GitHub

&nbsp;&nbsp;&nbsp; The tool installation, configuration and processing are automated and based on GitHub actions with [main.yml](https://github.com/dimanikulin/fva/blob/master/.github/workflows/main.yml)
All the steps are expected to be yml based only.
I used [[37]](FVADocMD/REFERENCES.md) to help me to set up the main GitHub action flow and [this link](https://github.com/jurplel/install-qt-action) to set up QT.
&nbsp;&nbsp;&nbsp; Once code change is pushed to GitHub, [main workflow](https://github.com/dimanikulin/fva/blob/master/.github/workflows/main.yml) is being executed and you will have new [Installation packages](https://github.com/dimanikulin/fva/releases) to use.
All steps to build a package are called on any push to master or TBD branch.
More details are located in comments and step names [here](https://github.com/dimanikulin/fva/blob/master/.github/workflows/main.yml).
TBD- explain how to install and cfg on github site

<https://forum.gitlab.com/t/help-regarding-googletest-and-how-to-integrate-it-with-the-ci-pipeline/46805>

<https://github.com/pothitos/gtest-demo-gitlab/blob/master/.gitmodules>

# Building the code locally

Still you can use [MS studio solution](https://github.com/dimanikulin/fva/blob/master/FVASW.sln) to build locally on Windows or [CMake](https://github.com/dimanikulin/fva/blob/master/CMakeLists.txt) to build locally on any Windows, Mac or Linux.

# Building the docs

&nbsp;&nbsp;&nbsp; To re-generate the docs you need to re-execute [documentation workflow](https://github.com/dimanikulin/fva/blob/master/.github/workflows/releaseDocs.yml) from workflow. As result you will have [this](./DoxyGeneratedDoc.pdf)

doxy.cfg

# Releasing code and docs

<img src="Images/FvaBuildingCode.png" alt="BuildingCode"/>

&nbsp;&nbsp;&nbsp; One more important point was a definition of [building and releasing the product and documentation](./BUILD_RELEASE.md)
Here you can find a description for:

- [Building the code](./BUILD_RELEASE.md#buildingthecode)
- [Building the code using GitHub](./BUILD_RELEASE.md#buildingthecodeusinggithub)
- [Building the code locally](./BUILD_RELEASE.md#buildingthecodelocally)
- [Building the docs](./BUILD_RELEASE.md#buildingthedocs)

Thus, I learned:

- how to build and release documentation using GitHub;
- how to release product using GitHub.

# Branch strategy

One more important point was a definition of [branch strategy](./BUILD_RELEASE.md#branchstrategy)
&nbsp;&nbsp;&nbsp; GitHub actions is used to implement the releasing of the product.
It is configured to call release flow to start the creation of release product artifacts on creation or update the release branch.
TBD - describe naming and flow for branches.
TBD - create picture.

# References

| # | Name                 | Source                | Release date           |  Author                 | Description   |
| - | ---------------------|---------------------- |----------------------- | ----------------------- |:-------------:|
| 1 | Using GitHub Actions with C++ and CMake | [Web](https://cristianadam.eu/20191222/using-github-actions-with-c-plus-plus-and-cmake/) | 22/12/2019| Cristian Adam |Providing a GitHub Actions configuration yaml file for C++ projects using CMake|
| 2 | Code scanning finds more vulnerabilities using machine learning|[Web](https://github.blog/2022-02-17-code-scanning-finds-vulnerabilities-using-machine-learning/)| 17/02/2022 | Tiferet Gazit, Alona Hlobina | |
| 3 | What I learned as an Application Architect |[GitHub](./WhatILearnedAsAppArchitect_en.md) | | | |
| 4 | What I learned as a Delivery Manager |[GitHub](./WhatILearnedAsDeliveryManager_en) | | | |
| 5 | What I learned as a Product Manager |[GitHub](./WhatILearnedAsProductManager_en.md) | | | |
| 6 | What I learned as a Software Developer |[GitHub](./WhatILearnedAsSoftwareDeveloper_en.md) | | | |
| 7 | What I learned as a Subject Matter Expert |[GitHub](./WhatILearnedAsSubjectMatterExpert_en.md) | | | |
| 8 | What I Learned As a Tester |[GitHub](./WhatILearnedAsTester_en.md) | | | |
| 9 | Why I decided to create my photo organizer? |[GitHub](./WhyCreatedPhotoOrganizer_en.md) | | | |
