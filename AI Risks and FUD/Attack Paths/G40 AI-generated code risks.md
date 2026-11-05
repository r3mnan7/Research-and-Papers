---
tags: [attack-path, ai-fud-whitepaper]
---
# G40 AI-generated code risks

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):** Software or data compromise when AI-generated code introduces exploitable flaws or pulls in attacker-controlled "hallucinated" packages. The secondary claim is a feedback loop in which insecure AI code degrades future models' training data (CSET).

**Path A (compromise):**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | Developer or non-developer builds software with an AI code generator | 🟢 | CVE-2025-48757, CVE Program record, published 2025-05-30, https://raw.githubusercontent.com/CVEProject/cvelistV5/main/cves/2025/48xxx/CVE-2025-48757.json. The record concerns Lovable-"generated sites". |
| 2 | AI emits a flaw. Alternatives: (a) insecure code or config; (b) a reference to a non-existent package | 🟢 (a); 🟡 (b) | (a) Same CVE: "insufficient database Row-Level Security policy" in generated sites; the vendor disputes it, saying customers are responsible. (b) Spracklen et al., "We Have a Package for You!", arXiv 2406.10279 (USENIX Security 2025), https://arxiv.org/abs/2406.10279v3: hallucinated packages "at least 5.2% for commercial models and 21.7% for open-source"; "205,474 unique" names. CSET, Nov 2024, https://cset.georgetown.edu/publication/cybersecurity-risks-of-ai-generated-code/: "almost half of the code snippets… contain bugs" (lab evaluation). |
| 3 | Flaw ships to production, or the hallucinated name is registered by an attacker and installed | 🟢 (a); 🟡 (b) | (a) The CVE covers deployed generated sites: Matt Palmer, "Statement on CVE-2025-48757," 29 May 2025, https://mattpalmer.io/posts/statement-on-CVE-2025-48757/: 170 of 1,645 analysed apps (10.3%) had inadequate row-level security, exposing 303 endpoints. (b) Bar Lanyado (Lasso Security), "Diving Deeper into AI Package Hallucinations," 28 Mar 2024, https://lasso.security/blog/ai-package-hallucinations: a researcher registered a hallucinated name with an empty package; "In three months the fake and empty package got more than 30k authentic downloads!" No malicious registration found. |
| 4 | Attacker finds and exploits the flaw | 🟡 | The CVE says it lets "remote unauthenticated attackers to read or write arbitrary database tables". This comes from a researcher disclosure; This research found no primary source documenting malicious exploitation. |
| 5 | Confidentiality or integrity loss for the app's users | 🔴 | No primary source documents a confirmed breach caused by AI-generated code. Palmer's own tests were proof of concept; he points to a third party's tweet as "active exploitation." Lovable disputes the CVE. |

**Path B (feedback loop):**
1. Insecure AI code is published: 🟢 (as in Path A).
2. That code is ingested into future training data: 🔴.
3. Later models produce measurably more insecure code because of it: 🔴.

The only source is CSET, which names "downstream cybersecurity impacts" such as feedback loops as a risk category. It shows no demonstration.

**Weakest-link light:** 🔴 for both paths.

**In scope:** Yes. Necessary security failures at steps 2 and 4: authorization (missing row-level access control) and integrity/confidentiality (arbitrary read/write). On the slopsquatting route, step 3 is a supply-chain integrity failure.

**Gaps:**
- No primary source documents a malicious slopsquatting package or an exploited AI-generated vulnerability.
- No Lovable statement retrieved; NVD's page did not render.
- This research did not search the IASR 2026 for coding material.