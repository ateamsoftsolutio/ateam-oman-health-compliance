# Privacy policy: Oman Healthcare Compliance by ATeam

Effective date: 17 October 2026

This policy covers the "Oman Healthcare Compliance by ATeam" plugin (`ateam-oman-health-compliance`), published by ATeam Soft Solutions.

## What the plugin is

The plugin contains only written instructions for AI agents (skills) and a requirements library. It's built for Claude, Cursor and OpenAI Codex, and may load in other tools that support the same format. It has no MCP servers, hooks, scripts or other code that runs on its own. ATeam doesn't run any server or service for it.

## Data ATeam collects

None. No analytics, telemetry or accounts. ATeam receives nothing from your use of the plugin.

## Data the skills handle in your AI tool

The agent reads the code, configuration, infrastructure files and documents of the project you choose to check. These can contain personal or health data, for example in test fixtures, and secrets. The agent:

- writes the checklist, run summaries and Excel exports to the `.oman-health-compliance/` folder in your project
- is instructed never to display secret values, and to record only where a secret was found
- processes this content under the terms of the AI tool and model provider you use (for example Anthropic, Cursor or OpenAI) and your account settings. ATeam has no access to it.

## Outside services

The plugin doesn't send data to any outside service. If you ask the agent to check a regulator's current website, it may read public web pages through your AI tool. The skills tell the agent not to include project content in web searches.

## Retention

ATeam keeps nothing. The checklist and exports stay in your project until you delete them.

## Children

Not intended for anyone under 18.

## Changes and contact

Changes will be published in this file, with a new effective date. Contact: ATeam Soft Solutions, director@ateamsoftsolutions.com, https://www.ateamsoftsolutions.com
