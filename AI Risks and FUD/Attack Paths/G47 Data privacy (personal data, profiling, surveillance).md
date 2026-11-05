---
tags: [attack-path, ai-fud-whitepaper]
---
# G47 Data privacy (personal data, profiling, surveillance)

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):** Unlawful collection and processing of personal and biometric data, profiling, inaccurate outputs about people, and surveillance or misidentification.

**Path:**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | Personal data collected without a valid legal basis or notice (scraping or training) | 🟢 | Garante Provv. n.112, 30 Mar 2023, https://garanteprivacy.it/garante/doc.jsp?ID=9870832: temporary limitation on OpenAI. Grounds: no notice, no legal basis for training, possible inaccuracy, no age verification (GDPR Arts 5, 6, 8, 13, 25). |
| 2 | Data processed into biometric profiles or model parameters | 🟢 | Dutch DPA decision, 16 May 2024 (EDPB notice 3 Sep 2024), €30.5M, https://www.edpb.europa.eu/news/dutch-supervisory-authority-imposes-a-fine-on-clearview-because-of-illegal-data-collection-for_pl: "processes, without a legal basis to do so, personal data". |
| 3 | System is used to identify, track, or output information about individuals. Alternatives: surveillance and identification, or generated statements about people | 🟢 | Clearview's law-enforcement service (EDPB notice). Garante Provv. n.112 (Mar 2023): outputs may be inaccurate. |
| 4 | Harm to data subjects (loss of privacy or control, misidentification) | 🟢 | Regulator findings of violation (Garante, Dutch DPA). |

**Path B (leakage; the in-scope route):**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | An AI service holds personal data (accounts, conversations, payment details) | 🟢 | [\[246\]](../Sources.md#^s246): ChatGPT Plus subscribers' names, email and payment addresses, and partial card details were held by the service. |
| 2 | A flaw exposes the data to unauthorized parties (confidentiality) | 🟢 | [\[246\]](../Sources.md#^s246), an admission by the responsible party: a "bug in an open-source library" (the redis-py client) let some users see "another active ChatGPT Plus user's first and last name, email address, payment address," the card type, the last four digits, and the expiry date. "Full credit card numbers were not exposed at any time." |
| 3 | Harm to data subjects: loss of confidentiality | 🟢 | [\[246\]](../Sources.md#^s246): "1.2% of the ChatGPT Plus subscribers" active during a nine-hour window on Mar 20, 2023 were affected; OpenAI believes the number whose data was actually seen is "extremely low." |

The flaw was in a conventional component (a cache client), not in the model; the AI service is the place the data leaked from.

**Weakest-link light:** Path B (leakage, in scope) 🟢. The lawful-basis path above is 🟢 and outside scope.

**In scope:** In. Only Path B, leakage, requires a security failure (confidentiality). Outside scope: collection without a lawful basis, profiling (steps 1–2 of the first path), and generated statements about people; scraping public data isn't an access-control bypass.

**Gaps:**
- The Garante's Dec 2024 €15M fine on OpenAI was annulled in Mar 2026 on competence grounds, without a ruling on its findings (see [[G51 Regulatory - compliance|G51]]), and is not used.
- FTC v. Rite Aid is an allegation (see [[G37 Security-AI false positives - misclassification|G37]]) and is not used.
- UK ICO Clearview outcomes not checked.