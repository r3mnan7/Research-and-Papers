---
tags: [attack-path, ai-fud-whitepaper]
---
# G07 Training-data reconstruction / extraction / memorization

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):** Recovery of private training data (PII, verbatim text, images) from model outputs or from shared gradients.

**Path:**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | Model memorizes sensitive training data | 🟡 | Carlini et al., arXiv 2012.07805 (USENIX Sec 2021): "extract hundreds of verbatim text sequences" from GPT-2, including names, phone numbers and emails |
| 2 | Attacker gets access. Routes: query access to the model; or gradient access (federated learning server or eavesdropper) | 🟢 (query) / 🟡 (gradients) | GTIG Feb 2026 (legitimate access). Zhu et al., arXiv 1906.08935, 2019 (gradient setting) |
| 3 | Attacker extracts or reconstructs the data (AI emits it) | 🟡 | Nasr et al., arXiv 2311.17035, 2023: "extract gigabytes of training data" including from ChatGPT; "150x higher" emission rate (researcher demo on a production product). Zhu et al.: "pixel-wise accurate for images and token-wise matching for texts" |

**Weakest-link light:** 🟡

**In scope:** Yes. Necessary security failure at step 3: confidentiality.

**Gaps:**
- No in-the-wild malicious extraction found.
- Lee Luda (PIPC 2021) is a near-miss and does not qualify. The chatbot was retrieval-based (it picked real messages from a response database), and the PII exposure there came from published model files on GitHub, not from extraction of memorized data.
