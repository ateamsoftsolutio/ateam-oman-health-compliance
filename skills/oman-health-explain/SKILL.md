---
name: oman-health-explain
description: Explains Oman's healthcare compliance requirements to engineers in plain language, with sources and design guidance, covering the amended PDPL, Cyber Defence Centre approval, TRA cloud and MTCIT rules, the Ministry of Health, telehealth, Dhamani insurance and medical devices. Use when someone asks "can we use an AI API with Omani patient data", "do we need an MTCIT permit", "how does Dhamani integration work" or "explain PDPL-29".
---

# Oman Health Explain

This skill answers engineers' questions about Oman's healthcare requirements, using the library in `../oman-health-check/references/library/`, and helps them design a compliant way to build things.

## How to answer

1. **Find the requirement(s)** in `national.md`, `health-sector.md` or `insurance-devices.md`, by topic, regulator or ID.
2. **Answer in plain language:**
   - what the rule says
   - who it applies to: government health providers, private providers, insurers and TPAs, telehealth, medical-device software
   - what it means for the system
3. **Cite the library ID and source,** for example "PDPL-29 (CDC System Art. 4(5); MTCIT FAQ)", together with the item's confidence and its "as of" note. Mention that the Arabic text prevails and that the library's English is a working translation.
4. **Give a design suggestion:** one or two practical ways to meet it, for example Oman-hosted models, an MTCIT permit dossier generated from the data inventory, synthetic test data, versioned clinical records, or a Dhamani adapter layer.
5. **Flag uncertainty honestly:**
   - If the library marks an item Unconfirmed, say so and suggest how to confirm it.
   - If the library doesn't cover the question, say so. Label any general knowledge as unverified.
6. **Point out pending changes,** such as the Executive Regulations still to be updated for Royal Decree 68/2026, or the 31 December 2026 deadline for registering high-risk medical devices.
7. **Close with:** "Engineering guidance from a library dated <date>, not legal advice."

## Common questions to be ready for

- **Offshore services, AI APIs and offshore teams:** PDPL-28 to PDPL-30, MOH-14, MOH-13 and TEL-02. Explain the Cyber Defence Centre approval. For private providers, whether remote access from abroad counts as processing outside Oman is an open question; for government providers, the government policy treats it as a transfer (PDPL-05).
- **Whether the PDPL applies at all:** PDPL-04 and PDPL-05. Government units acting within their legal competences are outside it, and MTCIT's government policy applies instead.
- **The MTCIT permit:** PDPL-07 to PDPL-10. Since 7 September 2026, treatment based on a patient contract still needs the permit.
- **Consent and its exceptions:** PDPL-11 and PDPL-12, and how they relate to the MOH consent rules (MOH-03, MOH-17).
- **Deleting and correcting records:** PDPL-18 against MOH-06 and MOH-15. Clinical records are amended, not deleted, and retention follows the national records schedule.
- **Where to keep the data:** NAT-04 and NAT-05 (health-sector content in a Category 4 data centre in Oman), the "Cloud regions in and near Oman" table in `national.md`, and PDPL-29 and MOH-14 for anything abroad.
- **Automated decisions and AI:** PDPL-19, MOH-25, MOH-26 and NAT-30.
- **Electronic consent and signatures:** NAT-24, NAT-25 and NAT-27, with MOH-03.
- **Government projects:** NAT-09 to NAT-23, including source code ownership or escrow (NAT-21) and Omani-only staffing for security, network, database, development and support roles (NAT-22).
- **Dhamani integration:** INS-03 to INS-08 and INS-16.
- **Whether a feature is a medical device:** MDV-02 and MDV-03.

If the engineer wants the answer applied to their project, suggest running `oman-health-check`.
