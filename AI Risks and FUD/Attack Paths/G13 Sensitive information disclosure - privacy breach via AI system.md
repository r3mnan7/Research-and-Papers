---
tags: [attack-path, ai-fud-whitepaper]
---
# G13 Sensitive information disclosure / privacy breach via AI system

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):** The sources claim two severities. Baseline (accidental): one user's chat titles and payment data are exposed to other users. Maximal (adversarial): an AI assistant with broad data access is induced to exfiltrate enterprise data or credentials [\[76\]](../Sources.md#^s76)[\[40\]](../Sources.md#^s40).

**Path (baseline, accidental cross-user leak):**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | The AI service stores users' conversations and account data. | 🟢 | OpenAI, "March 20 ChatGPT outage: Here's what happened," 24 Mar 2023, https://openai.com/index/march-20-chatgpt-outage/ |
| 2 | The AI system does what the concern says: a session or cache isolation defect returns one user's data to another. | 🟢 | Same source: the bug "allowed some users to see titles from another active user's chat history" (cause: a redis-py client bug) Second case: Asana, "MCP Maintenance," status page, 5–17 Jun 2025, https://status.asana.com/incidents/5b9hhtgs3mxs: "We identified a bug affecting our Model Context Protocol (MCP) server"; MCP disabled 5–17 Jun; "organizations affected were contacted directly." |
| 3 | Another user receives and sees the data. | 🟢 | Same source: possible "visibility of payment-related information of 1.2% of the ChatGPT Plus subscribers". OpenAI says the number actually seen was "extremely low" |

**Weakest-link light (baseline):** 🟢

**Path (maximal, induced exfiltration):**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | The AI system has access to sensitive data or credentials. | 🟢 | [\[40\]](../Sources.md#^s40): the evaluation sandbox "held" credentials |
| 2 | The attacker induces disclosure through prompt injection (see [[G11 Indirect prompt injection - goal hijack\|G11]]). | 🟢 (qualified) | [\[40\]](../Sources.md#^s40): "caused the sandbox to hand over the credentials it held". Controlled 🟡: [\[76\]](../Sources.md#^s76) "first weaponizable zero-click attack chain on an AI agent" |
| 3 | The model does what the concern says: it discloses the data over a channel the attacker can reach. | 🟢 (qualified) | [\[40\]](../Sources.md#^s40): LiteLLM "prompt injection to exfiltrate the production API keys" |
| 4 | The attacker uses or holds the data. | 🟢 | [\[40\]](../Sources.md#^s40): the actor switched to using the victims' keys |

**Weakest-link light (maximal):** 🟢 (qualified; same caveat as [[G11 Indirect prompt injection - goal hijack|G11]])

**In scope:** Yes. Baseline step 2 is a confidentiality failure (tenant/session isolation). Maximal steps 2–3 are confidentiality failures.

**Gaps:** In the March 2023 incident the fault was in a third-party library inside the AI service, not in the model. Asana's own status page does not describe the bug as cross-tenant; that wording ("could have potentially exposed certain information from your Asana domain to other Asana MCP users") is from Asana's customer notice, seen only as quoted in secondary coverage (The Register, 18 Jun 2025).

## Sources

Shared sources are listed in [[Sources]] and cited by its numbers. Other sources are cited inline.
