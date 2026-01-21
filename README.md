# Evershop QA Project: Manual Testing & API Automation

## 1. Project Overview
This repository contains the complete Quality Assurance (QA) documentation for the **Evershop E-Commerce Application**. The project follows a structured testing lifecycle, moving from Test Planning and Manual Execution to Defect Logging and API Automation.

**Author**: TheSourav-001
**Application**: Evershop (E-Commerce Platform)
**Testing Methodology**: Hybrid (Manual Functional Testing + API Automation)

## 2. Repository Content & Analysis

The repository is structured into four specific modules based on the project workflow.

### Module 01: Test Planning
**File**: `Question 01/Question 01.docx`
* **Description**: This document establishes the Test Strategy for the **Search Functionality**.
* **Key Contents**:
    * **In-Scope**: Search Bar, Search Results Page, Filter/Sorting options.
    * **Out-of-Scope**: Payment processing and Shipping modules.
    * **Test Scenarios**: Detailed positive and negative scenarios (e.g., Valid Keywords, Invalid Characters, SQL Injection inputs).

### Module 02: Manual Test Execution (Search Module)
**File**: `Question 2 (TestCase and Execution).xlsx`
* **Description**: Contains the execution logs for the Search Bar functional tests.
* **Execution Metrics**:
    * **Test Columns**: Test Case ID, Scenario, Pre-condition, Steps, Test Data, Expected vs. Actual Result, Status.
    * **Scenarios Validated**:
        * Exact match search (Product Name).
        * Partial match search.
        * Case sensitivity checks.
        * Empty search queries.

**File**: `Bug List of Search.xlsx`
* **Description**: A dedicated defect log for issues found specifically within the Search module.
* **Defect Details**:
    * Tracks Bug ID, Severity, Priority, and Status.
    * Includes steps to reproduce issues where search results did not match specific keywords.

### Module 03: Integrated UI & API Testing
**File**: `UI & API TestCase and defect log.xlsx`
This master Excel file is divided into three critical sheets:
1.  **UI TEST CASES**: Validates frontend elements (Alignment, Font correctness, Button visibility on Homepage/Search Page).
2.  **API TEST CASES**: Validates backend endpoints for response codes (200 OK, 404 Not Found) and response time benchmarks.
3.  **DEFECT LOG**: A consolidated list of all UI and API defects identified during the integration phase.

**File**: `Test Analysis Feedback.docx`
* **Description**: A qualitative report summarizing the application's stability. It highlights critical functional risks and provides recommendations for regression testing.

### Module 04: API Automation
**File**: `EVERSHOP.postman_collection.json`
* **Tool**: Postman
* **Description**: An automated test suite covering core backend functionalities.
* **Covered Endpoints**:
    * **Auth**: User Login (`POST /login`) and Registration.
    * **Products**: Fetch Product Details (`GET /product/{id}`).
    * **Cart**: Add Items to Cart (`POST /cart`), Remove Items (`DELETE /cart`).
* **Automation Features**:
    * Includes test scripts to validate JSON structure.
    * Includes assertions for HTTP Status Codes (200, 201, 400).

## 3. Defect Summary & Key Findings
Based on the analysis of `UI & API TestCase and defect log.xlsx`, the following issues were highlighted:

* **Search Relevance**: The search engine occasionally returns unrelated products for broad keywords.
* **UI Alignment**: Product grid misalignment observed on the Search Results page.
* **API Error Handling**: Specific invalid inputs to the Login API return generic 500 Server Errors instead of specific 400 Bad Request messages.

## 4. How to Execute

### Manual Tests
1.  Open `Question 2 (TestCase and Execution).xlsx` in Microsoft Excel.
2.  Review the "Status" column to identify Failed test cases.
3.  Refer to `Bug List of Search.xlsx` for detailed reproduction steps.

### Automated API Tests
1.  Install **Postman**.
2.  Import `EVERSHOP.postman_collection.json`.
3.  Run the collection using the **Collection Runner**.
4.  Analyze the Run Summary for Pass/Fail percentages.

---
**Verified by**: TheSourav-001
