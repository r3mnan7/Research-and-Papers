---
tags: [attack-path, ai-fud-whitepaper]
---
# G32 AI used to evade detection

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):** AI-produced obfuscation, mutation or content variation makes attacks evade filters and detection, so they succeed undetected. NCSC, Jan 2024: AI "could evade detection by current security filters" if "trained on quality exploit data."

**Path:**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | The attacker uses AI to produce evasive artifacts. Routes: (a) obfuscated code; (b) LLM-generated decoy code; (c) unique text per message; (d) prompts aimed at LLM-based analysers; (e) just-in-time self-rewriting. | 🟢 | Microsoft, 24 Sep 2025 (URL under [[G28 AI-enhanced phishing - social engineering\|G28]]): the campaign "likely used AI-generated code to obfuscate its payload." GTIG, "GTIG AI Threat Tracker: Adversaries Leverage AI for Vulnerability Exploitation, Augmented Operations, and Initial Access," 11 May 2026, https://cloud.google.com/blog/topics/threat-intelligence/ai-vulnerability-exploitation-initial-access: CANFAIL and LONGSTREAM use LLM-generated decoy code meant to "appear benign." |
| 2 | The artifact is deployed against real targets. | 🟢 | GTIG, 11 May 2026: Russia-nexus actors targeting Ukrainian organisations. GTIG, 5 Nov 2025: FRUITSHELL's "hard-coded prompts meant to bypass detection or analysis by LLM-powered security systems," "Observed in operations." |
| 3 | Controls fail to detect it because of the AI-produced variation. | 🟢 (content-filter route only) | SentinelLABS, "AkiraBot," 9 Apr 2025, https://sentinelone.com/labs/akirabot-ai-powered-bot-bypasses-captchas-spams-websites-at-scale: OpenAI-generated unique messages made spam filtering harder. The bot spammed "at least 80,000 websites." For the malware vs. endpoint/network detection route, This research found no primary evidence of success in the wild. Microsoft "detected and blocked" its case, and PROMPTFLUX is experimental. Endpoint route is 🟡: Outflank (Kyle Avery), "Training Specialist Models: Automating Malware Development," Aug 2025 (Black Hat USA 2025), https://www.outflank.nl/blog/2025/08/07/training-specialist-models/: an RL-trained 7B model "completely evades MDE more than 8% of the time" in test VMs. Hu & Tan, MalGAN, arXiv 1702.05983 (2017). In the wild, AI-built malware with evasion intent exists (GTIG FRUITSHELL; Anthropic, Aug 2025, https://www.anthropic.com/news/detecting-countering-misuse-aug-2025) but no source shows it evading detection. |
| 4 | The attacker reaches the objective undetected. | 🟢 | AkiraBot, same source. |

**Weakest-link light:** 🟢 (driven by the AkiraBot content-filter route). The malware-evasion route is 🟡 at step 3.

**In scope:** Yes. Necessary security failure at step 3 (authentication, since CAPTCHA is human verification, in the spam route; detection failure leading to loss of system control in the malware route).

**Gaps:**
- No primary source quantifies how much detection outcomes worsen because of AI.
- The Outflank page carries no date; the URL path gives 7 Aug 2025.