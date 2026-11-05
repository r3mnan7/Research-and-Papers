---
tags: [attack-path, ai-fud-whitepaper]
---
# G25 Attack surface expansion

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):** Adding AI components gives attackers new entry points into the organisation's systems and data. NCSC, May 2025: AI integration "almost certainly presents an increased attack surface for adversaries to exploit."

**Path:**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | The organisation deploys an AI component that is exposed or connected to data and credentials (for example Ray, Langflow, or a copilot). | 🟢 | Oligo, "ShadowRay 2.0," 18 Nov 2025, https://oligo.security/blog/shadowray-2-0-attackers-turn-ai-against-itself-in-global-campaign-that-hijacks-ai-into-self-propagating-botnet: "more than 230,000 Ray servers exposed to the internet." |
| 2 | The component has an exploitable flaw or insecure default. Routes: (a) a missing-auth API (Ray Jobs, CVE-2023-48022, disputed); (b) an RCE bug (Langflow CVE-2025-3248); (c) zero-click prompt injection (EchoLeak). | 🟢 | Oligo, "ShadowRay," 26 Mar 2024, https://www.oligo.security/blog/shadowray-attack-ai-workloads-actively-exploited-in-the-wild. The vendor says Ray "is not intended for use outside of a strictly controlled network environment." |
| 3 | An attacker exploits it. | 🟢 | Same source: "Thousands of publicly exposed Ray servers compromised." Langflow CVE-2025-3248 was added to CISA KEV in May 2025 [via secondary; CISA page not fetched]. |
| 4 | The attacker reaches data, credentials or compute beyond the AI component. | 🟢 | Oligo 2024: stolen OpenAI, Stripe, Slack, AWS/GCP/Azure credentials and Hugging Face tokens. GTIG, 12 Feb 2026 (URL under [[G28 AI-enhanced phishing - social engineering\|G28]]): "Vulnerable open-source AI tools are commonly exploited to steal AI API keys." |

**Weakest-link light:** 🟢

**In scope:** Yes. Necessary security failure at step 2 (authentication/authorization), step 3 (system control) and step 4 (confidentiality).

**Gaps:**
- EchoLeak (CVE-2025-32711) was not exploited: MSRC lists "Exploited: No" and "fully mitigated by Microsoft"; it is not in CISA KEV (NVD API). It is a 🟡 demonstration, so this concern's 🟢 rests on the Ray and Langflow routes.
- The CISA KEV entry for Langflow was confirmed only through secondary reporting.