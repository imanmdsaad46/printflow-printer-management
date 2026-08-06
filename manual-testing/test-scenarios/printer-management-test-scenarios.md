# Printer Registration and Status Management Test Scenarios

## Document Information

| Item | Details |
|---|---|
| Project Name | PrintFlow |
| Module | Printer Registration and Status Management |
| Document Type | Test Scenarios |
| Version | 1.0 |
| Status | Draft |
| Prepared By | Muhammad Nur Iman |

## Test Scenarios

| Scenario ID | Module | Test Scenario | Test Type | Priority | Requirement Reference |
|---|---|---|---|---|---|
| TS-REG-001 | Printer Registration | Verify that an Administrator can access the printer registration form. | Functional | High | FR-001 |
| TS-REG-002 | Printer Registration | Verify that all required printer registration fields are displayed. | Functional | High | FR-002 |
| TS-REG-003 | Printer Registration | Verify successful registration using valid Wi-Fi printer information. | Positive | High | FR-003, FR-006, FR-012 |
| TS-REG-004 | Printer Registration | Verify successful registration using valid Ethernet printer information. | Positive | High | FR-003, FR-006, FR-012 |
| TS-REG-005 | Printer Registration | Verify successful registration of a USB printer without an IP address. | Positive | High | FR-007, FR-012 |
| TS-REG-006 | Printer Registration | Verify required-field validation when mandatory information is missing. | Negative | High | FR-003, FR-011 |
| TS-REG-007 | Printer Registration | Verify IP address is required for a Wi-Fi printer. | Negative | High | FR-006 |
| TS-REG-008 | Printer Registration | Verify IP address is required for an Ethernet printer. | Negative | High | FR-006 |
| TS-REG-009 | Printer Registration | Verify validation of an incorrectly formatted IPv4 address. | Negative | High | FR-008 |
| TS-REG-010 | Printer Registration | Verify registration is rejected when a duplicate serial number is submitted. | Negative | High | FR-009 |
| TS-REG-011 | Printer Registration | Verify registration is rejected when a duplicate network IP address is submitted. | Negative | High | FR-010 |
| TS-REG-012 | Printer Registration | Verify the available connection-type options. | Functional | Medium | FR-004 |
| TS-REG-013 | Printer Registration | Verify the available initial-status options. | Functional | Medium | FR-005 |
| TS-REG-014 | Printer Registration | Verify a success message is displayed after successful registration. | Functional | Medium | FR-013 |
| TS-REG-015 | Printer Registration | Verify a newly registered printer appears in the printer list. | Integration | High | FR-014, FR-015 |
| TS-REG-016 | Printer Registration | Verify a Standard User cannot access the printer registration function. | Authorization | High | FR-021, FR-039 |
| TS-STS-001 | Status Management | Verify the latest status is displayed for every registered printer. | Functional | High | FR-022 |
| TS-STS-002 | Status Management | Verify an Administrator can update a printer status. | Positive | High | FR-023 |
| TS-STS-003 | Status Management | Verify all supported printer statuses are available. | Functional | High | FR-024 |
| TS-STS-004 | Status Management | Verify valid status transitions are completed successfully. | Positive | High | FR-023, FR-024 |
| TS-STS-005 | Status Management | Verify a printer in Maintenance status cannot transition directly to Busy. | Negative | High | FR-025 |
| TS-STS-006 | Status Management | Verify an error message is displayed after an invalid status transition. | Negative | High | FR-026 |
| TS-STS-007 | Status Management | Verify the latest status is displayed immediately after an update. | Integration | High | FR-027 |
| TS-STS-008 | Status Management | Verify every successful status change is recorded in status history. | Integration | High | FR-028 |
| TS-STS-009 | Status Management | Verify the status history contains the previous status, new status, user and timestamp. | Functional | High | FR-028 |
| TS-STS-010 | Status Management | Verify users can view a printer’s status-change history. | Functional | Medium | FR-029 |
| TS-STS-011 | Status Management | Verify a Standard User cannot update printer statuses. | Authorization | High | FR-030, FR-039 |
| TS-SRH-001 | Search and Filter | Verify users can search for a printer using supported attributes. | Functional | Medium | FR-031, FR-032 |
| TS-SRH-002 | Search and Filter | Verify an appropriate message is displayed when no printer matches the search value. | Negative | Medium | FR-033 |
| TS-SRH-003 | Search and Filter | Verify users can filter printers by status. | Functional | Medium | FR-034 |
| TS-SRH-004 | Search and Filter | Verify users can filter printers by connection type. | Functional | Medium | FR-035 |
| TS-SRH-005 | Search and Filter | Verify users can clear applied searches and filters. | Functional | Low | FR-036 |