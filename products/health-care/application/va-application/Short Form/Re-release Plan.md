# 10-10EZ Short Form Release plan

## Phase 1: UAT

### Planning
- UAT Go / No Go: 09/16/2022
- Planned release to 5% of applicants: 09/19/2022
- Desired range or test duration: 09/26/2022 - 09/30/2022
- Desired number of users: 9
- Recruitment method: Perigean
- How testing will be conducted: Sessions over Zoom
- How users will be given access without making it fully available in production: Feature flag

### Testing
- Internal Team Testing: TBD
- [x] Internal team testing complete
- End-to-End testing with enrollment team: TBD
- [x] End-to-End testing with Enrollment Team complete
- [x] Confirmed generation of 10-10EZ PDF with Enrollment System
- Bugs identified to be addressed prior to launch: TBD
- **Note: Per Joshua Faulkner, testing was successfully completed with the Enrollment System Team**.

### Results
- Number of users: TBD
- Number of bugs identified / fixed: 0
- UX/Content changes required, based on feedback, logs, or challenges: TBD


## Phase 2: Staged Rollout

### Planning
- Launch Go / No Go: 09/16/2022
- Desired date range: 09/19/2022 - 10/10/2022
  - Dates pending; waiting on confirmation from ES Team
- Success criteria to be reviewed prior to advancing rollout to the next stage
  - Ensure 10-10EZ PDFs can be generated by the Enrollment System
- Dashboards showing success criteria metrics
  - [Domo Dashboard](https://va-gov.domo.com/page/447193050)
  - [Datadog Dashboard](https://vagov.ddog-gov.com/dashboard/p5g-fys-epz/1010-health-apps?from_ts=1657212129534&to_ts=1657215729534&live=true)

### Phased Rollout
- 5% of users (2 weeks): 09/19/2022
- 25% of users (1 week): 09/26/2022 (based on positive results)
- 50% of users (1 week): 10/03/2022 (based on positive results)
- 75% of users (1 week): 10/10/2022 (based on positive results)
- 100% of users (1 week): 10/17/2022 (based on positive results)


## Go Live!

### Planning
- Desired date: 10/17/2022
- Actual date: TBD

**Key Result:** Increase number of application submissions
*Using last 6 months (Mar-Aug 2022) to calculate Baselines*
| KPI / Metric | Baseline: Jan-June 2022 | Post-launch Week 1 | Post-launch Month 1 |
| ------------ | ------------- | ------------------ | ------------------- |
| Avg. Application starts per Month | 17.8k | TBD | TBD |
| Avg. Submissions per Month | 13.1k | TBD | TBD |
| Pct. Applications Completed | 74% | TBD | TBD |

**Key Result:** Reduce Sesssions / Time taken to complete application 
*Using last 6 months (Mar-Aug 2022) to calculate Baselines*
*To calculate, sum the number of sessions involved (1 session = 1, 2 sessions = 2, 3+ sessions = 3) and divide by the total number of applications submitted*
| KPI / Metric | Baseline: Mar-Aug 2022 | Post-launch Week 1 | Post-launch Month 1 |
| ------------ | ------------- | ------------------ | ------------------- |
| Avg. Sessions per Submission | 1.46 | TBD | TBD |
| Avg. 1 session per Month | 7,645 | TBD | TBD |
| Avg. 2 sessions per Month | 2,366 | TBD | TBD |
| Avg. 3 or more sessions per Month | 1,471 | TBD | TBD |

**Key Result:** Reduce abandoned applications
*Using last 6 months (Mar-Aug 2022) to calculate Baselines*
*To calculate, check how many people started the section* Service Information *and find out how many users abandoned in each of the following steps:*
- Additional Information
- Financial Disclosure
- Marital Status
- Dependent Information
- Annual Income
- Deductible Expenses
*This represents how many people abandoned applications in the middle of the fields that will be skipped during the short form*
| KPI / Metric | Baseline: Jan-June 2022 | Post-launch Week 1 | Post-launch Month 1 |
| ------------ | ------------- | ------------------ | ------------------- |
| Avg. Applications Abandoned per month | 6,513 (39,080 total) | TBD | TBD |
| Pct. Applications Abandoned per month | 39.3% | TBD | TBD |


## Post-Launch Questions
1. How do the KPIs you gathered compare to your pre-launch definition(s) of *success*?
2. What qualitative feedback have you gathered from users or other stakeholders, if any?
3. Which of the assumptions you listed in your product outline were / were not validated?
4. How might your product evolve now or in the future, based on these results?


---
Notes: See [this spreadsheet](https://docs.google.com/spreadsheets/d/e/2PACX-1vRXNLICZazDx55QsziZtW7q-1FIsSueMpIiTiZBGgsakh77jWIMVGqo0Y-jW2h_qZyyUbhf97hsqNSX/pubhtml) for examples on how several of the metrics were calculated.
