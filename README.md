# PrintFlow – Printer Registration and Status Management

PrintFlow is project that demonstrates the testing of a web-based printer management system.

The project focuses on requirements analysis, test design, manual testing, API validation, database validation and Playwright automation.

> Project Status: Requirements and test design in progress.

## Project Overview

PrintFlow allows authorized users to register printers, manage printer information and monitor operational statuses through a centralized system.

The project is inspired by real-world printer testing workflows. All product names, requirements and test data used in this repository are fictional and created exclusively for portfolio purposes.

## Project Objectives

- Analyse business and functional requirements
- Design risk-based test scenarios and test cases
- Validate printer registration and status-management workflows
- Perform positive, negative and boundary testing
- Validate application data through APIs and SQL queries
- Automate critical workflows using Playwright
- Execute automated tests through GitHub Actions

## Features Under Test

### Printer Registration

- Register a new printer
- Validate mandatory fields
- Validate IP address format
- Prevent duplicate serial numbers
- Prevent duplicate IP addresses
- Apply connection-specific validation
- Display successful and unsuccessful registration messages

### Printer Status Management

- Display the latest printer status
- Update printer status
- Validate permitted status transitions
- Prevent invalid status transitions
- Record printer status history
- Search and filter printers

## Printer Statuses

| Status | Description |
|---|---|
| Online | Printer is available for use |
| Offline | Printer cannot be reached |
| Busy | Printer is currently processing a job |
| Maintenance | Printer is temporarily unavailable due to maintenance |
| Error | Printer requires user or administrator attention |

## Testing Scope

The project will cover:

- Requirement analysis
- Functional testing
- Negative testing
- Boundary-value testing
- Integration testing
- API testing
- Database validation
- UI automation
- Regression testing

## Tools and Technologies

| Area | Tools |
|---|---|
| Test documentation | Microsoft Excel / Markdown |
| Defect management | Jira-style defect reports |
| API testing | Postman |
| Database testing | MySQL |
| UI automation | Playwright with Python |
| Version control | Git and GitHub |
| Continuous integration | GitHub Actions |

## Repository Structure

```text
printflow-printer-management-qa/
├── docs/
│   ├── project-overview.md
│   ├── business-requirements.md
│   └── functional-requirements.md
├── manual-testing/
│   ├── test-plan/
│   ├── test-scenarios/
│   ├── test-cases/
│   ├── traceability-matrix/
│   ├── defect-reports/
│   └── test-summary/
├── api-testing/
├── database-testing/
├── playwright-tests/
└── evidence/




Kemudian dekat bawah:

- **Commit message:** `Add project overview to README`
- Pilih **Commit directly to the main branch**
- Klik **Commit changes**

README ini sengaja menggunakan ayat seperti `will cover` dan checklist belum selesai supaya kita tak mendakwa API, SQL atau automation sudah siap. Selepas commit, langkah seterusnya ialah masukkan dokumen **Business Requirements** dan **Functional Requirements** ke folder `docs`.