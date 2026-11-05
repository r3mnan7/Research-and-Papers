---
tags: [attack-path, ai-fud-whitepaper]
---
# G52 Reputational / financial loss

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):** Organisations suffer financial and reputational loss when deployed AI fails. The concern implies significant losses.

**Path:**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | The organisation deploys AI in a customer-facing or professional workflow | 🟢 | Below |
| 2 | AI produces a wrong or harmful output. Alternatives: (a) unprompted error or hallucination; (b) adversarial manipulation such as prompt injection, or data leakage | 🟢 (via a) | Moffatt v. Air Canada, 2024 BCCRT 149 (14 Feb 2024), https://decisions.civilresolutionbc.ca/crt/crtd/en/525448/1/document.do: chatbot said "Air Canada offers reduced bereavement fares." Route (b) was not researched. |
| 3 | The output is relied on without verification | 🟢 | Mata v. Avianca, No. 22-cv-1461 (S.D.N.Y. 22 Jun 2023), Doc 54, https://law.justia.com/cases/federal/district-courts/new-york/nysdce/1:2022cv01461/575368/54: "non-existent judicial opinions with fake quotes and citations created by the artificial intelligence tool ChatGPT" Shared step SS10. |
| 4 | Liability, sanction or reputational loss | 🟢 | Air Canada ordered to pay CA$812.02; it "did not take reasonable care to ensure its chatbot was accurate." Mata: $5,000 sanction. |

**Weakest-link light:** 🟢 for the in-scope route (b), with step 2 via [[G11 Indirect prompt injection - goal hijack|G11]] and [[G13 Sensitive information disclosure - privacy breach via AI system|G13]]. Route (a) is 🟢 and outside scope.

**In scope:** In. Only route (b), adversarial manipulation such as prompt injection, or data leakage, requires a security failure (integrity or confidentiality); step 2 takes its light from [[G11 Indirect prompt injection - goal hijack|G11]] and [[G13 Sensitive information disclosure - privacy breach via AI system|G13]]. Outside scope: route (a), an unprompted error.

**Gaps:** The documented losses are small. The largest algorithmic-failure loss found is Knight Capital (SEC Rel. 34-70694, 16 Oct 2013, https://www.sec.gov/litigation/admin/2013/34-70694.pdf: "lost over $460 million"). That was a non-AI deployment error, so it does not count here. This research did not verify primary evidence of large AI-specific losses (e.g., Zillow Offers).
