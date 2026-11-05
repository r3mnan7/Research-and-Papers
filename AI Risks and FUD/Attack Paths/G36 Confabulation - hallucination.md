---
tags: [attack-path, ai-fud-whitepaper]
---
# G36 Confabulation / hallucination

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):** Two severities appear in the sources, so there are two paths. Baseline: legal sanctions or financial loss after people act on fabricated AI output. Maximal: injury in high-stakes settings such as health. NIST AI 600-1 says "Risks from confabulations may arise when users believe false content."

**Path A (baseline):**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | The AI generates false information presented as fact | 🟢 | *Mata v. Avianca*, No. 22-cv-1461 (PKC), S.D.N.Y. sanctions opinion, 22 Jun 2023, https://law.justia.com/cases/federal/district-courts/new-york/nysdce/1:2022cv01461/575368/54. Counsel "submitted non-existent judicial opinions with fake quotes and citations created by the artificial intelligence tool ChatGPT." *Moffatt*, 2024 BCCRT 149: an Air Canada agent admitted the chatbot used "misleading words." |
| 2 | The user does not verify and trusts the output | 🟢 | Same sources. NIST AI 600-1 (Jul 2024), https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf, §2.2. Shared step SS10. |
| 3 | The user acts on it (files a brief, buys a ticket) | 🟢 | Mata opinion; Moffatt decision. |
| 4 | Harm: sanctions or financial loss | 🟢 | Mata: $5,000 penalty. Moffatt: $812.02 ordered. "Air Canada did not take reasonable care to ensure its chatbot was accurate." |

**Path B (maximal):** Steps 1–3 are as in Path A, then:

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 4 | Physical or health injury from acting on confabulated advice | 🟢 | Eichenberger, Thielke, Van Buskirk, "A Case of Bromism Influenced by Use of Artificial Intelligence," *Annals of Internal Medicine: Clinical Cases* 4(8), 5 Aug 2025, https://doi.org/10.7326/aimcc.2024.1260. For 3 months the patient "replaced sodium chloride with sodium bromide obtained from the internet after consultation with ChatGPT," leading to bromism, psychosis, a 3-week admission, and an involuntary psychiatric hold. The authors "do not have access to his ChatGPT conversation log," but when they asked ChatGPT 3.5 what chloride can be replaced with, "we also produced a response that included bromide," with no specific health warning. A clinical case report, not a legal allegation; the link rests on the patient's account plus the authors' own reproduction. |

**Weakest-link light:** Path A 🟢. Path B 🟢.

**In scope:** Out. No route requires a security failure: the harm comes from a model producing false information, with no attacker and no security control defeated. Accuracy of output is not part of integrity as information security defines it (guarding against improper modification or destruction).

**Gaps:** Lawsuits alleging injury from ChatGPT medical advice (e.g., Winters v. OpenAI, San Francisco Superior Court, filed Jul 2026) are allegations, not findings, and do not count toward the light. IASR 2026 (exec. summary, 3 Feb 2026, https://internationalaisafetyreport.org/publication/2026-report-executive-summary) confirms the failure mode: "fabricating information."