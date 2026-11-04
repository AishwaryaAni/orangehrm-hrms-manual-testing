# OrangeHRM HR Management System: Manual Testing Project

Manual QA of an enterprise **HRMS**: user and role management, employee records (PIM), leave management with balance rules, recruitment workflow and role-based access control.

![Type](https://img.shields.io/badge/testing-manual-blue) ![Test cases](https://img.shields.io/badge/test%20cases-46-green) ![Requirements](https://img.shields.io/badge/requirements-7-orange) 

**Application under test:** [https://opensource-demo.orangehrmlive.com](https://opensource-demo.orangehrmlive.com)

## What this project covers
- **Test Plan**: scope, approach, design techniques, entry/exit criteria, risks. [`docs/Test_Plan.md`](docs/Test_Plan.md)
- **46 test cases** across 7 modules (positive, negative, boundary, business-rule, security). [`test-cases/ALL_test_cases.csv`](test-cases/ALL_test_cases.csv)
- **Requirement Traceability Matrix**: 7 requirements mapped to test cases. [`RTM.csv`](RTM.csv)
- **Jira-style defect reports** with severity, priority, steps, expected vs actual and business impact. [`bug-reports/Defect_Reports.md`](bug-reports/Defect_Reports.md)
- **Exploratory testing charters** (session-based). [`docs/Exploratory_Charters.md`](docs/Exploratory_Charters.md)
- **Test Summary Report** with exit-criteria checklist. [`reports/Test_Summary_Report.md`](reports/Test_Summary_Report.md)

## Coverage by module
| Module | Test cases |
|---|---|
| Login & Session | 6 |
| Admin User Management | 9 |
| PIM Employee | 9 |
| Leave | 9 |
| Recruitment | 6 |
| My Info & RBAC | 3 |
| Dashboard & Directory | 4 |

## Repository structure
```
docs/            Test plan, exploratory charters
test-cases/      ALL_test_cases.csv: every test case, filter by Module (opens in Excel / Google Sheets)
bug-reports/     Defect_Reports.md: defect log, full reports, Jira-style template
reports/         Test summary report
test-data/       Accounts, inputs, expected values
RTM.csv          Requirement traceability matrix
```

## How to use
1. Open `test-cases/ALL_test_cases.csv` in Excel or Google Sheets and filter by Module.
2. Execute against the live demo and update the `Status` column (Pass / Fail / Blocked).
3. Log new defects with the template in `bug-reports/` and fill in the summary report.

## Author
**Aishwarya Anil**, QA Engineer (Manual + Automation) | [LinkedIn](https://www.linkedin.com/in/aishwarya-anil20)
