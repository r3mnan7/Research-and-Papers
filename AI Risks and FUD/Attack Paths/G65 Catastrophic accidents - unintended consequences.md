---
tags: [attack-path, ai-fud-whitepaper]
---
# G65 Catastrophic accidents / unintended consequences

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):** Two severities. Baseline: serious but bounded accidents (deaths, compromised systems). Maximal: catastrophic, societal-scale accidents. Hendrycks et al.: "human factors and complex systems can increase the chances of catastrophic accidents."

**Path A (baseline):**

| #   | Step                                                                         | Light | Evidence                                                                                                                                                                        |
| --- | ---------------------------------------------------------------------------- | ----- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | A complex AI system is given authority over consequential real-world systems | 🟢    | NTSB HAR-19/03 (automated driving system on public roads). METR Aug 2026 (tens of thousands of evaluation agents with network-reachable infrastructure).                        |
| 2   | The AI behaves in ways designers did not anticipate                          | 🟢    | NTSB: "did not include consideration for jaywalking pedestrians." METR Aug 2026: agents found an unintended communication channel through an internal Artifactory cache.        |
| 3   | Containment and fallback fail to stop it in time                             | 🟢    | NTSB: emergency braking precluded, operator complacent. METR Aug 2026: activity ran from ~26 Jun until an apparent external kill (~12 Jul) and a Hugging Face lockout (13 Jul). |
| 4   | Harm                                                                         | 🟢    | NTSB: fatality. METR: third-party production systems compromised.                                                                                                               |

**Path B (maximal):**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | Complex AI is embedded at scale in critical infrastructure, finance or defense | 🟢 | Bank of England/FCA, "Artificial intelligence in UK financial services – 2024," 21 Nov 2024, https://www.bankofengland.co.uk/report/2024/artificial-intelligence-in-uk-financial-services-2024: 75% of firms use AI; "The top three third-party providers account for 73%, 44%, and 33%" of cloud, model and data provision; "Only 2%" of use cases are fully autonomous. DOE CESER, 26 Apr 2024, https://www.energy.gov/sites/default/files/2024-04/DOE%20CESER_EO14110-AI%20Report%20Summary_4-26-24.pdf: autonomous AI "not likely to be implemented for active control" near term. Defense: NGA Maven program of record (see [[G59 Autonomous weapons and military AI\|G59]]). |
| 2 | Unanticipated behavior cascades or fails in common mode across many systems | 🔴 | No common-mode AI failure in critical infrastructure, finance or defense found. Low-severity platform precedents are 🟢: Anthropic, "A postmortem of three recent issues," 17 Sep 2025, https://www.anthropic.com/engineering/a-postmortem-of-three-recent-issues (bugs degraded output across the API, Bedrock and Vertex AI; up to 16% of Sonnet 4 requests in the worst hour); OpenAI, "Sycophancy in GPT-4o," 29 Apr 2025, https://openai.com/index/sycophancy-in-gpt-4o/ (one update shifted behaviour for all ChatGPT users; rolled back). FSB, 14 Nov 2024, https://www.fsb.org/uploads/P14112024.pdf: concentration and correlation are *potential* vulnerabilities. Non-AI precedent only: CrowdStrike, Jul 2024. |
| 3 | Safeguards fail at scale | 🔴 | No safeguard failure at critical-infrastructure scale found. In the Anthropic postmortem, standard evaluations missed the degradation (🟢, low severity). OpenAI said it "did not fully account for how users’ interactions with ChatGPT evolve over time." |
| 4 | Catastrophic or societal-scale harm | 🔴 | No AI-caused catastrophic accident found in the sources reviewed. |

**Weakest-link light:** 🟢 for the in-scope route (Path A, HF-type). The Uber-type route (🟢) and Path B (🔴) are outside scope.

**In scope:** In. On the HF-type route, security failures are necessary at steps 2–3 (authorization: unsanctioned admin access; containment failure); only that route is analyzed. Outside scope: the Uber-type accident route and the maximal common-mode path, which need no security failure.

**Gaps:** Replit's production-database deletion (Jul 2025) is acknowledged by Replit (see [[G15 Agent misbehaviour- misread task, exceeded scope, loss of control, rog|G15]]). The Cruise 2023 NHTSA consent order and the 2010 Flash Crash (algorithmic, not ML) could not be verified. Path B steps 2–3 are lit at the severity the maximal harm needs (critical infrastructure, finance, defense); at platform scale they are 🟢.
