---
tags: [attack-path, ai-fud-whitepaper]
---
# G55 Not AI-specific context items

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):** Rising cybercrime losses driven by expanding connectivity (IIoT), traffic growth and criminal activity.

**Path:**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | Motivated, capable adversaries operate at scale | 🟢 | FBI IC3, *2024 Internet Crime Report* (Apr 2025), https://ic3.gov/AnnualReport/Reports/2024_IC3Report.pdf: 859,532 complaints |
| 2 | Exploitable exposure exists. Alternatives: human susceptibility (phishing, BEC), software vulnerabilities, connected OT/IIoT exposure | 🟢 | Same: phishing was top by count (193,407); BEC losses ~$2.77B. OT/IIoT route: FBI/CISA/NSA/EPA/DOE/CNMF, AA26-097A, 7 Apr 2026 (updated 22 Jul 2026), https://www.ic3.gov/CSA/2026/260407.pdf: internet-facing PLCs exploited, "resulting in operational disruption and financial loss"; the update says changes "disabled critical shutdown and alarm logic" (https://www.ic3.gov/CSA/2026/260722.pdf). Bitsight, 4 Jun 2026, https://www.bitsight.com/blog/2026-global-state-of-ics-ot-exposure: ~180,000 exposed ICS/OT IPs per month in 2025. |
| 3 | Compromise or fraud succeeds | 🟢 | Same |
| 4 | Financial loss | 🟢 | Same: "a staggering $16.6 billion," +33% from 2023 |
| — | *(AI check, not a necessary step)* AI used to scale or automate attacks | 🟢 | Anthropic, "Disrupting the first reported AI-orchestrated cyber espionage campaign" (Nov 2025), https://www-cdn.anthropic.com/d7dd50dd1185f59be051b307150d877f2b82bd2c.pdf: AI did ~80–90% of tactical work against ~30 targets and "validated a handful of successful intrusions." The model "frequently overstated findings and occasionally fabricated data." IC3 lists an FBI PSA from 3 Dec 2024 on generative AI used in fraud. |

**AI check:** AI is **not** a necessary step. All four steps occur and are documented without AI. AI is an observed accelerator for some routes.

**Weakest-link light:** 🟢

**In scope:** Out. These items are not AI-specific by definition; the security failure at step 3 would happen without AI.

**Gaps:** IC3 does not break losses down by AI involvement.
