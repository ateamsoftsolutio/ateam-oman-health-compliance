# Questions for the engineering team

Ask only what the code and documents couldn't answer. Group the questions into one round, offering your best guess where you have one. Record each answer with the person's name, marked "(stated)". If no name is given, record "Requester (stated)"; only a named person's answer can make an item Met (see `register-and-excel.md`). Route each question to the party that can answer it: the client (the facility, insurer or other controller) or the team building the system.

## Scope (asked first, in Step 1 of the check skill)

1. What does the system do, and who uses it (clinicians, patients, admin staff, insurers, pharmacists)?
2. Who is the customer?
   - a government health provider (a Ministry of Health hospital or health centre, or another government health body)
   - a private hospital, clinic, laboratory or pharmacy
   - an insurer, TPA or revenue cycle management (RCM) company
   - a product sold to many
3. Has the Cyber Defence Centre treated the customer as a "concerned entity" or as critical infrastructure, or given it directions? If unknown, say so.
4. Does it have AI features? Does any of them diagnose, treat, monitor, triage or support clinical decisions? Is any of it imaging AI?
5. Does it offer telehealth or virtual care? Teleradiology?
6. Does it handle insurance eligibility, prior approval or claims (Dhamani)? Does it prescribe? Does it dispense medicines?
7. Does it exchange data with Ministry of Health systems: the Shifa national health record, e-referral, Tarassud notifications, or a Ministry facility's Al-Shifa hospital information system?
8. Where is it hosted (provider, region or data centre), including backups and disaster recovery?
9. Does it hold data on patients under 18?
10. Does it send marketing messages, use CCTV or staff biometrics, take electronic signatures, or make automated decisions about people (by AI or by rules)? Does the vendor host or run it for its customers?

## Follow-up questions (only where evidence is missing)

**Data outside Oman and offshore access** *(Blocker-priority for every scope)*:

- Do any engineers, support staff or vendors access production systems or patient data from outside Oman? If yes, from where, and on what basis?
- Has the Cyber Defence Centre approved storing or processing any health data outside Oman? Which services does the approval cover?
- Which third-party services receive any patient data (AI models, error tracking, analytics, messaging, video)? Where do they process it?
- Do development or testing ever use real patient data, in Oman or abroad?

**Hosting:**

- Which provider runs production, backups and disaster recovery? Does it hold a TRA permit, with a Category 4 data centre in Oman for this content? Can it list every data centre it uses for the content (NAT-04, NAT-05)?
- Does the vendor run the system as a hosted service for its customers? If so, has it checked whether it needs its own TRA permit (NAT-07)?

**PDPL governance** *(private providers, insurers and products)*:

- Does the controller hold an MTCIT permit for processing health data? What are its number, issue and expiry dates, and scope? Does the scope cover this system's purposes, processors and hosting locations?
- Has a data protection officer been designated, published and notified to MTCIT?
- Has a written risk assessment been done for the processing?
- Is there a breach runbook that meets the PDPL 72-hour notice to MTCIT and the Ministry of Health 24-hour internal report?
- Are there written contracts with every processor? Is there a record of processing activities?
- Are patients asked for explicit consent, or does the contract-based exception apply with the PDPL wording in the patient contract?

**Government customers:**

- Does the vendor use any of the data for its own purposes (analytics, product improvement)? If so, the PDPL may apply to the vendor.
- Is any data processed outside Oman, including through remote access? If so, which of the government policy's three purposes does it serve (a contract with the patient, legal claims, vital interests), and is Cyber Defence Centre approval in hand (PDPL-05)?
- Is the contracting entity based in Oman?
- Who fills the security, network, database, development, systems analysis and support roles? Are they Omani nationals, as MTCIT's circulars require for government work (NAT-22)?
- Has the customer agreed with MTCIT whether it must own the source code, and if so, by direct ownership or escrow (NAT-21)?

**Ministry of Health:**

- Has the Ministry approved the facility's electronic health information system (MD 231/2024 Art. 8(4))? If not, when is it due?
- Who is the health information management (HIM) lead and the health data protection officer under the National Policy?
- Which national retention schedule (National Records and Archives Authority) does the facility follow?
- Is the facility connected, or planning to connect, to the Shifa national health record? Has MOH provided the FHIR specification?

**Security:**

- When was the last penetration test, and did it cover mobile apps?
- Who runs security monitoring, and from where?
- Has the Cyber Defence Centre given the customer standards, controls or directions to follow?

**Electronic signatures and identity:**

- Which signature level is used for patient consent and clinician sign-off: simple, advanced or certified (NAT-25)?
- Does the client want national digital identity (Thiqa or ID card PKI) for login or signing (NAT-27)?

**Insurance (Dhamani):**

- Is the facility registered with the FSA and connected to Dhamani? Do you hold the Dhamani technical specification and a test environment?
- Who does revenue cycle management, and where are they based?

**AI and medical devices:**

- Where are models hosted and where does inference run? Is patient data used for training, and with what approval?
- Has anyone assessed whether the software is a medical device? In which reference jurisdiction, and in which class?
- Is the product registered or listed with the Drug Safety Center?

**Telehealth:**

- Does the facility hold an MOH licence for telehealth, and is the platform approved?
- Where are video, chat logs and recordings stored?
- Are any clinicians outside Oman? Are they registered with MOH?
