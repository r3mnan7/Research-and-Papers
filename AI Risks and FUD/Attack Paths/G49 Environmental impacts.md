---
tags: [attack-path, ai-fud-whitepaper]
---
# G49 Environmental impacts

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):** Baseline: AI compute adds a material amount of electricity demand, water use and greenhouse-gas emissions. Maximal: AI-driven growth in data-centre demand (forecast to roughly double by 2030) materially worsens climate change and local water stress.

**Path (baseline):**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | AI models are trained and served at scale in data centres | 🟢 | Stanford HAI, *AI Index 2025* ch.1 (Apr 2025), https://hai-production.s3.amazonaws.com/files/hai_ai-index-report-2025_chapter1_final.pdf: Llama 3.1-405B training "estimated cost of $170 million" |
| 2 | Data centres draw a significant share of grid electricity | 🟢 | US DOE / LBNL bulletin, 20 Dec 2024, https://content.govdelivery.com/accounts/USEERE/bulletins/3c88056: "data centers consumed about 4.4% of total U.S. electricity in 2023." This research did not confirm the AI-specific share. |
| 3 | Cooling and power generation consume freshwater (alternative: fossil generation emits GHG) | 🟡 | Li, Yang, Islam, Ren, "Making AI Less 'Thirsty'", arXiv 2304.03271 v5 (26 Mar 2025; accepted by CACM), https://arxiv.org/abs/2304.03271: GPT-3 training "700,000 liters of clean freshwater." This is a model-based estimate, not a measurement, so it is rated 🟡 (borderline). Google, 2024 Environmental Report, Jul 2024, https://www.gstatic.com/gumdrop/sustainability/google-2024-environmental-report.pdf (p. 32): "a 13% year-over-year increase and a 48% increase compared to our 2019 target base year," "primarily due to increases in data center energy consumption and supply chain emissions." Microsoft, 15 May 2024, https://blogs.microsoft.com/on-the-issues/2024/05/15/microsoft-environmental-sustainability-report-2024/: emissions "up 29.1% from the 2020 baseline," mainly from datacenter construction. |
| 4 | The AI-attributable share produces measurable environmental harm (climate or local water stress) | 🔴 | No primary source found that measures harm attributable to AI rather than to resource use. Li et al.'s 2027 figure (4.2–6.6 billion m³ water withdrawal) is a pure forecast. |

**Path (maximal):** The same steps plus "AI demand doubles data-centre load by 2030". That step is a forecast (IEA *Energy and AI*, Apr 2025, "Data centre electricity consumption is set to more than double to around 945 TWh by 2030," with AI "the most important driver of this growth" (Executive summary, p. 14, https://www.iea.org/reports/energy-and-ai); DOE: "6.7 to 12% of total U.S. electricity by 2028"), so it is 🔴.

**Weakest-link light:** 🔴 (both paths)

**In scope:** No. No necessary step is a security-property failure.

**Gaps:** The International AI Safety Report 2026 says it dropped environmental impacts from its scope. A grid-reliability variant (AI load causing outages) would involve resilience, but This research did not research it.
