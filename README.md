# Front-end Automation

Selenium UI Automation Framework using **Java**, **Selenium WebDriver**, **TestNG**, **Maven**, **Page Object Model**, **Allure Reports**, and **Extent Reports**.

This repository demonstrates a maintainable UI automation framework for validating web application workflows through automated browser testing. It is structured for sanity, regression, and workflow-based test execution with reusable test classes, TestNG suite control, reporting support, and Maven-based dependency management.

---

## Table of Contents

- [About the Project](#about-the-project)
- [Key Features](#key-features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Running Tests](#running-tests)
- [Test Suite Configuration](#test-suite-configuration)
- [Reports](#reports)
- [QA Skills Demonstrated](#qa-skills-demonstrated)
- [Repository Links](#repository-links)
- [Author](#author)

---

## About the Project

This project is a front-end/UI automation framework created for browser-based testing of web application workflows.

The framework is designed to cover important UI flows such as:

- Login functionality
- CRM workflow validation
- Sanity test execution
- Regression test execution
- Browser-based end-to-end user journey validation
- UI form and navigation checks
- Workflow-level functional testing

The project uses **TestNG** for test execution and suite management, **Maven** for dependency management, and **Selenium WebDriver** for browser automation.

---

## Key Features

- Selenium WebDriver-based UI automation
- Java and Maven-based framework structure
- TestNG test suite execution
- Page Object Model-friendly structure
- Browser parameterization through `testng.xml`
- Parallel execution configuration support
- Data-driven testing support using Excel files
- WebDriverManager integration for browser driver handling
- Extent Reports support for HTML reporting
- Allure Reports support for test reporting
- Log4j and SLF4J support for logging
- Healenium integration support for improving locator stability
- Organized test cases for CRM, BRM, WOM, PCC, and login workflows

---

## Tech Stack

| Category | Tools / Technologies |
|---|---|
| Programming Language | Java |
| Automation Tool | Selenium WebDriver |
| Test Runner | TestNG |
| Build Tool | Maven |
| Reporting | Allure Reports, Extent Reports |
| Driver Management | WebDriverManager |
| Logging | Log4j, SLF4J |
| Test Data | Apache POI, Excel |
| Locator Stability | Healenium |

---

## Project Structure

```text
Front-end-Automation/
│
├── src/
│   └── test/
│       ├── java/
│       │   └── TestCases/
│       │       ├── BrmTest.java
│       │       ├── CrmTest.java
│       │       ├── CrmUiTest.java
│       │       ├── LoginAllTest.java
│       │       ├── PccTest.java
│       │       └── WomTest.java
│       │
│       └── resources/
│           └── test.xlsx
│
├── testng.xml
├── pom.xml
├── .gitignore
└── README.md
```

---

## Prerequisites

Before running this project, make sure the following are installed:

- Java JDK 8 or above
- Maven
- Git
- Google Chrome browser
- IntelliJ IDEA, Eclipse, or any Java-supported IDE

Check Java installation:

```bash
java -version
```

Check Maven installation:

```bash
mvn -version
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/RayanAhmad138/Front-end-Automation.git
```

Move into the project directory:

```bash
cd Front-end-Automation
```

Install Maven dependencies:

```bash
mvn clean install
```

---

## Running Tests

Run the full TestNG suite using Maven:

```bash
mvn clean test
```

Run tests directly from the TestNG suite file:

```bash
mvn test
```

The Maven Surefire plugin is configured to execute tests using the `testng.xml` suite file.

---

## Test Suite Configuration

Test execution is controlled through the `testng.xml` file.

Example configuration:

```xml
<!DOCTYPE suite SYSTEM "https://testng.org/testng-1.0.dtd">

<suite name="TAL One Sanity Suite" verbose="1" parallel="tests" thread-count="5">
    <test name="Login Functionality Tests" parallel="classes">
        <parameter name="browser" value="chrome"/>
        <classes>
            <class name="TestCases.CrmTest"/>
        </classes>
    </test>
</suite>
```

The suite can be updated to include or exclude test classes based on the required execution scope.

Available test classes include:

- `LoginAllTest`
- `CrmTest`
- `CrmUiTest`
- `BrmTest`
- `WomTest`
- `PccTest`

---

## Reports

This framework supports multiple reporting options.

### TestNG Reports

After execution, TestNG default reports are generated under:

```text
target/surefire-reports/
```

### Allure Reports

Generate Allure report:

```bash
mvn allure:report
```

Serve Allure report locally:

```bash
mvn allure:serve
```

### Extent Reports

Extent Reports support is included in the project dependencies and can be used for detailed HTML execution reporting.

---

## Test Data

The framework includes Excel-based test data support through Apache POI.

Test data file:

```text
src/test/resources/test.xlsx
```

This can be used for data-driven test execution where multiple input combinations are required.

---

## QA Skills Demonstrated

This repository demonstrates practical QA automation skills including:

- UI automation framework setup
- Selenium WebDriver test development
- TestNG suite management
- Maven dependency management
- Browser-based functional testing
- Sanity and regression test execution
- Data-driven testing using Excel
- Parallel execution configuration
- Reporting integration
- Logging and debugging support
- Maintainable test organization

---

## Repository Links

- GitHub Repository: `https://github.com/RayanAhmad138/Front-end-Automation`
- Backend Automation Repository: `https://github.com/RayanAhmad138/Backend-Automation`

---

## Author

**Muhammad Rayan Ahmad**  
QA Engineer | Automation Engineer

---

## Project Status

This project is maintained as a QA automation portfolio project and demonstrates front-end automation framework design, test execution, reporting, and practical workflow validation.
