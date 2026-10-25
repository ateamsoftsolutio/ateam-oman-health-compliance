# Which requirements apply

Use the scope answers to pick requirements from the library: `library/national.md` (PDPL, NAT), `library/health-sector.md` (MOH, TEL) and `library/insurance-devices.md` (INS, MDV, RX). When in doubt, include the requirement and let the engineer mark it Not applicable with a reason.

## Who is the customer?

| Customer | What changes |
|---|---|
| **Government health provider**: a Ministry of Health hospital or health centre, or another government health body | The PDPL doesn't apply to a government unit's processing within its legal competences (PDPL-04). MTCIT's government Personal Data Protection Policy applies instead (PDPL-05): process in Oman and use Oman-based third parties. Processing abroad, including remote access from abroad, is allowed only for three purposes (a contract with the patient, legal claims, vital interests) and only with Cyber Defence Centre approval (PDPL-05, PDPL-30). Use PDPL-04, PDPL-05, PDPL-29 and PDPL-30 from the PDPL section, plus the government set of NAT items below. Name the other PDPL items once in `scope.md` as out of scope. Ask whether the vendor processes any data for its own purposes: if it does, the PDPL applies to the vendor for that processing. |
| **Private hospital, clinic, laboratory or pharmacy** | The PDPL applies in full, including the MTCIT permit for health data (PDPL-07 to PDPL-09). MD 231/2024 applies, including MOH approval of the electronic health information system (MOH-19). |
| **Insurer, TPA or RCM company** | The PDPL in full, plus the FSA rules for its role (INS-xx). The Ministry of Health's National Policy is written for health institutions, so MOH items aren't in an insurer's base set. Insurance-sector content is Level 3 by sector. The regulation doesn't say how health data held by an insurer is classed, so prefer a Category 4 data centre and ask the provider or an adviser. (NAT-04) |
| **Product sold to many facilities** | Each private customer is a controller with its own MTCIT permit, and the vendor is usually a processor (PDPL-25). Government customers come under the government policy instead (PDPL-05). Check the product against each customer type it will be sold to, and give customers a "permit pack" (PDPL-07). Record every customer type in `customerType`, select the sets for all of them, and say in an item's `notes` when it applies to only some (for example "Government customers only"). MOH-19 applies, because the product becomes part of the information system MOH approves at each private facility. |

The Ministry of Health's National Policy for Health Information Governance (MOH-xx) applies to government and private health institutions alike.

## Cybersecurity scope

The Cyber Defence Centre (CDC) System, Royal Decree 64/2020, binds "concerned entities": government bodies, private institutions in Oman within the CDC's remit, and bodies the Chairman of the Internal Security Service names. There is no public list, and no public designation of healthcare as critical national infrastructure was found. The CDC's own standards and controls aren't public either.

Use the customer type and the answer to scope question 3, and record the result in `cyberScope`:

| Answer | What applies |
|---|---|
| Government health provider (`Government`) | NAT-01 and NAT-02 in full, with the government set below |
| The client says the CDC has designated it or given it directions (`Designated by the CDC (stated)`) | NAT-01 and NAT-02 in full. Ask the client for the CDC standards and controls it was given, and check against them |
| Private, and designation isn't known (`Not known`) or the client says it isn't designated (`Not designated (stated)`) | NAT-01 and NAT-02 as Needs confirmation questions to the client, not hard requirements |

For a product sold to several customer types, record each type's value (for example "Government customers: Government; private clinics: Not known"). List NAT-01 and NAT-02 once, set the status for the stricter case, and say in `notes` how it differs for the others.

Whatever the answer, PDPL-29 still applies: MTCIT ties Cyber Defence Centre approval for data abroad to sensitive personal data, not to designation.

NAT-03 is the CDC rule behind PDPL-29, and NAT-18 is the government policy behind PDPL-05. Don't list them as separate items; cite them in the source of PDPL-29 and PDPL-05.

## Base set: every system processing health data of people in Oman

**Private providers and products:**

- PDPL-02 to PDPL-04, PDPL-07 to PDPL-09, PDPL-11 to PDPL-14, PDPL-16 to PDPL-18, PDPL-20 to PDPL-30, PDPL-32, PDPL-33
- MOH-01 to MOH-17, MOH-20 to MOH-22
- MOH-19 for private health establishments and products sold to them
- NAT-04 to NAT-06, NAT-08, NAT-24 and NAT-28. NAT-06 and NAT-08 are the cloud provider's duties: check the hosting contract and the provider's terms for them.

**Insurers, TPAs and RCM companies:** PDPL-02 to PDPL-04, PDPL-07 to PDPL-09, PDPL-11 to PDPL-14, PDPL-16 to PDPL-18, PDPL-20 to PDPL-30, PDPL-32, PDPL-33; NAT-04 to NAT-06, NAT-08, NAT-24 and NAT-28; the INS items for the role, from the add-ons; MOH-13 for an RCM company working under a provider's contract. For NAT-04: Insurance-sector content is Level 3 by sector. The regulation doesn't say how health data held by an insurer is classed, so prefer a Category 4 data centre and ask the provider or an adviser.

**Government health providers:** PDPL-04, PDPL-05, PDPL-29, PDPL-30; MOH-01 to MOH-17, MOH-20 to MOH-22; NAT-01, NAT-02, NAT-04 to NAT-06, NAT-08 to NAT-12, NAT-14 to NAT-17, NAT-21, NAT-22, NAT-24 and NAT-28. Add NAT-13 for a mobile app; NAT-19 for integration with other government systems, including the Ministry's own Al-Shifa hospital information system; NAT-20 if the system receives civil registry data that comes from the National Records Centre, directly or through another system; and NAT-23 if the vendor runs, hosts or supports the system for the unit (a managed service, including vendor-hosted SaaS with support). Don't add PDPL items from the add-ons table for a government provider: the government policy (PDPL-05) covers those topics. The exception is a vendor that uses the data for its own purposes (see the customer table). For a government provider, automated decisions are covered by MOH-25 and NAT-30, and consent for children by MOH-03 (consent through a guardian when the patient lacks capacity).

PDPL-01 (no grace period) and PDPL-34 (penalties), where the PDPL applies, and INS-01 (who regulates insurance), where insurance is in scope, are status or penalty provisions. Record them as **Informational**.

List each ID once, even when the base set and an add-on both name it.

When the scope says nothing about a feature, ask about it in the question round rather than selecting its items. "When in doubt, include" is for features you know exist but aren't sure trigger an item.

## Add-ons by feature or situation

For a government health provider, leave out the PDPL items in this table (see the base set). For an insurer, TPA or RCM company, leave out the MOH and TEL items, apart from MOH-13 for an RCM company working under a provider's contract.

| If the system… | Add |
|---|---|
| Stores or processes data outside Oman, uses an offshore service that receives health data (AI models, error tracking, analytics, messaging, video, backups), or gives offshore staff remote access | PDPL-28, PDPL-29, PDPL-30, MOH-13, MOH-14 |
| Has AI features of any kind | PDPL-13, PDPL-19, MOH-25, NAT-30; MOH-26 for imaging AI |
| Makes automated decisions about people, by AI or by rules (triage or priority, eligibility, claim decisions, fraud flags) | PDPL-19 |
| Might have a medical purpose (diagnosis, treatment, monitoring, triage, dose calculation, clinical decision support), or is part of a medical device | **Gate first:** add MDV-02 and MDV-03 only, as the qualification question. Add MDV-01 and MDV-04 to MDV-09 only once the software is confirmed as a medical device. MDV-10 goes in the watch items, not the register. Records, scheduling, billing and e-prescribing without dose calculation or decision support don't trigger the gate on their own. |
| Offers telehealth or virtual care | TEL-01 to TEL-07; TEL-08 for teleradiology |
| Handles insurance eligibility, prior approval or claims | INS-03 to INS-08 and INS-16; INS-01 and INS-02 as Informational; INS-11 if an RCM company is involved; INS-15 for e-prescriptions to pharmacies; RX-07 when claims include medicines. For a government provider, follow the FSA's Dhamani specification (INS-16), and ask whether the national integration platform (NAT-19) is involved |
| Is an insurer, TPA or insurer platform | INS-09, INS-10, INS-12, INS-13, INS-14 |
| Supports prescribing | RX-02, RX-03, RX-07; TEL-05 with telehealth; INS-15 for insured patients |
| Is a pharmacy or dispensing system | RX-01 to RX-07 |
| Exchanges data with the Shifa national health record | MOH-18 |
| Sends or receives electronic referrals with Ministry of Health facilities | MOH-23 |
| Uses patient data for research, or to train or evaluate AI models | PDPL-06, PDPL-13, MOH-24 |
| Holds data on patients under 18, or adults who lack capacity | PDPL-15 |
| Sends marketing messages, or promotes services, practitioners, medicines or devices | PDPL-31; MOH-27 if a health institution promotes its services or practitioners; RX-05 if it promotes medicines; MDV-08 if it promotes a medical device |
| Uses staff biometrics or CCTV | PDPL-10 |
| Takes electronic signatures (signed consent forms, clinician sign-off, signed reports or prescriptions) | NAT-25 and NAT-27; NAT-26 if it issues certificates, electronic seals or identity checks to other organisations. A tick-box consent is covered by PDPL-11 and NAT-24 in the base set |
| Tracks patients' location, records calls or stores patient photos or video, or offers medicines online | NAT-29 (live video consultations that aren't recorded don't count) |
| Is hosted or run by the vendor for its customers, as a product (SaaS) or as a bespoke system in the vendor's own cloud account | NAT-07, as a question where the arrangement isn't clear |
| Holds patient data in the source code repository, CI logs or build artefacts | Treat the git service and CI region as storage and processing under PDPL-28 to PDPL-30 and MOH-14 |

## Always ask: offshore access and development

- Health data stored or processed outside Oman needs Cyber Defence Centre approval first (PDPL-29).
- The Ministry of Health allows health data to be hosted abroad only for software as a service, only where no Omani alternative exists, and only with that approval (MOH-14).
- For private providers, whether remote access from outside Oman to data hosted in Oman counts as a transfer, or as processing outside Oman, is not settled (PDPL-30). Until an adviser says otherwise, treat it as both.
- For government providers, the government policy settles it: remote access from abroad is a transfer, allowed only for the policy's three purposes and with CDC approval (PDPL-05). Treat offshore support and offshore AI APIs as not allowed unless the client confirms otherwise in writing.
- Telehealth platforms, teleradiology and imaging AI must be hosted in Oman (TEL-02, TEL-08, MOH-26).
- Revenue cycle management companies must carry out their operations inside Oman (INS-11).
- Clinicians outside Oman who treat patients in Oman must be registered with MOH (TEL-07).
- For government customers, security, network, database, development, systems analysis and technical support roles must be held by Omani nationals, including at ICT contractors and subcontractors (NAT-22). Ask how the delivery team is staffed.

Include this as a **Blocker-priority question** for every scope. It matters most for teams with offshore engineering or support. Flag it; don't decide it.

## Pending changes to watch

Mention those that touch the scope in every summary:

- The PDPL Executive Regulations haven't been updated for Royal Decree 68/2026 (in force 7 September 2026). New rules are expected on objections to automated decisions, permit exceptions and marketing consent.
- The Ministry of Health plans to activate its National Policy in private hospitals in 2026, and to expand FHIR integration with the Shifa national record in 2026 and 2027.
- High-risk (Class C and D) medical devices and their manufacturers must be registered by 31 December 2026 (MDV-04).
- The Gulf Health Council's central registration and Ta'awon 2.0 may change how devices are registered (MDV-10).
- Dhamani's pharmacy e-prescription roll-out (INS-15).
- The Electronic Transactions Law (Royal Decree 39/2025) is waiting for its executive regulation, which will set trust-service licensing.
- The CDC's National Cybersecurity Strategy 2026–2030 makes updated legislation a priority. Watch for a cybersecurity law, critical infrastructure rules or published national controls.
- MTCIT's Cloud First Policy 2026 is a version 0.4 document, and the CDC's circular on external cloud services (6/2025) isn't public.
- The cybercrime law was replaced by Royal Decree 61/2026 on 8 June 2026. Update anything that still cites Royal Decree 12/2011.

## Items that are partly unconfirmed

Keep the confirmed part as the requirement, and add the unconfirmed detail as a question in the same item. Use Needs confirmation only when the outcome depends on the unconfirmed detail. If the confirmed part alone already shows a gap, mark it Missing (or Partly met) and keep the question open.

## Conflicting rules

Some Ministry of Health documents conflict with each other (for example on when the patient breach-notice clock starts, and on showing the diagnosis on sick-leave certificates). The library lists them under "Questions for advisers". Build to the stricter reading and record the question.

## Regulator value in the register

Use `PDPL/MTCIT`, `MTCIT` (government policy, AI policy and other MTCIT rules), `CDC`, `MOH`, `MOH/DSC` (medical devices and pharmacy), `FSA/Dhamani`, `TRA`, `Other law` (for example the Cybercrime Law or the Electronic Transactions Law) or `Internal`.

## What to list

List the base set and the add-ons that apply. Don't list library sections that don't apply to this scope. Instead, name them once in `scope.md` under "Out of scope", for example "PDPL-01 to PDPL-03, PDPL-06 to PDPL-28 and PDPL-31 to PDPL-34: Ministry of Health facility within its legal competences; the government policy applies (PDPL-05)". Use Not applicable only for items inside a selected set that don't apply, and give a reason.

## Who is responsible

Many duties belong to the client rather than the team building the system: the MTCIT permit, the DPO, risk assessments, Cyber Defence Centre approval, MOH licences and approvals, FSA registration, processor contracts. Record a `responsible` value on every item:

- `Client` (the controller, facility or licensee)
- `Vendor` (the team building or running the system)
- `Shared`

Route each question to the right party.
