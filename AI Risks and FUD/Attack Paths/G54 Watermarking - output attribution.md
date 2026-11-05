---
tags: [attack-path, ai-fud-whitepaper]
---
# G54 Watermarking / output attribution

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):** Synthetic content cannot be reliably identified or traced to its source, which enables deception, fraud and election interference.

**Path:**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | Generative AI produces deceptive synthetic content | 🟢 | FCC press release on NAL FCC 24-59, 23 May 2024, https://docs.fcc.gov/public/attachments/DOC-402762A1.pdf: "President Biden's cloned voice telling prospective voters not to vote." |
| 2 | Provenance is absent, removed or forged. Alternatives: (a) never applied; (b) metadata stripped in sharing; (c) watermark removed (regeneration or paraphrase); (d) watermark spoofed | 🟢 (a, b) / 🟡 (c, d) | NIST AI 100-4, Nov 2024, https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-4.pdf: "Many internet platforms strip at least some metadata from uploaded files"; "most current watermarking schemes have been consistently found vulnerable to removal"; attackers may "forge, or 'spoof,' a watermark." Zhao et al., arXiv:2306.01953 (NeurIPS 2024): "pixel-level invisible watermarks are vulnerable to this regeneration attack." |
| 3 | The content is distributed and received without being identified as synthetic | 🟢 | FCC: calls went out on 21 Jan 2024, two days before the NH primary, and were identified only afterwards. The calls also spoofed caller ID ("maliciously spoofing the number of a prominent local political consultant"). |
| 4 | Harm: recipients deceived, or deception attempted (shared step SS11) | 🟢 | FCC: messages urged voters to "save your vote for the November election." $6M proposed forfeiture. Whether recipients were deceived is evidenced generally by SS11 ([[G29 Deepfakes - impersonation\|G29]]); turnout effects are not measured ([[G45 Information integrity - dis- and misinformation\|G45]] step 4). |

**Weakest-link light:** 🟢

**In scope:** Yes. A security failure is necessary at step 2: content provenance fails (authentication of origin, integrity of the provenance signal). Step 3 adds a caller-ID authentication failure in the FCC case.

**Gaps:** No primary source documents a real case where a watermark was present and then stripped or defeated; the 🟢 rests on the absent and stripped routes. The FCC release does not name the voice tool. The effect on turnout is undocumented. C2PA specifications were not fetched.
