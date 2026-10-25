# Checklist register and Excel export

The register in the project is the source of truth. The Excel file is generated from it after every check or recheck.

## Folder layout

```
.oman-health-compliance/
├── scope.md            Scope answers, customer type, regulators, library version used
├── checklist.json      The register (source of truth)
├── CHECKLIST.md        Readable view, regenerated after every change
├── history.jsonl       Append-only event log
├── runs/C1.md          One summary per check run
└── export/             Excel checklists, one per run
```

**Git:** advise the team to commit the folder in private repositories, so everyone shares one checklist, and never in public ones, because it describes the system's compliance gaps. Don't run git commands that change the repository yourself.

## checklist.json

```json
{
  "schema": "oman-health-checklist/1",
  "project": "Clinic booking portal",
  "libraryAsOf": "2026-10-17",
  "customerType": "Private hospital",
  "cyberScope": "Not designated by the Cyber Defence Centre (stated)",
  "regulators": ["PDPL/MTCIT", "CDC", "MOH"],
  "runs": [{ "id": "C1", "date": "2026-10-18", "commit": "a1b2c3d", "agent": "<agent and model, as reported>",
             "readiness": { "met": 18, "partly": 9, "missing": 14, "confirm": 11, "na": 22, "info": 4, "percent": 35 } }],
  "items": [
    {
      "ref": "PDPL-29",
      "regulator": "CDC",
      "source": "CDC System (RD 64/2020) Art. 4(5); MTCIT PDPL FAQ",
      "requirement": "Get Cyber Defence Centre approval before storing or processing health data outside Oman.",
      "engineeringTask": "Move error tracking to an Oman-hosted instance or strip all patient data before sending; don't send health data to any offshore service until CDC approval is recorded.",
      "taskId": "T-03",
      "satisfies": ["PDPL-28", "PDPL-29", "MOH-14"],
      "theme": "Offshore data flows",
      "priority": "Blocker",
      "responsible": "Shared",
      "status": "Missing",
      "evidence": "src/app.js:3 Sentry DSN to a US ingest endpoint with sendDefaultPii: true ✘",
      "statedBy": null,
      "owner": null,
      "due": null,
      "libraryConfidence": "Confirmed (primary)",
      "regressed": false,
      "notes": ""
    }
  ]
}
```

Record the agent and model that did the check in each run's `agent` field, using the names given in your own instructions or by the user. Don't run commands or open settings or environment files to find them. If they aren't stated, write "not reported".

For a product sold to several customer types, `customerType` is a list, for example `["Private hospital", "Government health provider"]`.

**Themes.** Use one of these in `theme`, in this order (they follow `evidence-guide.md`):

1. Hosting and residency
2. Offshore data flows
3. Offshore access and development
4. Identity and access
5. Audit logging
6. Data model and records
7. Encryption and keys
8. National platforms and insurance
9. Development lifecycle and vendors
10. Backup and continuity
11. AI features
12. Telehealth
13. Patient-facing language and notices
14. Marketing and promotion
15. Prescribing and pharmacy
16. Governance, permits and approvals
17. Incident readiness

## Status values

| Status | Meaning |
|---|---|
| **Met** | Evidence found that satisfies the requirement. Cite it. For things outside the system, a named person's stated answer, recorded as below. |
| **Partly met** | Some evidence, with a gap. Say what's missing. |
| **Missing** | No evidence, or evidence that contradicts the requirement. |
| **Not applicable** | Doesn't apply to this scope. A reason is required. |
| **Needs confirmation** | Can't be decided from the system: waiting for an answer, a document, or confirmation of an unconfirmed library item. |
| **Informational** | A scope, penalty or status provision with nothing to build or test. Listed for awareness. |

**Readiness** = Met ÷ (all items − Not applicable − Informational), as a whole-number percentage. Always label it "indicator only, not certification".

Show how many Met items rest on stated answers ("Met 18, of which stated 3") wherever readiness is shown, so the reader can tell evidence from statements.

**Stated answers.** Never mark an item Met on someone's word alone when the evidence should be visible in the system. A stated answer can close an item only for things outside the system: permits, approvals, contracts, policies, appointments, team location. Then:

- set the status to Met and put the person in `statedBy`, for example "Meera, tech lead (stated)"
- the person must be named. If the requester gives no name, ask once. Without a name, keep the item Needs confirmation
- for a permit, approval, licence or registration (the MTCIT permit, Cyber Defence Centre approval, the Ministry of Health's approval of the information system, a telehealth licence, FSA registration, medical device registration), record its reference number, issue and expiry dates, and scope in `evidence`. Without them, the item stays Needs confirmation
- check that the recorded scope covers what the system does now: its purposes, data categories, processors and hosting locations. If the MTCIT permit doesn't cover them, PDPL-07 is Partly met, and PDPL-09 stays Missing until the change has been notified to MTCIT

`regressed` is set to true by `oman-health-recheck` when an item that was Met loses its evidence.

## Priority

| Priority | When to use it |
|---|---|
| **Blocker** | A legal prohibition, or a gate on going live: processing health data without an MTCIT permit, storing or processing health data outside Oman without Cyber Defence Centre approval, offshore access without a confirmed basis, an MOH licence or approval that the service needs (approved health information system, telehealth licence, medical device authorisation), a regulator deadline |
| **High** | Core security and privacy controls: access control, audit logging, encryption, consent, breach readiness, retention, patient rights |
| **Medium** | Process and documentation controls with a clear engineering element |
| **Low** | Good practice and future-proofing |

Not applicable and Informational items have no task; give them Low priority. A Met item keeps the priority it would have if it were open.

If nobody has assessed whether a feature is a medical device, MDV-02 is Missing. Give it Blocker priority when the feature triages, diagnoses or supports clinical decisions, and High otherwise.

## Shared tasks

Where one piece of work satisfies several items, give it one task ID (`T-01`, `T-02`, …). Put the same `taskId` on each of those items, and list every item the task closes in `satisfies`, including the item itself. The recheck then closes them together, but only on evidence for each item. If an item needs two pieces of work, give it the main task's ID and name the other task in `notes`.

A task's theme is the theme of the first item in its `satisfies` list.

## Blocker grouping

In summaries, group Blockers by root cause, for example:

- offshore data flows and hosting outside Oman
- offshore access and development
- MTCIT permit and PDPL governance
- MOH approvals and licences (health information system, telehealth, teleradiology)
- government data and hosting
- medical device authorisation
- national platforms and insurance (Shifa, Dhamani)

Show the item references under each group, so the list stays scannable.

## Ordering the "next tasks"

A task's priority is the highest priority among its items. List the next 10 Blocker and High-priority tasks in this order:

1. Leave out tasks whose items are all Needs confirmation; those go in the Questions sheet.
2. Put first any task about a possible breach, such as real patient data found in the repository.
3. Then Blocker tasks, then High tasks.
4. Within each, order by theme: Identity and access, Audit logging, Data model and records, Encryption and keys, Incident readiness, Development lifecycle and vendors, Patient-facing language and notices, then the other themes in the order listed above.
5. Within a theme, put first the tasks that close the most items (`satisfies` count).
6. Then order by the task's lowest reference, in library order (PDPL, NAT, MOH, TEL, INS, MDV, RX, then INT).

## Engineering task wording

Each item needs one concrete, testable task. Examples:

- Good: "Lock accounts after 3 failed logins and disable accounts unused for 180 days (auth/login.ts, a nightly job)."
- Bad: "Improve password security."

## history.jsonl

One JSON object per line, append only. Fields: `ts` (ISO 8601, UTC), `event`, `ref` (or `-` for run events), `run`, `commit`, and as relevant `from`, `to`, `by` (as stated, with "(stated)"), `evidence` and `note`.

Events: `run-start`, `created`, `status`, `owner`, `priority`, `note`, `run-end`. If a run is interrupted and its outputs are written again, add a `note` event saying so; never rewrite earlier lines.

```json
{"ts":"2026-10-18T09:00:00Z","event":"run-start","ref":"-","run":"C1","commit":"a1b2c3d"}
{"ts":"2026-10-18T09:40:00Z","event":"created","ref":"PDPL-29","run":"C1","commit":"a1b2c3d","to":"Missing","evidence":"src/app.js:3 Sentry US ingest"}
```

## Excel export

File name: `export/Oman-Health-Compliance-<project>-C<n>-<date>.xlsx`.

Build it with Python and openpyxl if available, with a spreadsheet skill if the session has one, or as CSV files if neither is available, and say so. Don't install packages without the user's agreement. Use the font from the house rules: Arial by default, 10 pt. No headers or footers.

**Sheets:**

1. **Summary:**
   - project, date, commit, regulators, customer type, cybersecurity scope, library date, agent and model, approver
   - counts by status, by priority and by regulator (static values, so they can be checked against the register), with Met split into evidence and stated answers
   - open Blockers listed by name
   - a "Readiness" line (formula above), labelled as an engineering readiness indicator, not a compliance certification
   - Blockers grouped by root cause
2. **Checklist:** one row per item. Columns: Ref · Regulator · Theme · Requirement · Source · Task ID · Engineering task · Also satisfies (the other items) · Priority · Responsible · Status · Evidence · Stated by · Owner · Due · Library confidence · Notes.
   - Colour the Status cell of Informational items light grey.
   - Freeze the header row and turn on filters.
   - Add a drop-down for Status and Priority.
   - Colour Status: Met green, Partly met amber, Missing red, Needs confirmation blue, Not applicable grey.
   - Wrap text and set sensible column widths.
3. **Questions:** open questions, who should answer, and the item each one unblocks. Include the library's "Questions for advisers" only where they decide an item in this scope, and mark them "for an adviser". List any "Possible additional requirements (not in library)" at the end of this sheet, under that heading. The summary's "Open questions" count is the number of open questions on this sheet, adviser questions included; give the possible additional requirements as a separate count.
4. **Watch items:** pending rules and deadlines from the library that touch this scope.
5. **Sources:** each regulator document used, with its link and the library's "as of" date.

Put this note at the bottom of the Summary sheet:

> "Engineering readiness checklist generated from a requirements library dated <date>. Not legal advice or certification; confirm requirements with the regulator or a qualified adviser."
