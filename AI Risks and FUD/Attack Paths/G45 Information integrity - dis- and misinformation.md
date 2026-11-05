---
tags: [attack-path, ai-fud-whitepaper]
---
# G45 Information integrity / dis- and misinformation

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):**
- **Baseline:** voters are deceived or discouraged in a specific election.
- **Maximal:** AI-scaled influence operations shift public opinion or election outcomes.

**Path (baseline, New Hampshire robocall):**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | Actor generates synthetic deceptive content (cloned voice) | 🟢 | FCC press release on the Notice of Apparent Liability (NAL) against Kramer, 23 May 2024, https://docs.fcc.gov/public/attachments/DOC-402762A1.pdf: deepfake robocalls using Biden's cloned voice before the New Hampshire primary. |
| 2 | Content is delivered at scale. Alternatives: robocalls with spoofed caller ID, or social media | 🟢 | FCC Forfeiture Order, *In re Steve Kramer*, FCC 24-104, adopted 26 Sep 2024, https://docs.fcc.gov/public/attachments/FCC-24-104A1_Rcd.pdf: $6,000,000 under the Truth in Caller ID Act (47 U.S.C. § 227(e)); 9,581 calls placed; the message "imitated U.S. President Joseph R. Biden, Jr.'s voice." |
| 3 | Recipients are exposed and believe it (shared step SS11) | 🟢 | Calls were placed (FCC). Shared step SS11: people acting on synthetic media they believed genuine is documented in fraud ([[G29 Deepfakes - impersonation\|G29]]). No primary measurement of how many New Hampshire recipients were deceived. |
| 4 | Turnout is suppressed or the vote affected | 🔴 | No primary measurement found. |

Regulatory response: the FCC's 2024 declaratory ruling says AI-generated voices are "artificial" under the Telephone Consumer Protection Act (same release).

**Path (maximal, influence operations):**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | State or commercial actors generate content with AI | 🟢 | OpenAI, 30 May 2024, https://openai.com/index/disrupting-deceptive-uses-of-AI-by-covert-influence-operations/: five covert operations disrupted. |
| 2 | Content is distributed through inauthentic accounts | 🟢 | Same source. |
| 3 | Content reaches and persuades authentic audiences at scale | 🟡 | IASR 2026: "In experimental settings, AI-generated content can be as effective as human-written content". Real world: "documented but not yet widespread". OpenAI: operations "do not appear to have meaningfully increased their audience engagement"; none scored above 2 on the Brookings Breakout Scale. |
| 4 | Opinion or election outcomes shift | 🔴 | No primary demonstration. Slovakia 2023 (audio purporting to be Šimečka, 28 Sep 2023) is documented only by secondary sources (CEDMO, 25 Nov 2024; SITA quoting Slovak police), with no outcome finding. |

**Weakest-link light:** Baseline 🔴 (step 4) · Maximal 🔴

**In scope:** In. Step 2 is an authentication failure on routes that need spoofed caller ID or fake accounts; only those routes are analyzed. Outside scope: synthetic content that deceives an audience with no security failure.

**Gaps:**
- No official Slovak police, prosecutor or EEAS source retrieved for Slovakia.
- Meta's adversarial threat reports were not retrieved.