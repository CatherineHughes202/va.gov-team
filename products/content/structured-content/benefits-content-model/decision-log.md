# Decision Log – Benefit Content Model

## Purpose of document: 

Record what considerations have contributed to the evolution of a "hardened" Benefit Content Model. This will enable via a COPE model (create once publish everywhere) centralized benefit content to be made available to a growing array of presentation layers – VA.gov website, virtual agent, mobile app, etc.

## Background

### Need for a hardened benefit content model (BCM)

As Veteran-facing presentation layers grow, keeping content in sync across more places has become difficult. The Drupal CMS is intended to provide that source of truth for Veteran-facing content. However, content must be structured to enable apps to pull the content they need. The current state, which does not serve this purpose, has the Benefit Hub pages themselves being the source of truth for benefits. Applications can't pull any particular aspect of that content for specific purposes.

Applications/consumers of structured content
- Virgual agent (chatbot)
- Facilities pages on VA.gov, which tell Veterans what services (benefits) they can receive at a given facility
- Mobile app
- Benefit hubs on VA.gov

Public websites epic covering content design and general discovery for this work: [issue 9628 in va.gov-cms repo](https://github.com/department-of-veterans-affairs/va.gov-cms/issues/9628)

## Decision log

### 2/2/23 MVP Workshop

Sitewide Content (SWC) - Danielle Thierry and Randi Hecht
Public Websites – Dave Pickett (content strategy/design), Wes Rowe (PM), Jill Adams (DM)
VA PO – Dave Conlon

Resources:
- Link to the Airtable - https://airtable.com/invite/l?inviteId=invOnjHhGJyDe5VWI&inviteToken=66aa9d3dd492b6f1e7f1e36d8968b2a914b9c9e7b97e1cc7e867abd338eee47a
- Link to the Mural - https://app.mural.co/t/vagov6717/m/vagov6717/1660845137501/6eadf59a3f4d8dcd29da572a68115a22d6114fe4?sender=u20829d1b64855e281dde2585
- For those unable to directly manipulate the Airtable because of VA network restrictions, I exported the tables to csv and quickly combined them into an Excel. The fields won't be interlinked, but it gives access to the data -
https://github.com/department-of-veterans-affairs/va.gov-cms/files/10564545/Benefit.Content.Model.export.20230201.xlsx

Agenda:
- Review Dave P's content anlysis and audit work in Airtable
- Hypothesize MVP scope
- Review approximate schedule and sequence of activities to reach MVP development

**MVP hypothesis:** "How to apply" content within Benefit Hubs. 
- Sometimes HtA is its own Benefit Detail page, sometimes it's a section within another page
- Has a few structured fields that jump out: 
- Seems less blobby than other options; e.g., Eligibility had this problem, where the MVP version would be a large blob that's difficult to get started structuring

MVP fields (starter list)
- Each Benefit will have at least one Category; these may or may not correspond to existing Hub names
- Beneficiaries will be a blob for now; i.e., don't try to facet with "Depdendent" and "Surviving" as separate fields
  - We expect discoveries about possible structure to emerge as SW Content team builds benefit content, writes "beneficiary" blobs
- Legislation related to benefit, e.g. PACT Act, Mission Act. Can be multiple per benefit.
  - Useful for managing content efforts when legislation spins up or winds down, can also be useful for Veterans.
  - Has potential to apply to multiple content types down the road.
- Ways to apply: in-person, phone, online, mail/PDF, etc
  - Details around specific ways – e.g., online form url
- Evidence or documents that may be required for application

Future / fast-follow considerations
- Parts of speech differences for different channels – e.g., some channels talk about VA as "we," vs. some talk about VA in third person. We determined that MVP will not know about these things and anticipate that channels can use language to insulate content model from verb/voice.
- Pre-requisite benefit field

Process and next steps:
- PW will audit Benefit Detail pages for "How to apply" content; SWC will review and help synthesize for implications for MVP design
- PW will draft a blueprint for the Drupal implementation of MVP – entity relationship diagram or similar. Loop Christia T (PW) in with Steve Wirt. Define relationship models/fields, type of field: what’s a taxonomy / content type / field, min/max, required fields, etc.
- Later: PW/SWC will audit other content types within our portfolio for opportunities for re-use of the MVP content model – specifically, Resources & Support, FAQs.
  - E.g., adding a field to those content types indicating what Category(s) it relates to
- Later: present MVP hypothesis (once it has settled) to Chatbot team to ensure it meets their MVP needs.

### 12/21/22 Workshop
Danielle, Dave Conlon, Dave Pickett, Daniel Sasser, Wes

Document under discussion: [Excel from August](https://dvagov-my.sharepoint.com/:x:/r/personal/danielle_thierry_va_gov/Documents/Benefits%20for%20content%20modeling%20work.xlsx?d=wb36115531f894fdc87f64ba53d27576e&csf=1&web=1&e=dPAc0R), **see tab "Modeled version (DJC)"**

MVP
- For sub-benefit About pages, which are also eligibility pages, are we going to render the whole page from the CM for MVP, or just the Eligibility section? (8/19)
  - Eventually we’ll want to do the whole page
- Migration experience at high level – is editor UX added to the Benefit Detail edit screen, or are there new screens for entering Benefits and Eligibility info?
  - No decision
- Benefit category/Hub will be a one-to-many – i.e., a benefit can be associated with multiple categories/Hubs
- "Pre-requisite benefit name" (col B in excel) is not MVP.
  - Rationale: complicated, not broadly applicable, and unlikely to be leveraged by MVP consumers of the content model.
- "Main benefit recipient(s)" - this field should re-use an audiences (or similar) taxonomy, e.g., Veterans, Family members, Caregivers

Next steps:
- Transfer the excel info into Airtable, which has more database-like capabilities that are helpful to testing model
  - [Github issue for Airtable-ing](https://github.com/department-of-veterans-affairs/va.gov-cms/issues/12058)


### Gap; had trouble prioritizing this work

### 8/22/22 mvp meeting
Danielle, Steve Wirt, PW
- We are unlikely to do any automated migration from old Hub content into content model
- Next steps:
  - Use a spreadsheet as a "draft content model" – we can iterate there, ensure content and model fit real benefits
  - Danielle has begun an [Excel listing all benefits (sharepoint)](https://dvagov-my.sharepoint.com/:x:/r/personal/danielle_thierry_va_gov/Documents/Benefits%20for%20content%20modeling%20work.xlsx?d=wb36115531f894fdc87f64ba53d27576e&csf=1&web=1&e=dPAc0R) – Wes and Florence to modify columns to relfect MVP content model hypothesis and return it to Danielle to attempt entering all ~48 benfits into the spreadsheet

### 8/17/22 Deep dive on Pattern Guide for benefit hubs
(Wes, Florence)
[Pattern guide](https://design.va.gov/patterns/benefit-applications#eligibility-hierarchy) used by Sitewide Content team to manage benefit hubs.

- Gathered examples of "blue box" eligibility content in [Mural](https://app.mural.co/invitation/mural/vagov6717/1660845137501?sender=u907f83e01e35bb04de6f8139&key=96ac157c-b924-483d-96c7-8831613a101b)

### 8/12/22 Workshop

Docs shared:
- Danielle’s [content model outline](https://github.com/department-of-veterans-affairs/va.gov-team/blob/master/products/content/structured-content/core-benefit-content-structure.md)

Sub-categories among the 9 benefit areas
- Benefit Hubs are actually categories – ”a benefit” is a smaller molecule
- Use case: chatbot tells Vet list of benefits under health care
- Use case: (far future) we personalize that list for the specific Vet based on their service, parameters
- Education is a good example of complexity/categories
  - Main “about” page focuses on GI Bill, but links out to sub-pages about other benefits

"Core benefits" = the 9 with Hub Landing Pages

MVP thoughts:
- Eligibility might be the first type of page in DT's content model (link above) that we take on
  - Some benefits, especially the 9 main ones, tend to have dedicated eligibility pages
  - In others, eligibility is a blue "blobby" area with all the details
  - The eligibility content itself is not going to be hardened – it would be a blob in the CMS

**Schema.org** – benefits Veterans by making organic search results better, even answering questions without visiting site. 
- KPI idea: reduction in traffic on pages where the organic search experience is able to leverage the schema really well, while at the same time benefit delivery is unchanged
- [Schema.org details for gov’t services](https://schema.org/GovernmentService)
- Christia to look into it; Swirt has experience
- Dave C: let’s build the BE around schema.org, so all the consumers can follow the standards
- The drupal machine name is the thing that should correspond to schema.org
- **Schema.org research**: Christia's notes in [CMS-repo ticket 10240](https://github.com/department-of-veterans-affairs/va.gov-cms/issues/10240#issuecomment-1228727561).
  - Drupal has two modules that could apply 
    - [Blueprint module](https://www.drupal.org/project/schemadotorg) - (still in development as of Aug 2022)
    - [Metatag Module and Schema.org Metatag](https://www.drupal.org/project/schema_metatag) - stable sub-module, we already use Metatag (parent module)
    - recommendation: due to lack of maturity of Blueprint, better solution may be to use the Schema.org Metatag sub module for Metatag module, which we already have installed.

Next steps:
- Build [Mural](https://app.mural.co/invitation/mural/vagov6717/1660845137501?sender=u907f83e01e35bb04de6f8139&key=96ac157c-b924-483d-96c7-8831613a101b) to look at patterns in existing Hub content
- Github issue https://github.com/department-of-veterans-affairs/va.gov-cms/issues/10242 – She gathered tons of good background materials in the comments, including both content-model background and Drupal implementation details from the Benefit Hubs.


### 8/4/22 – deeper dive with Content
Danielle T, Dave C

- Editor group will continue to be very small, just the SWContent team
- DC: chatbot and ourselves (PW/Benefit Hubs) are first customers (fast publishing, content API)
- Node count: Target Zero impact or improvement to speed of publishing (?)
  - (Current speed is node-count dependent)
- DC quite interested/concerned about permissions, who will need to be able to make changes to each atomic piece/field

Technical discovery ticket (Christia took on): https://github.com/department-of-veterans-affairs/va.gov-cms/issues/9910

### 7/28/22 Tech background meeting with Steve Wirt (CMS team)

Focused on Facilities team's experience with hardening content model.

Every Fac page had a map page, a top task page (eg benefits description)
- Created specific content type for common page types
- Bulk generated those pages for every system, left in draft mode
- It would auto-archive old version when the new one was published
- Major challenge: broken links – links in content were to node ID, which didn’t get auto-fixed. **Watch for cross-links.**
  - If old content migrated from junk drawer node to hardened node, references to the old page broke. 
  - VAMC editor pages vs. Sitewide Content pages - may be less frequent with SWC content
- Why Fac made a new content type vs. restructuring existing:  took 4 pieces of recurring content & made them into their own types – DaveC and Kev Walsh decided that
  - Can be a Data driven decision around fields


### 7/25/22 Kickoff
Danielle Thierry (DT) + Public Websites team members (PM: Wes Rowe)

We have 2 content types: Resources & Support, and Benefit Detail pages. They are very similar. We need to understand the differences that matter between them.

Benefit Detail pages are used to manage 4 types of Benefit eligibility content right now, listed here: https://github.com/department-of-veterans-affairs/va.gov-team/blob/master/products/content/structured-content/core-benefit-content-page-templates.md 

Sitewide Content wants to codify capturing the data for those 4 types of pages, in addition to making chunks of that content reusable across various places in the site. We need to more deeply understand which chunks should be reusable and where, in order to understand if they need to be smaller component content types ( like Q&A) or what. 
 
Our team needs to also understand / decide / propose whether the Benefit Detail content type can be updated to manage the 4 page types, or whether we need separate freestanding content types to manage the 4 flavors. We should factor FE, Backend, data effort & maintenance into that thinking.
One content type = more conditional logic in the front end to manage
Multiple content types = more templates to manage / more Drupal definitions / configs to manage

Key documents that Danielle provided to get us started:
- [Core benefit content page templates](https://github.com/department-of-veterans-affairs/va.gov-team/blob/master/products/content/structured-content/core-benefit-content-page-templates.md)
- [Content structure](https://github.com/department-of-veterans-affairs/va.gov-team/blob/master/products/content/structured-content/core-benefit-content-structure.md)

