# Printer Registration and Status Management Test Plan

## Document Information

| Item | Details |
|---|---|
| Project Name | PrintFlow |
| Module | Printer Registration and Status Management |
| Document Type | Test Plan |
| Version | 1.0 |
| Status | Draft |
| Prepared By | Muhammad Nur Iman |

## 1. Introduction

This test plan defines the testing approach for the Printer Registration and Status Management modules within PrintFlow.

The purpose of testing is to verify that authorized users can register and manage printers, view accurate printer statuses and perform permitted status transitions according to the defined business and functional requirements.

## 2. Test Objectives

The testing objectives are to:

- Verify successful printer registration using valid data.
- Validate mandatory fields and input formats.
- Prevent duplicate serial numbers and network IP addresses.
- Verify connection-specific registration rules.
- Validate printer status-management workflows.
- Prevent invalid printer status transitions.
- Verify role-based access restrictions.
- Validate printer search and filtering.
- Verify status-history records.
- Confirm that appropriate success and error messages are displayed.

## 3. In Scope

The following features are included:

- Printer registration
- Printer information validation
- Duplicate printer validation
- Printer information display
- Printer information updates
- Printer deletion
- Printer status updates
- Status-transition validation
- Printer status history
- Role-based access
- Printer search
- Printer filtering

## 4. Out of Scope

The following features are excluded:

- Communication with physical printers
- Automatic printer discovery
- Actual print-job submission
- Automatic printer-status detection
- Firmware installation
- Consumable-level monitoring
- Mobile application testing
- Performance and load testing
- Email and push notifications

## 5. Test Approach

Testing will be performed using a risk-based approach. High-priority business workflows and validation rules will receive the greatest coverage.

The following testing types will be performed:

| Test Type | Description |
|---|---|
| Functional Testing | Verify that each feature behaves according to its functional requirements |
| Positive Testing | Verify successful operations using valid inputs |
| Negative Testing | Verify system behaviour using invalid or incomplete inputs |
| Boundary-Value Testing | Validate input values at and around defined limits |
| Integration Testing | Verify data consistency between registration, printer list and status history |
| Authorization Testing | Verify access restrictions for Administrator and Standard User roles |
| Regression Testing | Re-execute critical tests after application changes |

## 6. Test Environment

| Component | Configuration |
|---|---|
| Application Type | Web application |
| Operating System | Windows 11 |
| Browser | Google Chrome and Microsoft Edge |
| Database | MySQL |
| API Testing Tool | Postman |
| Automation Tool | Playwright with Python |
| Version Control | Git and GitHub |

The exact browser and tool versions will be recorded during test execution.

## 7. Test Data

Testing will use fictional printer information.

Example:

| Field | Test Data |
|---|---|
| Printer Name | Finance Room Printer |
| Model | NovaJet X100 MFP |
| Serial Number | NJX100-00001 |
| IP Address | 192.168.10.25 |
| Connection Type | Ethernet |
| Location | Finance Department |
| Firmware Version | 2.1.0 |
| Initial Status | Online |

Test data will include:

- Valid printer information
- Missing mandatory values
- Duplicate serial numbers
- Duplicate IP addresses
- Valid and invalid IPv4 addresses
- Wi-Fi, Ethernet and USB connection types
- Valid and invalid status transitions
- Administrator and Standard User accounts

## 8. Entry Criteria

Testing can begin when:

- Business requirements are documented.
- Functional requirements are documented.
- Test scenarios are reviewed.
- The test environment is accessible.
- Required user accounts are available.
- The application build is available for testing.

## 9. Exit Criteria

Testing can be completed when:

- All planned test cases have been executed.
- All critical and high-priority test cases have passed.
- No unresolved Critical or High-severity defects remain.
- Medium and Low-severity defects are documented and accepted.
- Regression testing has been completed.
- The test execution summary has been prepared.

## 10. Suspension and Resumption Criteria

Testing may be suspended when:

- The application is unavailable.
- A blocking defect prevents further execution.
- The test environment is unstable.
- Required test data or user access is unavailable.

Testing may resume after the blocking condition has been resolved and the affected functionality has been verified.

## 11. Defect Management

Defects will be documented with:

- Defect ID
- Summary
- Environment
- Preconditions
- Steps to reproduce
- Actual result
- Expected result
- Severity
- Priority
- Reproducibility
- Supporting evidence
- Current status

## 12. Risks and Mitigation

| Risk | Impact | Mitigation |
|---|---|---|
| Application is not yet available | Test execution cannot begin | Complete requirement analysis and test design using specifications |
| Requirements change during development | Existing test cases may become outdated | Maintain requirement traceability and review affected test cases |
| Limited role-based test accounts | Authorization coverage may be incomplete | Prepare Administrator and Standard User test accounts |
| Shared test data causes duplicate records | Test execution may produce inconsistent results | Use unique and reusable test-data conventions |
| Browser-specific behaviour | Defects may only occur in certain browsers | Execute critical workflows in Chrome and Edge |

## 13. Deliverables

The following testing deliverables will be produced:

- Business Requirements Document
- Functional Requirements Document
- Test Plan
- Test Scenarios
- Detailed Test Cases
- Requirements Traceability Matrix
- Defect Reports
- Test Evidence
- Test Execution Summary
- Postman API Collection
- SQL Validation Queries
- Playwright Automated Tests

## 14. Roles and Responsibilities

| Role | Responsibility |
|---|---|
| Project Owner | Defines the portfolio project scope and requirements |
| QA Engineer | Designs, executes and maintains all testing deliverables |
| Developer | Implements application features and resolves defects |

For this independent portfolio project, the project owner, QA and development activities may be performed by the same individual.