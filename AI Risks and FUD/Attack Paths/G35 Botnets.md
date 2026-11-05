---
tags: [attack-path, ai-fud-whitepaper]
---
# G35 Botnets

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):**
- **Baseline:** Bot networks use AI to generate per-target content or code, or to decide bot actions. The result is spam, influence operations, hijacked compute and DDoS at scale.
- **Maximal:** A self-propagating botnet whose AI autonomously drives targeting and propagation.

**Path A (baseline):**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | The attacker controls a network of nodes or accounts. Routes: compromised servers; fake social accounts; an automation framework. | 🟢 | Oligo, ShadowRay 2.0, 18 Nov 2025 (URL under [[G25 Attack surface expansion\|G25]]): a "self-propagating worm" across Ray clusters. Anthropic, Apr 2025: "more than 100 social media bot accounts." |
| 2 | AI generates bot content or code, or decides bot actions. | 🟢 | Anthropic, Apr 2025: "Claude was used as an orchestrator deciding what actions social media bot accounts should take." SentinelLABS, 9 Apr 2025: "uses OpenAI to generate custom outreach messages." Oligo: "attackers leveraged LLM-generated payloads," inferred from code style. |
| 3 | The bots act at scale. | 🟢 | AkiraBot: "at least 80,000 websites." Oligo: XMRig mining and sockstress against production websites. |
| 4 | Harm results (spam, hijacked compute, DDoS). | 🟢 | Same sources. The Anthropic influence operation had "no content went viral." |

**Path B (maximal):**

| #   | Step                                                                            | Light | Evidence                                                                         |
| --- | ------------------------------------------------------------------------------- | ----- | -------------------------------------------------------------------------------- |
| 1   | The botnet is established.                                                      | 🟢    | Oligo 2025.                                                                      |
| 2   | AI inside the botnet autonomously chooses targets and adapts propagation or C2. | 🔴    | None found. In ShadowRay 2.0, AI's role is inferred authorship of payloads only. |
| 3   | Scaled autonomous impact.                                                       | 🔴    | None found.                                                                      |

**Weakest-link light:** Path A 🟢. Path B 🔴.

**In scope:** In. The compromised-node route (ShadowRay) requires a failure at step 1 (authorization), and CAPTCHA bypass in AkiraBot is an authentication failure; only these routes are analyzed. Outside scope: fake-account and contact-form spam routes with no authentication bypass.

**Gaps:**
- AI authorship of the ShadowRay 2.0 payloads is Oligo's stylistic inference.
- No GTIG report reviewed (Nov 2025, Feb 2026, May 2026) discusses AI botnets.
