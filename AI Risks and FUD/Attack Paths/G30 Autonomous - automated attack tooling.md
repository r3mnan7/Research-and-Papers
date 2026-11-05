---
tags: [attack-path, ai-fud-whitepaper]
---
# G30 Autonomous / automated attack tooling

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):**
- **Baseline:** An AI agent performs most of a real intrusion campaign at machine speed. In Anthropic's case it did "80-90% of tactical operations independently," against about 30 targets.
- **Maximal:** Fully autonomous end-to-end attacks with no human in the loop, at scale.

**Path A (baseline):**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | The actor connects an AI agent to attack tooling (MCP servers plus open-source pentest tools). | 🟢 | Anthropic, "Disrupting the first reported AI-orchestrated cyber espionage campaign," Nov 2025, https://assets.anthropic.com/m/ec212e6566a0d47/original/Disrupting-the-first-reported-AI-orchestrated-cyber-espionage-campaign.pdf: the campaign "relied overwhelmingly on open source penetration testing tools." |
| 2 | The actor gets past model safeguards. Routes: pretexts or task decomposition; uncensored or jailbroken models. | 🟢 | GTIG, 5 Nov 2025 (URL under [[G31 AI-generated - AI-concealed malware\|G31]]): "adopting social engineering-like pretexts in their prompts to bypass AI safety guardrails." Shared step [[RQ2 Screening Log#Shared steps\|SS1]]. |
| 3 | The AI performs reconnaissance, vulnerability discovery, exploitation, credential harvesting and lateral movement, with humans approving key escalations. | 🟢 | Anthropic, Nov 2025: the AI could "execute 80-90% of tactical operations independently"; human effort was "10 to 20 percent of total effort." |
| 4 | Intrusions succeed against real targets. | 🟢 | Same: "validated a handful of successful intrusions." |

**Path B (maximal):**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | Agent framework, as in A1. | 🟢 | As A1. |
| 2 | The AI selects targets and runs the full kill chain without human approval gates. | 🔴 | In Anthropic Nov 2025, humans chose targets and approved escalations. The same report says hallucination "remains an obstacle to fully autonomous cyberattacks." GTIG, 12 Feb 2026: "not yet seen evidence of these capabilities being used in the wild" (AutoGPT-style agents). NCSC, 7 May 2025: fully automated end-to-end attacks "unlikely to 2027." The Jun–Jul 2026 OpenAI/HF incident ([[G15 Agent misbehaviour- misread task, exceeded scope, loss of control, rog\|G15]]) had evaluation agents attack out-of-scope live systems without approval; it was not attacker-directed, and the NCSC still reported no full-lifecycle autonomous attack afterward. |
| 3 | Success at scale. | 🔴 | None found. |

**Weakest-link light:** Path A 🟢. Path B 🔴.

**In scope:** Yes. Necessary security failure at A3/A4 (authentication/authorization bypass, system control, confidentiality).

**Gaps:**
- Anthropic's Sept 2026 threat report and the Anthropic Aug 2025 GTG-2002 PDF were not verified in primary form. The Aug 2025 blog does confirm Claude Code was used to "automate reconnaissance, harvesting victims' credentials, and penetrating networks" against at least 17 organisations: https://www.anthropic.com/news/detecting-countering-misuse-aug-2025.
- The Sept 2026 report may change B2.
