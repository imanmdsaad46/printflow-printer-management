# Functional Requirements Document

## Project Information

| Item | Details |
|---|---|
| Project Name | PrintFlow |
| Module | Printer Registration and Status Management |
| Document Type | Functional Requirements Document |
| Version | 1.0 |
| Status | Draft |
| Prepared By | Muhammad Nur Iman |

## 1. Purpose

This document defines the functional requirements for the Printer Registration and Status Management modules within PrintFlow.

The requirements describe the expected system behaviour, user interactions, validation rules and access controls that will be used as the basis for test design and execution.

## 2. User Roles

| Role | Permissions |
|---|---|
| Administrator | View, register, update and delete printers; update printer statuses |
| Standard User | View, search and filter registered printers |

## 3. Printer Registration Requirements

| ID | Functional Requirement | Priority | Related Business Requirement |
|---|---|---|---|
| FR-001 | The system shall allow an Administrator to access the printer registration form. | High | BR-004, BR-009 |
| FR-002 | The system shall provide fields for Printer Name, Model, Serial Number, IP Address, Connection Type, Location, Firmware Version and Initial Status. | High | BR-001 |
| FR-003 | Printer Name, Model, Serial Number, Connection Type, Firmware Version and Initial Status shall be mandatory. | High | BR-001, BR-002 |
| FR-004 | The Connection Type field shall provide Wi-Fi, Ethernet and USB options. | High | BR-001 |
| FR-005 | The Initial Status field shall provide Online, Offline and Maintenance options. | High | BR-005, BR-006 |
| FR-006 | The system shall require an IP address when Wi-Fi or Ethernet is selected. | High | BR-003 |
| FR-007 | The system shall allow the IP Address field to remain empty when USB is selected. | Medium | BR-003 |
| FR-008 | The system shall validate that the entered IP address follows the IPv4 format. | High | BR-003 |
| FR-009 | The system shall reject a serial number that is already assigned to another printer. | High | BR-002 |
| FR-010 | The system shall reject an IP address that is already assigned to another Wi-Fi or Ethernet printer. | High | BR-003 |
| FR-011 | The system shall display a validation message for every invalid or missing required field. | High | BR-010 |
| FR-012 | The system shall register the printer when all submitted information is valid. | High | BR-001, BR-004 |
| FR-013 | The system shall display a success message after successful printer registration. | Medium | BR-010 |
| FR-014 | The newly registered printer shall appear in the printer list. | High | BR-001, BR-005 |

## 4. Printer Information Management Requirements

| ID | Functional Requirement | Priority | Related Business Requirement |
|---|---|---|---|
| FR-015 | The system shall display all registered printers in a printer list. | High | BR-001, BR-005 |
| FR-016 | The printer list shall display Printer Name, Model, Serial Number, IP Address, Connection Type and Status. | High | BR-005 |
| FR-017 | The system shall allow an Administrator to update existing printer information. | High | BR-004, BR-009 |
| FR-018 | The system shall apply the registration validation rules when printer information is updated. | High | BR-002, BR-003 |
| FR-019 | The system shall allow an Administrator to delete a printer record after confirmation. | Medium | BR-004, BR-009 |
| FR-020 | The system shall display a confirmation prompt before deleting a printer. | Medium | BR-010 |
| FR-021 | The system shall prevent a Standard User from registering, updating or deleting printers. | High | BR-009 |

## 5. Printer Status Management Requirements

| ID | Functional Requirement | Priority | Related Business Requirement |
|---|---|---|---|
| FR-022 | The system shall display the latest status of every registered printer. | High | BR-005 |
| FR-023 | The system shall allow an Administrator to update a printer status. | High | BR-004, BR-006 |
| FR-024 | The available statuses shall be Online, Offline, Busy, Maintenance and Error. | High | BR-006 |
| FR-025 | A printer in Maintenance status shall not be changed directly to Busy. | High | BR-006 |
| FR-026 | The system shall display an error message when an invalid status transition is attempted. | High | BR-006, BR-010 |
| FR-027 | The updated status shall be displayed immediately after a successful status change. | High | BR-005 |
| FR-028 | The system shall record the previous status, new status, user and timestamp for every successful status change. | High | BR-007 |
| FR-029 | The system shall allow users to view the status-change history of a printer. | Medium | BR-007 |
| FR-030 | The system shall prevent a Standard User from changing printer statuses. | High | BR-009 |

## 6. Search and Filter Requirements

| ID | Functional Requirement | Priority | Related Business Requirement |
|---|---|---|---|
| FR-031 | The system shall allow users to search by Printer Name, Model, Serial Number or IP Address. | Medium | BR-008 |
| FR-032 | The search result shall display printers matching the entered search value. | Medium | BR-008 |
| FR-033 | The system shall display an appropriate message when no matching printer is found. | Medium | BR-008, BR-010 |
| FR-034 | The system shall allow users to filter printers by Status. | Medium | BR-008 |
| FR-035 | The system shall allow users to filter printers by Connection Type. | Medium | BR-008 |
| FR-036 | The system shall allow users to clear the applied search and filters. | Low | BR-008 |

## 7. General Requirements

| ID | Functional Requirement | Priority | Related Business Requirement |
|---|---|---|---|
| FR-037 | The system shall display a clear message after every successful or unsuccessful operation. | Medium | BR-010 |
| FR-038 | The system shall preserve submitted valid values when validation fails for another field. | Medium | BR-010 |
| FR-039 | The system shall prevent unauthorized users from directly accessing restricted management pages. | High | BR-009 |
| FR-040 | The system shall display the date and time using a consistent format throughout the module. | Low | BR-007 |