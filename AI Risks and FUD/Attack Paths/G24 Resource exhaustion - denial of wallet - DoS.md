---
tags: [attack-path, ai-fud-whitepaper]
---
# G24 Resource exhaustion / denial of wallet / DoS

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):** Two harms.
- **Denial of wallet:** Uncontrolled inference runs up costs. Sysdig's worst-case estimate is "over $46,000 of LLM consumption costs per day for the victim."
- **Denial of service:** The AI service is unavailable to legitimate users. OWASP LLM10:2025 covers both: "exploit the cost-per-use model of cloud-based AI services."

**Path A (denial of wallet):**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | The attacker gains the ability to run inference billed to the victim. Routes: (a) stolen cloud or API keys; (b) an unauthenticated or unthrottled endpoint. | 🟢 | Sysdig, "LLMjacking: Stolen Cloud Credentials Used in New AI Attack," 6 May 2024, https://www.sysdig.com/blog/llmjacking-stolen-cloud-credentials-used-in-new-ai-attack. The credentials came from a host with a vulnerable Laravel version (CVE-2021-3129). |
| 2 | The victim has no effective spend or quota cap. | 🟢 | Same source. The attack targeted Claude on AWS Bedrock, and the attacker's credential checker covered 10 AI services. |
| 3 | The attacker consumes inference that the victim pays for. | 🟢 | Same source: Sysdig "recently observed a new attack that leveraged stolen cloud credentials." The $46k/day figure is Sysdig's worst-case estimate. |

**Path B (DoS):**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | The attacker sends abnormal-volume traffic or resource-heavy queries to an AI service. | 🟢 | OpenAI status page, incident "Periodic outages across ChatGPT and API," 8 Nov 2023, https://status.openai.com/incidents/21vl32gvx3hb: "abnormal traffic pattern reflective of a DDoS attack." |
| 2 | Capacity and rate limiting do not absorb it. | 🟢 | Same source. |
| 3 | Legitimate users lose service. | 🟢 | Same source: "periodic outages." |

**Weakest-link light:** 🟢 for both paths.

**In scope:** Yes. Necessary security failure at A1 (authentication/authorization) and B3 (availability/resilience).

**Gaps:** Path B has no AI-specific step: the OpenAI outage was a volumetric DDoS against an AI service. The AI-specific variants are 🟡 only: Shumailov et al., "Sponge Examples," IEEE EuroS&P 2021, https://arxiv.org/abs/2006.03463 ("increasing energy consumption by a factor of 10 to 200"); Kumar et al., "OverThink," arXiv 2502.02542 (reasoning tokens up 13–46x). Sourcegraph, "Security update," 30 Aug 2023, https://sourcegraph.com/blog/security-update-august-2023, is a second denial-of-wallet case (a leaked admin token used to "increase API rate limits"). The widely repeated "$47,000 agent loop" has no primary source. Sysdig's $46,000/day is a projection.