# VA Online Scheduling
VA online scheduling (VAOS) is a Veteran-facing healthcare appointment scheduling tool on VA.gov.

[Other Veteran-facing healthcare appointment tools](../README.md)

## Product vision
Deliver a seamless and positive experience for any Veteran who wants to schedule an appointment online.

## User Problem Statement
A very small percentage of Veteran appointments with VA Medical Centers are scheduled online. Other avenues for scheduling appointments like phone, secure messaging, reminder letters, and return to clinic orders can lead to clerical errors, miscommunications, and a heavier burden for schedulers. These issues cause delays in scheduling care and are frustrating for Veterans.

[VAOS Product Outline](vaos-product-outline.md)

**Jump to**

[TBD - add links to all headings]

## What we're working on

High-level overview of our current projects:
- [Product roadmap]()
- [Main epics Zenhub board](https://app.zenhub.com/workspaces/vaos-team-603fdef281af6500110a1691/board?repos=133843125,194202180&showPRs=false&showReleases=false&showReviewers=false)

The main board rolls up tickets from two other boards: 
* [Engineering board]() - Work currently being developed
* [Product/design board]() - Product, design, and research

## Documentation

New to the team? [Read the onboarding docs]().

This GitHub folder is the central document hub for the VAOS product, but other important documentation exists in:

- [GitHub sensitive repo]()
- [DSVA Mural]()
- [Teams]()
- [Figma]()
- [Confluence]() (Requires VA network)

### Product and User Experience

| Product | User Experience |
|---|---|
| [Product roadmap]() | [Screen templates]() |
| [Open issues]() | [Design files]()
| [Closed issues]() | |

### Engineering

| Engineering | Front end | Back end |
|---|---|---|
| [MAPSUP ticket creation]() | [Front-end practices and tips]() | [Back-end engineering practices and tips]() |
| [Users for staging]() | [Front-end code reviewer guide]() | [Vets API developer setup]() |
| [Swagger editor]() | [Front-end testing guidance]() | [Vets API user creation and VAOS session validation]() |
| [VAOS internal tools]() | [Using Sentry on VAOS]() | [Vets API Review Instances]() |
| [VAOS incident response playbook]() | [Maintenance messages in VAOS]() | [LogQL (Querying with Loki)]() |
|  |  | [Application monitoring with Datadog]() |

### Support and Incident Response

- [VAOS incident response process](department-of-veterans-affairs/va.gov-team/products/health-care/appointments/va-online-scheduling/engineering/incident_response/readme.md)
- [VAOS support process](department-of-veterans-affairs/va.gov-team/products/health-care/appointments/va-online-scheduling/product/vaos-support-process.md)

### Research and analytics

- [User research]()
- [Analytics]()

## How VAOS works

- [Business rules]()
- [User flows]()
- [Copy docs]()
- [Page templates]()

### View appointment lists
An overview of appointments and requests. Helps get a sense of appointments at a high level.

| Feature | Usage | Documentation | 
|---|---|---|
| Upcoming appointments | View all future and in progress appointments | [Staging URL](https://staging.va.gov/health-care/schedule-view-va-appointments/appointments) <br> [Content](https://github.com/department-of-veterans-affairs/va.gov-team/blob/master/products/health-care/appointments/va-online-scheduling/content/copy-docs/homepage.md#appointment-list-cards) <br> [Design template](https://www.figma.com/file/twogqAIoOL9WAFRqvUbwiS/VAOS-Templates?node-id=182%3A18201&t=VF6bPXzS8n4lnB6O-4) <br/> [Logic](https://github.com/department-of-veterans-affairs/va.gov-team/blob/master/products/health-care/appointments/va-online-scheduling/engineering/vaos_business_rules.md#upcoming-appointments) |
| Past appointments | View all appointments from the last two years | [Staging URL](https://staging.va.gov/health-care/schedule-view-va-appointments/appointments/past) <br> [Content](https://github.com/department-of-veterans-affairs/va.gov-team/blob/master/products/health-care/appointments/va-online-scheduling/content/copy-docs/homepage.md#past-1) <br> [Design template](https://www.figma.com/file/twogqAIoOL9WAFRqvUbwiS/VAOS-Templates?node-id=1125%3A28605&t=VF6bPXzS8n4lnB6O-4) <br/> [Logic](https://github.com/department-of-veterans-affairs/va.gov-team/blob/master/products/health-care/appointments/va-online-scheduling/engineering/vaos_business_rules.md#past-appointments) |
| Pending appointments | View all pending and canceled requests | [Staging URL](https://staging.va.gov/health-care/schedule-view-va-appointments/appointments/pending) <br> [Content](https://github.com/department-of-veterans-affairs/va.gov-team/blob/master/products/health-care/appointments/va-online-scheduling/content/copy-docs/homepage.md#requests-1) <br> [Design template](https://www.figma.com/file/twogqAIoOL9WAFRqvUbwiS/VAOS-Templates?node-id=1125%3A28986&t=VF6bPXzS8n4lnB6O-4) <br/> [Logic](https://github.com/department-of-veterans-affairs/va.gov-team/blob/master/products/health-care/appointments/va-online-scheduling/engineering/vaos_business_rules.md#pending-appointments) |

### View appointment details
All the information about a single appointment. VAOS can display 8 types of appointments.

| Feature | Description | Documentation |
|---|---|---|
| VA In person  | | |
| VA In person Vaccine | | |
| VA Video Care at Home | | |
| VA Video Care at a VA location | | |
| VA Video Care on GFE | | | 
| VA Video Care at an ATLAS location | | |
| VA Phone Appointment | | |
| Community Care Appointment | | |

### View request details
All the information about a single appointment.

| Feature | Description | Documentation |
|---|---|---|
| VA Appointment Request  | | |
| Community Care Appointment request | | |

### Manage appointments and requests
Tools Veterans can use to manage their appointments and requests.

| Feature | Description | Documentation | 
|---|---|---|
| Cancel appointment/request | | |
| Add to calendar | | |
| Print | | | 

### Schedule and request appointments
How Veterans can schedule or request appointments through VAOS

| Feature | Description | Documentation |
|---|---|---|
| Direct-schedule or request appointment at VA  | | |
| Direct-schedule COVID-19 vaccine at VA | | |
| Request community care | | |


## The team

### Team members

**OCTO Product Owners**
- Kay Lawyer
- Patrick Bateman
- Kristen McConnell

**Program Management**
- Katie Riddle

**Product Management**
- Jeff Roof (lead)
- Leah De La Costa

**User Experience**
- Peter Russo (lead)
- Ciera Maddox

**Engineering**
- Simi Adebowale (lead)
- AJ Magdub
- Corey Ferris
- Ryan Shaw
- Jennie McGibney
- Tony Williams

### How we we work together

[Team Charter](team/charter.md)

### Communication channels

Find team members and channels in the [DSVA Slack Space]().

| Channel | Used for | 
|---|---|
| **#vaos-team** | Start here. Main channel for any general product, engineering, or design questions for VAOS front-end or backend teams, including: <br> - Team announcements, broad notifications <br> - Coordinated communication related to rollouts, releases, and launches <br> - SQA- and testing-related questions. |
| #vaos-fe-meetup | VAOS FE team internal discussions. Private channel for [VAOS FE team members](#team-members). |
| #vaos-engineering | VAOS engineering PPG channel. | 
| #vaos-eng | Engineering practice and technical discussions. |
| #vaos-alerts | Grafana alerts | 
| #vaos-pull-requests | Pull request reminders |
| #va-appointments-ux | User experience questions and coordination for VAOS, check-in, and mobile teams |

## Who We Work With

- VA Mobile Framework (VAMF) Team:
  - Steve Eaton, Portfolio Manager
  - Steven Brush, Engineering Lead
  - Brad Crosby, Engineering Lead
  - Judy Mercado, Business Analyst
  - Steve Alcocer, Business Analyst
  - Grace Palino, Production Support/SQA Project Manager
  - Marcy Nadeau, SQA Tester