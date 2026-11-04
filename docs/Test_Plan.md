# Test Plan: OrangeHRM HR Management System

**Author:** Aishwarya Anil  |  **Version:** 1.0  |  **Approach:** Manual, risk-based (IEEE 829 structure)

## 1. Objective
Verify core HR workflows end to end, including business rules (leave balance, overlapping leave, hiring workflow states) and role-based access, across Admin and ESS roles.

## 2. Application Under Test
OrangeHRM open-source demo (https://opensource-demo.orangehrmlive.com). Admin account: Admin / admin123. ESS users are created during testing.

## 3. Scope
**In scope:** Login/session, Admin > User Management, PIM, Leave, Recruitment, My Info, Dashboard, Directory, role-based access.

**Out of scope:** Time/attendance and performance modules, reports export, API, load testing.

## 4. Test Types
Functional, business-rule, role-based access (RBAC), state transition (leave and candidate lifecycle), boundary and file-upload validation, UI and responsive checks, exploratory.

## 5. Requirements and Traceability
7 requirements are mapped to 46 test cases in [`RTM.csv`](../RTM.csv).

## 6. Test Design Techniques
| Technique | Where used |
|---|---|
| Equivalence partitioning | User roles (Admin/ESS), leave types, file types |
| Boundary value analysis | Leave balance = requested, +1; file size 1MB limit |
| State transition | Leave: Pending > Scheduled > Taken / Cancelled; Candidate: Initiated > Shortlisted > Interview > Offered > Hired |
| Decision table | Leave approval vs balance vs overlap |
| Error guessing | Duplicate ids/usernames, direct URL access by ESS user |

## 7. Entry Criteria
- Application / API reachable and test accounts working
- Requirements understood; test cases reviewed and baselined
- Test data prepared (see `test-data/`)

## 8. Exit Criteria
- 100% of P1 and at least 95% of all test cases executed
- No open Critical defects; Major defects triaged with an agreed workaround
- RTM shows every requirement covered; Test Summary Report published

## 9. Defect Management
Defects are logged in `bug-reports/` using a Jira-style template: ID, module, severity, priority, environment, steps, expected vs actual, impact, linked test case.

| Severity | Meaning |
|---|---|
| Critical | Blocks a core business flow, data loss, security exposure, no workaround |
| Major | Core feature works incorrectly, workaround exists |
| Minor | Non-core feature affected or cosmetic issue with functional impact |
| Trivial | Cosmetic / text issue |

## 10. Environment
OrangeHRM public demo (shared, resets periodically); Chrome / Firefox / Edge latest.

## 11. Risks and Mitigation
| Risk | Mitigation |
|---|---|
| Shared demo data is changed by other users | Use unique test data prefixes (aish.*) and create own records per cycle |
| Demo resets periodically | Re-create preconditions at start of each session |
| Holiday/work-week config may differ | Record configuration before leave tests |

## 12. Deliverables
Test Plan, Test Cases (CSV), RTM, Defect Reports, Exploratory session charters, Test Summary Report.
