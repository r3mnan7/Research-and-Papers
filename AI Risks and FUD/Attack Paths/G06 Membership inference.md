---
tags: [attack-path, ai-fud-whitepaper]
---
# G06 Membership inference

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):** Disclosure that a specific person's record was in a sensitive training set (for example hospital discharge data). This is a privacy breach.

**Path:**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | Model is trained on data where membership itself is sensitive | 🟢 (weak) | PIPC (Korea) 28 Apr 2021 decision on Scatter Lab, which used ~100M private KakaoTalk messages. Read via FPF, https://fpf.org/blog/south-korea-the-first-case-where-the-personal-information-protection-act-was-applied-to-an-ai-system/ ; the PIPC primary was not retrieved |
| 2 | Attacker gets query or output access | 🟢 | Ordinary API access. GTIG 12 Feb 2026 documents adversaries probing via "legitimate access" |
| 3 | Attacker runs membership inference and determines membership (AI's outputs leak it) | 🟡 | Shokri et al., arXiv 1610.05820, 2017: attacks on models "trained by commercial 'machine learning as a service' providers such as Google and Amazon," using "a hospital discharge dataset whose membership is sensitive" |

**Weakest-link light:** 🟡

**In scope:** Yes. Necessary security failure at step 3: confidentiality.

**Gaps:**
- No in-the-wild membership inference incident found.
- NIST AI 100-2e2025 p.16 notes that "many of the attacks discussed… were demonstrated only in research settings."
