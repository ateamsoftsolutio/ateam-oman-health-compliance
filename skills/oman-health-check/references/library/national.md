# National layer: data protection, cybersecurity, cloud, e-transactions and AI (Oman)

> **Library status:** researched from primary and secondary sources on 2026-10-17. Each item shows its source and confidence. Omani instruments are authoritative in Arabic; English wording here is a working translation, mostly AI-assisted from the Arabic, and is not official. Most texts were read on qanoon.om, an unofficial mirror of the Official Gazette. Rules change: check the "As of" note and the current official text before relying on an item, and treat "Unconfirmed" items as questions, not requirements. Engineering guidance, not legal advice.

Part of the Oman healthcare requirements library. Scope: the **national** layer. The Personal Data Protection Law (Royal Decree 6/2022, as amended by Royal Decree 68/2026) and its Executive Regulations, enforced by the Ministry of Transport, Communications and Information Technology (MTCIT) (PDPL-xx). Cybersecurity under the Cyber Defence Centre (CDC), the Telecommunications Regulatory Authority's (TRA) cloud and data-centre regulation, MTCIT's rules for government systems, the Electronic Transactions Law, national digital identity, the cybercrime law and MTCIT's AI policy (NAT-xx). Ministry of Health rules are in `health-sector.md`; health insurance, medical devices and pharmacy are in `insurance-devices.md`.

Researched: 2026-10-17. Not legal advice. The Arabic text of every Omani instrument prevails over any English translation.

---

## How to read this file

- **ID**: a stable identifier for one requirement (for example `PDPL-07`). IDs are not legal references; the legal reference is in the *Source* field.
- **Requirement**: what the rule requires, in plain language.
- **Engineering implication**: what the build team has to design, configure or produce.
- **Source**: the instrument, plus the article or clause number **only where it was checked** against the text, with a URL.
- **Confidence**:
  - **Confirmed (primary)**: checked against the official text, or its reproduction on qanoon.om with the Official Gazette reference, or a government website or form.
  - **Confirmed (secondary)**: taken from a reputable law-firm guide, academic paper or reputable news, because the primary text could not be read in full.
  - **Unconfirmed**: not verified. Do not build hard logic on it; ask.
- **As of 2026-10**: the status at the research date, including pending changes.
- **Applicability tags** in brackets: **[All]** any system processing health data of people in Oman; **[Gov]** Ministry of Health or other government health facilities and their vendors; **[Private]** private hospitals, clinics and other private providers; **[Insurer]** insurers and TPAs; **[Claims]** provider systems handling eligibility, prior approval or claims; **[Telehealth]**; **[AI]**; **[Device]** software that may be a medical device; **[Research]**; **[Prescribing]**; **[Pharmacy]**; **[HIE]** systems exchanging data with national platforms; **[CNI]** critical national infrastructure; **[Cloud]**.

---

## Key instruments

| Instrument | Issuer | Number and date | Binding on | Status at 2026-10 | Source URL |
|---|---|---|---|---|---|
| Personal Data Protection Law (PDPL) | Sultan (Royal Decree) | RD 6/2022, issued 9 Feb 2022; Official Gazette (OG) 1429, 13 Feb 2022; in force one year after publication (13 Feb 2023) | Controllers and processors, unless an Art 3 exemption applies | In force; amended by RD 68/2026 | https://qanoon.om/p/2022/rd2022006/ ; consolidated English (unofficial): https://decree.om/2022/l20220006/ |
| Amendments to the PDPL | Sultan (Royal Decree) | RD 68/2026, issued 3 Sep 2026; OG 1664, 6 Sep 2026; in force 7 Sep 2026 | As above | In force. No transition period stated. ER not yet aligned | https://qanoon.om/p/2026/rd2026068/ ; https://decree.om/2026/rd20260068/ |
| Executive Regulations of the PDPL (ER) | Minister of Transport, Communications and IT (MTCIT) | Ministerial Decision (MD) 34/2024, issued 28 Jan 2024; OG 1531, 4 Feb 2024; in force 5 Feb 2024 | Controllers and processors | In force. Compliance deadline passed on 5 Feb 2026. No later amendment found | https://qanoon.om/p/2024/mtcit20240034/ |
| Extension of the ER compliance period | MTCIT | MD 6/2025, issued 14 Jan 2025; OG 1580, 19 Jan 2025 | Those subject to the ER | Spent. Changed the period from one year to two years, which ended on 5 Feb 2026 | https://qanoon.om/p/2025/mtcit20250006/ |
| Fees for the personal data processing permit | MTCIT | MD 448/2025, issued 3 Dec 2025; OG 1625, 7 Dec 2025; effective 1 Jan 2026 | Applicants for Art 5 permits | In force | https://qanoon.om/p/2025/mtcit20250448/ |
| Judicial police powers for MTCIT data protection staff | Minister of Justice and Legal Affairs | MD 46/2025, issued 27 Feb 2025; OG 1586, 2 Mar 2025 | Holders of the "personal data protection specialist" post in MTCIT's Directorate General of Policies and Governance | In force | https://qanoon.om/p/2025/mjla20250046/ |
| Personal Data Protection Policy for Units of the State Administrative Apparatus | MTCIT | Circular 6/2024, dated 31 Mar 2024 | Government units (the PDPL does not apply to them) | Applies 24 months after adoption and circulation (about end of March 2026). Its legal force is debated | https://qanoon.om/p/2024/mtcit20240006/ |
| Cyber Defence Centre (CDC) System | Sultan (Royal Decree) | RD 64/2020, issued 10 Jun 2020; OG 1345, 14 Jun 2020 | "Concerned entities", including private-sector institutions in Oman linked to the CDC's remit | In force. Art 4(5): CDC approval before storing or processing sensitive data outside Oman | https://qanoon.om/p/2020/rd2020064/ |
| MTCIT data protection online services, FAQ, forms and guidance | MTCIT Personal Data Protection Department; Directorate General of Policies and Governance | Forms dated 2024 to 2026; guidance at version 0.1 (Dec 2025 to Sep 2026) | Forms are the ones the ER call "the form prepared for that". Guidance is non-binding | Published. Some items pre-date RD 68/2026 | https://mtcit.gov.om/sectors/governance/personal (Arabic: https://mtcit.gov.om/ar/sectors/governance/personal) |
| Child Law (definition of "child") | Sultan (Royal Decree) | RD 22/2014; OG 1058, 25 May 2014; Art 1(d) | Used here only to infer the PDPL age threshold | In force | https://qanoon.om/p/2014/rd2014022/ |
| Civil Transactions Law (legal capacity) | Sultan (Royal Decree) | RD 29/2013; Art 41 | Used here to read "full legal capacity" in ER Art 4 | In force | https://qanoon.om/p/2013/rd2013029/ |
| Regulation on Cloud Computing Services and Data Centres | Telecommunications Regulatory Authority (TRA) | Decision 1152/2/19/2024-20, 26 Sep 2024; Official Gazette 1564, 29 Sep 2024 | Anyone providing cloud computing or data-centre services in Oman (permit holders and fixed public telecom licensees) | In force since 30 Sep 2024; 6-month period to comply has ended | https://qanoon.om/p/2024/tra20249905/ |
| Electronic Transactions Law | Sultan | Royal Decree 39/2025, 9 Apr 2025; Official Gazette 1591, 13 Apr 2025 | Everyone (electronic transactions, documents, signatures, trust services) | In force since 14 Apr 2025. Repealed RD 69/2008. Executive regulation not found | https://mtcit.gov.om/library-3/legislations-policies-8/laws-75/electronic-transactions-law-1031 |
| Law on Combating Information Technology Crimes | Sultan | Royal Decree 61/2026, 1 Jun 2026; Official Gazette 1651, 7 Jun 2026 | Everyone | In force since 8 Jun 2026. Repealed the Cybercrime Law, RD 12/2011 | https://mtcit.gov.om/library-3/legislations-policies-8/laws-75/cybercrime-combat-law-1030 |
| Law on Classification of State Documents and Regulation of Protected Places | Sultan | Royal Decree 118/2011; Official Gazette 949, 29 Oct 2011; amended, including by RD 26/2019 (24 Apr 2019) | Government units and their staff | In force | https://qanoon.om/p/2011/rd2011118/ |
| National Records Law | Sultan | Royal Decree 52/2024, 3 Nov 2024; Official Gazette 1570, 10 Nov 2024 | State administrative units, other public legal persons, companies over 40% state-owned, certain concession holders | In force | https://qanoon.om/p/2024/rd2024052/ |
| Cloud First Policy 2026 (updates the 2021 Cloud First / Cloud Computing Policy) | MTCIT | Ministerial Circular 10/2026, 14 Jun 2026; policy v0.4 | State administrative units (not security or military units); also distributed to the private sector | In force from circulation | https://mtcit.gov.om/library-3/legislations-policies-8/policies-73/cloud-first-policy-1416 |
| Cloud and Hosting Services Standard v1.0 | MTC (now MTCIT) | Ref. GC_S2, 17 May 2018; issued 2019 | Cloud providers serving government agencies | Still in MTCIT library; fit with newer rules unclear | https://mtcit.gov.om/library-3/guidelines-documentation-7/standards-64/cloud-and-hosting-services-standard-263 |
| IT Risk Management Policy | MTCIT | Ministerial Circular 3/2026, 5 Mar 2026; policy dated Feb 2026, v0.1 | State administrative units and their external IT providers and contractors | In force from circulation | https://mtcit.gov.om/library-3/legislations-policies-8/policies-73/it-risks-management-policy-1277 |
| IT Operations Continuity Policy v2 | MTCIT | Listed as Circular 4/2026, 12 Apr 2026; policy dated Apr 2026 | State administrative units | In force from circulation | https://mtcit.gov.om/library-3/legislations-policies-8/policies-73/it-operations-continuity-policy-1328 |
| General Electronic Integration Policy | MTCIT | Ministerial Circular 16/2026, 7 Sep 2026 | State administrative units; bodies integrating with them, including private sector under approved controls | In force from circulation | https://mtcit.gov.om/library-3/legislations-policies-8/policies-73/general-electronic-integration-policy-388 |
| Regulatory Framework for National Data Governance and Management (NDGF) | MTCIT | Ministerial Circular 2/2025 and cover letter 113/2025, both 14 Jan 2025 | State administrative units and other public legal persons | In force; framework documents link now returns 404 | https://mtcit.gov.om/library-3/guidelines-documentation-7/circulars-66/ministerial-circular-on-the-regulatory-framework-for-national-data-governance-and-management-762 |
| Governance of software development, use and publication in government units | MTCIT | Ministerial Circular 20/2025, 9 Oct 2025 | State administrative units (and so their software suppliers by contract) | In force | https://mtcit.gov.om/web/content/mtcit.content/1265/attachment?download=True |
| Administrative Standards for Managed Services | MTCIT | Circular 7/2025, 9 Mar 2025 | State administrative units buying managed IT services | In force | https://mtcit.gov.om/library-3/guidelines-documentation-7/circulars-66/administrative-standards-for-managed-services-technical-support-infrastructure-information-systems-755 |
| Basic Standards for Developing Government Mobile Applications | MTCIT | Ministerial Circular 19/2023, 28 Nov 2023 | State administrative units | In force | https://mtcit.gov.om/web/content/mtcit.content/775/attachment?download=True |
| Security assessments for government websites, portals and applications | MTCIT | Ministerial Circular 11/2022, 25 Jul 2022 | State administrative units | In force | https://mtcit.gov.om/library-3/guidelines-documentation-7/circulars-66/the-necessity-of-adhering-to-conducting-security-assessments-for-websites-portals-service-windows-and-government-electronic-applications-827 |
| Basic Standards for Database Security | MTC | Circular 3/2020, 5 Apr 2020 | State administrative units | In force as far as found | https://mtcit.gov.om/web/content/mtcit.content/1098/attachment?download=True |
| Omani-only staffing for IT roles | MTC / MTCIT | Circular 7/2020, 5 Jul 2020; Ministerial Circular 11/2021, 3 Jun 2021 | State administrative units, government companies and their ICT providers | In force as far as found | https://mtcit.gov.om/web/content/mtcit.content/1100/attachment?download=True ; https://mtcit.gov.om/web/content/mtcit.content/1102/attachment?download=True |
| Information Security Management Policy v1.0 | ITA (now MTCIT) | Sep 2019; circulated as Circular 4/2019 (per Circular 19/2023) | Government administrative units | In force; no replacement found | https://cert.gov.om/files/laws/Information_Security_Management_Policy_EN.pdf |
| Basic Security Controls v1.0 | ITA (now MTCIT) | 30 Jul 2017 | Guidance baseline for government organisations | Published; guidance wording | https://cert.gov.om/files/laws/Basic_Security_Controls_EN.pdf |
| Security Assessment Services Standard | MTC (now MTCIT) | 2019 | Security assessment providers serving government (accreditation) | Published | https://mtcit.gov.om/web/content/mtcit.content/264/attachment?download=True |
| Public Policy for Safe and Ethical Use of Artificial Intelligence Systems | MTCIT | Apr 2025, v0.1 (in force 9 Apr 2025 per decree.om) | Government units; private bodies regulated by sector regulators that develop or use AI | In force as policy; commentators say not legally binding | https://mtcit.gov.om/library-3/legislations-policies-8/policies-73/general-policy-for-the-safe-and-ethical-use-of-artificial-intelligence-systems-291 |
| National Cybersecurity Strategy 2026–2030 | Cyber Defence Centre | Reported 29 Aug 2026 | Strategy (not a binding rule) | Launched | https://www.muscatdaily.com/2026/08/29/oman-unveils-2026-2030-cybersecurity-strategy/ |
| Artificial Intelligence Special Zone | Sultan | Royal Decree 50/2026, 30 Apr 2026; Official Gazette 1646, 3 May 2026 | Economic zone; no AI rules | In force | https://decree.om/2026/rd20260050/ |

---

## Requirements

### A. Scope, exemptions and government units

#### PDPL-01: Comply now, because no grace period remains [All]
- **Requirement**: The PDPL has been in force since 13 February 2023. The ER came into force on 5 February 2024. MD 6/2025 extended the ER compliance period from one year to two, and it ended on 5 February 2026. RD 68/2026 amended the law with effect from 7 September 2026 and gives no transition period.
- **Engineering implication**: Treat every item in this file as live for any Oman deployment. Make release checklists block go-live when a mandatory control is missing: permit, consent capture, rights handling, breach process or transfer controls. Give the controls added by RD 68/2026 a dated fix plan now, not a roadmap slot. These are objections to automated decisions, erasure at end of purpose, explicit consent for marketing and the wider offshore scope.
- **Source**: RD 6/2022, Article Four of the decree (in force one year after publication), https://qanoon.om/p/2022/rd2022006/ . MD 34/2024, Articles Two and Four of the decision, https://qanoon.om/p/2024/mtcit20240034/ . MD 6/2025, Article One, https://qanoon.om/p/2025/mtcit20250006/ . RD 68/2026, Article Three of the decree, https://qanoon.om/p/2026/rd2026068/ . CMS (Feb 2026) and Trowers (Jun 2026) both give 5 Feb 2026 as the end of the transition, https://cms.law/en/omn/legal-updates/oman-personal-data-protection-law-entering-the-enforcement-phase
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: All in force. One secondary source (Trowers, Feb 2024) gives 29 Jan 2024 as the ER start date. The Gazette-based reading is 5 Feb 2024, and that is consistent with the 5 Feb 2026 deadline that CMS and Trowers report.

#### PDPL-02: The law now reaches processing outside Oman [All] [Telehealth] [AI]
- **Requirement**: Since 7 September 2026 the law applies to the processing of personal data of natural persons in Oman, whether the processing happens inside or outside Oman. Before that, Art 2 said only that the law applies to personal data that is processed.
- **Engineering implication**: Apply Omani PDPL controls to any system that processes data of people in Oman, wherever it is hosted. This includes offshore telehealth, SaaS, AI services and support centres. Store a jurisdiction attribute on data-subject records, such as country of residence or location at collection, so that Omani rules can be applied and reported. Offshore vendors should budget for an Omani permit, a DPO, consent capture and breach handling.
- **Source**: PDPL Art 2 as replaced by RD 68/2026, Art 2 of the attached amendments. https://qanoon.om/p/2026/rd2026068/ ; https://decree.om/2026/rd20260068/
- **Confidence**: Confirmed (primary). The meaning of "natural persons in the Sultanate of Oman" is Unconfirmed: it could mean residents, people physically present, or both.
- **As of 2026-10**: In force since 7 Sep 2026. We found no MTCIT guidance on the new scope.

#### PDPL-03: Classify health, genetic and biometric data as sensitive, and record the roles [All] [Device] [Insurer]
- **Requirement**: The key definitions are as follows.
  - **Personal data**: data that identifies a natural person, or makes them identifiable, directly or indirectly. This can be by identifiers such as name, civil number, electronic identifiers or location data. It can also be by factors of genetic, physical, mental, psychological, social, cultural or economic identity.
  - **Health data** (redefined in 2026): personal data about a person's physical, mental or psychological health, or about the healthcare services provided to them, that reveals their health status.
  - **Genetic data**: data on inherited or acquired genetic characteristics that results from analysis of a biological sample.
  - **Biometric data**: data from specific technical processing of physical, psychological or behavioural characteristics, such as a facial image or DNA fingerprint data.
  - **Sensitive data (the Art 5 list)**: genetic, biometric and health data; racial origin; sex life; political or religious opinions or beliefs; criminal convictions; and data on security measures.
  - **Controller** (redefined in 2026): the *legal person* that processes the data itself or entrusts the processing to a processor.
  - **Processor**: the person who processes on the controller's behalf.
  - **Automated processing** (new): processing by a programme or system that runs automatically, either with no human involvement or with only limited human supervision.
- **Engineering implication**: Build a data classification scheme. Tag every field, table, document and event stream as ordinary personal data, health, genetic, biometric or another Art 5 category. Treat appointment, referral, billing, claims, pharmacy and device telemetry data as health data when they reveal health status. Treat face images (photos, face ID) and fingerprints as biometric. Use the tags to drive permit scope, access control, encryption, transfer blocking and retention. For each deployment, record which legal person is the controller and who is the processor.
- **Source**: PDPL Art 1 ("health data" and "controller" replaced by RD 68/2026 Art 1; "automated processing" added by RD 68/2026 Art 3) and Art 5. https://qanoon.om/p/2022/rd2022006/ ; https://qanoon.om/p/2026/rd2026068/
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: The amended definitions have been in force since 7 Sep 2026.

#### PDPL-04: Check whether an Article 3 exemption applies, and record it [All] [Gov] [Research]
- **Requirement**: Under the amended Art 3, the law does not apply to processing for these purposes:
  - (a) national security or the public interest;
  - (b) "the performance by units of the State's administrative apparatus and other public legal persons of the competences assigned to them by law". In Arabic: «تنفيذ وحدات الجهاز الإداري للدولة وغيرها من الأشخاص الاعتبارية العامة للاختصاصات المقررة لها قانونا»;
  - (c) the State's economic and financial interests;
  - (d) detecting or preventing a crime, on a formal written request from investigation authorities;
  - (e) a person's processing in a personal or family setting, unless the data is published;
  - (f) historical, statistical, scientific, literary or economic research by authorised entities, on conditions (see PDPL-06).

  Since 7 September 2026, four grounds are no longer scope exemptions: legal obligation, vital interests, performance of a contract with the data subject, and publicly available data. They now only remove the need for consent (see PDPL-12), so the rest of the law applies to them, including the Art 5 permit.
- **Engineering implication**: Keep an exemption register for each processing activity. It should record the Art 3 ground, the reasoning, who approved it and the date. Do not reuse pre-September 2026 analyses that relied on the contract, vital-interest or legal-obligation exemptions. Those activities now need full PDPL controls, including a permit if they involve health data.
- **Source**: PDPL Art 3 as replaced by RD 68/2026 Art 2. The original Art 3 is in RD 6/2022. https://qanoon.om/p/2026/rd2026068/ ; https://qanoon.om/p/2022/rd2022006/
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: In force. MTCIT's English permit application form (file dated Jan 2026) still asks applicants to confirm that none of the *old* ten exemptions applies, so a revised form is likely.

#### PDPL-05: Ministry of Health and other government facilities sit outside the PDPL but inside MTCIT's government policy [Gov]
- **Requirement**:
  - **PDPL exemption.** Under Art 3(b), processing by government units and other public legal persons in performing their legal competences is outside the PDPL. MTCIT's FAQ says: "The Law exempts state administrative units and other public legal entities from its scope of application. However, the Personal Data Protection Policy issued under Circular No. (6/2024), directed to state administrative units, applies to regulate their processing of personal data." So a Ministry of Health hospital acting within the Ministry's legal competences is outside the PDPL, and the Circular 6/2024 Policy applies instead.
  - **What the Policy requires.** Government units must:
    - protect all personal data they hold;
    - collect data lawfully and fairly, and only what is necessary;
    - keep data accurate and up to date;
    - not keep data in identifiable form once its purpose is exhausted;
    - get the person's knowledge and consent through a statement on the service application, which also covers disclosure to other government units;
    - apply security and organisational measures;
    - use processors and third parties only under a written contract that sets retention and deletion terms and gives the unit a right to audit security controls;
    - publish a privacy statement on their website (its annex lists the minimum content);
    - destroy data securely;
    - notify the CDC of any leak, damage or breach;
    - process personal data inside Oman. Processing abroad is allowed only to perform a contract with the data subject, to pursue or defend legal claims, or to protect vital interests, and only after CDC approval.
  - **Third parties.** The Policy defines a "third party" as an entity acting under the unit's supervision and *based in Oman*.
  - **Timing and oversight.** The Policy applies 24 months after adoption and circulation. MTCIT monitors compliance and reports the results to the Council of Ministers.
- **Engineering implication**: For Ministry of Health and other government deployments:
  - Host and process in Oman. Processing abroad is allowed only for the three purposes in the Policy (a contract with the data subject, legal claims, vital interests) and only with CDC approval, so CDC approval alone is not enough. Offshore replicas, backups, support access and AI APIs rarely fit those purposes: plan for none.
  - Contract through an entity based in Oman, with retention, deletion and audit-right clauses.
  - Publish a privacy statement in the web or app with the Policy's listed contents. These are: purpose; mandatory and optional fields; data types; how data is collected, stored and destroyed; who collects it; recipients, and whether data is processed outside Oman; the effect of not providing data; and the rights to know, access, get a readable copy and correct.
  - Build secure destruction and a breach runbook for notifying the CDC.
  - Keep evidence that the processing falls within the unit's legal competence.
  - If the vendor uses the data for its own purposes, such as analytics or product improvement, assume the PDPL applies to the vendor.
- **Source**: PDPL Art 3(b), https://qanoon.om/p/2026/rd2026068/ . MTCIT FAQ, English and Arabic, https://mtcit.gov.om/sectors/governance/personal . MTCIT Circular 6/2024: definitions, Policy sections 1.1 to 1.13 and 2.1 to 2.2, document-management item 2, compliance item 1 and the privacy-notice annex, https://qanoon.om/p/2024/mtcit20240006/
- **Confidence**: Confirmed (primary) for the exemption text, MTCIT's position and the Policy content. Unconfirmed: whether the exemption covers a private vendor's processing for the Ministry of Health, and how binding the Policy is. decree.om says Omani policies are not legally binding and the Policy has no penalties.
- **As of 2026-10**: The Policy has applied from about 31 Mar 2026 (24 months after the circular dated 31 Mar 2024). Confirm the actual circulation date.

#### PDPL-06: Research is exempt only under conditions [Research]
- **Requirement**: Research processing is outside the law only if all three conditions are met. The purpose is historical, statistical, scientific, literary or economic research. The work is done by an entity authorised to carry it out. Published research and statistics contain no indication or reference to the data subject, so that no data can be attributed to an identified or identifiable person. Research that does not meet these conditions is fully subject to the law, including consent, the Art 5 permit and the transfer rules.
- **Engineering implication**: For research data pipelines:
  - record the authorising body and the approval reference;
  - make published outputs de-identified or aggregated, with disclosure checks before release (for example, suppressing small cells and stripping identifiers);
  - keep research extracts separate from clinical systems, with access logging.

  If the entity is not "authorised", or its outputs could identify people, apply full PDPL controls.
- **Source**: PDPL Art 3(f) as replaced by RD 68/2026 (formerly Art 3(i)). https://qanoon.om/p/2026/rd2026068/
- **Confidence**: Confirmed (primary). Which bodies count as "authorised" (for example, research ethics committees) is Unconfirmed.
- **As of 2026-10**: In force. Its substance was unchanged by RD 68/2026.

### B. Permit for sensitive data

#### PDPL-07: Get an MTCIT permit before processing health, genetic or biometric data [Private] [Insurer] [Telehealth] [Device] [AI] [Research]
- **Requirement**: Processing genetic, biometric or health data, or any other Art 5 category, is prohibited unless the controller first gets a permit from MTCIT. The exceptions to consent in Art 10 bis (contract, legal obligation, vital interests, public data) do not lift the permit requirement. A breach of Art 5 carries a fine of OMR 15,000 to 20,000 (Art 28).
- **Engineering implication**: Make "permit in place" a release gate for any production processing of health, genetic or biometric data. Store the permit number, scope (purposes, data categories, processors, locations) and expiry in configuration, and check them in deployment pipelines. Build data-inventory exports that fill MTCIT's application form. For SaaS, telehealth or AI products sold to many clinics, each controller needs its own permit. Give customers a "permit pack": data categories, purposes, hosting locations, sub-processors and a security description.
- **Source**: PDPL Art 5 and Art 28; ER Art 5; MTCIT FAQ ("What data requires a permit from the Ministry before processing?"). https://qanoon.om/p/2022/rd2022006/ ; https://qanoon.om/p/2024/mtcit20240034/ ; https://mtcit.gov.om/sectors/governance/personal
- **Confidence**: Confirmed (primary). Whether processors need their own permit is Unconfirmed. ER Art 5 puts the duty on the controller, but MTCIT's online service form asks for the "Name of the Controller/Processor".
- **As of 2026-10**: In force. Before 7 Sep 2026, processing to perform a patient contract could arguably fall outside the law under the old Art 3(g). Since then it cannot. Government units within Art 3(b) do not apply for permits.

#### PDPL-08: Permit application content and decision procedure [Private] [Insurer] [Telehealth] [Device] [AI] [Research]
- **Requirement**:
  - **Application content.** Apply on MTCIT's form with:
    - the DPO's name, address and email;
    - the purpose of the processing;
    - the identification and classification of the data;
    - any processor to be contracted;
    - any third parties that will receive the data;
    - the places where the data will be transferred or stored;
    - the data management and protection systems;
    - anything else MTCIT asks for.
  - **Attachments.** Attach the personal data protection policy and the precautionary measures adopted for breaches.
  - **Decision.** MTCIT decides within 45 days of receiving a complete file. A refusal must give reasons, and silence counts as refusal.
  - **Grievance.** The applicant can lodge a grievance with the Minister within 60 days. No reply within 30 days counts as rejection.
  - **Online service.** MTCIT's online "Permits Services" (New, Renew, Amend, Cancel, Appeal) ask for a subject, DPO name, Civil ID, phone, email, controller or processor name, commercial registration (CR) number and attachments.
  - **January 2026 form.** The English form dated January 2026 also asks for: sector (for example "Health"), website, DPO phone, how far the processing is consistent with its purpose, and transfers outside Oman with their safeguards. It also asks for declarations that no Art 3 exemption applies and that the data will not be used for other purposes.
- **Engineering implication**: Build a "permit dossier" generator from the data inventory: purposes, data categories and classification, processors, recipients, storage and transfer locations, and security controls. Keep the privacy policy and a written breach-precautions plan ready as attachments. Plan release dates around the 45-day decision period. Keep a submission log with date, reference and decision.
- **Source**: ER Arts 5, 6, 7. https://qanoon.om/p/2024/mtcit20240034/ . MTCIT data protection page (Permits Services), https://mtcit.gov.om/sectors/governance/personal . English permit form, file dated Jul 2024: https://mtcit.gov.om/web/content/65556 . English permit form, file dated Jan 2026: https://mtcit.gov.om/web/content/55067
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: Two versions of the form are online. The January 2026 version lists the pre-amendment exemptions.

#### PDPL-09: Permit lifecycle: 5-year validity, fees, change notices and cancellation [Private] [Insurer] [Telehealth] [Device] [AI] [Research]
- **Requirement**:
  - **Validity.** The Minister issues the permit for up to 5 years, after the fee is paid. It can be renewed for the same period by the same procedure.
  - **Fees from 1 January 2026, for issue or renewal:**
    - OMR 30 for holders of an entrepreneurship card;
    - OMR 60 for small and medium enterprises;
    - OMR 210 for other establishments and companies.
  - **Changes.** Notify MTCIT on the form of any change to the permit data within 15 days of making the change.
  - **Cancellation.** The permit is cancelled:
    - at the controller's request;
    - for a breach of the law or the ER;
    - for failing to notify changes in time;
    - if it was obtained by fraud or false information.
  - **Administrative sanctions.** These include suspending or cancelling the permit.
- **Engineering implication**: Keep a permit register with expiry alerts, for example six months ahead. Build change control so that any change to purposes, data categories, processors or sub-processors, recipients, hosting or transfer locations, security systems or the DPO raises an MTCIT amendment notice within 15 days. Link infrastructure changes, such as a new cloud region or a new vendor, to this workflow.
- **Source**: ER Arts 8, 9, 10 and 44, https://qanoon.om/p/2024/mtcit20240034/ . MD 448/2025, Articles One and Two, https://qanoon.om/p/2025/mtcit20250448/ . MTCIT amendment, renewal and cancellation forms: https://mtcit.gov.om/web/content/29069 ; https://mtcit.gov.om/web/content/29068 ; https://mtcit.gov.om/web/content/29067
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: The fees have applied since 1 Jan 2026.

#### PDPL-10: Permit exceptions for staff data and CCTV [All]
- **Requirement**: Since 7 September 2026, a controller may process Art 5 categories without a permit in three cases.
  1. Its own staff's data, if the processing is for internal organisation of work, complies with the law, and the data is not disclosed to third parties without the person's written consent.
  2. Surveillance devices and cameras used to meet security requirements issued by the competent authorities.
  3. Other cases set by a decision of the Minister, under controls to be set in the ER.
- **Engineering implication**: Separate staff systems (fingerprint or face attendance, staff health records) and security CCTV from patient data, so the exception can be applied cleanly. Block third-party sharing of staff sensitive data unless written consent is recorded. The exception does not cover patient biometrics (for example face check-in) or CCTV analytics beyond the security requirement. Those need a permit.
- **Source**: PDPL Art 5 bis (added by RD 68/2026 Art 4). https://qanoon.om/p/2026/rd2026068/
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: In force since 7 Sep 2026. We found no Minister's decision under Art 5 bis(3).

### C. Consent, purpose and transparency

#### PDPL-11: Explicit consent: content, form and proof [All]
- **Requirement**:
  - **Default rule.** Unless an Art 10 bis exception or an Art 3 exemption applies, personal data may be processed, or its purpose changed, only in a framework of transparency, honesty and respect for human dignity, and with the data subject's explicit consent. The controller must be able to prove that consent.
  - **The consent request.** It must be written clearly, explicitly and understandably. It must include:
    - the controller's details, and the processor's if any;
    - how to contact the DPO;
    - the objectives and nature of the processing;
    - any other information needed.
  - **Validity (ER).** Consent counts only if it is:
    - given by a person with full legal capacity (the Civil Transactions Law gives full capacity at 18 to a person of sound mind who is not under interdiction);
    - clear and free of coercion;
    - written, electronic or given by another means the controller sets.
  - **MTCIT template.** MTCIT's consent template (cover dated September 2026) sets a minimum content list:
    - controller name, CR number and contact details;
    - objectives (its example: "providing healthcare");
    - specific purposes (its example: "registration in health insurance");
    - data types;
    - sharing, and transfers abroad;
    - the retention period;
    - rights and how to use them;
    - an explicit consent statement.

    It also says withdrawal must be possible.
  - **Penalty.** A breach of Art 10 carries a fine of OMR 500 to 2,000 (Art 25).
- **Engineering implication**: Build a consent service with:
  - versioned Arabic and English consent texts that hold all mandatory elements;
  - unticked, granular checkboxes or signature capture;
  - records of who consented, which text version, when, by what channel, and on what capacity basis (self, guardian or curator);
  - a tamper-evident consent ledger;
  - a withdrawal API that stops dependent processing;
  - a re-consent flow when the text or purpose changes.
- **Source**: PDPL Art 10 and Art 25 (both replaced by RD 68/2026), https://qanoon.om/p/2026/rd2026068/ . ER Art 4, https://qanoon.om/p/2024/mtcit20240034/ . Civil Transactions Law Art 41, https://qanoon.om/p/2013/rd2013029/ . MTCIT consent template (Arabic), https://mtcit.gov.om/web/content/65865
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: In force. ER Art 4 is unchanged. The MTCIT template is the first MTCIT guidance to cite RD 68/2026.

#### PDPL-12: When consent is not needed (Art 10 bis) [Private] [Insurer] [Telehealth]
- **Requirement**: Explicit consent is not needed where the processing:
  - (a) fulfils a legal obligation on the controller under a law, judgment, order or court decision;
  - (b) uses publicly available data in a way that does not breach the law;
  - (c) protects a vital interest of the data subject when they cannot be contacted;
  - (d) performs a contract to which the data subject is a party, *provided the contract includes wording showing that the processing complies with the PDPL*.

  These grounds remove only the consent requirement. The permit, privacy policy, security, rights and transfer rules still apply.
- **Engineering implication**: Keep a lawful-basis register for each purpose. For example:
  - treatment: contract;
  - statutory reporting and record retention: legal obligation, with the legal citation;
  - emergency care: vital interest, with a "patient unreachable" reason logged;
  - marketing and AI training: consent.

  Add a PDPL clause to patient registration forms, treatment agreements, insurance policies and telehealth terms, and store the signed or accepted version. Make the emergency "break-glass" flow record its justification.
- **Source**: PDPL Art 10 bis (added by RD 68/2026 Art 4). https://qanoon.om/p/2026/rd2026068/ ; https://decree.om/2026/rd20260068/
- **Confidence**: Confirmed (primary). Unconfirmed: whether these exceptions also remove the separate explicit-consent condition for transfers abroad (ER Art 37).
- **As of 2026-10**: In force since 7 Sep 2026.

#### PDPL-13: Purpose limitation and secondary use, including AI training [All] [AI] [Research]
- **Requirement**: Changing the purpose of processing needs the data subject's explicit consent, unless an exemption or exception applies. The permit application includes a declaration that the data will not be used for any purpose other than the one stated. The law has no general "legitimate interests" basis.
- **Engineering implication**: Tag data with its collection purpose. Enforce purpose checks in data-access layers and analytics pipelines. Block copies of clinical data into analytics, product-improvement or model-training stores unless consent for that purpose is recorded or a research exemption is documented. Make sure the new purpose is also covered by the permit.
- **Source**: PDPL Art 10 (replaced by RD 68/2026, which added "or change the purpose of its processing"), https://qanoon.om/p/2026/rd2026068/ . MTCIT permit form declarations, https://mtcit.gov.om/web/content/55067
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: The change-of-purpose wording has been in force since 7 Sep 2026.

#### PDPL-14: Publish a privacy policy before processing [All]
- **Requirement**: The controller or processor must put its personal data protection policy in a visible place, so that data subjects can read it before their data is processed. At minimum, it must explain how to exercise rights.
  - **MTCIT's guide.** The guide and template (version 0.1, December 2025) suggest these sections: objectives; scope (data categories including Art 5 data, processing operations, purposes and the people covered); rights and the request channel; retention and secure disposal; DPO contact; security measures; breach procedures and notification timing; children's data; and transfers abroad.
  - **Notice duty.** The old Art 14 duty to give written notice before processing was replaced on 7 September 2026. Transparency now rests on the content of the consent request (Art 10) and on this policy.
- **Engineering implication**: Publish the policy on the website and in apps, including pre-registration screens and kiosks. Link to it from consent forms, and version and date it. Make it bilingual. CMS recommends Arabic as the primary version, but we found no legal rule on language. Keep earlier versions. The same policy is attached to the permit application.
- **Source**: ER Art 21, https://qanoon.om/p/2024/mtcit20240034/ . MTCIT policy guide and template (Arabic), https://mtcit.gov.om/web/content/55069 . PDPL Art 14 (replaced by RD 68/2026).
- **Confidence**: Confirmed (primary). The language rule is Unconfirmed.
- **As of 2026-10**: In force.

#### PDPL-15: Children and people who lack legal capacity [All] [Telehealth]
- **Requirement**:
  - **The law.** Processing a child's data needs the guardian's consent, unless the processing is in the child's best interest.
  - **The ER.** They require:
    - the guardian's *explicit* consent before processing;
    - the controller may ask the child for the minimum guardian details needed to verify the guardian and get their consent;
    - a purpose that is clear, direct, safe and not misleading;
    - only the minimum data;
    - a way for the guardian to access the child's data to update and amend it;
    - no disclosure to third parties without the guardian's explicit consent.
  - **People who lack capacity.** People with no, reduced or lost legal capacity are represented by their guardian, custodian or curator, and the same rules apply.
  - **Age.** Neither the PDPL nor the ER defines "child". The Child Law defines a child as anyone under 18 (Gregorian), and the Civil Transactions Law sets full capacity at 18.
  - **Penalty.** A breach of Art 6 carries a fine of OMR 15,000 to 20,000.
- **Engineering implication**:
  - Capture date of birth and flag patients under 18 as children.
  - Link guardians or proxies to the child, with identity checks and evidence of guardianship.
  - Give guardians a portal to view and update the child's record.
  - Block sharing of a child's data without recorded guardian consent.
  - Keep children's forms to the minimum.
  - Support proxy consent for adults who lack capacity, with curator or custodian documents stored.
  - Log when "best interest" is relied on, for example in urgent paediatric care.
- **Source**: PDPL Art 6 and Art 28, https://qanoon.om/p/2022/rd2022006/ . ER Arts 11 to 15, https://qanoon.om/p/2024/mtcit20240034/ . Child Law (RD 22/2014) Art 1(d), https://qanoon.om/p/2014/rd2014022/ . Civil Transactions Law (RD 29/2013) Art 41, https://qanoon.om/p/2013/rd2013029/
- **Confidence**: Confirmed (primary) for the rule. Using 18 as the PDPL age threshold is Unconfirmed, because it is inferred from other laws.
- **As of 2026-10**: In force. Not changed by RD 68/2026.

### D. Rights, erasure and automated decisions

#### PDPL-16: Data subject rights and the 45-day deadline [All]
- **Requirement**:
  - **The rights.** A data subject can:
    - withdraw consent (earlier processing is not affected);
    - ask for their data to be amended, updated or blocked;
    - get a copy;
    - move their data to another controller;
    - ask for erasure, unless the processing is needed for national archiving and documentation;
    - be told of any breach and the steps taken;
    - object to automated decisions (see PDPL-19);
    - complain to MTCIT.
  - **Procedure.** For the first five rights, the data subject makes a written request. It is free. The controller must decide within 45 days of receipt. The data subject may ask for processing to be suspended until the decision.
  - **Refusal.** The controller may refuse in whole or in part if the request is unjustifiably repetitive or needs extraordinary effort. It must give reasons within the same 45 days.
  - **MTCIT guidance.** The FAQ says controllers must provide a "window" (a channel) for exercising rights. MTCIT's rights template (file dated March 2026) suggests that a request gives the full name, civil number, the right requested, the data concerned and any supporting documents, and that the controller may verify identity.
- **Engineering implication**:
  - Provide a rights request portal or form in Arabic and English, across web, app, email and front desk.
  - Add an identity-verification step.
  - Run case management with a 45-day timer from receipt, reminders and escalation.
  - Add a "suspend processing" flag that downstream services respect.
  - Prepare templates for decisions and reasoned refusals.
  - Keep a full audit trail, and report to the DPO.
- **Source**: PDPL Arts 11, 12 and 14 (Art 14 as replaced). ER Arts 16 and 17, https://qanoon.om/p/2024/mtcit20240034/ . MTCIT FAQ, https://mtcit.gov.om/sectors/governance/personal . MTCIT rights template (Arabic), https://mtcit.gov.om/web/content/38034
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: In force.

#### PDPL-17: Copies and portability [All]
- **Requirement**: A copy must be in a readable, clear electronic or paper format, and must not include personal data that identifies anyone else. The data subject may move their data to a new controller. The ER say the controller transfers it to the new controller "if it is legally obliged to do so".
- **Engineering implication**: Build a patient-data export: a readable PDF plus a structured format such as JSON or HL7 FHIR. Redact other people's personal data, such as family members, other patients and, where appropriate, staff. Deliver securely, provide a controller-to-controller transfer package, and log what was released.
- **Source**: PDPL Art 11(c) and (d); ER Arts 19 and 20. https://qanoon.om/p/2024/mtcit20240034/
- **Confidence**: Confirmed (primary). The scope of "if legally obliged" in ER Art 20 is Unconfirmed.
- **As of 2026-10**: In force.

#### PDPL-18: Erase data when its purpose ends, and handle erasure requests [All]
- **Requirement**:
  - **Erasure at end of purpose.** Since 7 September 2026, the controller *and the processor* must erase personal data as soon as the purpose of processing ends. They must keep it only where there is an existing dispute with the data subject, or a legal obligation to keep it under a law, judgment, order or court decision.
  - **Erasure on request.** A data subject can ask for erasure when the purpose has ended, consent is withdrawn, or the processing breaks the law. The controller may refuse because of a legal obligation or an existing dispute.
  - **Processing documents.** These may be kept only for a specific, legitimate reason, for a period that fits the purpose, and with technical protection.
  - **Penalty.** A breach of Art 15 carries a fine of OMR 1,000 to 5,000 (Art 26).
- **Engineering implication**:
  - Keep a retention schedule per data category, citing the legal basis for each period. Medical-record retention periods come from health legislation, which is outside this file.
  - Run automated deletion or anonymisation jobs.
  - Add legal-hold flags for disputes.
  - Propagate deletions to replicas, backups (on rotation), caches, search indexes, analytics stores and processors.
  - Log deletion evidence.
  - Build an erasure-request workflow with reasoned refusals.
- **Source**: PDPL Art 11(e), Art 15 (replaced by RD 68/2026), Art 17 and Art 26. ER Arts 18 and 27. https://qanoon.om/p/2026/rd2026068/ ; https://qanoon.om/p/2024/mtcit20240034/
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: The Art 15 duty to erase at end of purpose is new from 7 Sep 2026.

#### PDPL-19: Automated processing and human review [AI] [Insurer] [Telehealth] [Device]
- **Requirement**: When using automated processing, the controller and processor must take suitable measures to protect the privacy and confidentiality of the data, and must not harm the data subject. Data subjects may object to decisions that result from automated processing. The controller or processor must then bring in a human to review the contested decision, under controls the ER are to set. "Automated processing" includes systems that run with only limited human supervision. A breach of Art 14 carries a fine of OMR 5,000 to 10,000 (Art 27).
- **Engineering implication**:
  - List the AI or rules-based decisions in scope: triage scores, appointment prioritisation, claim decisions, eligibility checks, fraud flags, and clinical decision support that drives outcomes.
  - For each one, tell users that the decision was automated and how to object.
  - Provide an objection button or API that routes to a qualified human reviewer with authority to change the outcome.
  - Log the inputs, model and version, output, reviewer and final decision.
  - Protect model pipelines: access control, no leakage of personal data into prompts or logs, and suitable vendor terms.
  - Test for harmful or biased outcomes before release.
- **Source**: PDPL Art 1 (definition added), Art 14 and Art 27 (both replaced by RD 68/2026). https://qanoon.om/p/2026/rd2026068/ ; https://decree.om/2026/rd20260068/
- **Confidence**: Confirmed (primary). The detailed ER controls have not been issued yet.
- **As of 2026-10**: In force since 7 Sep 2026. The ER controls are still to come.

### E. Governance, security and records

#### PDPL-20: Documented controls and risk assessment [All]
- **Requirement**: The controller must set controls and procedures for processing. They must include: identifying the risks the processing poses to data subjects; procedures for transfers; technical and procedural measures to keep processing lawful; and any other controls the ER set. The law does not name a "DPIA", but identifying risks is mandatory. A breach of Art 13 carries a fine of OMR 5,000 to 10,000 (Art 27).
- **Engineering implication**: Write a risk assessment (DPIA-style template) for each system or processing activity, and update it when anything material changes. Link each risk to a control in the security plan. Keep the assessment as evidence for permit applications, audits and MTCIT requests.
- **Source**: PDPL Art 13 and Art 27. https://qanoon.om/p/2022/rd2022006/ ; https://qanoon.om/p/2026/rd2026068/
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: In force.

#### PDPL-21: Security and confidentiality controls [All]
- **Requirement**: The controller must keep personal data confidential and must not publish it without the data subject's prior consent. The ER require three things:
  - electronic systems that stop unlawful access, leakage, tampering and misuse;
  - data recovery systems for physical or technical incidents;
  - testing of how well the technical measures work.

  A breach of Art 21 carries a fine of OMR 15,000 to 20,000 (Art 28).
- **Engineering implication**:
  - Role-based, least-privilege access with periodic access reviews.
  - Multi-factor authentication for privileged and remote access.
  - Encryption in transit and at rest.
  - Data-loss prevention and egress controls.
  - Tamper-evident audit logs, with alerts on unusual access (for example, browsing of VIP records).
  - Backups with tested restores.
  - Periodic penetration and control tests, with records kept.
  - No publication of patient data, such as testimonials or case photos, without prior consent.
- **Source**: PDPL Art 21 and Art 28; ER Art 26. https://qanoon.om/p/2022/rd2022006/ ; https://qanoon.om/p/2024/mtcit20240034/
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: In force.

#### PDPL-22: Limit disclosure of health data to third parties [All] [Insurer]
- **Requirement**: The controller and processor must not publish, share or disclose Art 5 data, including health data, except within the limits and cases set by law, or to carry out a judgment or court decision. "Disclosure" means letting others, by any means and for any purpose, view, obtain or use personal data. The permit application must name the third parties that will receive data.
- **Engineering implication**: Keep a disclosure register recording recipient, data, purpose, legal basis and permit reference. Use integration allow-lists for labs, insurers, referral hospitals and statutory reporting. Block ad-hoc bulk exports. Check consent or the legal basis in data-sharing APIs, and log every disclosure for the record of processing.
- **Source**: ER Art 1 (definition of disclosure), Art 5(5) and Art 25; PDPL Art 21. https://qanoon.om/p/2024/mtcit20240034/
- **Confidence**: Confirmed (primary). Unconfirmed: whether patient consent on its own is a "case set by law" that allows disclosure to insurers or other providers.
- **As of 2026-10**: In force.

#### PDPL-23: Record of processing activities and processing documents [All]
- **Requirement**: The controller or processor must keep a record of processing activities. At minimum it holds:
  - the DPO's details;
  - the categories of personal data, and the people authorised to access it;
  - the periods, limits and scope of processing;
  - how data is erased, amended or processed;
  - the purpose;
  - recipients, and the purposes of disclosure;
  - details of any entity that receives transfers;
  - data on cross-border movement;
  - technical and organisational security measures;
  - breaches, with the facts, effects and remedial action.

  The record must be kept up to date and given to MTCIT on request. Processing documents must also be kept under ER Art 27. MTCIT publishes a "Personal Data Processing Record Form".
- **Engineering implication**: Generate a machine-readable record of processing from the data catalogue and infrastructure inventory: systems, data stores, flows, vendors, regions and access roles. Add change hooks that keep it current. Make it exportable in MTCIT's form layout. Set a retention policy for audit logs as processing documents. Processors, such as hosting or SaaS vendors, keep their own record.
- **Source**: PDPL Art 17 and Art 26. ER Arts 27, 28 and 29, https://qanoon.om/p/2024/mtcit20240034/ . MTCIT record form (English), https://mtcit.gov.om/web/content/29065
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: In force.

#### PDPL-24: Data protection officer [All]
- **Requirement**:
  - **Who.** Every controller must designate a DPO. The DPO must be qualified, know the law, the ER and the organisation's practices, and be professionally competent. The DPO may be a new hire or an existing employee (MTCIT FAQ).
  - **Tasks.** The DPO advises, monitors policies, monitors compliance and coordinates with MTCIT.
  - **Publication.** Publish the DPO's name and contact details. Data subjects may contact the DPO about any processing of their data, and consent requests must say how to reach the DPO.
  - **MTCIT appointment form.** The form asks for the DPO's Civil Number, home address, CV, experience certificate, certificate of good conduct and photo. In it the controller undertakes to tell MTCIT immediately if the DPO changes. MTCIT's online services also ask for the DPO's name and Civil ID.
  - **Penalty.** A breach of Art 20 carries a fine of OMR 1,000 to 5,000.
- **Engineering implication**: Make the DPO's name, email and phone configurable. Show them in the privacy policy, consent screens, rights portal and breach notices. Route privacy enquiries to a monitored DPO mailbox or queue. Give the DPO a dashboard covering rights requests, breaches and the processing record. Add a step to update MTCIT when the DPO changes.
- **Source**: PDPL Art 10(b), Art 20 and Art 26. ER Arts 34 to 36, https://qanoon.om/p/2024/mtcit20240034/ . MTCIT FAQ. DPO appointment form (English), https://mtcit.gov.om/web/content/29058
- **Confidence**: Confirmed (primary). Unconfirmed: whether filing the form is mandatory, and whether the DPO must live in Oman. CMS reports that MTCIT prefers a DPO in Oman, and the form's Civil ID and home-address fields point the same way.
- **As of 2026-10**: In force.

#### PDPL-25: Processor contracts and processor duties [All]
- **Requirement**:
  - **Contracting.** A controller may contract a processor. Towards third parties, the processor acts as the controller's agent for civil and administrative liability. The processor stays criminally liable for its own breaches.
  - **Duties that fall on processors directly:**
    - erasure at end of purpose (Art 15);
    - safeguards for automated processing (Art 14);
    - external audit on request (Art 16);
    - keeping processing documents (Art 17);
    - cooperation with MTCIT (Art 18);
    - the record of processing (ER Art 28);
    - providing documents within 30 days (ER Art 2).
  - **MTCIT guideline (April 2026).** It expects the controller to do the following.
    - **Before contracting:** define the purpose; identify Art 5 data and children's data; check the processor's competence and security; set the duration and the retention policy; confirm the processor can handle data subject requests; allow third-party processing only with the controller's prior approval; and agree liability and compensation.
    - **During the contract:** sign a written processing contract that follows the controller's instructions; supervise continuously; check security (encryption, access control, backup); manage changes; coordinate on breaches, including notice to MTCIT; and keep records.
    - **At the end:** have data returned or securely deleted; manage any hand-over to a new processor; keep records; and keep confidentiality in place.
- **Engineering implication**:
  - A data processing agreement template that covers every point in the guideline.
  - A vendor due-diligence questionnaire.
  - A sub-processor list with an approval workflow.
  - Customer-facing tools: rights-request support APIs, data return or deletion export, and audit logs.
  - The vendor's own record of processing and retention controls.
  - A contractual deadline for the processor to notify the controller of a breach, short enough for the controller to meet 72 hours.
- **Source**: ER Arts 2, 3 and 28, https://qanoon.om/p/2024/mtcit20240034/ . PDPL Arts 14 to 18 as amended. MTCIT processor guideline (Arabic), https://mtcit.gov.om/web/content/48307
- **Confidence**: Confirmed (primary) for the law and ER. The guideline itself is non-binding.
- **As of 2026-10**: The guideline is at version 0.1 (April 2026).

### F. Breaches

#### PDPL-26: Notify MTCIT of a breach within 72 hours [All]
- **Requirement**:
  - **The duty.** On a breach that leads to destruction, alteration, disclosure, access or unlawful processing, the controller must notify MTCIT and the data subject.
  - **Timing.** Notify MTCIT's competent department within 72 hours of becoming aware, if the breach could pose a risk to data subjects' rights.
  - **Minimum content:**
    - the nature of the breached data and the consequences;
    - contact details;
    - the likely effects;
    - the measures planned, including mitigation;
    - the measures taken immediately and before reporting.
  - **MTCIT's response.** MTCIT may record the report, assess the measures, direct that data subjects be told, and give guidance.
  - **Documentation.** Document every breach (causes, consequences and corrective measures) in the processing record, and keep it for the period MTCIT sets.
  - **Channel.** Use MTCIT's "Personal Data Breach Reporting Service" and Breach Report Form. MTCIT also gives PDPC@mtcit.gov.om for reports.
  - **Penalty.** A breach of Art 19 carries a fine of OMR 15,000 to 20,000.
- **Engineering implication**:
  - An incident runbook with an "awareness" timestamp and a 72-hour countdown.
  - A risk triage step.
  - An incident record that mirrors MTCIT's form: date of knowledge, data nature, consequences, effects, contact, documentation status, actions before reporting, planned actions and evidence.
  - Pre-approved templates and evidence collection (logs, forensics).
  - A breach register.
  - Processor contracts that require fast notice to the controller.
  - A separate check on cyber-incident reporting to the CDC (CDC System Art 4(2)).
- **Source**: PDPL Art 19 and Art 28. ER Art 1 (definition of breach) and Arts 28(10), 30, 31 and 33, https://qanoon.om/p/2024/mtcit20240034/ . MTCIT data protection page and reports page, https://mtcit.gov.om/library-3/report-studies-9/reports-79/personal-data-protection-reports-379 . Breach form (English), https://mtcit.gov.om/web/content/29062 . CDC System Art 4(2), https://qanoon.om/p/2020/rd2020064/
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: In force. MTCIT received 22 breach reports up to the end of May 2026 (Al Roya, 13 Sep 2026).

#### PDPL-27: Tell affected people within 72 hours when harm is serious [All]
- **Requirement**: Data subjects have a right to be told of any breach and the steps taken. The controller must tell each affected person within 72 hours of becoming aware, if the breach could cause serious harm or high risk to them. The notice gives the type and nature of the breach, details of the data affected, and advice on limiting the effects where needed. MTCIT can also direct that people be told.
- **Engineering implication**: Keep good patient contact data (mobile, email, address). Build bulk notification by SMS, email and letter, in Arabic and English. Prepare templates with the required content, track delivery, and write a call-centre script. Log who was told, and why.
- **Source**: PDPL Art 11(f) and Art 19; ER Arts 31(2) and 32. https://qanoon.om/p/2024/mtcit20240034/
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: In force.

### G. Transfers and processing outside Oman

#### PDPL-28: Transfers outside Oman: consent, equivalent protection and an assessment [All] [Telehealth] [AI]
- **Requirement**:
  - **The basic rule.** The controller may transfer personal data outside Oman under the ER controls, without prejudice to the CDC's powers.
  - **Banned transfers.** A transfer is banned if the data was processed unlawfully, or if the transfer could harm the data subject.
  - **Before any transfer:**
    - Get the data subject's explicit consent. Consent is not needed to meet an international obligation under a treaty Oman has joined, or where the transfer is anonymised so that no one can be identified by any means.
    - Make sure the transfer does not affect national security or the State's higher interests.
    - Make sure the foreign recipient gives protection at least equal to the PDPL and ER.
    - Assess the recipient's protection and the risks. Cover the nature, volume and sensitivity of the data; the purpose, scope and recipients; the duration and frequency; the transfer stages, transit countries and final destination; and the effects on the data subject.
  - **MTCIT's role.** MTCIT may ask for the assessment and publishes a form for it. There is no list of approved countries.
  - **Penalty.** A breach of Art 23 carries a fine of OMR 100,000 to 500,000, the highest fine in the law.
- **Engineering implication**:
  - A data-flow map and a transfer register: destination country, recipient, data categories, purpose, frequency and safeguards.
  - Explicit transfer consent captured where needed.
  - An MTCIT assessment completed for each transfer.
  - Storage and compute locked to region, with egress allow-lists.
  - Vendor contracts that give equivalent protection.
  - Anonymisation before transfer where possible.
  - The ability to stop transfers if MTCIT orders it.
- **Source**: PDPL Art 8(d), Art 23 and Art 29, https://qanoon.om/p/2022/rd2022006/ . ER Arts 37 to 40, https://qanoon.om/p/2024/mtcit20240034/ . MTCIT FAQ. Transfer assessment form (English), https://mtcit.gov.om/web/content/29057
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: In force. Art 23 and ER Arts 37 to 40 were not changed by RD 68/2026.

#### PDPL-29: Get CDC approval before storing or processing health data outside Oman [All] [AI] [Telehealth] [Device]
- **Requirement**:
  - **MTCIT's statement.** The FAQ says CDC approval "is required only if sensitive personal data will be stored or processed outside Oman", and must be obtained "before transferring sensitive personal data abroad". In Arabic: «لا تتطلب موافقة مركز الدفاع الإلكتروني إلا في حالة كانت البيانات الشخصية المعالجة حساسة وأن المتحكم سيعمل على حفظها أو معالجتها خارج السلطنة».
  - **The CDC System.** Art 4(5) requires "concerned entities" to get the CDC's approval before storing any sensitive data, or processing it, outside Oman. "Concerned entities" covers government bodies and private-sector institutions in Oman that fall within the CDC's remit.
  - **The transfer form.** MTCIT's transfer form repeats the CDC requirement.
- **Engineering implication**: By default, store and process health, genetic and biometric data in Oman, either in an in-country cloud region or on-premises. Do not send such data to offshore AI or LLM APIs, analytics, backup, logging and monitoring, or support tools until CDC approval is in hand. Use feature flags and egress controls to block offshore processors for sensitive data. Record CDC approval references in the transfer register.
- **Source**: CDC System (RD 64/2020) Art 4(5), https://qanoon.om/p/2020/rd2020064/ . MTCIT FAQ (English and Arabic), https://mtcit.gov.om/sectors/governance/personal . MTCIT transfer form, note 2, https://mtcit.gov.om/web/content/29057
- **Confidence**: Confirmed (primary). The CDC application procedure and timelines are Unconfirmed: we found no public procedure.
- **As of 2026-10**: In force.

#### PDPL-30: Does remote access from outside Oman count as a transfer? [All] [AI] [Telehealth]
- **Requirement**: Unconfirmed. **Question for advisers:** if engineers or support staff outside Oman can view or query health data held in Oman, is that a "transfer" under ER Arts 37 to 40, "processing outside Oman" that needs CDC approval, or both? Examples are remote support, database administration, an offshore NOC or SOC, and AI services. Three points bear on the answer:
  - The PDPL's definition of processing covers retrieval, review and "making available by other means".
  - MTCIT ties CDC approval to sensitive data "stored or processed outside Oman".
  - The government Policy (Circular 6/2024) defines a cross-border transfer to include making data available, displaying, using or retrieving it from inside Oman to outside.

  We found no MTCIT guidance on remote access by private-sector controllers. For government units the Policy's definition settles the point: remote access from abroad is a cross-border transfer, allowed only for the Policy's three purposes and with CDC approval (see PDPL-05).
- **Engineering implication**: Until this is answered, treat offshore access to identifiable health data as a transfer. Limit production access to staff in Oman. Give offshore support de-identified datasets or masked screens. Allow any offshore access only just-in-time, logged and approved, and only after consent, an assessment and CDC approval. Record it in the transfer register.
- **Source**: PDPL Art 1 (definition of processing); ER Arts 37 to 40; MTCIT FAQ; Circular 6/2024 (definitions). https://qanoon.om/p/2024/mtcit20240006/
- **Confidence**: Unconfirmed
- **As of 2026-10**: Open question.

### H. Marketing, audit and enforcement

#### PDPL-31: Direct marketing needs explicit opt-in and an easy way to stop [Private] [Insurer] [Telehealth]
- **Requirement**: Get the data subject's explicit consent before sending any commercial advertising or marketing material. Before 7 September 2026 the law said "written".
  - **The ER also require:**
    - written consent;
    - telling the person which channel will be used;
    - a way to stop the messages;
    - stopping immediately on request, free of charge.
  - **MTCIT's FAQ** (written before the amendment) says marketing consent must be written and in a form the person can document.
  - **Penalty.** A breach of Art 22 carries a fine of OMR 1,000 to 5,000.
- **Engineering implication**: Keep marketing preferences separate from care messages. Use unticked opt-ins per channel and store the evidence (text, time, channel). Show the channel at opt-in. Put an unsubscribe link or STOP keyword in every message. Apply the suppression list in real time across all systems and vendors. Never target marketing on health data without explicit consent and permit cover.
- **Source**: PDPL Art 22 (replaced by RD 68/2026) and Art 26, https://qanoon.om/p/2026/rd2026068/ . ER Art 22, https://qanoon.om/p/2024/mtcit20240034/ . MTCIT FAQ.
- **Confidence**: Confirmed (primary). Unconfirmed: whether the ER's "written" requirement still applies now that the law says "explicit". Recorded written or electronic consent satisfies both.
- **As of 2026-10**: In force.

#### PDPL-32: External audit when MTCIT asks [All]
- **Requirement**: If MTCIT asks, the controller and processor must appoint an external auditor to check compliance with the law and with the controller's Art 13 controls, and send MTCIT the report.
  - **The auditor** must be accredited and licensed by MTCIT, and independent.
  - **Access.** Give the auditor access to records, processing systems and data.
  - **Deadline.** Send the report within 60 days of appointing the auditor.
  - **Accreditation.** MTCIT accredits auditors under the amended Art 7(f). Its accreditation project launched on 1 February 2026, and the first auditor has been accredited.
- **Engineering implication**: Keep an audit-ready evidence pack: the processing record, risk assessments, policies, consent logs, access reviews, test results and the breach register. Set up read-only auditor access to logs and configurations. Make sure all evidence can be produced within the 60-day window.
- **Source**: PDPL Art 7(f) (replaced), Art 16 and Art 26. ER Arts 23 and 24, https://qanoon.om/p/2024/mtcit20240034/ . MTCIT news on auditor accreditation, https://mtcit.gov.om/media-4/events-competitions-10/event-81/implementation-and-launch-of-the-external-auditor-accreditation-project-in-the-field-of-personal-data-protection-1381
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: Accreditation has run since February 2026. We found no published audit orders.

#### PDPL-33: Cooperate with MTCIT, act on its orders and answer complaints [All]
- **Requirement**:
  - **Documents.** Give MTCIT requested documents and data within 30 days.
  - **MTCIT's powers.** MTCIT can issue warnings; order correction or erasure; suspend processing temporarily or permanently; suspend transfers abroad; or take other measures. Designated MTCIT data protection specialists have judicial police powers.
  - **Complaints:**
    - a data subject, or anyone with an interest, may complain on MTCIT's form within 30 days of becoming certain of the violation (MTCIT's FAQ says the right lapses after that);
    - MTCIT sends the controller a copy within 7 days;
    - the controller may respond within 14 days;
    - MTCIT decides within 60 days, and silence counts as rejection.
  - **Penalty.** A breach of Art 18 carries a fine of OMR 1,000 to 5,000.
- **Engineering implication**:
  - A regulator-request playbook with an owner, evidence sources and a 30-day tracker.
  - The technical ability to suspend specific processing or cross-border flows quickly, with switches per integration and per region.
  - The ability to correct or erase data on order, with audit evidence.
  - A complaint-response workflow with a 14-day clock.
- **Source**: PDPL Arts 8, 9, 12, 18 and 26, https://qanoon.om/p/2022/rd2022006/ . ER Arts 2 and 41 to 43, https://qanoon.om/p/2024/mtcit20240034/ . MD 46/2025, https://qanoon.om/p/2025/mjla20250046/ . MTCIT FAQ and complaint form (English), https://mtcit.gov.om/web/content/29056
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: In force.

#### PDPL-34: Penalties and enforcement to date [All]
- **Requirement**:
  - **Court fines by article breached (OMR):**
    - Art 10 (consent): 500 to 2,000.
    - Arts 15, 16, 17, 18, 20 and 22 (erasure, external audit, processing documents, cooperation, DPO, marketing): 1,000 to 5,000.
    - Arts 13 and 14 (risk controls, automated processing): 5,000 to 10,000.
    - Arts 5, 6, 19 and 21 (sensitive-data permit, children, breach notification, confidentiality): 15,000 to 20,000.
    - Art 23 (transfers abroad): 100,000 to 500,000.
  - **Legal persons.** A legal person faces OMR 5,000 to 100,000 if the offence is committed in its name or for its account by its chair, a board member, its manager or another official, with its consent, concealment or gross negligence.
  - **Confiscation.** Courts may confiscate the tools used.
  - **Administrative penalties.** MTCIT may issue a warning, suspend the permit, impose an administrative fine of up to OMR 2,000 per violation, or cancel the permit. A grievance to the Minister is possible within 60 days, and the Minister decides within 30 days.
  - **Other laws.** These penalties apply without prejudice to heavier penalties in other laws.
- **Engineering implication**: Prioritise the backlog by exposure. Cross-border controls and CDC approval come first. Next come the permit, breach notification, confidentiality and children's controls. Then risk controls and safeguards for automated decisions. Keep evidence that would help defend against an allegation.
- **Source**: PDPL Arts 24 to 32 (Arts 25 and 27 replaced by RD 68/2026), https://qanoon.om/p/2022/rd2022006/ ; https://qanoon.om/p/2026/rd2026068/ . ER Arts 44 and 45, https://qanoon.om/p/2024/mtcit20240034/ . Enforcement figures: Al Roya, 13 Sep 2026, https://alroya.om/post/394000
- **Confidence**: Confirmed (primary) for the penalties. Confirmed (secondary) for the enforcement figures, which come from a press report quoting MTCIT's head of personal data protection.
- **As of 2026-10**: MTCIT reported 20 complaints and reports, and 22 breach reports, up to the end of May 2026. We found no published fines or named enforcement decisions.

### I. Cyber Defence Centre

#### NAT-01: Co-operate with the Cyber Defence Centre's supervision, audits and standards [Gov] [CNI] [Private]
- **Requirement**: The Cyber Defence Centre (CDC) sits under the Internal Security Service. It is the competent national authority for cyber defence. "Concerned entities" must let the CDC exercise its powers. They must give it the documents, data and reports it needs, and let it inspect their devices, networks, systems and software. They must follow the systems, standards and controls the CDC issues. Concerned entities are civil, military and security government bodies, private-sector institutions in Oman linked to the CDC's competences, and any body named by decision of the ISS Chairman. The CDC may classify and identify critical cyber infrastructure and sectors, set technical specifications for security devices and systems and approve their use or import, monitor concerned entities' networks, isolate a non-compliant network (with the committee chair's approval), intervene technically in incidents, audit compliance, and keep a register of cyber security service providers that meet its standards.
- **Engineering implication**: Assume a client may face a CDC inspection. Keep a current asset inventory, network and data-flow diagrams, and security logs that can be exported on request. Put a clause in client and hosting contracts that lets the client give the CDC access to vendor-hosted systems and records. Keep a bill of materials for the security products in your stack, so the client can check it against any CDC specifications. Use CDC-registered security service providers where the client asks for them.
- **Source**: Royal Decree 64/2020, Cyber Defence Centre System, Art. 1(7), Art. 2, Art. 4(1), 4(3), 4(4), Art. 6(4), 6(5), 6(7), 6(9), 6(12), 6(14). Arabic text: https://qanoon.om/p/2020/rd2020064/ (reproduction of Official Gazette 1345; machine translation). Decree articles in English: https://decree.om/2020/rd20200064/
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: In force since 15 Jun 2020. The list of designated concerned entities and sectors, and the CDC's standards and controls, are not public. Whether private hospitals are concerned entities is unconfirmed.

#### NAT-02: Notify the CDC immediately of any actual or potential breach [Gov] [CNI] [Private]
- **Requirement**: Concerned entities must notify the CDC immediately of any actual or potential risk, threat or breach of their cyber security. The System sets no number of hours. Government units must also notify the CDC of any leak, damage or breach of personal data under MTCIT's personal data policy for government units.
- **Engineering implication**: Build detection and an incident runbook with a "notify the CDC now" step that does not wait for root cause. Pre-fill a notification template (what happened, when, systems, data types, containment). As a vendor, commit by contract to tell the client immediately and formally (see NAT-14), so the client can notify the CDC. Record the time of detection and of each notification.
- **Source**: RD 64/2020 System, Art. 4(2): https://qanoon.om/p/2020/rd2020064/ . Personal Data Protection Policy for Units of the State Administrative Apparatus, clause 1.11: https://mtcit.gov.om/web/content/mtcit.content/1342/attachment?download=True (Arabic; machine translation). The eGA cyber index cites Art. 4(2) as Oman's incident notification duty: https://ncsi.ega.ee/country/om/
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: In force. The CDC's reporting channel on cdc.gov.om could not be opened during this research. Confirm the channel, and any internal deadline, with the client.

#### NAT-03: Get CDC approval before storing or processing sensitive data outside Oman [Gov] [CNI] [Private] [Cloud]
- **Requirement**: Concerned entities must obtain the CDC's approval before saving or processing any sensitive data outside Oman. The System does not define "sensitive data". MTCIT policies repeat this approval rule for government data and government-held personal data (NAT-16, NAT-18).
- **Engineering implication**: Default to hosting, backups, disaster recovery, logs, analytics and support tooling inside Oman. Map every sub-processor and SaaS tool (email, ticketing, monitoring, error tracking, AI APIs) that could receive client or patient data, and where it stores it. Where data must leave Oman, prepare a data-flow description and risk assessment the client can submit to the CDC. Keep the feature switched off until approval arrives.
- **Source**: RD 64/2020 System, Art. 4(5): https://qanoon.om/p/2020/rd2020064/ (machine translation)
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: In force. What counts as "sensitive data" for a private entity is unconfirmed.

### J. Cloud and data centres (TRA)

#### NAT-04: Host health-sector content only in Category 4 data centres (TRA Level 4) [All] [Cloud]
- **Requirement**: TRA's regulation gives each customer's content an information security level from 1 to 4. Content of institutions operating in the health sector (except open data) is Level 4, the highest. Content of the financial and banking sectors is also Level 4. Insurance-sector content is Level 3, which still cannot leave Oman without TRA approval (NAT-05). The annex lists health care information as an example of sensitive content, but classes Levels 3 and 4 by the institution's sector, so it doesn't say how health data held by an insurer is classed. Building to Category 4 is the safer reading. The regulation lists health care information as an example of "sensitive content". Cloud providers must process content according to data-centre categories. Only Category 4 data centres may hold Level 4 content. Category 3 may hold every level except Level 4. All categories must follow ISO/IEC 22237. A customer may ask for a higher level. It may lower the level only with TRA approval.
- **Engineering implication**: Treat all patient and clinical data as Level 4. Choose a TRA-permitted provider whose data centre in Oman is Category 4. Get the permit and data-centre category in writing, and record them in the architecture decision log. Keep any non-production copy of real patient data at the same level, or use synthetic data. Do not lower the level without TRA approval.
- **Source**: TRA Decision 1152/2/19/2024-20, Regulation on Cloud Computing Services and Data Centres, Art. 9; Annex 2 (information security levels); Annex 3 (data-centre categories). Arabic text: https://qanoon.om/p/2024/tra20249905/ (reproduction of Official Gazette 1564; machine translation). Commentary by SASLO (Said Al Shahry & Partners): https://www.mondaq.com/data-protection/1540350/navigating-the-new-telecommunications-regulatory-authority-tra-regulations-on-cloud-computing-and-data-centres-in-oman-legal-implications-and-subscriber-challenges
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: In force since 30 Sep 2024. Providers had 6 months to comply. Unconfirmed whether a digital-health company that is not itself a licensed health institution counts as "operating in the health sector".

#### NAT-05: Keep Level 3 and 4 content in Oman unless TRA approves a transfer [All] [Cloud]
- **Requirement**: A cloud provider may not transfer Level 3 or Level 4 customer content outside Oman without TRA approval. It may transfer Level 1 or 2 content only after notifying the customer, and with the customer's prior consent if the content may be affected. A data-centre provider needs TRA approval before transferring any data outside Oman. Cloud providers must tell TRA where their data centres in Oman are, and which data centres inside or outside Oman they use to process, store, transit or transfer customer content. These rules apply without prejudice to the PDPL.
- **Engineering implication**: Pin all regions, replicas, backups, CDN origins, log sinks and support access paths to Oman. Turn off provider features that copy or process data abroad (global backup vaults, cross-region DR, global AI or analytics services, telemetry that carries content). Get the provider's list of data centres used for your content and keep it with your records of processing. Add a contract clause that bans transfer abroad without your written approval and any TRA approval.
- **Source**: TRA Regulation, Art. 12, Art. 14, Art. 16(11): https://qanoon.om/p/2024/tra20249905/ (machine translation)
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: In force. How TRA approval fits with the PDPL transfer rules (and RD 68/2026 amending the PDPL) is for the PDPL workstream.

#### NAT-06: Cloud provider breach notices: 72 hours to customers, 12 hours to TRA and the CDC [All] [Cloud]
- **Requirement**: Cloud providers must tell customers within 72 hours of any security breach or data leak that may affect their content, data or services. They must tell TRA within 12 hours of any incident or technical fault that affects services. They must tell TRA and the CDC within 12 hours of a breach or leak that may affect Level 3 or 4 content, more than 30% of customers, or a large group of people in Oman who rely on the affected services. Data-centre providers must notify TRA of breaches, cyber attacks and other incidents that affect services, and tell customers.
- **Engineering implication**: Write these clocks into the hosting contract and SLA. Give the provider a 24/7 security contact. Make sure your monitoring covers provider-managed layers (cloud audit logs, key management logs). If you are the provider of record (see NAT-07), build the 12-hour TRA and CDC workflow and the 72-hour customer notice.
- **Source**: TRA Regulation, Art. 10, Art. 11, Art. 16(9): https://qanoon.om/p/2024/tra20249905/ (machine translation)
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: In force.

#### NAT-07: Check whether your hosted product needs a TRA permit, and MTCIT accreditation for government work [Cloud] [Gov] [Private]
- **Requirement**: Apart from fixed public telecom licensees, nobody may set up, operate or provide cloud computing services or data-centre services in Oman without a TRA permit. "Cloud computing services" means ICT services provided on a cloud system to process customer content. An applicant must be a legal person whose commercial registration is limited to ICT activities. A permit lasts 3 years and renews automatically. Providers are classed as main providers, aggregators, resellers or brokers. Providers must get MTCIT accreditation before serving state administrative units and other public legal persons. Providers must keep non-Omani staff under set ratios, falling to 10% overall 48 months after the permit starts. The Cloud First Policy 2026 tells government units to use only providers with a valid "Category Four" TRA authorisation.
- **Engineering implication**: Before offering a hosted health product in Oman, get legal advice on whether your SaaS is itself a "cloud computing service". If it is, obtain a permit through an Omani entity, or deliver through a permitted provider that acts as provider of record. For government work, plan for MTCIT accreditation and keep the evidence (ISO 27001 certificate, audit reports). Record the permit holder and category for every environment.
- **Source**: TRA Regulation, Art. 1(2), Art. 2, Art. 3, Art. 6, Art. 8, Art. 19, Art. 21, Annex 4: https://qanoon.om/p/2024/tra20249905/ (machine translation). Cloud First Policy 2026, section 4.1.2: https://mtcit.gov.om/web/content/65140?unique=3fa2201e361918b0a91a95c4949bd6e45c8ed02a
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: In force. Unconfirmed whether a SaaS application vendor, as opposed to its infrastructure host, needs its own permit. MTCIT's service page for cloud hosting accreditation returned 404 during research. A secondary source says MTCIT keeps a register of approved hosting providers and issues an approval letter after the TRA licence: https://btw.media/en/duqm-data-centre-and-the-price-of-omani-cloud-locality

#### NAT-08: Build customer data rights, liability terms and exit into the cloud service [All] [Cloud]
- **Requirement**: Cloud providers must give customers the technical means to access, check, change and delete their data, and must publish their data retention policy. Contracts must include SLA details. They may not exclude the provider's liability for loss of content, poor service quality or security breaches. Providers must report actual SLA performance every 12 months. Providers may not give customer content to others, use it for purposes outside the contract, or let their own contractors operate, manage, maintain or access government or sensitive systems and data. Providers are liable for agents, subcontractors and staff, inside or outside Oman. When a contract ends, the provider must give the customer a copy in a usable format, or move it to a new provider, within 7 days of the request. It must then delete the content beyond recovery, including metadata and backups.
- **Engineering implication**: Provide self-service export in standard formats (for example FHIR or CSV, plus attachments) and verified deletion that covers backups and metadata. Publish a retention policy. Do not let subcontractors administer production health systems without legal advice. Produce an annual SLA performance report. Rehearse the 7-day exit before go-live.
- **Source**: TRA Regulation, Art. 15, Art. 22, Art. 23, Art. 24, Art. 25, Art. 26, Art. 27: https://qanoon.om/p/2024/tra20249905/ (machine translation)
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: In force.

### K. Government information security

#### NAT-09: Meet the government Information Security Management Policy and Basic Security Controls [Gov]
- **Requirement**: Each government unit must set up an information security committee chaired by its head, appoint a dedicated information security officer who reports to the head, run regular risk assessments, classify data under the state classification law, train staff, manage incidents in a structured way and manage IT continuity. ITA's Basic Security Controls set a baseline in 12 areas, with a checklist of control IDs. The controls are written as guidance ("should"). They name solution architects and developers as an intended audience.
- **Engineering implication**: Map your product's controls to the Basic Security Controls checklist IDs (AC.1–AC.11, SAT.1–SAT.3, AA.1–AA.9, SAA.1–SAA.3, CM.1–CM.8, IR.1–IR.7, MP.1–MP.7, PEP.1–PEP.9, PS.1–PS.6, RA.1–RA.4, SCP.1–SCP.6) and include the mapping in tenders. Provide time-stamped, protected audit logs (AA.7, AA.8), least privilege and separation of duties (AC.5, AC.6), PKI certificate support (SCP.4), and malware protection and patching (SCP.5, SCP.6). Give the client's information security officer the evidence they need.
- **Source**: ITA Information Security Management Policy v1.0 (Sep 2019), sections 5.1–5.6 and 7: https://cert.gov.om/files/laws/Information_Security_Management_Policy_EN.pdf ; listed as Circular 4/2019 in the references of Circular 19/2023: https://mtcit.gov.om/web/content/mtcit.content/775/attachment?download=True ; ITA Basic Security Controls v1.0 (30 Jul 2017), sections 4–6: https://cert.gov.om/files/laws/Basic_Security_Controls_EN.pdf
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: No replacement found. A news report (2024) says MTCIT also released "Basic Cybersecurity Controls" and governance guides; these were not seen: https://meatechwatch.com/?p=3678

#### NAT-10: Classify data before hosting it, using the state classification law and the National Data Governance Framework [Gov]
- **Requirement**: Government units must classify government data before hosting it in the cloud, under the Data Classification Policy of the National Data Governance and Management Framework (NDGF). The NDGF has three documents: national data governance policies in 13 domains, which are mandatory; a guide to setting up a data governance office; and a compliance assessment guide. It applies to state administrative units and other public legal persons. The state classification law sets four levels: Top Secret, Secret, Restricted and "Maktoum" (MTCIT's English uses "Confidential"). MTCIT's 2021 cloud policy treated all four as "sensitive data" and told units to add a fifth level for public or open data. Disclosing classified documents is a criminal offence.
- **Engineering implication**: Add a classification attribute to every data store, document type and API. Support at least open data plus the four statutory levels, and mark patient data as sensitive. Enforce access by classification and label exports and prints. Produce a data inventory and classification register that the client's data governance office can adopt. Keep the level set configurable until the client confirms its NDGF policy.
- **Source**: Cloud First Policy 2026, section 4.1.1: https://mtcit.gov.om/web/content/65140?unique=3fa2201e361918b0a91a95c4949bd6e45c8ed02a ; MTCIT Ministerial Circular 2/2025 and letter 113/2025 (14 Jan 2025): https://mtcit.gov.om/web/content/mtcit.content/762/attachment?download=True (Arabic; machine translation); RD 118/2011, Art. 3 (levels) and Arts. 4–7 (criteria): https://qanoon.om/p/2011/rd2011118/ (machine translation); Cloud Computing Policy 2021, glossary and section 6.2: https://mtcit.gov.om/web/content/43341?unique=563eccfb2288d046f25161ed0afdbfae2cb91be2
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: In force. The NDGF document link (www.mtcit.gov.om/NDGF) returned 404, so the NDGF Data Classification Policy's own levels are unconfirmed.

#### NAT-11: Apply the government database security baseline, including application-level encryption [Gov]
- **Requirement**: Government units must apply separation of duties and least privilege. They must keep a documented, current list of user permissions for periodic audit, keep root administrator credentials in a protected vault for use only when needed, and log all direct database access that does not go through the application. They must classify data under the state classification law and design databases so sensitive fields can be separated and encrypted. The application must encrypt sensitive data before it reaches the database, so that people with database access cannot read it. Units must control access by classification, follow change management, patch databases and related systems, monitor audit trails, and run staff awareness.
- **Engineering implication**: Implement field-level encryption in the application for sensitive fields (for example identifiers and clinical notes), with keys held outside the database. Design schemas so encrypted fields remain usable (for example blind indexes for lookup). Separate database administrator, developer, auditor and user roles. Turn on database audit logging for direct sessions and ship it to tamper-resistant storage. Provide a permissions report for audits.
- **Source**: MTC Circular 3/2020 (5 Apr 2020), Basic Standards for Database Security for Units of the State Administrative Apparatus, controls 1–10: https://mtcit.gov.om/web/content/mtcit.content/1098/attachment?download=True (Arabic; machine translation)
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: In force as far as found.

#### NAT-12: Pass a security assessment before go-live, then every one to two years and after changes [Gov]
- **Requirement**: Government units must complete a security assessment before launching any internet-facing website, portal, service window, platform or electronic application, and must fix any findings before launch. They must repeat the assessment periodically (every year or every two years) and whenever they add or change anything. Government mobile apps must be assessed by an accredited company before launch. Units hosting with MTCIT-accredited cloud providers must ask for data protection to be added before or at contract. Security assessment providers for government must hold ISO 27001, pass a security background check and clearance (company and named staff), and use assessors with recognised certifications (for example CREST, OSCP, CEH or GIAC).
- **Engineering implication**: Build an independent penetration test by an MTCIT-accredited provider into every release plan for an internet-facing government service, with time to fix findings before launch. Keep a remediation log. Re-test after major changes. Check the tester's accreditation before booking.
- **Source**: MTCIT Ministerial Circular 11/2022 (25 Jul 2022): https://mtcit.gov.om/web/content/mtcit.content/827/attachment?download=True (Arabic; machine translation); Circular 19/2023, security requirement 6: https://mtcit.gov.om/web/content/mtcit.content/775/attachment?download=True ; MTC Security Assessment Services Standard (2019), sections 1–5: https://mtcit.gov.om/web/content/mtcit.content/264/attachment?download=True
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: In force.

#### NAT-13: Follow MTCIT's basic standards for government mobile apps [Gov]
- **Requirement**: A government unit's app must run on Android and iOS, be the unit's single app, be listed in the Omani Apps Directory, and be in Arabic and English. It must include a support contact, terms of use and a privacy statement. It must be usable by people with disabilities and older people, available 24/7 with outage notices, free, and free of private-sector advertising. It must mark mandatory and optional fields, ask for confirmation before submission, acknowledge receipt and show request status. Security rules: assess privacy risks (camera, location) first; show privacy and content notices before use; store sensitive data securely and only when needed; use strong encryption; complete a security assessment by an accredited company and get the unit's formal approval before launch; comply with the PDPL and the Electronic Transactions Law; keep fixing vulnerabilities; offer login at the available levels, such as commercial registration number, ID card number or PKI digital identity; and use an approved Omani e-payment gateway.
- **Engineering implication**: Build a bilingual interface (Arabic right-to-left and English) and test accessibility (use WCAG as a working benchmark and confirm the client's standard). Integrate national PKI or Thiqa login (NAT-27) and the approved payment gateway. Encrypt local storage with the platform keystore and keep little or no cached patient data. Show a privacy notice before first use. Use no advertising SDKs. Add receipts and status tracking.
- **Source**: MTCIT Ministerial Circular 19/2023 (28 Nov 2023), Basic Standards for Developing Government Applications on Mobile and Smart Devices: basic standards 1–21 and security requirements 1–10: https://mtcit.gov.om/web/content/mtcit.content/775/attachment?download=True (Arabic; machine translation)
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: In force. MTCIT's library lists the date as 28 Feb 2023; the signed circular says 28 Nov 2023.

#### NAT-14: Accept the IT Risk Management Policy's supplier clauses [Gov]
- **Requirement**: Government units must write IT risk controls into contracts with external IT providers for the whole project, from contract to handover or end of service. The provider must: comply with national law, including the PDPL and IT and cybersecurity laws; follow the unit's IT risk policy; carry out a full risk assessment of any system or service before implementation, including sensitive and critical systems; share the results and get the unit's approval before operation starts; apply technical controls such as encryption, access control, backup and network segregation, and update them as risks change; send periodic reports on security status, incidents and non-compliance; notify the unit immediately and formally of any security or technical incident that could affect government systems or data; and co-operate fully with audits, including access to documents, records and systems.
- **Engineering implication**: Produce a pre-implementation risk assessment for each system (threats, controls, residual risk) and get written sign-off before production. Keep a risk register per client. Send a regular security status report. Trigger incident notice to the client on suspicion, not only on confirmation. Keep an audit pack ready (policies, logs, test results, access lists).
- **Source**: MTCIT Circular 3/2026 (5 Mar 2026) and IT Risk Management Policy (Feb 2026, v0.1): scope and section B, items 1–8: https://mtcit.gov.om/web/content/mtcit.content/1277/attachment?download=True (Arabic; machine translation). Commentary: https://www.tamimi.com/law_update_articles/omans-issues-mandatory-it-risk-management-policy/
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: In force from circulation (March 2026).

#### NAT-15: Supply a service continuity plan and take part in annual continuity tests [Gov]
- **Requirement**: Each government unit must have an internal IT continuity plan, a business impact analysis, a formal continuity team, the resources to recover, an actual test at least once a year, KPIs (such as recovery time, test completion and system coverage), periodic review and staff training. When it contracts a third party, the unit must require that third party to prepare a dedicated continuity plan for its services and submit it for review and approval.
- **Engineering implication**: Write a continuity and DR plan for each service, with RTO and RPO agreed with the client, backed by tested restores and failover inside Oman (NAT-05, NAT-17). Join the client's annual test and hand over evidence (timings, issues, fixes). Report achieved recovery times as KPIs.
- **Source**: MTCIT IT Operations Continuity Policy v2 (Apr 2026), policy statements 1–10: https://mtcit.gov.om/web/content/mtcit.content/1328/attachment?download=True . MTCIT's library lists it as Circular 4/2026 (12 Apr 2026); the circular itself was not opened.
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: In force from circulation.

### L. Government cloud, data and integration

#### NAT-16: Government cloud: permitted providers, SLAs, encryption, audit access and CDC approval for hosting abroad [Gov] [Cloud]
- **Requirement**: Government units (except security and military units) must treat cloud as the preferred option for new or upgraded systems. They must contract only with cloud and data-centre providers holding a valid Category Four TRA authorisation. Hosting classified data in categories other than those the regulation allows needs MTCIT's prior approval. Data must be classified first. SLAs must cover availability, reliability, scalability and continuity, and must set each party's incident roles. Government data in the cloud must be encrypted. Systems handling payment cards must meet PCI DSS. Contracts must give the unit access to security audit reports, assessment reports and incident logs. Units must run periodic cloud risk assessments. To host or process government data or applications outside Oman, the service must be SaaS, must comply with the CDC's Policy and Controls for the Use of External Cloud Computing Services (CDC Circular 6/2025), and needs the CDC's prior approval. New or expanded government data centres need MTCIT co-ordination.
- **Engineering implication**: Deploy government workloads only with Category 4 permitted providers in Oman. Encrypt data at rest and in transit, with client-controlled keys where possible. Hand over audit reports, penetration test reports and incident logs on request. If one component has to be foreign SaaS (for example a specialised imaging or AI service), isolate it, minimise the data it receives, and give the client what it needs for a CDC request. Do not put government data on foreign IaaS or PaaS.
- **Source**: MTCIT Cloud First Policy 2026 (v0.4): sections 3, 4.1.1–4.1.4, 4.2.1–4.2.6, 5.1–5.3: https://mtcit.gov.om/web/content/65140?unique=3fa2201e361918b0a91a95c4949bd6e45c8ed02a ; MTCIT Ministerial Circular 10/2026 (14 Jun 2026): https://mtcit.gov.om/web/content/54749?unique=890129923ec3607c7af38ba3fbbd5ff95cb053ba (Arabic; machine translation)
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: In force; updates Circular 9/2021. CDC Circular 6/2025 is not public, so its controls are unconfirmed.

#### NAT-17: Keep government data, backups and DR in Oman and give the government audit and scan rights [Gov] [Cloud]
- **Requirement**: MTC's Cloud and Hosting Services Standard says government data may be hosted, transacted and processed only within Oman, including primary storage, backup and disaster recovery. Cloud providers serving government must apply ISO/IEC 27001, 27017 and 27018 and the CSA Cloud Controls Matrix (and PCI DSS for online payments). They must give the government access to facilities, records and databases for inspection within 72 hours, allow government vulnerability scans and penetration tests, mitigate vulnerabilities within 30 days of formal identification, supply requested data within one business day at no cost, keep a disengagement plan, and return all data, including backup and DR copies, on exit. Accreditation lasts while the provider keeps its ISMS certification, security clearance and team skills.
- **Engineering implication**: Put DR in a second site in Oman, not abroad. Track vulnerabilities with a 30-day fix target for government findings. Keep test windows and credentials ready for government-led scans. Script data extraction so you can meet a one-business-day request.
- **Source**: MTC Cloud and Hosting Services Standard v1.0 (ref. GC_S2, 17 May 2018; issued 2019), sections 3.1–3.5 and 4–4.2: https://mtcit.gov.om/web/content/mtcit.content/263/attachment?download=True
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: Still in MTCIT's library. How it sits with the 2024 TRA regulation and the 2026 Cloud First Policy is unconfirmed.

#### NAT-18: Government personal data: process in Oman, use Oman-based processors, get CDC approval for transfers [Gov]
- **Requirement**: Government units must process personal data within Oman's borders. They may transfer it or process it abroad only to perform a contract with the data subject, to pursue or defend legal claims, or to protect the data subject's vital interests, and only with the CDC's prior approval. Processing by a processor or third party needs a written contract with retention and deletion terms and a right for the unit to audit the processor's security controls. The policy defines a third party as a body working under the supervision of the controller or processor and based in Oman. Units must publish a privacy statement with set contents (including whether data will be processed outside Oman), destroy data securely, and notify the CDC of leaks or breaches. Processors may act only on the unit's instructions.
- **Engineering implication**: For government clients, use an Omani legal entity as processor of record and host in Oman. Sign a written processing contract with retention, deletion and audit clauses. Build the required privacy notice content into onboarding screens. Build secure deletion (for example crypto-shredding) with a destruction record.
- **Source**: MTCIT Personal Data Protection Policy for Units of the State Administrative Apparatus (Mar 2024, v1): definitions, clauses 1.7, 1.9–1.13, 2.1–2.2 and annex: https://mtcit.gov.om/web/content/mtcit.content/1342/attachment?download=True ; Circular 6/2024 (31 Mar 2024): https://mtcit.gov.om/web/content/mtcit.content/765/attachment?download=True (both Arabic; machine translation)
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: Enters into force 24 months after approval and circulation by MTCIT, so about 31 Mar 2026 if circulated with the circular. Confirm the date with the client. It runs alongside the PDPL (PDPL workstream).

#### NAT-19: Integrate with government systems only through the National Platform for Government Integration [Gov]
- **Requirement**: State administrative units, and bodies allowed to integrate with them (including the private sector under approved controls), must use the National Platform for Government Integration as the main and only channel for electronic integration and data exchange. Direct integration outside the platform needs MTCIT's prior approval. APIs are the basic integration method and must follow national standards and lifecycle management. Every API must be registered and approved in the National API Catalog before others may use it, with documented service levels. Bodies must apply a unified access model with least privilege, protect data in transit and at rest, log operations and monitor use continuously. Private-sector, regional and international integrations need prior approvals. Sharing sensitive or restricted data needs approval from the data governance authorities.
- **Engineering implication**: Design integrations with the Ministry of Health and other government systems as APIs published through the national platform, not as point-to-point links or file drops. Allow time for API Catalog registration and MTCIT approval. Use scoped tokens, strong transport security and full request logging. Document SLAs for any API you expose.
- **Source**: MTCIT Ministerial Circular 16/2026 (7 Sep 2026): https://mtcit.gov.om/web/content/mtcit.content/772/attachment?download=True ; General Electronic Integration Policy (scope, definitions, general provisions, roles): https://mtcit.gov.om/web/content/mtcit.content/388/attachment?download=True (both Arabic; machine translation)
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: In force from circulation. Onboarding procedures for the platform and the API Catalog were not found.

#### NAT-20: Do not re-share National Records data without the Centre's approval [Gov]
- **Requirement**: The National Records Law sets up a National Records Centre in the Royal Oman Police. It applies to state administrative units, other public legal persons, companies more than 40% state-owned, and some concession holders. These bodies must supply data to the Centre and meet data quality standards (accuracy, completeness, structure, source reliability, readiness of flows, regular updates). They must use the national records for integration and data exchange as the executive regulation sets out. A body that receives national records data may not make it available to any other body without the Centre's approval.
- **Engineering implication**: Tag data obtained from national records (for example civil identity or demographic fields) with its source. Block onward sharing of those fields to third parties (labs, insurers, other vendors) unless an approval is recorded. Add validation, completeness checks and update timestamps to data you send to national records.
- **Source**: RD 52/2024, National Records Law, Arts. 1, 2, 10, 12, 14: https://qanoon.om/p/2024/rd2024052/ (reproduction of Official Gazette 1570; machine translation)
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: In force. The executive regulation was not checked.

### M. Government contracts: source code, staffing and managed services

#### NAT-21: Agree source-code ownership or escrow for government software [Gov]
- **Requirement**: At the planning stage, and before financial approval, government units must co-ordinate with MTCIT and get its approval on whether owning the source code of a new system is mandatory. If it is, the unit picks one model. Model 1: direct ownership and management, with a secure environment and version control, a named custodian, strict access, periodic security reviews, off-site backups, full documentation, and contract clauses to receive complete, current source code, technical and operational documents, installation and maintenance guides, and knowledge transfer. Model 2: ownership with custody by a specialised software escrow company, with full and exclusive ownership for the unit, access and release on termination or on request, regular deposits during development, release if the developer fails or stops trading, and a ban on publishing the code on any public cloud platform outside Oman, or reselling or sharing it, without written permission.
- **Engineering implication**: Price and plan source-code deliverables or escrow deposits in government bids. Keep the code buildable from the deposited material (build scripts, dependency lists, infrastructure as code). Host government project repositories in Oman or self-hosted, not on public cloud Git services outside Oman, unless the contract says otherwise. Keep version history and release notes complete. Separate your reusable product core from client-owned code early.
- **Source**: MTCIT Ministerial Circular 20/2025 (9 Oct 2025), items 1–2 and both models: https://mtcit.gov.om/web/content/mtcit.content/1265/attachment?download=True (Arabic; machine translation)
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: In force. The public-cloud ban is written into the escrow model; applying it to Model 1 projects is a safe default, not a stated rule.

#### NAT-22: Staff security, network, database, development and support roles on government contracts with Omani nationals [Gov]
- **Requirement**: In state administrative units and government companies, jobs in information security, network management and databases must be held by Omanis only. ICT providers, whether contracted directly or as subcontractors, must supply only Omani staff for that work. The same rule covers systems development and analysis, website design and technical support roles. Existing contracts had to be reviewed within 12 months to move to Omani staff without extra cost or delay.
- **Engineering implication**: Plan delivery teams for Ministry of Health and other government projects so that security, network, database, development, analysis, web and support roles are filled by Omani nationals, or get a written exception. Restrict production access by role, so only approved staff can reach government systems. Record who performs each role in the project RACI. Get legal advice on whether offshore development work is caught.
- **Source**: MTC Circular 7/2020 (5 Jul 2020), items 1–3: https://mtcit.gov.om/web/content/mtcit.content/1100/attachment?download=True ; MTCIT Ministerial Circular 11/2021 (3 Jun 2021), items 1–4: https://mtcit.gov.om/web/content/mtcit.content/1102/attachment?download=True (both Arabic; machine translation)
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: In force as far as found. Whether the rules reach offshore delivery teams is unconfirmed.

#### NAT-23: Meet MTCIT's standards for managed IT services [Gov]
- **Requirement**: When a government unit buys managed services (technical support, infrastructure, information systems), the provider must be officially registered in Oman with the licences needed; have relevant experience; employ qualified staff under Omani law; meet the required Omanisation percentage; sign binding SLAs with response and resolution times; follow ISO 20000 and ITIL; and meet minimum technical standards. These include proactive monitoring and alerts; backup and recovery; at least 99.99% availability; role-based access, multi-factor authentication and regular access audits; firewalls, intrusion detection and VPN for remote access; ISO 27001 as a minimum; regular vulnerability assessments and penetration tests; encryption; 24/7 incident response with root-cause analysis; configuration, change and release management; a 24/7 network operations centre and an ITIL service desk; and secure APIs for integration with national platforms.
- **Engineering implication**: If you run or support Ministry of Health systems, operate through an Omani-registered entity, hold ISO 27001 and ISO 20000 (or run ITIL-aligned processes), staff a 24/7 operations centre and service desk, enforce MFA for every admin login, and design for 99.99% availability. Add SLA results to monthly reports.
- **Source**: MTCIT Circular 7/2025 (9 Mar 2025) and Administrative Standards for Managed Services (Feb 2025, v1), sections 5–6 and Annex 1: https://mtcit.gov.om/web/content/mtcit.content/755/attachment?download=True (Arabic; machine translation)
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: In force from circulation.

### N. Electronic transactions, signatures and digital identity

#### NAT-24: Electronic records count as legal writing only if they meet the Electronic Transactions Law's conditions [All]
- **Requirement**: The 2025 Electronic Transactions Law covers electronic transactions, documents, signatures and trust services. An electronic document counts as written and has legal effect if its creation and adoption meet the law, its executive regulation and implementing decisions. A record is validly retained if it is kept in its original form (or encrypted, or in a form that shows no change), stays accessible for later use, and identifies the originator, the addressee, and the date and time of creation, sending or receipt. An electronic document counts as an original if its content can be shown clearly and its integrity can be checked technically. Courts weigh how reliable the creation, storage and sending were, how integrity was kept, the source, and how the originator's identity was checked. Unlike the 2008 law, the 2025 law has no list of excluded transactions; it only preserves the Central Bank's powers. Other laws on record keeping still apply.
- **Engineering implication**: For e-consent forms and medical record entries, store a tamper-evident copy (hash or signature) of exactly what the patient or clinician saw and accepted, with who, when (trusted time) and from which device. Keep an append-only, versioned audit trail for every change. Make records retrievable in readable form for the whole retention period. Check health-law consent formalities separately (health workstream).
- **Source**: RD 39/2025, Electronic Transactions Law, Arts. 2, 3, 8, 9, 10, 11 (Official Gazette 1591): https://mtcit.gov.om/web/content/mtcit.content/1031/attachment?download=True ; https://qanoon.om/p/2025/rd2025039/ (Arabic; machine translation). Exclusions removed: https://blog.decree.om/2025/new-electronic-transactions-law-issued/
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: In force since 14 Apr 2025. RD 69/2008 is repealed. The executive regulation was not found in MTCIT's library.

#### NAT-25: Choose the right e-signature level and verify signatures, certificates and e-IDs [All]
- **Requirement**: The law recognises simple, advanced and certified electronic signatures. A simple e-signature has evidential weight if the reliability factors in Art. 11 are met. An advanced and certified e-signature has evidential weight if its creation tool is linked to the signatory alone and under the signatory's control at signing, and if later changes to the signature (and, where integrity is the purpose, to the signed data) can be detected. A certified signature is an advanced signature linked to an electronic authentication certificate. An electronic service provider that relies on trust services must verify the signatory, the signature certificate, the electronic identity and the authentication certificate. It must set the assurance level of the signature or seal according to the nature and importance of the transaction, and must check that signatures, seals and certificates are valid. It stays liable to third parties if it does not.
- **Engineering implication**: Define an assurance matrix. For example: simple e-signature plus strong login for routine acknowledgements; certified PKI signatures (national ID card or Thiqa) for high-risk records such as clinician sign-off of reports, prescriptions or consent for major procedures, subject to health-law advice. Check certificate chains and revocation (OCSP or CRL) at signing time. Store the validation evidence and a trusted timestamp with the record.
- **Source**: RD 39/2025, Art. 1(15)–(17), Art. 16, Art. 17, Art. 30: https://mtcit.gov.om/web/content/mtcit.content/1031/attachment?download=True ; https://qanoon.om/p/2025/rd2025039/ (machine translation)
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: In force.

#### NAT-26: Do not provide trust services without an MTCIT licence [All]
- **Requirement**: Trust services are: issuing electronic authentication certificates, certified e-signatures, electronic seals, electronic identity verification, electronic delivery services, and any others the Ministry names. Nobody may provide them without a licence from the Ministry. The exception is trust services inside a closed system within one body and the bodies under it, which deals with no third party and is not used for external transactions. A Trust Services Management Committee in MTCIT grants licences, sets standards for electronic identity systems and identity verification, accredits foreign trust service providers and recognises their certificates, and approves root keys. Providing trust services without a licence carries 3 to 5 years' imprisonment and/or a fine of OMR 20,000 to 50,000. A legal person can be fined double. Holders of encryption keys must let authorised officers inspect key information, except keys named by the National Security Council.
- **Engineering implication**: Do not run your own certificate authority, e-seal or identity verification service for patients or other organisations unless you hold a licence or fit the closed-system exception. Use national or licensed providers (NAT-27). If you use a foreign e-signature platform, check whether its certificates are recognised in Oman. Keep key management records ready for lawful inspection.
- **Source**: RD 39/2025, Arts. 4, 5, 7, 24, 25, 26, 29, 34, 35: https://mtcit.gov.om/web/content/mtcit.content/1031/attachment?download=True ; https://qanoon.om/p/2025/rd2025039/ (machine translation)
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: In force. Licensing conditions depend on the executive regulation, which was not found.

#### NAT-27: Use the national PKI and Thiqa digital ID for strong authentication and signing [All] [Gov]
- **Requirement**: MTCIT's National Cyber Security Center (المركز الوطني للسلامة المعلوماتية, which hosts cert.gov.om) runs Oman's digital trust services. These include the Thiqa (ثقة) mobile digital ID, civil ID card certificates, electronic authentication for subscribing service providers (using the civil card or Thiqa), digital signatures, time-stamping, real-time certificate status checks, employee and device certificates, a unified e-identity gateway and signature verification. MTCIT lists an Electronic Identity Gateway service for individuals, businesses and government. Government mobile apps must offer login at the available levels, including PKI digital identity.
- **Engineering implication**: Integrate national e-ID (Thiqa or ID card PKI) through MTCIT's gateway for patient and clinician login where the client requires it. Support certificate-based login and signing, real-time certificate validation and time-stamping. Allow weaker fallbacks (such as SMS one-time codes) only where your assurance matrix permits. Apply for integration early.
- **Source**: Digital Trust Services page: https://cert.gov.om/sp/pki ; MTCIT Electronic Identity Gateway service: https://mtcit.gov.om/services-5/services-13/services-92/electronic-identity-gateway-for-government-and-private-services-817 ; Circular 19/2023, security requirement 9: https://mtcit.gov.om/web/content/mtcit.content/775/attachment?download=True
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: Available. Integration protocols, fees and eligibility for private health providers and foreign vendors are unconfirmed.

### O. Cybercrime

#### NAT-28: Protect medical records against the offences in the 2026 cybercrime law [All]
- **Requirement**: The Law on Combating Information Technology Crimes (RD 61/2026) replaced the 2011 Cybercrime Law from 8 Jun 2026. It is an offence to intentionally and without right obtain, change, modify, block, encrypt, cancel, destroy or disclose, through an information system, electronic data relating to an examination, diagnosis, medical record, dispensing of medicines or medical care (1 month to 3 years and/or OMR 3,000 to 10,000; Art. 8). Unauthorised access is an offence. It is aggravated where data is deleted, altered, added to, copied, disclosed, blocked or encrypted (which covers ransomware), and aggravated further for personal data (Art. 5). Committing the Art. 5 access offences in or because of one's job carries higher penalties, even after leaving the job (Art. 7). Art. 11 does the same for Art. 10 offences against government data. Neither aggravation is written into Art. 8. Obtaining passwords or access codes without right (Art. 6) and intercepting, tracking or redirecting data (Art. 9) are offences. "Information system" includes AI systems (Art. 1(7)). The law applies to acts outside Oman that harm Oman's interests or people, or have effects in Oman (Art. 2).
- **Engineering implication**: Enforce least privilege and need-to-know on clinical data, with logged and reviewed emergency ("break-glass") access. Keep immutable access logs that show who viewed or changed each record. Remove access the day staff leave. Encrypt data in transit. Keep offline or immutable backups so ransomware cannot destroy records. Tell users that viewing a record without a reason can be a crime.
- **Source**: RD 61/2026 (1 Jun 2026; Official Gazette 1651), decree Art. 2 (repeal of RD 12/2011) and law Arts. 1(7), 2, 5, 6, 7, 8, 9, 10, 11: Gazette scan on MTCIT: https://mtcit.gov.om/web/content/mtcit.content/1030/attachment?download=True ; https://qanoon.om/p/2026/rd2026061/ (Arabic; machine translation)
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: In force since 8 Jun 2026. Many guides still cite RD 12/2011 (its Art. 5 was the old medical-data offence: https://qanoon.om/p/2011/rd2011012/). Treat those as out of date.

#### NAT-29: Avoid privacy, evidence and online-medicine offences; note corporate liability [All]
- **Requirement**: It is an offence to use IT to intrude on private or family life by, among other things, eavesdropping on or recording communications; capturing or keeping images of others; photographing injured or dead people or accident victims and sharing the images without permission; or tracking or monitoring other people's location data, or disclosing, copying or keeping it (Art. 36). Promoting or selling unlicensed medicines, substances or herbal products online is an offence (Art. 38). A person responsible for digital evidence who hides it, refuses to give it to judicial officers or tampers with it commits an offence (Art. 15). A public employee who intentionally fails to take the measures issued by MTCIT or another competent authority, and so exposes a system to a crime, commits an offence (Art. 13). A legal person can be fined double the maximum fine where an offence is committed in its name or for its benefit (Art. 57). Courts may order a system, website or premises closed (Art. 60).
- **Engineering implication**: Collect location data only for a stated purpose with consent, and do not keep location histories by default. Restrict image capture of patients in clinical apps to clinical need with consent. In telehealth or e-pharmacy features, check that every medicine offered is licensed. Keep logs and forensic evidence with a chain of custody, so they can be handed over intact. Help government clients show they applied MTCIT measures (control evidence).
- **Source**: RD 61/2026, Arts. 13, 15, 36, 38, 57, 60: https://mtcit.gov.om/web/content/mtcit.content/1030/attachment?download=True ; https://qanoon.om/p/2026/rd2026061/ (Arabic; machine translation)
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: In force since 8 Jun 2026.

### P. AI policy

#### NAT-30: Apply MTCIT's AI policy to AI features, especially clinical ones [AI] [Gov] [Private]
- **Requirement**: MTCIT's Public Policy for Safe and Ethical Use of Artificial Intelligence Systems (April 2025) applies to government administrative units and to private bodies regulated by sector regulators that develop or use AI. Bodies using AI must: provide human supervision and control of sensitive and impactful decisions; show clear benefit before adoption; give understandable explanations, especially in areas such as healthcare; monitor and record errors and harms; give documents to regulators in an investigation; limit use of personal data; classify data and protect it (for example encryption, multi-factor authentication, anonymisation); document processes; set retention and deletion rules; and use outputs only for their original purpose. Bodies developing AI must: document purpose, components and data; assess ethical, social and environmental effects before deployment; label AI-generated content; document decision logic; review and update systems; test accuracy, including independent audits; monitor bias; protect data; provide tools that explain decisions; let people access, correct and delete their data; and apply security practices such as patching and penetration testing. People have a right to human intervention in sensitive decisions. There is no risk-tier classification. Sector regulators may add rules with MTCIT's approval.
- **Engineering implication**: For each AI feature (for example triage, summarisation, coding or image reading), keep a model card and data sheet, a pre-deployment impact assessment, bias and accuracy test results, and a monitoring log. Keep a clinician in the loop for clinical decisions, with override and a reason field. Show the evidence behind outputs. Label AI-generated text in records. Log prompts and outputs, with privacy controls, for audit. Check where any external model API processes data (NAT-03, NAT-05).
- **Source**: MTCIT Public Policy for Safe and Ethical Use of AI Systems (Apr 2025, v0.1): scope, policy statements (first to third) and ethical principles: https://mtcit.gov.om/web/content/43446?unique=e7cce2bd929945913acb8a932e3067e70aeadbe4 (English PDF, read by OCR). Status commentary: https://blog.decree.om/2025/mtcit-issues-public-policy-for-ethical-use-of-ai/ ; https://www.trowers.com/insights/2026/june/personal-data-and-artificial-intelligence-recent-regulatory-developments-in-oman
- **Confidence**: Confirmed (primary)
- **As of 2026-10**: In force as policy since April 2025. Commentators say it is not legally binding and has no penalties. No AI law or draft AI law was found. No national health-specific AI rule was found. RD 50/2026 created an AI Special Zone in Muscat but adds no AI rules. A 2021 MTCIT circular set six AI principles for government units: https://www.omanobserver.om/ampArticle/1104392

## Cloud regions in and near Oman

Notes for engineers:
- A provider's region being in Oman does not by itself meet NAT-04 and NAT-05. Ask each provider for its TRA permit, the data-centre category (Category 4 for health content) and the list of data centres used for your content. No public TRA register of permit holders was found.
- An AWS Local Zone is an extension of its parent Region (Bahrain). Check which services and which copies of data (snapshots, backups, logs) stay in Muscat.

| Provider | Region name or code | Location | Status at 2026-10 | Source URL |
|---|---|---|---|---|
| **In Oman** | | | | |
| AWS | Local Zone, network border group `me-south-1-mct-1` (parent Region `me-south-1`, Bahrain) | Muscat, Oman | Live since 28 Nov 2022. Listed under `me-south-1` in AWS IP ranges on 17 Oct 2026. Local Zone, not a full Region: services not offered in the zone, such as object storage, and the control plane run in Bahrain | https://aws.amazon.com/about-aws/whats-new/2022/11/aws-local-zones-buenos-aires-copenhagen-helsinki-muscat ; https://ip-ranges.amazonaws.com/ip-ranges.json |
| AWS | Full Region in Oman | – | None (not in AWS Regions list) | https://docs.aws.amazon.com/global-infrastructure/latest/regions/aws-regions.html |
| Oracle | OCI Dedicated Region (primary) | Muscat, Oman | Live. Launched Dec 2021 by Oman ICT Group and Oman Data Park; now described as hosted by ITHCA Group. A Dedicated Region, not a public region. Offered to public and private sectors at launch (2021 report); ask about current access | https://oerlive.com/technology/oman-information-and-communication-technology-group-launches-the-first-oracles-hyper-scale-cloud-infrastructure-data-center-in-oman/ ; https://www.datacenterdynamics.com/en/news/oracle-launches-second-oci-dedicated-region-in-oman/ |
| Oracle | OCI Dedicated Region (secondary) | Ibri, Oman | Live; announced 29 Sep 2025. Mirrors Muscat for failover. Hosted by ITHCA Group with Oman Data Park. Launch reports describe it as serving Oman government entities; ask about private-sector access | https://www.datacenterdynamics.com/en/news/oracle-launches-second-oci-dedicated-region-in-oman/ ; https://www.zawya.com/en/press-release/companies-news/oman-data-park-launches-oci-secondary-dedicated-region-in-partnership-with-ithca-and-oracle-in-ibri-suqtqnyi |
| Oracle | Public cloud region in Oman | – | None listed | https://www.oracle.com/cloud/public-cloud-regions/ |
| Microsoft Azure | – | – | No Azure region in Oman, live or announced | https://azure.microsoft.com/en-us/explore/global-infrastructure/geographies/ |
| Google Cloud | – | – | No Oman region (only `me-central1`, `me-central2`, `me-west1` in the Middle East). Ooredoo and Google Cloud announced "locally hosted" sovereign AI for Omani enterprises (30 Jun 2026); hosting model not stated | https://www.gstatic.com/ipranges/cloud.json ; https://www.samenacouncil.org/samena_daily_news?news=111292 |
| Huawei Cloud | – | – | No Huawei Cloud public region in Oman found. Omantel's "National Cloud" (Feb 2024) is built with Huawei but run by Omantel | https://www.huaweicloud.com/intl/en-us/news/20240226211706598.html ; https://timesofoman.com/article/142298-omantel-unveils-cloud-dominance-with-launch-of-national-cloud |
| Alibaba Cloud | – | – | No Oman region in Alibaba's list. A 2021 agreement with Datamount and ETCO to set up a cloud centre in Oman; current status unknown | https://www.alibabacloud.com/help/en/ecs/user-guide/regions-and-zones ; https://www.omanobserver.om/article/1101963/business/economy/chinas-alibaba-to-invest-in-cloud-computing-centre-in-oman |
| Omantel | National Cloud | Oman (sites not stated) | Launched Feb 2024 (news); claims data residency in Oman | https://timesofoman.com/article/142298-omantel-unveils-cloud-dominance-with-launch-of-national-cloud |
| Oman Data Park | Local cloud and hosting; partner for the Oracle Dedicated Regions | Oman | Operating. Accredited by MTCIT as a cloud and hosting provider in 2020 | https://www.omanobserver.om/ampArticle/8180 ; https://www.zawya.com/en/press-release/companies-news/oman-data-park-launches-oci-secondary-dedicated-region-in-partnership-with-ithca-and-oracle-in-ibri-suqtqnyi |
| data2cloud (Duqm Data Centre SAOC; majority-owned by Ooredoo Oman), Datamount, Cloud Acropolis | Local hosting providers | Oman | Reported as operating and on MTCIT's register of approved hosting providers (secondary source only) | https://btw.media/en/duqm-data-centre-and-the-price-of-omani-cloud-locality ; https://www.omanobserver.om/ampArticle/8180 |
| SAP | Private cloud data centre (RISE with SAP) | Oman (site not stated) | Launched 21 Jun 2023 | https://news.sap.com/mena/2023/06/sap-launch-omans-first-data-center-for-private-cloud/ |
| **Nearby, not in Oman** | | | | |
| AWS | `me-south-1` Middle East (Bahrain) | Bahrain | Live (opt-in Region) | https://docs.aws.amazon.com/global-infrastructure/latest/regions/aws-regions.html |
| AWS | `me-central-1` Middle East (UAE) | UAE | Live (opt-in Region) | https://docs.aws.amazon.com/global-infrastructure/latest/regions/aws-regions.html |
| AWS | Saudi Arabia Region (code not announced; `me-west-1` already appears in AWS IP ranges and may be this Region) | Saudi Arabia | Not live. Target launch December 2026 | https://www.channelinsider.com/infrastructure/news-aws-cloud-region-launch-emea-saudi-arabia/ ; https://ip-ranges.amazonaws.com/ip-ranges.json |
| Microsoft Azure | UAE North; UAE Central | UAE | Listed by Microsoft as "available or coming soon" | https://azure.microsoft.com/en-us/explore/global-infrastructure/geographies/ |
| Microsoft Azure | Saudi Arabia East | Saudi Arabia | Listed as "available or coming soon"; live status not confirmed | https://azure.microsoft.com/en-us/explore/global-infrastructure/geographies/ |
| Microsoft Azure | Qatar Central | Qatar | Listed; Microsoft reports it open | https://azure.microsoft.com/en-us/explore/global-infrastructure/geographies/ |
| Google Cloud | `me-central2` | Dammam, Saudi Arabia | Live. KSA-billed customers buy through CNTXT | https://docs.cloud.google.com/docs/dammam-region-access |
| Google Cloud | `me-central1` | Doha, Qatar | Live since Apr 2023 (code-to-city mapping from a third-party catalogue) | https://datacenterdynamics.com/en/news/google-launches-cloud-region-in-doha-qatar ; https://observer.cloud-mercato.com/providers/google/me-central1 |
| Oracle | UAE East (Dubai); UAE Central (Abu Dhabi) | UAE | Live | https://www.oracle.com/cloud/public-cloud-regions/ |
| Oracle | Saudi Arabia West (Jeddah); Saudi Arabia Central (Riyadh) | Saudi Arabia | Live | https://www.oracle.com/cloud/public-cloud-regions/ |
| Alibaba Cloud | `me-east-1` | Dubai, UAE | Live | https://www.alibabacloud.com/help/en/ecs/user-guide/regions-and-zones |
| Alibaba Cloud | `me-central-1` (partner region) | Riyadh, Saudi Arabia | Live | https://www.alibabacloud.com/help/en/ecs/user-guide/regions-and-zones |
| Huawei Cloud | Riyadh region | Riyadh, Saudi Arabia | Live since Sep 2023 | https://www.huaweicloud.com/intl/en-us/news/20240226211706598.html |

## Watch items

### Data protection (PDPL)

- **ER not yet aligned with RD 68/2026.** RD 68/2026 has been in force since 7 Sep 2026. At 17 Oct 2026 we found no draft, consultation or amendment of the ER. Expect new ER provisions on: controls for objecting to automated processing (Art 14); the controls for Minister's decisions under Art 5 bis(3); and the manner of marketing consent (Art 22).
- **Possible new permit exceptions.** We found no Minister's decision under Art 5 bis(3) yet. One could add permit exceptions, including for health-sector processing.
- **Permit form out of date.** MTCIT's permit application form (English file dated Jan 2026) still lists the ten pre-amendment Art 3 exemptions. A revised form is likely.
- **Guidance at version 0.1.** MTCIT's guidance documents are early versions:
  - privacy policy guide, December 2025;
  - rights template, file dated March 2026;
  - processor guideline, April 2026;
  - consent template, cover dated September 2026 (the first to cite RD 68/2026).

  Expect revisions.
- **External audits.** Auditor accreditation has run since 1 Feb 2026, so MTCIT may start ordering external audits under Art 16.
- **Government Policy.** Circular 6/2024 has applied from about 31 Mar 2026. MTCIT reports compliance to the Council of Ministers. Its legal force is not settled.
- **Enforcement.** We found no published sanctions. The latest MTCIT figures run to the end of May 2026 (Al Roya, 13 Sep 2026): 20 complaints and reports, and 22 breach reports.
- **Permit fees and renewals.** Fees have applied since 1 Jan 2026. Permits last up to 5 years, so track each permit's expiry. We did not find when MTCIT began issuing permits.
- **Recent amendment history.** Trowers (June 2026) reported that the Shura Council was reviewing PDPL amendments in May 2026. RD 68/2026 followed in September. We know of no further amendment bill.

### Cybersecurity, cloud, government IT and AI (NAT)

- **New cybercrime law**: RD 61/2026 has been in force since 8 Jun 2026 and repealed RD 12/2011. Update any checklist, contract or training material that cites the 2011 law.
- **Electronic Transactions Law executive regulation**: RD 39/2025 (Art. II of the decree) leaves it to the MTCIT Minister. It was not in MTCIT's library at 15 Oct 2026. The regulation will set trust-service licensing, the Trust Services Management Committee's working rules and conditions for automated electronic agents.
- **CDC National Cybersecurity Strategy 2026–2030** (reported 29 Aug 2026): "updating legislation" is a stated priority. Watch for a cybersecurity law, critical-infrastructure rules or published national controls.
- **PDPL amendment**: MTCIT's library lists RD 68/2026 amending the PDPL (6 Sep 2026). The PDPL workstream should check how it interacts with TRA Art. 12 and CDC System Art. 4(5).
- **Government personal data policy**: in force about 31 Mar 2026 (24 months after circulation). Confirm the exact date.
- **Cloud First Policy 2026** is version 0.4. Expect revisions. CDC Circular 6/2025 (external cloud) is not public.
- **General Electronic Integration Policy** (Sep 2026): watch for National API Catalog onboarding rules.
- **TRA Omanisation ratios** for permit holders step down at 24, 36 and 48 months after a permit starts (Annex 4).
- **AWS Saudi Arabia Region**: target December 2026. It will not be in Oman.
- **AI**: watch for Ministry of Health or other sector rules adopted under the AI policy, and the AI Special Zone operator's rules.
- **National Records Law executive regulation** (data sources, sharing conditions).

## Questions for advisers

### Data protection (PDPL)

- **Gazette check.** We could not open the Official Gazette PDFs (HTTP 403) or the MJLA site (TLS failure). Advisers should check the texts against OG 1429, 1531, 1580, 1586, 1625 and 1664.
- **No official English text.** We found no official English translation of the law or the ER. The ER English in this file is our own working translation.
- **Ministry of Health exemption (Art 3(b)).**
  - Does it cover a private vendor that processes data for the Ministry?
  - Does it cover Ministry activities outside its legal competence, such as commercial research partnerships?
  - Is Circular 6/2024 legally binding on government units and their vendors?
- **Permits:**
  - Is one permit needed per controller, per facility or per processing activity?
  - Do processors need their own permit?
  - How do foreign controllers without an Omani CR number or Civil ID apply?
  - How will MTCIT treat processing that has needed a permit only since 7 Sep 2026, such as contract-based patient processing, given that RD 68/2026 has no transition period?
- **Controller as "legal person".** The amended definition makes the controller a legal person. Where does that leave clinics run as sole proprietorships, or individual practitioners?
- **Territorial scope.** What does "natural persons in the Sultanate of Oman" mean in practice: residents, people present in Oman, or Omani citizens abroad (for example, medical tourists)?
- **Remote access** from outside Oman (PDPL-30).
- **Transfer consent.** Do the Art 10 bis exceptions also relieve the explicit consent for transfers in ER Art 37, which itself lists only two exceptions?
- **CDC approval.** What is the procedure and form, and how long does it take? Does Art 4(5) bind offshore controllers that are now within the PDPL's scope?
- **Children.** Is 18 the age threshold for the PDPL? How far does the "best interest" exception reach, for example in urgent paediatric care?
- **Disclosure of sensitive data.** What counts as a "case set by law" under ER Art 25? Does patient consent allow disclosure to insurers or other providers?
- **DPO.** Must the DPO live in Oman? Is filing the appointment form mandatory? Can one DPO serve a group of companies?
- **Breach details.** The ER set no deadline for a processor to notify its controller. The retention period for the breach record is "as MTCIT sets", but we found no published figure.
- **Medical-record retention.** Retention periods for medical records come from health legislation, which another workstream covers. They are the main "legal obligation" exception to erasure under Art 15.
- **Accuracy and minimisation.** Neither the law nor the ER sets a general accuracy or data-minimisation duty for private controllers. The exception is the minimum-data rule for children's data. MTCIT's policy guide treats minimisation as a principle, and the government Policy requires accuracy and minimum collection.
- **Language.** We found no rule on the language of notices or consent forms.
- **Conflicting secondary sources:**
  - Trowers (Feb 2024) gives 29 Jan 2024 as the ER start date. The Gazette-based date is 5 Feb 2024.
  - Al Tamimi's ER summary describes guardian consent and transfer consent as "written". The Arabic says "explicit".
  - A vendor blog (BeamSec) misstates the 2026 penalty changes. We did not rely on it.
- **Related instruments covered elsewhere in the library:**
  - The CDC System and its duties (NAT-01 to NAT-03). The CDC's own standards and controls are not public.
  - MTCIT's General Policy for the Safe and Ethical Use of AI Systems, April 2025 (NAT-30).
  - TRA cloud and data-centre rules (NAT-04 to NAT-08).
  - Ministry of Health rules, including the confidentiality of health records (`health-sector.md`).
  - Financial Services Authority rules for health insurers (`insurance-devices.md`).
- **Related instruments not reviewed:**
  - MD 108/2025, the Government Digital Transformation Regulation (OG 1592, 20 Apr 2025). It requires a security assessment before government systems launch (compare NAT-12).
  - The Biometric Prints Law, RD 21/2024 (OG 1539, 31 Mar 2024). A secondary summary says it governs a forensic biometric database and restricts DNA testing. Genetic-testing products should check it.

### Cybersecurity, cloud, government IT and AI (NAT)

- **Is healthcare critical national infrastructure?** No public CDC designation was found. Are the Ministry of Health and private hospitals "concerned entities" under RD 64/2020 Art. 1(7)? In May 2026 the head of the CDC called healthcare cybersecurity part of national security, but that is not a legal designation (https://www.zawya.com/en/economy/gcc/oman-healthcare-sector-urged-to-strengthen-cyber-defences-342008).
- **CDC standards and controls** (System Art. 4(4)) and **CDC Circular 6/2025** are not public. Ask the client or the CDC for the current set. Some commercial websites describe an "Oman National Cybersecurity Framework" with control IDs. No official source for it was found; do not rely on them.
- **CDC incident reporting**: "immediately" has no hour limit, and the reporting channel on cdc.gov.om could not be checked.
- **"Sensitive data"** in CDC System Art. 4(5) is not defined. Does it cover all personal health data of a private provider?
- **TRA permits**: Does a health SaaS vendor need its own permit, or only its host? Which permit class applies to SaaS? Is the Cloud First Policy's "Category Four authorisation" the same as a Category 4 data-centre permit? Is a digital-health company that is not a licensed health institution "in the health sector" (Level 4)?
- **Provider permits**: No public list of TRA permit holders or their data-centre categories was found (AWS Muscat Local Zone, Oracle and ITHCA or Oman Data Park, Omantel, Ooredoo, others). Ask each provider.
- **NDGF**: the framework documents (including the Data Classification Policy) could not be opened. Their classification levels for health data are unknown.
- **Older standards**: Is the 2018/2019 Cloud and Hosting Services Standard still applied alongside the TRA regulation? Has the 2017 Basic Security Controls been replaced by the "Basic Cybersecurity Controls" reported in 2024?
- **Omani-only staffing** (Circulars 7/2020 and 11/2021): Do they reach offshore development and support teams? Do they cover all government-owned hospitals and companies?
- **Electronic transactions**: Do regulations made under the repealed 2008 law still apply where they do not conflict with the 2025 law? Which signature level does the Ministry of Health expect for e-consent and e-prescriptions (health workstream)?
- **e-ID integration**: protocols, fees and eligibility of private hospitals and foreign vendors for the Thiqa / e-identity gateway. Status of the older SIM-based mobile PKI was not checked.
- **AI policy status**: binding on government units as policy, but commentators call it non-binding. Its effect on private providers depends on the Ministry of Health adopting it as sector regulator.
- **Foreign vendor set-up**: foreign investment and commercial registration rules, government tender rules and staff security clearance (seen here only for security assessors and accredited cloud providers) were not researched.
- **Translation**: all Arabic-only texts were machine-translated by the AI researcher. Key wording (TRA Annex 2, CDC System Art. 4, Circulars 7/2020, 11/2021 and 20/2025, RD 61/2026 Art. 8) should be checked by an Arabic-reading Omani adviser.
- **Library dates**: MTCIT's library dates sometimes differ from the signed circulars (Circular 19/2023; Circular 10/2026; Circular 9/2021 is listed as 27 May 2020). This file uses the signed dates.

## Primary and secondary sources used

### Data protection (PDPL)

- https://qanoon.om/p/2022/rd2022006/ — Full Arabic text of RD 6/2022 and the original PDPL (Arts 1–32); gazette number and dates.
- https://qanoon.om/p/2026/rd2026068/ — Full Arabic text of RD 68/2026 amendments; OG 1664 and in-force rule.
- https://decree.om/2026/rd20260068/ — Unofficial English translation of RD 68/2026, used to cross-check our reading.
- https://decree.om/2022/l20220006/ — Unofficial English consolidated PDPL (to RD 68/2026); English wording of articles.
- https://qanoon.om/p/2024/mtcit20240034/ — Full Arabic text of MD 34/2024 and the ER (Arts 1–45); gazette and in-force rule; original one-year compliance period.
- https://qanoon.om/p/2025/mtcit20250006/ — MD 6/2025 extending the compliance period to two years.
- https://qanoon.om/p/2025/mtcit20250448/ — MD 448/2025 permit fees and effective date.
- https://qanoon.om/p/2025/mjla20250046/ — MD 46/2025 giving judicial police powers to MTCIT PDP specialists.
- https://qanoon.om/p/2024/mtcit20240006/ — MTCIT Circular 6/2024, government Personal Data Protection Policy (full Arabic text).
- https://qanoon.om/p/2020/rd2020064/ — CDC System, Art 4 (duties of concerned entities, including CDC approval for sensitive data outside Oman).
- https://qanoon.om/p/2014/rd2014022/ — Child Law Art 1(d), definition of child.
- https://qanoon.om/p/2013/rd2013029/ — Civil Transactions Law Art 41, age of majority and full capacity.
- https://qanoon.om/p/2026/og1664/ , https://qanoon.om/p/2024/og1531/ , https://qanoon.om/p/2025/og1580/ , https://qanoon.om/p/2025/og1625/ , https://qanoon.om/p/2022/og1429/ — Gazette issue listings used to confirm publication dates.
- https://qanoon.om/p/2024/rd2024021/ — Title and gazette data of the Biometric Prints Law (not reviewed in detail).
- https://qanoon.om/p/2025/mtcit20250108/ — MD 108/2025 Government Digital Transformation Regulation (scanned for data clauses only).
- https://mtcit.gov.om/sectors/governance/personal and https://mtcit.gov.om/ar/sectors/governance/personal — MTCIT PDP Department remit, online services (permits, complaints, breach reporting), forms list, FAQ (government exemption, permits, consent, DPO, complaints, 72-hour breach notice, CDC approval, transfer consent), contact PDPC@mtcit.gov.om.
- https://mtcit.gov.om/web/content/65556 — Permit application form, English (file dated Jul 2024).
- https://mtcit.gov.om/web/content/55067 — Permit application form, English (file dated Jan 2026; includes the Art 3 exemption declaration).
- https://mtcit.gov.om/web/content/29069 , https://mtcit.gov.om/web/content/29068 , https://mtcit.gov.om/web/content/29067 , https://mtcit.gov.om/web/content/29066 — Permit amendment (15 days), renewal (5 years), cancellation and grievance forms, English.
- https://mtcit.gov.om/web/content/29065 — Personal data processing record form, English.
- https://mtcit.gov.om/web/content/29062 — Personal data breach report form, English (72 hours).
- https://mtcit.gov.om/web/content/29058 — DPO appointment form, English.
- https://mtcit.gov.om/web/content/29057 — Transfer protection-level and risk assessment form, English (CDC note).
- https://mtcit.gov.om/web/content/29056 — Complaint/report form, English.
- https://mtcit.gov.om/web/content/55069 — Privacy policy guide and template, Arabic (v0.1, Dec 2025).
- https://mtcit.gov.om/web/content/38034 — Data subject rights guideline template, Arabic (file dated Mar 2026).
- https://mtcit.gov.om/web/content/48307 — Guideline on controller responsibility when contracting a processor, Arabic (v0.1, Apr 2026).
- https://mtcit.gov.om/web/content/65865 — Explicit consent guideline and template, Arabic (cover dated Sep 2026; cites RD 68/2026).
- https://mtcit.gov.om/library-3/report-studies-9/reports-79/personal-data-protection-reports-379 — MTCIT page on reporting violations and breaches (PDPC@mtcit.gov.om).
- https://mtcit.gov.om/media-4/events-competitions-10/event-81/implementation-and-launch-of-the-external-auditor-accreditation-project-in-the-field-of-personal-data-protection-1381 — External auditor accreditation launch (1 Feb 2026).
- https://prod.mtcit.gov.om/ITAPortal/MediaCenter/NewsDetail.aspx?NID=91274 — MTCIT English news summary of the ER (permit, 5-year term, 72 hours, DPO, transfers, sanctions).
- https://alroya.om/post/394000 — Al Roya, 13 Sep 2026: MTCIT figures (20 complaints/reports, 22 breach reports to end May 2026) and comment on RD 68/2026.
- https://cms.law/en/omn/legal-updates/oman-personal-data-protection-law-entering-the-enforcement-phase — CMS, Feb 2026: transition end 5 Feb 2026; DPO-in-Oman preference; CDC approval.
- https://cms.law/en/omn/legal-updates/oman-updates-its-personal-data-protection-law — CMS, 2026: summary of RD 68/2026; OG 1664; effective 7 Sep 2026.
- https://www.bakermckenzie.com/en/insight/publications/2026/09/oman-strengthening-its-data-protection-regime — Baker McKenzie, Sep 2026: effective date 7 Sep 2026.
- https://www.trowers.com/insights/2026/june/personal-data-and-artificial-intelligence-recent-regulatory-developments-in-oman — Trowers, Jun 2026: Circular 6/2024, deadline 5 Feb 2026, Shura review May 2026.
- https://www.trowers.com/insights/2024/february/omans-data-protection-law---new-regulations — Trowers, Feb 2024: ER summary (gives 29 Jan 2024 start date; conflicts with Gazette).
- https://turtl.tamimi.com/story/the-new-executive-regulations-of-the-personal-data-protection-law-of-oman/page/1 — Al Tamimi, May 2024: ER summary (cross-check only).
- https://blog.decree.om/2026/new-amendments-to-the-personal-data-protection-law — decree.om blog, 7 Sep 2026: amendment overview (staff biometrics under Art 5 bis).
- https://blog.decree.om/2024/mtcit-issues-personal-data-protection-policy-for-government-entities/ — decree.om blog, Apr 2024: scope and legal force of the government Policy.
- https://blog.decree.om/2025/4-differences-between-the-personal-data-protection-law-and-the-personal-data-protection-policy/ — decree.om blog, 2025: Policy said to be non-binding; no DPO duty for government units.

### Cybersecurity, cloud, government IT and AI (NAT)

- https://qanoon.om/p/2020/rd2020064/ — Arabic text of RD 64/2020 and the CDC System (Arts. 1, 2, 4, 6).
- https://decree.om/2020/rd20200064/ — English decree articles, dates and Gazette number for RD 64/2020.
- https://ncsi.ega.ee/country/om/ — eGA National Cyber Security Index entry for Oman: cites CDC System Art. 4(2), RD 39/2025, OCERT, PKI and ISMP/BSC URLs.
- https://www.muscatdaily.com/2026/08/29/oman-unveils-2026-2030-cybersecurity-strategy/ and https://timesofoman.com/article/176173-oman-launches-national-cyber-security-strategy-20262030-to-strengthen-digital-resilience — CDC National Cybersecurity Strategy 2026–2030.
- https://moh.gov.om/en/hospitals-directorates/news-details/?id=88544d32-607e-4698-ba3d-4e760cf92fa0&p=184569 and https://www.zawya.com/en/economy/gcc/oman-healthcare-sector-urged-to-strengthen-cyber-defences-342008 — May 2026 healthcare cyber exercise and conference; no CNI designation.
- https://qanoon.om/p/2024/tra20249905/ — Arabic text of the TRA Regulation on Cloud Computing Services and Data Centres (all articles and annexes).
- https://www.mondaq.com/data-protection/1540350/navigating-the-new-telecommunications-regulatory-authority-tra-regulations-on-cloud-computing-and-data-centres-in-oman-legal-implications-and-subscriber-challenges — SASLO commentary on the TRA regulation (cross-check of Arts. 10–12).
- https://tra.gov.om/files//uploads/altqryr_alsnwy_2024_ENG_compressed_59a23dcc7b.pdf — TRA Annual Report 2024 confirming the regulation's issue (26 Sep 2024).
- https://mtcit.gov.om/library-3/legislations-policies-8/policies-73 — MTCIT policy library listing.
- https://mtcit.gov.om/library-3/legislations-policies-8/policies-73/cloud-first-policy-1416 and https://mtcit.gov.om/web/content/65140?unique=3fa2201e361918b0a91a95c4949bd6e45c8ed02a — Cloud First Policy 2026 (English).
- https://mtcit.gov.om/library-3/guidelines-documentation-7/circulars-66/cloud-computing-first-circular-1417 and https://mtcit.gov.om/web/content/54749?unique=890129923ec3607c7af38ba3fbbd5ff95cb053ba — Circular 10/2026.
- https://mtcit.gov.om/library-3/legislations-policies-8/policies-73/the-cloud-computing-policy-644 and https://mtcit.gov.om/web/content/43341?unique=563eccfb2288d046f25161ed0afdbfae2cb91be2 — 2021 Cloud First / Cloud Computing Policy (English).
- https://mtcit.gov.om/library-3/guidelines-documentation-7/standards-64/cloud-and-hosting-services-standard-263 and https://mtcit.gov.om/web/content/mtcit.content/263/attachment?download=True — Cloud and Hosting Services Standard.
- https://mtcit.gov.om/web/content/mtcit.content/264/attachment?download=True — Security Assessment Services Standard.
- https://mtcit.gov.om/library-3/guidelines-documentation-7/circulars-66/ministerial-circular-on-the-regulatory-framework-for-national-data-governance-and-management-762 — MTCIT circulars listing and NDGF circular page.
- https://mtcit.gov.om/web/content/mtcit.content/762/attachment?download=True — Circular 2/2025 and letter 113/2025 (NDGF).
- https://mtcit.gov.om/web/content/mtcit.content/1277/attachment?download=True — Circular 3/2026 and IT Risk Management Policy.
- https://mtcit.gov.om/web/content/mtcit.content/1328/attachment?download=True — IT Operations Continuity Policy v2.
- https://mtcit.gov.om/web/content/mtcit.content/1342/attachment?download=True and https://mtcit.gov.om/web/content/mtcit.content/765/attachment?download=True — Personal Data Protection Policy for government units and Circular 6/2024.
- https://mtcit.gov.om/web/content/mtcit.content/772/attachment?download=True and https://mtcit.gov.om/web/content/mtcit.content/388/attachment?download=True — Circular 16/2026 and General Electronic Integration Policy.
- https://mtcit.gov.om/web/content/mtcit.content/1265/attachment?download=True — Circular 20/2025 (source code).
- https://mtcit.gov.om/web/content/mtcit.content/755/attachment?download=True — Circular 7/2025 and managed services standards.
- https://mtcit.gov.om/web/content/mtcit.content/775/attachment?download=True — Circular 19/2023 (mobile apps); also reference to ISMP as Circular 4/2019.
- https://mtcit.gov.om/web/content/mtcit.content/827/attachment?download=True — Circular 11/2022 (security assessments).
- https://mtcit.gov.om/web/content/mtcit.content/1098/attachment?download=True — Circular 3/2020 (database security).
- https://mtcit.gov.om/web/content/mtcit.content/1100/attachment?download=True and https://mtcit.gov.om/web/content/mtcit.content/1102/attachment?download=True — Circulars 7/2020 and 11/2021 (Omani-only roles).
- https://cert.gov.om/files/laws/Information_Security_Management_Policy_EN.pdf — ITA Information Security Management Policy.
- https://cert.gov.om/files/laws/Basic_Security_Controls_EN.pdf — ITA Basic Security Controls.
- https://meatechwatch.com/?p=3678 — news of further MTCIT cybersecurity guides (not seen).
- https://www.tamimi.com/law_update_articles/omans-issues-mandatory-it-risk-management-policy/ and https://www.lexis.ae/2026/04/17/oman-ministry-enacts-unified-it-risk-management-policy-for-government/ — commentary on the IT Risk Management Policy.
- https://blog.decree.om/2024/mtcit-issues-personal-data-protection-policy-for-government-entities/ — commentary on the government personal data policy.
- https://btw.media/en/duqm-data-centre-and-the-price-of-omani-cloud-locality — secondary report on MTCIT's register of approved hosting providers and local providers.
- https://www.omanobserver.om/ampArticle/8180 and https://timesofoman.com/article/106966-accreditation-programme-for-it-service-providers-starts-in-oman — MTCIT IT service provider accreditation programme.
- https://mtcit.gov.om/library-3/legislations-policies-8/laws-75/electronic-transactions-law-1031 and https://mtcit.gov.om/web/content/mtcit.content/1031/attachment?download=True — RD 39/2025 (Official Gazette 1591 text).
- https://qanoon.om/p/2025/rd2025039/ — Arabic text of RD 39/2025.
- https://decree.om/2025/rd20250039/ — decree articles, dates, repeal of RD 69/2008.
- https://blog.decree.om/2025/new-electronic-transactions-law-issued/ , https://tamimi.com/news/oman-enacts-new-electronic-transactions-law-royal-decree-no-39-2025 and https://www.omanobserver.om/article/1168977/business/economy/new-law-offers-safety-net-legal-framework-for-e-transactions — commentary on RD 39/2025.
- https://mtcit.gov.om/library-3/legislations-policies-8/laws-75/cybercrime-combat-law-1030 and https://mtcit.gov.om/web/content/mtcit.content/1030/attachment?download=True — RD 61/2026 (Official Gazette 1651 scan).
- https://qanoon.om/p/2026/rd2026061/ — Arabic text of RD 61/2026.
- https://qanoon.om/p/2011/rd2011012/ — repealed Cybercrime Law RD 12/2011 (for comparison).
- https://qanoon.om/p/2011/rd2011118/ and https://qanoon.om/p/2019/rd2019026/ — classification law RD 118/2011 and amending RD 26/2019.
- https://qanoon.om/p/2024/rd2024052/ — National Records Law RD 52/2024.
- https://cert.gov.om/sp/pki and https://cert.gov.om/ — National Cyber Security Center digital trust services (Thiqa, PKI).
- https://mtcit.gov.om/services-5/services-13/services-92/electronic-identity-gateway-for-government-and-private-services-817 — Electronic Identity Gateway service.
- https://oman.om/en/home-top-level/whole-of-government/central-initiative/oman-national-cert — OCERT background.
- https://mtcit.gov.om/library-3/legislations-policies-8/policies-73/general-policy-for-the-safe-and-ethical-use-of-artificial-intelligence-systems-291 and https://mtcit.gov.om/web/content/43446?unique=e7cce2bd929945913acb8a932e3067e70aeadbe4 — AI policy (English).
- https://blog.decree.om/2025/mtcit-issues-public-policy-for-ethical-use-of-ai/ and https://blog.decree.om/2024/omans-national-artificial-intelligence-policy/ — AI policy status and 2024 draft.
- https://www.trowers.com/insights/2026/june/personal-data-and-artificial-intelligence-recent-regulatory-developments-in-oman — AI policy status, AI Special Zone, PDPL amendment context.
- https://decree.om/2026/rd20260050/ — RD 50/2026 (AI Special Zone).
- https://www.omanobserver.om/ampArticle/1104392 — 2021 MTCIT AI principles circular for government units.
- Cloud region sources: https://aws.amazon.com/about-aws/whats-new/2022/11/aws-local-zones-buenos-aires-copenhagen-helsinki-muscat ; https://ip-ranges.amazonaws.com/ip-ranges.json ; https://docs.aws.amazon.com/global-infrastructure/latest/regions/aws-regions.html ; https://www.channelinsider.com/infrastructure/news-aws-cloud-region-launch-emea-saudi-arabia/ ; https://oerlive.com/technology/oman-information-and-communication-technology-group-launches-the-first-oracles-hyper-scale-cloud-infrastructure-data-center-in-oman/ ; https://www.datacenterdynamics.com/en/news/oracle-launches-second-oci-dedicated-region-in-oman/ ; https://www.zawya.com/en/press-release/companies-news/oman-data-park-launches-oci-secondary-dedicated-region-in-partnership-with-ithca-and-oracle-in-ibri-suqtqnyi ; https://www.oracle.com/cloud/public-cloud-regions/ ; https://azure.microsoft.com/en-us/explore/global-infrastructure/geographies/ ; https://www.gstatic.com/ipranges/cloud.json ; https://docs.cloud.google.com/docs/dammam-region-access ; https://datacenterdynamics.com/en/news/google-launches-cloud-region-in-doha-qatar ; https://observer.cloud-mercato.com/providers/google/me-central1 ; https://www.samenacouncil.org/samena_daily_news?news=111292 ; https://www.huaweicloud.com/intl/en-us/news/20240226211706598.html ; https://timesofoman.com/article/142298-omantel-unveils-cloud-dominance-with-launch-of-national-cloud ; https://www.alibabacloud.com/help/en/ecs/user-guide/regions-and-zones ; https://www.omanobserver.om/article/1101963/business/economy/chinas-alibaba-to-invest-in-cloud-computing-centre-in-oman ; https://news.sap.com/mena/2023/06/sap-launch-omans-first-data-center-for-private-cloud/
