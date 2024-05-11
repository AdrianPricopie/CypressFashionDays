# Automated Testing Project for FashionDays Website :computer:
Welcome to the documentation for the automated testing project designed for the FashionDays website. This project leverages Cypress  implement a robust suite of tests, ensuring the functionality and reliability.
## Table of Contents

1. [Introduction/Tools and version](#introduction-notebook)
2. [Project Structure](#project-structure)
3. [Test Scenario](#test-scenarios-for-login-functionality)
4. [Getting-Started](#getting-started--pushpin)
7. [Reports](#reports)
8. [Conclusion](#conclusion)

# Introduction :notebook:
 
This project aims to implement automated tests for the FashionDays opensource website using Cypress.
The primary objectives include simulating user interactions on  several functionalities ,such as : main page , wishlist ,cart ,filter product ,search,login and register.

- Language:**JavaScript**
- Editor code:**VsCode**
- Library:
  - [![Cypress](https://img.shields.io/npm/v/cypress?color=33ff99&label=cypress&logo=cypress&logoColor=33ff99&style=for-the-badge)](https://www.cypress.io)
  - cypress-mochawesome-reporter 3.8.2
  -[cypress-mailosaur](https://mailosaur.com/)

**FashionDays** is a platform tailored for the fashion industry, offering a suite of tools for efficiently managing clothing and accessory businesses. 
It enables easy product catalog management, inventory control, online store integration, and customer relationship management. 
The platform also includes order processing, data analytics, and extensive support to aid growing businesses. 
Available in both cloud and on-premise options, FashionDays is the ideal solution for fashion brands and retailers.


- [Website](https://www.fashiondays.ro/)

# Project Structure 

- **cypress/**: This is the main directory of the Cypress project.
- **cypress/fixtures/**: Static test data, such as JSON files, is stored here.
- **cypress/integration/**: All spec files for tests are stored here. Inside this directory, each subdirectory corresponds to a specific testing module.
- **cypress/PageObject/**: This directory is typically used to store Page Object Model (POM) files. Page objects represent the pages of FashionDays application and encapsulate their functionality, making tests more modular and easier to maintain.
- **cypress/Utils/**: This directory contain utility files or helper functions that are used across tests. These utilities include functions for interacting with elements on the page and performes common actions in tests.
- **cypress/support/**: Custom Cypress commands and other support files are defined here.
- **cypress/integration/Tests/**: All the tests are stored here.
- **cypress/reports/**: This directory is where Cypress generates test reports.

- Advantages: Utilizing POM brings several benefits, including:
  - **Reusability**: POM methods can be reused across different tests without the need to rewrite code.
  - **Easy maintenance**: A change in a page requires updating only the corresponding POM file, without affecting other tests.
  - **Clarity and organization**: POM separates logically the elements from the specific actions of the page, making the code more understandable and maintainable.

## Getting Started  :pushpin:

1.**Prerequisites:**

Make sure you have installed the following prerequisites on your development machine:

| OS      | Node                                    |
| ------- | --------------------------------------- |
| Windows | `winget install --id OpenJS.NodeJS.LTS` |
|         | ` npm i --save-dev cypress-mochawesome-reporter`        |
| macOS   | `brew install node@20`    
|         | ` npm i --save-dev cypress-mochawesome-reporter`        |


2. **Clone the Repository:**

    ```bash
    git clone https://github.com/RobertFurtuna10/CypressFashionDays.git
    ```

4. **Run all the tests with html report:**

    ```bash
    npm tests run
    ```
5. **Run all the tests with html report in headed mode:**

    ```bash
    npm HeadTests run
    ```
# Report 

This report outlines the testing conducted on 11 May 2024 and documents all the functionalities that have been thoroughly tested. The report comprises 29 tests, all of which have successfully passed within a total time of 1 minute and 33 sec.

![TestsReport](https://github.com/AdrianPricopie/CypressFashionDays/blob/main/ScreenshotsForGit/Report11May.png)
![TestsReport](https://github.com/AdrianPricopie/CypressFashionDays/blob/main/ScreenshotsForGit/Screenshot%202024-05-11%20at%2018.12.53.png)
![TestsReport](https://github.com/AdrianPricopie/CypressFashionDays/blob/main/ScreenshotsForGit/Screenshot%202024-05-11%20at%2018.12.59.png)

# Conclusion

- **Test Coverage/**: The test suite covers various aspects of the FashionDays website, including the main page functionalities, search functionality, filtering options, adding/removing products from the cart and wishlist, navigating between search result pages, and verifying URLs.
- **Positive Scenarios/**: The tests verify positive scenarios such as checking if elements are visible on the main page, ensuring correct URLs, filtering products by brand, color, and price, adding products to the cart and wishlist, and checking if search results return the expected products.
- **Negative Scenarios/**: Negative scenarios are also covered, such as searching for non-existent products and verifying appropriate error messages, removing products from the cart and wishlist, and ensuring the wishlist is empty after removal.
- **Assertions and Verifications/**: The test suite includes various assertions and verifications to ensure that the website behaves as expected. These include checking text content, verifying URLs, comparing product prices, and confirming the presence of specific elements.
- **Modularization and Reusability/**: The test suite demonstrates good practices by modularizing the code, using fixtures for test data, and creating custom commands like SearchProduct and VerifyIncludesInUrl, which enhance reusability and maintainability.
- **UI Interactions/**: Tests involve interactions with UI elements such as clicking buttons, searching for products, selecting filters, and verifying visual changes based on user actions.
- **Data-Driven Testing/**: The test suite uses data-driven testing by fetching test data from fixtures, which allows for easy parameterization and scalability of tests.
- **Reporting/**: While there's no explicit mention of reporting in the provided code, integrating a reporting mechanism such as mochawesome could enhance test visibility and provide detailed HTML reports for better analysis.

Overall, the test suite appears comprehensive, covering a wide range of functionalities and scenarios, and employing best practices for automated testing. Further enhancements could include adding more assertions for edge cases, implementing test retries for flaky tests, and integrating with continuous integration tools for automated test execution.

