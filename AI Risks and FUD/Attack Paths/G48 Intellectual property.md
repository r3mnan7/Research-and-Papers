---
tags: [attack-path, ai-fud-whitepaper]
---
# G48 Intellectual property

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):** Unlicensed copying of copyrighted works for training, plus model reproduction of protected works, causing legal infringement and market harm to creators.

**Path:**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | Developer acquires copyrighted works, including from pirate sources | 🟢 | Bartz v. Anthropic, N.D. Cal. C 24-05417 WHA, Order on Fair Use, 23 Jun 2025, https://storage.courtlistener.com/recap/gov.uscourts.cand.434709/gov.uscourts.cand.434709.231.0.pdf: on pirated library copies, "Every factor points against fair use". |
| 2 | Works are copied into training or reference datasets | 🟢 | Same order: training was "exceedingly transformative", so fair use. Thomson Reuters v. Ross, D. Del. 1:20-cv-613, 11 Feb 2025, https://storage.courtlistener.com/recap/gov.uscourts.ded.72109/gov.uscourts.ded.72109.770.0.pdf: "I grant summary judgment for Thomson Reuters on fair use"; Ross's AI "is not generative AI". |
| 3 | Model memorizes or outputs substantially similar protected content | 🟢 | GEMA v. OpenAI, LG München I (42 O 14139/24), 11 Nov 2025, appealable, summarized by the EU IP Helpdesk: https://intellectual-property-helpdesk.ec.europa.eu/news-events/news/german-court-rules-favour-music-rights-management-organisation-against-openai-nyt-vs-openai-dispute-2025-11-14_en. Memorized lyrics held to be reproduction, and outputs a communication to the public. NYT v. OpenAI regurgitation claims are allegations, still pending (MDL 1:25-md-03143). |
| 4 | Legal infringement found or creators suffer market harm | 🟢 | Ross (Feb 2025) and GEMA (Nov 2025) found infringement. Bartz: the court granted final approval of the $1.5B settlement on 20 Jul 2026 (settlement site, https://www.anthropiccopyrightsettlement.com/); the 23 Jun 2025 order had held the pirated-library copying not fair use. Counterpoint: Getty v. Stability, [2025] EWHC 2863 (Ch), 4 Nov 2025, https://www.judiciary.uk/judgments/getty-images-v-stability-ai/: Getty dropped its training and output claims; "the model weights are not themselves an infringing copy" (para 600, via the European Audiovisual Observatory summary); limited trade mark infringement for watermarked images. |

**Weakest-link light:** 🟢

**In scope:** No. No necessary step is a security-property failure; acquiring from pirate sites isn't a failure of the AI system's own security. Training-data extraction by adversarial prompting could be framed as a confidentiality issue, but these are public works.

**Gaps:**
- Outcomes vary by jurisdiction and are under appeal.
- The NYT April 2025 motion-to-dismiss opinion was not retrieved; NYT's regurgitation claims are allegations.
- Getty paras 600+ were read via a summary, not the judgment text.