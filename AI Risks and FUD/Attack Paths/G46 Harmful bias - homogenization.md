---
tags: [attack-path, ai-fud-whitepaper]
---
# G46 Harmful bias / homogenization

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):** Unlawful discriminatory outcomes in consequential decisions (hiring, policing, retail security). The homogenization claim is systemic exclusion when many deciders use the same model.

**Path:**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | An automated or AI system is deployed in a consequential decision | 🟢 | Dutch Tax Administration childcare-benefits risk model. Autoriteit Persoonsgegevens (AP), report z2018-22445, 2020 (attachment to Kamerstuk 31066 nr. 683, 17 Jul 2020), https://zoek.officielebekendmakingen.nl/blg-945542.pdf: "Het risico-classificatiemodel is een zelflerend model" (the risk-classification model is self-learning). |
| 2 | System produces disparate outcomes or error rates by protected class. Alternatives: an explicit rule, or learned or measured differentials | 🟢 | Same AP report: three types of nationality processing were "onrechtmatig" (unlawful); two were "discriminerend en daarmee onbehoorlijk" (discriminatory and therefore improper). NIST IR 8280, Dec 2019 (lab, 🟡), https://nvlpubs.nist.gov/nistpubs/ir/2019/NIST.IR.8280.pdf: face-recognition "false positives rates often vary by factors of 10 to beyond 100 times." |
| 3 | Decision is applied without effective human correction | 🟢 | Parliamentary inquiry "Ongekend onrecht," Kamerstuk 35 510 nr. 2, 17 Dec 2020, https://zoek.officielebekendmakingen.nl/kst-35510-2.pdf: parents "ten onrechte gebrandmerkt als opzettelijke fraudeurs" (wrongly branded as deliberate fraudsters). Shared step SS10. |
| 4 | Harm to individuals (lost opportunity, wrongful arrest) | 🟢 | Same inquiry: parents put "in grote financiële problemen" (into serious financial trouble). AP fine €2.75M (Kamerstuk 31066 nr. 936, 7 Dec 2021, https://zoek.officielebekendmakingen.nl/kst-31066-936.pdf). |
| alt 2–4 | Homogenization: the same model used across deciders systematically excludes the same people | 🟡 | Bommasani et al., NeurIPS 2022, arXiv 2211.13972, https://export.arxiv.org/abs/2211.13972: "We test this hypothesis on algorithmic fairness benchmarks." This research found no real-world documentation. |

**Weakest-link light:** 🟢 (discrimination path) · 🟡 (homogenization variant)

**In scope:** Out. No route requires a security failure. Harm from inaccurate outputs involves no attacker and no defeated security control, and accuracy of output is not part of integrity as information security defines it. A model that accurately applies an unlawful criterion involves no security failure either.

**Gaps:**
- EEOC v. iTutorGroup (Sep 2023) is not used: it settled by consent decree (allegations), and the software was a programmed rule, not ML.
- FTC v. Rite Aid and Williams v. Detroit are allegations or settlements (see [[G37 Security-AI false positives - misclassification|G37]]).
- The discrimination path now overlaps [[G62 Ethical dilemmas in AI decision-making|G62]] (same case).