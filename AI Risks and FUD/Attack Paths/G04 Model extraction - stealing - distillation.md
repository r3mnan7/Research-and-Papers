---
tags: [attack-path, ai-fud-whitepaper]
---
# G04 Model extraction / stealing / distillation

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):** Baseline: an attacker copies a production model's functionality or parameters by querying it, causing IP and competitive loss. Maximal (Anthropic): distilled models "lack necessary safeguards, creating significant national security risks," with dangerous capabilities spreading and "many protections stripped out entirely."

**Path (baseline):**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | Attacker gets query access. Routes: legitimate accounts, or fraudulent accounts and proxies | 🟢 | Anthropic, "Detecting and preventing distillation attacks", 23 Feb 2026, https://www.anthropic.com/news/detecting-and-preventing-distillation-attacks : ~24,000 fraudulent accounts, >16M exchanges (DeepSeek, Moonshot, MiniMax) |
| 2 | Systematic high-volume querying aimed at target capabilities | 🟢 | Same source. Google GTIG, "GTIG AI Threat Tracker: Distillation, Experimentation…", 12 Feb 2026, https://cloud.google.com/blog/topics/threat-intelligence/distillation-experimentation-integration-ai-adversarial-use : "observed and mitigated frequent model extraction attacks"; one campaign used >100,000 prompts |
| 3 | Outputs are used to train a surrogate, or parameters are recovered (AI's outputs reproduce its function) | 🟡 | Parameter recovery is 🟡: Tramèr et al., arXiv 1609.02943, 2016: "near-perfect fidelity" against BigML and Amazon ML; Carlini et al., arXiv 2403.06634, 2024: "extracts the entire projection matrix of OpenAI's Ada and Babbage" for under $20. Surrogate training in the wild rests on allegations only (🔴): Anthropic says named labs ran campaigns to "illicitly extract Claude's capabilities to improve their own models." |
| 4 | Copied capability is used or released by the attacker (IP loss) | 🔴 (allegation only) | Anthropic, same source: an accusation against named labs, not an established fact. |

**Path (maximal):** Steps 1–3 as above, then:

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 4 | Distilled model lacks safeguards | 🔴 | Anthropic states this as a likely result; no demonstration found |
| 5 | It is used for offensive cyber or other national-security harm | 🔴 | Anthropic: could enable "authoritarian governments to deploy frontier AI for offensive cyber operations" (a projection, not documented). GTIG: "we did not observe any direct attacks on frontier models from tracked APT or information operations (IO) actors" |

**Weakest-link light:** Baseline 🔴 (step 4 rests on allegation). Maximal 🔴.

**In scope:** In. Only the routes below, which require a security failure, are analyzed. Outside scope: behavioural distillation through permitted outputs.
- Step 1 is an authentication/authorization failure only on the fraudulent-account or proxy route. GTIG defines extraction as using "legitimate access."
- Step 3 is a confidentiality failure only on the exact-parameter route (Tramèr, Carlini). Behavioural distillation through permitted outputs needs no security failure.

**Gaps:** Rule applied: a victim's record counts when it produces evidence; words without proof are allegations. Anthropic describes its evidence for the fraudulent querying (IP correlation, request metadata, infrastructure indicators, coordinated payment and timing) but does not publish the indicators, and it offers no evidence that the labs trained models on the output (no comparison of model behaviour); that part is inference. So steps 1–2 stand and steps 3–4 are treated as allegations.
