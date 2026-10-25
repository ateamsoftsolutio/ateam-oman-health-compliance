# Oman Healthcare Compliance by ATeam

**Know what Oman's regulators require, see what your system already does, and build the rest.**

This plugin checks a healthcare software system against Oman's healthcare rules. It produces an engineering checklist: every applicable requirement, its source, the evidence found in your system, and the concrete task to close each gap. The checklist is kept as a register in your project and exported to Excel, and it is re-checked as engineers build.

It's built for **Claude Code**, the **Claude app** (with a project folder), **Cursor** and **OpenAI Codex**. It was built by [ATeam Soft Solutions](https://www.ateamsoftsolutions.com), a software and AI engineering firm that builds healthcare systems for GCC providers, including in Oman. We share it as a contribution to the community.

## Install

### Claude Code and the Claude app

Search for "Oman Healthcare Compliance by ATeam" in Claude's plugin directory, or in Claude Code run:

```
/plugin install ateam-oman-health-compliance --marketplace ateamsoftsolutio/ateam-oman-health-compliance
```

On older versions of Claude Code, add the marketplace first:

```
/plugin marketplace add ateamsoftsolutio/ateam-oman-health-compliance
/plugin install ateam-oman-health-compliance@ateam-oman-health
```

If you installed it with one of the commands above, update it later with these two commands, then restart Claude Code. The first fetches the new version; without it, the second reports that you're already up to date.

```
claude plugin marketplace update ateam-oman-health
claude plugin update ateam-oman-health-compliance@ateam-oman-health
```

### Cursor

1. Open a terminal in Cursor's local plugin folder, `.cursor/plugins/local` inside your home folder. Create the folder if it doesn't exist.
2. Run:

   ```
   git clone https://github.com/ateamsoftsolutio/ateam-oman-health-compliance
   ```

3. In Cursor, run **Developer: Reload Window**.

To update later, run `git pull` in the `ateam-oman-health-compliance` folder and reload again. On Cursor Enterprise, local plugin imports are off by default, so ask your Cursor admin.

### OpenAI Codex

```
codex plugin marketplace add ateamsoftsolutio/ateam-oman-health-compliance
codex plugin add ateam-oman-health-compliance@ateam-oman-health
```

You can also install it from the plugin browser (`/plugins`) after adding the marketplace. Start a new Codex session after installing. To update later, run `codex plugin marketplace upgrade ateam-oman-health`.

### Other agents

The repository also has a root `plugin.json` in the open [Agent Plugins](https://agent-plugins.org) format, so other agents that support that format may load it. We support Claude, Cursor and Codex.

## The three skills

| Skill | Say | What it does |
|---|---|---|
| `oman-health-check` | "Run Oman Health Check" | Scopes the system (customer type, AI, telehealth, insurance claims, national platforms), checks code, configuration and infrastructure for evidence, asks about what code can't show, and writes the checklist and Excel file |
| `oman-health-recheck` | "Recheck Oman compliance" | Re-checks after fixes, updates statuses on evidence, flags anything that went backwards, and re-exports the Excel file |
| `oman-health-explain` | "Can we use an AI API with Omani patient data?" | Explains any requirement in plain language, with its source and a design suggestion |

Asking in plain words works in every tool. You can also call a skill directly: type `/oman-health-check` in Cursor's Agent chat, or type `$` in Codex and choose the skill.

## What it covers (library dated 17 October 2026)

| Layer | Covers |
|---|---|
| Data protection (MTCIT) | The Personal Data Protection Law and its Executive Regulations, as amended by Royal Decree 68/2026 (in force 7 September 2026): the MTCIT permit for health data, explicit consent and its exceptions, patient rights and the 45-day deadline, erasure at the end of the purpose, objections to automated decisions, 72-hour breach notice, processors, the DPO, transfers abroad, and the government exemption with MTCIT's policy for government units |
| Data outside Oman (Cyber Defence Centre) | Approval before health data is stored or processed outside Oman. Remote access from abroad is an open question for private providers, and a transfer under the government policy for government units |
| Cybersecurity, cloud and AI | The Cyber Defence Centre System; the TRA regulation on cloud and data centres (health-sector content at the top security level, in Category 4 data centres, kept in Oman); MTCIT's rules for government systems (security baseline, database security, security assessments, mobile apps, continuity, cloud, integration, source code ownership, Omani staffing, managed services); the 2025 Electronic Transactions Law and national digital identity; the 2026 cybercrime law; and MTCIT's AI policy |
| Health sector (Ministry of Health) | Confidentiality and disclosure, consent, clinical documentation and record integrity, the National Policy for Health Information Governance (accounts, audit trails, break-glass, classification, encryption, incidents, vendors, cloud and hosting abroad, retention, patient requests), MOH approval of private facilities' information systems, the Shifa national record, e-referral, notifications, practitioner licensing, research and AI guidance |
| Telehealth | Licensing and platform approval, in-country hosting, consent and identity checks, documentation, remote prescribing, clinical safety, practitioners abroad, teleradiology |
| Health insurance (FSA and Dhamani) | All health insurance transactions through Dhamani, coding, data and downtime duties, prior approval and claims rules, eligibility checks, TPAs, revenue cycle management inside Oman, insurer digital channels |
| Medical devices and pharmacy (MOH Drug Safety Center) | Whether software is a medical device, registration (high-risk deadline 31 December 2026), change approval, incident reporting, labelling and e-IFU, prescriptions, controlled drugs, medicine promotion |

Every requirement cites its source and is marked **Confirmed (primary)**, **Confirmed (secondary)** or **Unconfirmed**, with an "as of" note. Unconfirmed items become questions in your checklist, never hard requirements. Omani instruments are authoritative in Arabic, and the library's English is a working translation.

## How it works

1. Open your project folder and say **"Run Oman Health Check"**.
2. Confirm the scope the agent drafts from your project.
3. The agent checks the system theme by theme: hosting and residency, offshore data flows, offshore access and development, identity and access, audit logging, data model and records, encryption, national platforms and insurance, development lifecycle, backup, AI, telehealth, patient-facing language, marketing, and prescribing.
4. Answer one round of questions about what code can't show, such as permits, approvals, contracts and team location.
5. You get `.oman-health-compliance/CHECKLIST.md`, plus an Excel checklist with Summary, Checklist, Questions, Watch items and Sources sheets.
6. Build the tasks, then say **"Recheck Oman compliance"**.

## Make it yours

Copy `compliance-house-rules.template.md` into your project as `compliance-house-rules.md` and edit it. You can set the approver, the Excel font, whether the register is committed to git, the library staleness warning, and your own internal requirements.

## Important limits

- **Engineering readiness, not certification.** The plugin shows which requirements have evidence in your system. It does not replace a regulator's assessment, an audit or legal advice.
- **Rules change.** The library is dated, and the agent warns you when it's out of date or a watch item has moved. Check the current official text before relying on a requirement.
- **Translations.** Most Omani texts exist only in Arabic. The library's English is a working translation that an Omani legal adviser should check before you rely on specific wording.
- **The check is only as good as the model running it.** The skills run on whichever model your tool uses. Each run records the agent and model, where the tool states them.
- **Instructions only.** It contains instructions for the agent and a requirements library. It has no MCP servers, hooks or scripts, and the plugin itself sends no data anywhere. The skills tell the agent to review files without connecting to live systems, and not to put project content into web searches.

## Privacy

See the [Privacy policy](PRIVACY.md). In short: ATeam collects nothing, and the plugin has no servers of its own. Your code is processed by the AI tool you run it in, under that tool's terms.

## Files in this repository

| File | Used by |
|---|---|
| `.claude-plugin/plugin.json`, `.claude-plugin/marketplace.json` | Claude Code and Claude's plugin directory. Codex also reads the marketplace file. |
| `.cursor-plugin/plugin.json` | Cursor |
| `plugin.json` | Codex and other agents that support the Agent Plugins format |
| `skills/` | All of them |

## Licence

MIT. See [LICENSE](LICENSE).
