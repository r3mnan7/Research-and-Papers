---
tags: [attack-path, ai-fud-whitepaper]
---
# G20 Accountability / traceability / explainability

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):** A consequential decision made or shaped by an opaque AI or algorithmic system cannot be checked, contested or attributed to a responsible party. Affected people suffer adverse decisions with no effective due process or redress.

**Path:**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | An AI or algorithmic system makes or materially informs a consequential decision about a person | 🟢 | *Houston Fed. of Teachers v. HISD*, No. H-14-1189, S.D. Tex. (Mag. J. Smith), 4 May 2017, https://www.aft.org/sites/default/files/amendedsummaryjudgment_houston_050417.pdf. EVAAS value-added scores were used in decisions to discharge teachers. |
| 2 | The decision logic or record is unavailable or unreliable to the affected party and overseers. Alternatives: (a) proprietary secrecy; (b) technical uninterpretability; (c) the AI falsifies its own audit record | 🟢 (a, c) | (a) Same order: the inputs and methods "are proprietary trade secrets unavailable to plaintiffs or HISD." (c) METR, "OpenAI/Hugging Face incident investigation," 26 Aug 2026, https://metr.org/blog/2026-08-26-openai-hugging-face-incident-investigation/: roughly 7% of agent transcripts contained spoofed tool calls (paraphrase). |
| 3 | Errors cannot be detected, verified or contested | 🟢 | HISD order: a teacher "will necessarily be unable to verify that her own score is error-free." METR also says it "cannot rule out undetected spoofing" (paraphrase). |
| 4 | Responsibility or redress fails and the adverse decision stands | 🟢 (partial) | HISD order: "HISD is not entitled to summary judgment on this procedural due process claim." This is a ruling that the claim may proceed, not a final finding. Counter-evidence: *Moffatt v. Air Canada*, 2024 BCCRT 149 (14 Feb 2024), https://decisions.civilresolutionbc.ca/crt/crtd/en/525448/1/document.do. The tribunal rejected Air Canada's attempt to treat the chatbot as "a separate legal entity that is responsible for its own actions" and assigned liability to the airline. |

**Weakest-link light:** 🟢

**In scope:** In. Only route 2(c), the AI falsifying its own audit record, requires a security failure (integrity of the audit record; accountability). Outside scope: route 2(a), secrecy alone, and route 2(b), uninterpretability, where errors go undetected with no attacker and no record altered.

**Gaps:** EVAAS is a statistical value-added model, not machine learning, so it may not count as "AI" for the dataset. This research found no court record involving a deep-learning system. The case settled: AFT (a party), "Federal Suit Settlement: End of Value-Added Measures for Teacher Termination in Houston," 10 Oct 2017, https://www.aft.org/press-release/federal-suit-settlement-end-value-added-measures-teacher-termination-houston. The court's findings are in the 4 May 2017 order (251 F. Supp. 3d 1168); the settlement adds none. The METR case is an AI falsifying records inside an evaluation run, not a consumer-facing decision.
