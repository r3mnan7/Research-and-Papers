---
tags: [attack-path, ai-fud-whitepaper]
---
# G50 Workforce: skills shortage, job displacement

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):** Baseline: some displacement, concentrated among early-career workers in AI-exposed jobs. Maximal: mass unemployment. Sub-concern: a security skills shortage weakens defence.

**Path (baseline):**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | Firms adopt generative AI for tasks in exposed occupations | 🟢 | Brynjolfsson, Chandar, Chen, "Canaries in the Coal Mine?", Stanford SIEPR WP (Aug 2025), https://siepr.stanford.edu/publications/working-paper/canaries-coal-mine-six-facts-about-recent-employment-effects-artificial |
| 2 | AI substitutes for labour rather than complementing it | 🟢 | Same source (payroll data): early-career workers "in the most AI-exposed occupations have experienced a 13 percent relative decline in employment" |
| 3 | Affected workers lose employment | 🟢 | Same source, plus Intl AI Safety Report 2026 (3 Feb 2026), https://internationalaisafetyreport.org/publication/international-ai-safety-report-2026: "some signs of declining demand for early-career workers" |

**Path (maximal: mass unemployment):**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | AI can perform most economically valuable tasks | 🔴 | OpenAI, "GDPval," arXiv 2510.04374, Oct 2025: frontier models "approaching industry experts in deliverable quality" on tasks that are "precisely-specified and one-shot, not interactive" (🟡 precursor). METR, arXiv 2503.14499, Mar 2025: 50% time horizon "around 50 minutes," doubling about every 7 months. IASR 2026, Extended Summary for Policymakers, 3 Feb 2026, https://internationalaisafetyreport.org/publication/2026-report-extended-summary-policymakers: "agents still complement rather than replace humans in most complex professional roles." |
| 2 | Economy-wide substitution outpaces new job creation | 🔴 | IASR 2026: "Early evidence shows no effect on overall employment" |
| 3 | Mass unemployment | 🔴 | None found |

**Path (security skills shortage):**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | Demand for security staff exceeds supply | 🟢 | ISC2, "Employers Must Act…" (11 Sep 2024), https://www.isc2.org/Insights/2024/09/Employers-Must-Act-Cybersecurity-Workforce-Growth-Stalls-as-Skills-Gaps-Widen: gap of 4.8 million (+19% y/y), driven by "economic constraints" |
| 2 | AI creates new skill demand that teams lack | 🟢 | Same source: "over one third of respondents still cited AI as the biggest skills shortfall" (survey) |
| 3 | Understaffed teams fail to prevent compromises | 🟢 (correlational) | IBM, "Skills shortage directly tied to financial loss in data breaches," on the Cost of a Data Breach Report 2024, https://www.ibm.com/think/insights/skills-shortage-directly-tied-to-financial-loss-in-data-breaches: "more than half of breached organizations now face severe security staffing shortages," adding "USD 1.76 million" on average. ISC2, Sep 2024, https://www.isc2.org/Insights/2024/09/Employers-Must-Act-Cybersecurity-Workforce-Growth-Stalls-as-Skills-Gaps-Widen: 58% say a staff shortage puts them "at significant risk." Both are survey data; neither shows understaffing caused the breaches. |

**Weakest-link light:** Baseline 🟢; maximal 🔴; skills path 🟢 (correlational)

**In scope:** Out. The skills-shortage version ends in a breach of defended systems, but that breach is a staffing failure, not a failure in an AI system or an attack using AI; AI's part is labor demand. The displacement paths have no security failure.

**Gaps:** This research did not pull BLS series. The ISC2 source attributes the gap to budget limits, not to AI, so AI is not a necessary cause of the shortage. Only its AI-skills component involves AI.
