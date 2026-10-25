# Finding evidence in the system

For each applicable requirement, look for evidence in the code, configuration, infrastructure files and documents. Record what you found and where (file and line, or document and section).

Some things can't be seen in code: permits, approvals, contracts, the DPO, Cyber Defence Centre designation and team location. Ask the right party for those (see `questions.md`) and record the answer as **stated by** that person.

## Handling what you find

- **Secrets:** never print any part of them. Record only the file, the line and the kind of secret (for example "cloud access key in src/config.js:4"), and recommend a security audit.
- **Real patient data in the repository** (seed files, fixtures, logs, dumps, screenshots):
  - don't reproduce it anywhere, including the register, the Excel file or the chat
  - to check a file you suspect holds real patient data, look at its structure only: count rows and columns, and look for markers such as "copied from production". Never print values, even masked
  - record only the file and the type of data, for example "db/seed.sql: names and civil numbers described as copied from production"
  - record it under PDPL-21 at High priority, and note it under PDPL-26 and MOH-12 as a possible reportable breach. It also uses patient data outside the purpose it was collected for (PDPL-13) and breaks the access rules for health data (MOH-08)
  - recommend removing it from the repository and its history
- **Application-security flaws** (for example IDOR, self-assigned roles, injection) are outside this library. Note them under the closest access-control item, and recommend a security audit (for example the Security Audit Loop plugin).

## 1. Hosting and data residency

PDPL-28, PDPL-29, MOH-14, NAT-04, NAT-05; NAT-16 and NAT-17 for government providers; TEL-02 and MOH-26 where they apply

- **Where to look:**
  - infrastructure as code (Terraform, CloudFormation, Bicep, Pulumi)
  - Kubernetes and Helm values, docker-compose files
  - CI/CD deploy steps, `.env.example`, cloud SDK configuration
  - database server names (never print credentials)
  - operations documents and runbooks
- **What the rules expect:**
  - Health-sector content held in the cloud is at the TRA's top security level. It belongs in a Category 4 data centre of a TRA-permitted provider in Oman, and the provider may not move it abroad without TRA approval (NAT-04, NAT-05).
  - Storing or processing health data outside Oman needs Cyber Defence Centre approval first (PDPL-29), and the Ministry of Health allows hosting abroad only for software as a service where no Omani alternative exists (MOH-14).
  - Government data, backups and disaster recovery stay in Oman (NAT-16, NAT-17).
  - Insurance-sector content is at the TRA's Level 3 by sector, and it stays in Oman unless the TRA approves (NAT-05). The regulation doesn't say how health data held by an insurer is classed, so prefer a Category 4 data centre and ask (NAT-04).
- **Cloud locations in and near Oman** (from the library table "Cloud regions in and near Oman" in `library/national.md`, which has the sources; confirm each provider's TRA permit and data-centre category in writing):

| Location | Cloud services |
|---|---|
| **In Oman** | AWS Muscat Local Zone (`me-south-1-mct-1`). It's an extension of the Bahrain Region (`me-south-1`): only services offered in the zone run in Muscat. Object storage, volume snapshots, most managed services and the control plane are in Bahrain unless shown otherwise. Treat anything not pinned to the zone as Bahrain |
| **In Oman** | Oracle OCI Dedicated Regions in Muscat and Ibri, hosted by ITHCA Group with Oman Data Park. The Muscat region was offered to the public and private sectors at launch (2021); reports on Ibri (2025) describe it as serving government entities. Ask about access |
| **In Oman** | Local providers, such as Oman Data Park, Omantel's National Cloud, data2cloud (Ooredoo), Datamount, and SAP's private cloud data centre |
| **Not Oman** | AWS `me-south-1` (Bahrain) and `me-central-1` (UAE). AWS has no full Region in Oman |
| **Not Oman** | Azure `uaenorth` and `uaecentral` (UAE), Qatar Central, Saudi Arabia East. Azure has no region in Oman |
| **Not Oman** | Google Cloud `me-central1` (Doha), `me-central2` (Dammam) and `me-west1`. Google Cloud has no region in Oman |
| **Not Oman** | Oracle public regions in the UAE and Saudi Arabia; Alibaba Cloud `me-east-1` (Dubai) and `me-central-1` (Riyadh); Huawei Cloud Riyadh |

Any other region is outside Oman. A region in Oman doesn't by itself meet NAT-04: ask for the provider's TRA permit, the data-centre category, and the list of data centres it uses for this content.

- **Also check:**
  - backup, disaster recovery and replica regions
  - CDN caching of patient data
  - where logs, analytics, error reports and backups land
  - object storage and snapshots behind a Local Zone deployment

## 2. Offshore data flows through third-party services

PDPL-28, PDPL-29, PDPL-30, MOH-14; TEL-02 for video and messaging in telehealth; MOH-26 for imaging AI

Search dependencies and code for SDKs and endpoints that could receive patient data:

| Category | Examples |
|---|---|
| Analytics and session replay | Google Analytics, Mixpanel, Segment, Amplitude, Hotjar, FullStory |
| Error tracking and logging or APM | Sentry, Bugsnag, Datadog, New Relic |
| Email, SMS, push and WhatsApp | SendGrid, Twilio, Firebase messaging, WhatsApp Business |
| Video and voice for telehealth | Zoom, Agora, Twilio Video, Vonage |
| AI and LLM APIs | OpenAI, Anthropic, Google Gemini, Azure OpenAI (check the region) |
| Storage and backend-as-a-service | Firebase, Supabase |
| Support and ticketing | Zendesk, Intercom, Freshdesk |

For each one, decide:

- whether patient data or identifiers can reach it: prompts, error payloads and request bodies, event properties, message bodies, call recordings, screenshots. Civil and resident numbers are "Confidential" identifiers under the Ministry of Health's classification (MOH-08).
- where it processes and stores data
- whether Cyber Defence Centre approval is recorded (PDPL-29), and whether the PDPL transfer conditions are met: consent where needed, equivalent protection and an assessment (PDPL-28)

Settings that widen the flow count as evidence, for example error tracking set to send personal data by default, or recording switched on for every call.

## 3. Offshore access and development

PDPL-30, MOH-13; NAT-22 for government providers; INS-11 for revenue cycle management; TEL-07 for clinicians abroad

- **Where to look:** operations documents, runbooks, on-call rotas, support procedures, bastion or VPN configuration in the infrastructure files, IAM definitions in the infrastructure files, and CI workflows that deploy to production. Read the files; don't query live systems.
- **Check:**
  - who can reach production systems or patient data, and from which countries
  - whether remote access is approved in advance and runs over an approved VPN, with sessions that can be ended (MOH-13)
  - whether offshore staff see identifiable patient data, or only masked or synthetic data (PDPL-30)
  - for government providers, whether security, network, database, development, systems analysis and support roles are held by Omani nationals, including at contractors (NAT-22)
  - whether revenue cycle work (coding, claim submission, denials) is done inside Oman (INS-11)

For private providers, whether remote access from abroad counts as processing outside Oman isn't settled (PDPL-30). For government providers, it's a transfer under the government policy (PDPL-05). Record what happens, and raise it as a Blocker-priority question.

## 4. Identity and access

MOH-09, PDPL-21; NAT-11 for government providers; NAT-27 where national digital identity is used

- **Authentication:** the auth library or identity provider. Multi-factor authentication for privileged and remote access (PDPL-21).
- **The Ministry of Health's account rules (MOH-09):**
  - lock accounts after no more than 3 failed logins
  - disable accounts unused for 180 days
  - one active session per user ID
  - passwords of at least 8 characters with upper and lower case, digits and special characters, changed at first login and every 180 days, and not reused within a year. If multi-factor authentication replaces the 180-day change, it's a deviation to record and have an adviser sign off.
  - a login banner warning that unauthorised use is prohibited
  - a privilege administration page, roles by job function, and yearly privilege reviews
  - leavers and staff on leave handled promptly, ideally from the HR system; trainee accounts that expire
  - remote-work devices locking after 15 minutes of inactivity
- **Least privilege:** roles assigned by an administrator, never chosen by the user. Highly confidential data is limited to the care team (MOH-08).
- **Patient and clinician login with national digital identity** (Thiqa or ID card PKI), where the client needs it (NAT-27).

## 5. Audit logging

MOH-10, PDPL-21; NAT-09 and NAT-11 for government providers

- **What to log:** reads as well as writes, with user ID, date and time, device, and the patients whose data was accessed (MOH-10). Logs must be tamper-evident and kept on a separate server from the application database.
- **Review:** an activity dashboard for the health information management unit and the data protection officer.
- **Printing:** limited to listed roles and documents, with the user ID on every printed page and a print log.
- **Break-glass:** a recorded reason, an alert for review, and logs kept for at least 5 years.
- **Direct database access** outside the application is logged (NAT-11, government).
- **Breach scoping:** a query that answers "which patients were affected?" (PDPL-26, MOH-12).

## 6. Data model and records

MOH-03 to MOH-08, MOH-15 to MOH-17, PDPL-11, PDPL-15 to PDPL-18, NAT-24

- **Patient identifier:** civil or resident number, required, validated and unique, with name parts stored separately, duplicate detection, and temporary numbers for newborns, visitors without ID and downtime (MOH-07).
- **Record integrity (MOH-06):** look for hard deletes and in-place updates. Clinical entries are amended, not overwritten. Deletion is logical, with a reason, and stays visible as strikethrough. Copy-paste keeps its source. Duplicate records are merged by HIM staff with full lineage.
- **Classification and masking:** classification at field or document level, highly sensitive categories (psychiatry, infectious disease, addiction, assault, suicide, media, genetics), and masking or sealing with a visible marker (MOH-08).
- **Consent:**
  - versioned Arabic and English consent texts, unticked granular choices, and a record of who consented, to which version, when, through which channel and in what capacity (PDPL-11)
  - the Ministry of Health's consent types, including written consent for surgery and a "left against medical advice" form (MOH-03), and consent before photos and recordings (MOH-04)
  - a tamper-evident copy of what was shown and accepted, for electronic consent (NAT-24)
- **Children and adults who lack capacity:** date of birth, a linked guardian with proof of guardianship, and no sharing without guardian consent (PDPL-15).
- **Patient requests:** tracked with timers. The PDPL allows 45 days (PDPL-16). The Ministry of Health allows 15 working days for medical reports and corrections, and 15 days for restrictions and disclosure lists (MOH-16, MOH-17). Build to the shorter one. Copies come as PDF and in a machine-readable format (PDPL-17, MOH-16).
- **Retention:** clinical records follow the national records schedule, with 10-year triggers, a freeze after death and a permanent destruction log (MOH-15). Don't auto-delete clinical records until the schedule is confirmed. Other personal data is erased or anonymised when its purpose ends, including in backups, caches and processors (PDPL-18).

## 7. Encryption and keys

MOH-08, MOH-11, PDPL-21; NAT-11 and NAT-16 for government providers

- TLS on all endpoints and internal calls, and encrypted file exchange between institutions with agreed keys (MOH-11).
- Encryption at rest for databases, files and backups (PDPL-21). Field-level encryption for highly sensitive data (MOH-08).
- For government providers, the application encrypts sensitive fields before they reach the database, with keys held outside it (NAT-11).
- Key management: where keys are kept, who can use them, and rotation.

## 8. National platforms and insurance

MOH-18, MOH-19, MOH-20, MOH-23; NAT-19 for government providers; INS-03 to INS-08, INS-15, INS-16

- **Shifa national health record:** FHIR exchange matched on civil or resident number, a patient "do not share" flag that the integration honours, and a log of every submission and retrieval (MOH-18, MOH-17).
- **E-referral and notifications** to the Ministry of Health (MOH-23, MOH-20).
- **Government integration:** through the National Platform for Government Integration, with APIs registered in the National API Catalog (NAT-19).
- **Dhamani (insurance):**
  - every insured eligibility check, prior approval, claim and remittance goes through Dhamani, with no direct payer integrations (INS-03)
  - codes from the FSA-specified code sets, validated before submission (INS-04)
  - named user accounts, logged actions, and a downtime queue (INS-05)
  - prior approval above OMR 100 for outpatients, with 30-minute timers and implied approval on expiry (INS-06)
  - eligibility checked before each billable service, with the response stored against the encounter as evidence (INS-08). Writing whole responses into application logs is a separate problem (PDPL-21).
  - Dhamani's technical specification isn't public (INS-16). Ask whether the team holds it.
- **The Ministry of Health's approval of a private facility's information system** (MOH-19) is a question for the client.

## 9. Development lifecycle and vendors

MOH-11, MOH-13, PDPL-25, PDPL-21; NAT-12, NAT-14 and NAT-21 for government providers

- **CI pipeline:** static analysis, dependency scanning and vulnerability management. Change control with pre-change backups and tested rollback (MOH-11).
- **Security testing:** penetration tests covering everything internet-facing, including mobile apps (PDPL-21). For government providers, an assessment by an MTCIT-accredited provider before go-live and after major changes (NAT-12).
- **Test data:** no production patient data in development or test. Use synthetic data (PDPL-13, PDPL-21, NAT-04).
- **Vendors and processors:** written contracts with the required terms (PDPL-25), and the Ministry of Health's 17 contract points for third-party access (MOH-13).
- **Government work:** a pre-implementation risk assessment signed off by the client (NAT-14), and source code ownership or escrow (NAT-21).

## 10. Backup and continuity

MOH-11, INS-05, NAT-05; NAT-15 and NAT-17 for government providers

- Backup schedules, restore tests, recovery time and recovery point objectives, and backup locations in Oman.
- A disaster recovery plan tested every year (MOH-11), with disaster recovery in Oman for government data (NAT-17).
- A downtime kit: printable forms, pre-allocated temporary record numbers and a reconciliation workflow (MOH-11), and a Dhamani transaction queue (INS-05).

## 11. AI features

PDPL-13, PDPL-19, PDPL-29, MOH-25, MOH-26, NAT-30, MDV-02, MDV-03

- **Hosting:** where models are hosted and where inference runs. Offshore model APIs that receive patient data need Cyber Defence Centre approval (PDPL-29). Imaging AI is hosted in Oman (MOH-26).
- **Inputs:** what goes into prompts, and whether identifiers can be removed first.
- **Training:** whether patient data is used for training, and on what basis (PDPL-13).
- **Automated decisions, by AI or by rules:** patients told that a decision was automated, a way to object, and review by a person who can change the outcome (PDPL-19). Look for AI output or rule results written straight into clinical, administrative or claim fields without review.
- **Governance:** an AI register, validation and bias testing, monitoring, logged inputs, outputs and overrides, and AI-generated content labelled (MOH-25, NAT-30).
- **Medical purpose:** if the feature diagnoses, treats, monitors or triages, raise the medical device questions (MDV-02, MDV-03).

## 12. Telehealth

TEL-01 to TEL-08

- Licensed service and approved platform (TEL-01).
- The whole stack hosted in Oman, including video media and relay servers, chat logs and recordings (TEL-02).
- Before the consultation: identity check, proxy details, a check for minors, consent stored with version and time, and recording off by default (TEL-03).
- Encounter documentation written back to the medical record (TEL-04).
- Remote prescribing rules (TEL-05), triage and escalation with fallback to a phone call (TEL-06).
- Clinicians outside Oman registered with the Ministry of Health (TEL-07). Teleradiology (TEL-08).

## 13. Patient-facing language and notices

PDPL-14, MOH-17, MDV-08; NAT-13 for government apps

- A privacy policy published before processing, in Arabic and English, versioned and linked from consent forms (PDPL-14).
- A patient rights charter in Arabic and English for private facilities (MOH-17).
- Instructions for use in Arabic and English for medical device software (MDV-08).
- Government mobile apps in Arabic and English, with a privacy statement shown before use (NAT-13).

## 14. Marketing and promotion

PDPL-31, MOH-27, RX-05

- Marketing consent separate from care messages, unticked by default, per channel, with evidence and an easy way to stop (PDPL-31). Look for marketing flags that default to true.
- Advertising of services and practitioners (MOH-27), and promotion of medicines, which needs a Drug Safety Center licence (RX-05).

## 15. Prescribing and pharmacy

MOH-22, RX-01 to RX-07, INS-15, TEL-05

- Every required prescription field mandatory, with the prescriber's identity and licence number (RX-02, MOH-22).
- Controlled drugs stay on official paper forms unless the Drug Safety Center confirms an electronic route (RX-03).
- Dhamani e-prescriptions for insured patients (INS-15), and online ordering run as a channel of a licensed pharmacy (RX-06).

## 16. Source code and CI hosting

PDPL-28 to PDPL-30, MOH-14; NAT-21 for government providers

Where the repository and CI runners are hosted, if they can contain patient data. For government software held in escrow, the code may not be published on a public cloud platform outside Oman without permission (NAT-21).

## 17. Possible additional checks (not in the library)

Raise these only as questions, under "Possible additional requirements (not in library)":

- Tax Authority e-invoicing and VAT rules for any billing module
- PCI DSS where the system takes card payments
- sender registration for SMS messages to patients
- accessibility standards for patient apps outside government
- how long telehealth recordings and chat logs are kept

## 18. Things only people can answer

- the MTCIT permit, its scope and expiry (PDPL-07 to PDPL-09)
- the DPO, risk assessment and record of processing (PDPL-20, PDPL-23, PDPL-24)
- Cyber Defence Centre approval for data abroad (PDPL-29) and any designation (NAT-01)
- the hosting provider's TRA permit and data-centre category (NAT-04, NAT-07)
- processor and vendor contracts (PDPL-25, MOH-13)
- the Ministry of Health's approval of the information system (MOH-19), and any telehealth licence (TEL-01)
- FSA registration and the Dhamani connection (INS-03)
- medical device qualification and registration (MDV-02 to MDV-04)
- the national records retention schedule the facility follows (MOH-15)
- team location, remote access and, for government work, staffing (PDPL-30, NAT-22)

Use `questions.md`.
