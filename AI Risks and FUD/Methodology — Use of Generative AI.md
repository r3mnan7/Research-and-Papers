---
tags: [methodology, ai-fud-whitepaper]
---
# Methodology — Use of Generative AI

Back to [[Addressing Fear, Uncertainty, and Doubt in the Security and Safety of Artificial Intelligence Models|main note]]

## Disclosure

Everything in this research folder was produced in part or in whole with the assistance of generative AI (Anthropic's Claude models, used through the Claude desktop app and Claude Code, September–November 2026). This research is a work in progress and the author's review is ongoing, so a note may contain claims the author has not yet reviewed or approved. Approval means agreement with the content as the author's own position, not an acknowledgment that it exists: where the author disagrees, the note is changed, and where the author cannot verify a claim, it is removed or logged for follow-up. The author is responsible for the whole.

Per-note `#claude-draft` tags were used during drafting to mark text written in the AI's voice and were removed after review; this note is the single disclosure that replaces them. A "Drafting and review" callout at the top of [[RQ3 Control Coverage]] and [[RQ3.1 Minimum Control Set]] points here.

## What the AI did

**Research and retrieval.** Searched for and fetched primary sources, extracted quotations, and compiled the master [[Sources]] list. The project rule was that a source must be fetched and read before being cited, and that a source whose text could not be found is removed rather than cited from memory. The Verification log in [[Sources]] records the later rechecks, including sources that could not be reopened and quotations that could not be matched automatically. Quotations in the attack-path and scenario notes came through automated extraction and carry a "verify before citing" note until checked; the checks done so far are in the Verification log at the end of [[Sources]].

**Drafting under a fixed method.** The attack-path notes (`Attack Paths/`), the catastrophe-pathway notes (`Catastrophe Pathways/`), the [[RQ2 Screening Log]], the control analyses in [[RQ3 Control Coverage]] and [[RQ3.1 Minimum Control Set]], and the step tables and tallies were drafted by the AI under methods the author fixed in advance: the relevance criterion and scope rules in the main note's Scope section, the classification rubric, the traffic-light evidence scale, the attack-path-step unit of analysis, and the one-shot rule for the minimum control set. Wording of the hypothesis, the rubric, the falsification criteria, and the status lines was drafted by the AI and revised by the author.

**Control catalogs.** The seven general-purpose frameworks tested in [[RQ3 Control Coverage|RQ3]] were pulled from their primary sources into `Control Catalogs/` by the AI (NIST's CPRT service for CSF 2.0 and SP 800-53; the ASVS repository; the CIS v8.1.2 guide; the CISA, NIST SP 800-161r1 and SP 800-63-4 publications). Each catalog's header records its extraction method and spot checks. Control citations in [[RQ3 Control Coverage|RQ3]] and [[RQ3.1 Minimum Control Set|RQ3.1]] link to the catalog text so that a cited identifier can be checked against the framework's own words. The CIS catalog stays in the author's private vault because of its license; readers can check CIS citations against the CIS document ([[CIS Note]]).

**Second rating and independent review.** AI was used as a second rater and as an independent reviewer, separately from the AI that drafted:

- *[[RQ2 Risk Classification|RQ2]] classification.* The author classified every row blind, without seeing the AI's classes ([[RQ2 Blind Classification Worksheet]]), then settled the final classes in discussion. Agreement between the author's first pass and the AI's original classes was 15 of 40 single-letter answers, κ = 0.12; the final classes match the AI's original classes on 44 of 47 rows. A separate AI agent, seeing only the rubric and a shuffled row list, also classified the rows blind: agreement with the final classes 40 of 47 (85%), Cohen's κ = 0.79 ([[RQ2 Risk Classification]], "AI second rater").
- *[[RQ3 Control Coverage|RQ3]] step verdicts.* The author's verdicts (rater 1, entered into the note with AI assistance) were compared with a separate AI agent that rated every attack-path step blind, seeing only the step and its light: agreement 79 of 102 cells (77.5%), κ = 0.65; 24 of 29 path verdicts (82.8%). The AI wrote rater 1's step tables for [[S02 Bio-chemical|S02]] and [[S04 Rogue AI|S04]], so those two scenarios are left out of the agreement figures. Procedure, contamination disclosures, and every disagreement with reasoning are in [[RQ3 Second Rating]].
- *[[RQ3 Control Coverage|RQ3]] verification.* An AI agent that had not seen the [[RQ3 Control Coverage|RQ3]] drafting reviewed the rebuilt note against [[RQ2 Risk Classification|RQ2]] and the Sources list and verified the cited control identifiers and quotations (Sources, Verification log, "Independent review").

**Bookkeeping.** Maintaining a working to-do list, not published (every assumption, judgment call, and open question the AI made or found is logged there as an item for the author), link and consistency checks across notes, and the arithmetic in the tallies (computed by script, not by the model).

## What the AI did not do

- Decide the hypothesis, the scope, the rubric classes, the final [[RQ2 Risk Classification|RQ2]] classes, the H1b wording, or what counts as evidence. Those are the author's decisions, recorded in the main note. During the [[RQ3 Control Coverage|RQ3]] rebuild the AI also made working judgment calls, which stand unless the author changes them.
- Supply facts from its own training. The project rule is that nothing is included without a citation to a source the AI or the author actually read.
- Replace a human reviewer where one was available: the [[RQ2 Risk Classification|RQ2]] blind classification and the [[RQ3 Control Coverage|RQ3]] rater-1 verdicts are the author's, except the [[S02 Bio-chemical|S02]] and [[S04 Rogue AI|S04]] tables described above.
- Settle a disagreement between raters. Rater disagreements are listed for the author, and the author's verdict stands unless the author changes it. One exception: the AI applied the Bounded versus within-limits convention on its own judgment, changing [[G10 Direct prompt injection - jailbreak|G10]] step 4, [[G16 Tool misuse - coerced tool use|G16]] step 1, and [[G24 Resource exhaustion - denial of wallet - DoS|G24]] step A2.

## Known limitations of the method

- The [[RQ3 Control Coverage|RQ3]] second rating is an AI rater against a human rater; the [[RQ2 Risk Classification|RQ2]] check had the same shape. Neither is a check against a second human, and both raters read the same notes.
- The [[RQ3 Control Coverage|RQ3]] second rater was not fully blind: it had read the To-Do note, which records two of rater 1's conventions, and one step table's third column is its controls column. Both are disclosed in [[RQ3 Second Rating]].
- The final [[RQ2 Risk Classification|RQ2]] classes sit close to the AI's original classes although the author's first pass did not, so the AI's classes may have influenced the settled result.
- Automated quotation extraction has been spot-checked and machine-matched, not exhaustively verified, and no full check has confirmed that each source supports each claim. The Verification log in [[Sources]] says what has and has not been checked.
- Residual-analysis claims of "no control in the catalog" rest on a search of the catalogs for these terms: intent, trigger, provenance, pedigree, output filtering, human review, fail-safe, known state, physical. In the rebuilt 261-entry SP 800-161r1 catalog, pedigree, output filtering, human review, fail-safe and known state have no hits; intent has one, trigger two (IR-4 and SA-8, neither about model intent or triggers), provenance nine, physical 24; a second searcher with their own terms would strengthen them.
