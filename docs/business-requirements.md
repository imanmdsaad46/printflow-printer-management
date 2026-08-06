# Business Requirements Document

## Project Information

| Item | Details |
|---|---|
| Project Name | PrintFlow |
| Module | Printer Registration and Status Management |
| Document Type | Business Requirements Document |
| Version | 1.0 |
| Status | Draft |
| Author | Muhammad Nur Iman |

## 1. Purpose

This document defines the business requirements for the Printer Registration and Status Management modules within PrintFlow.

PrintFlow is a web-based printer management system designed to provide centralized printer registration, visibility and status monitoring.

## 2. Business Objectives

The system aims to:

- Centralize printer information within a single platform.
- Improve visibility of printer availability and operational status.
- Prevent duplicate or invalid printer registrations.
- Allow authorized users to manage printer information.
- Maintain a history of printer status changes.
- Support faster identification of printers requiring attention.

## 3. Stakeholders

| Stakeholder | Responsibility |
|---|---|
| System Administrator | Registers printers and manages printer information and status |
| Standard User | Views registered printers and their latest statuses |
| IT Support Team | Monitors printer conditions and investigates connectivity or operational issues |
| Business Owner | Defines business expectations and approves the solution |

## 4. Business Requirements

| ID | Business Requirement | Priority |
|---|---|---|
| BR-001 | The organization requires a centralized platform for registering and managing printers. | High |
| BR-002 | Every registered printer must be uniquely identifiable using its serial number. | High |
| BR-003 | The system must prevent duplicate network printer registrations using the same IP address. | High |
| BR-004 | Authorized administrators must be able to add and update printer information. | High |
| BR-005 | Users must be able to view the latest operational status of every registered printer. | High |
| BR-006 | The system must support Online, Offline, Busy, Maintenance and Error printer statuses. | High |
| BR-007 | The system must maintain a history of printer status changes for traceability. | Medium |
| BR-008 | Users must be able to locate printers using search and filtering capabilities. | Medium |
| BR-009 | The system must restrict printer-management operations based on the user’s assigned role. | High |
| BR-010 | The system must provide clear feedback when an operation succeeds or fails. | Medium |

## 5. Business Rules

| ID | Business Rule |
|---|---|
| RULE-001 | Every printer must have a unique serial number. |
| RULE-002 | Wi-Fi and Ethernet printers must have a valid IP address. |
| RULE-003 | Two Wi-Fi or Ethernet printers cannot share the same IP address. |
| RULE-004 | An IP address is optional for printers using a USB connection. |
| RULE-005 | A newly registered printer can have Online, Offline or Maintenance as its initial status. |
| RULE-006 | A printer in Maintenance status cannot transition directly to Busy. |
| RULE-007 | Every status change must record the previous status, new status, user and timestamp. |
| RULE-008 | Only administrators can register, update or delete printer records. |
| RULE-009 | Standard users have read-only access to printer information and status. |

## 6. Assumptions

- Users are authenticated before accessing the system.
- Each user has an assigned role.
- Printer information used in this project is fictional.
- Printer statuses are simulated and are not retrieved from physical devices.
- Network connectivity with physical printers is outside the current project scope.

## 7. Constraints

- The initial version will be developed as a web-based application.
- The project will not communicate directly with physical printers.
- Automatic status detection is not included in the first release.
- Mobile application testing is outside the initial scope.

## 8. Out of Scope

The following features are excluded from the current release:

- Actual print-job submission
- Physical printer discovery
- Automatic firmware installation
- Consumable-level monitoring
- Mobile application support
- Real-time printer communication
- Email or push notifications

## 9. Success Criteria

The module will be considered successful when:

- An administrator can register a printer using valid information.
- Duplicate serial numbers and network IP addresses are rejected.
- Users can view accurate printer information and status.
- Administrators can perform permitted status transitions.
- Invalid status transitions are prevented.
- Status changes are recorded for traceability.
- Standard users cannot modify printer records.