Selenium UI Automation Framework

This repository contains a UI automation framework built with Java, Selenium WebDriver, TestNG, and Maven.
It is designed to automate browser-based regression and sanity test cases for web applications using a maintainable Page Object Model structure.

The framework demonstrates practical QA automation skills including test execution, browser handling, reporting, reusable utilities, and scalable test organization.

Key Features
UI automation using Selenium WebDriver
Java-based automation framework
Test execution using TestNG
Maven-based build and dependency management
Page Object Model structure
Cross-browser execution support
Parallel test execution support through TestNG
Extent Reports integration
Allure reporting support
WebDriverManager for browser driver management
Logging support using Log4j
Healenium support for improved locator stability
Data-driven testing support through Apache POI
Tech Stack
Java
Selenium WebDriver
TestNG
Maven
WebDriverManager
Extent Reports
Allure Reports
Apache POI
Log4j
Healenium
Project Structure
Front-end-Automation/
│
├── src/
│   └── test/                  # Test classes, page objects, and utilities
│
├── pom.xml                    # Maven dependencies and build configuration
├── testng.xml                 # TestNG suite configuration
├── README.md
└── .gitignore
What This Framework Tests

This framework is suitable for automating:

Login functionality
CRM workflow validations
Form submission flows
UI regression test cases
Sanity test cases
Role-based UI behavior
End-to-end user journeys
Browser compatibility checks
Prerequisites

Before running the project, make sure the following are installed:

Java JDK 8 or above
Maven
Chrome browser
Git
IDE such as IntelliJ IDEA or Eclipse

Verify Java and Maven installation:

java -version
mvn -version
Installation

Clone the repository:

git clone <repository-url>
cd Front-end-Automation

Install Maven dependencies:

mvn clean install
Running Tests

Run the complete TestNG suite:

mvn test

Run tests using the testng.xml suite file:

mvn clean test

The framework uses testng.xml for suite-level execution and can be configured for parallel browser execution.

TestNG Suite

The testng.xml file controls test execution, browser parameters, test classes, and parallel execution settings.

Example configuration:

<suite name="UI Automation Suite" parallel="tests" thread-count="5">
    <test name="Regression Tests">
        <parameter name="browser" value="chrome"/>
        <classes>
            <class name="TestCases.CrmTest"/>
        </classes>
    </test>
</suite>
Reporting

The framework supports reporting through:

Extent Reports
Allure Reports
TestNG default reports

Generate Allure report:

mvn allure:report

Serve Allure report locally:

mvn allure:serve
Framework Highlights

This project demonstrates QA automation practices such as:

Clean test structure
Reusable page methods
Browser setup handling
TestNG suite management
Parallel execution readiness
Reporting integration
Logging and debugging support
Scalable UI automation architecture
QA Value

This project reflects practical frontend automation skills, including:

UI regression testing
Test case automation
Test suite execution
Defect detection through automated flows
Maintainable test design
Reporting and execution tracking
Framework-level automation understanding
Author

Muhammad Rayan Ahmad
QA Engineer | Automation Engineer
