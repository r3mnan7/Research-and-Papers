---
tags: [attack-path, ai-fud-whitepaper]
---
# G29 Deepfakes / impersonation

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):**
- **Baseline:** Voice-clone "relative in crisis" scams cause individual financial losses (FBI).
- **Maximal:** Real-time multi-person deepfake video calls cause multi-million-dollar corporate fraud (Arup, about US$25M). The same maximal path covers deepfake identity documents that defeat financial-institution identity verification (FinCEN).

**Path A (baseline):**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | The attacker clones a trusted person's voice with AI. | 🟢 | FBI PSA I-120324-PSA, 3 Dec 2024, https://www.ic3.gov/PSA/2024/PSA241203: criminals "impersonate a close relative in a crisis situation." |
| 2 | The victim accepts the impersonation. | 🟢 | Same source. Shared step SS11. |
| 3 | The victim sends money. | 🟢 | Same source: the calls request money. |

**Path B (maximal):**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | The attacker creates deepfake video or audio of executives. The alternative route is deepfake or altered identity documents. | 🟢 | WEF interview with Arup CIO Rob Greig, "'This happens more frequently than people realize'," 4 Feb 2025, https://www.weforum.org/stories/2025/02/deepfake-ai-cybercrime-arup. The employee was speaking to "deepfakes created by artificial intelligence." |
| 2 | The target accepts the synthetic identity. Routes: a live video call; KYC or identity verification. | 🟢 | Same. FinCEN Alert FIN-2024-Alert004, 13 Nov 2024, https://www.fincen.gov/sites/default/files/shared/FinCEN-Alert-DeepFakes-Alert508FINAL.pdf: "altering or creating fraudulent identity documents to circumvent identity verification." Shared step SS11. |
| 3 | A transfer or account is authorised without out-of-band verification. | 🟢 | WEF/Arup: the employee was "tricked into sending $25 million to criminals." |
| 4 | Funds are lost. | 🟢 | Same. Greig: Arup's systems were not compromised. |

**Weakest-link light:** 🟢 for both paths.

**In scope:** Yes. Necessary security failure at step 2 (authentication: a synthetic identity is accepted as genuine) in both paths.

**Gaps:**
- This research found no fetchable Hong Kong Police primary statement. The info.gov.hk page returned only a script, and the police details come via CNN/SCMP.
- The WEF piece is an interview with Arup's CIO, not an Arup-issued statement.
- Per Greig, no technical system failure occurred. The authentication failure was in a human or business process.
