---
tags: [catastrophe-pathway, ai-fud-whitepaper]
---
# S11 Elections: cyberattack on election infrastructure, and whether AI enables it

Back to [[RQ2 Screening Log]] · [[Catastrophe Pathways]]

> [!info] Method
> Map the attack path, then light each step by evidence: 🟢 happened in the real world · 🟡 shown only in a lab, court demonstration or evaluation · 🔴 never shown. The scenario is only as real as its weakest step. Allegations (indictments, unadjudicated claims, dismissed cases) are not established facts; court findings, guilty pleas, verdicts, official findings and admissions are. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):** Attackers, possibly using AI, compromise election infrastructure: they steal or change voter data, disrupt voting, or change results without detection.

**Weakest-link light:** 🔴 Speculative for the claimed harm. Intrusion into registration systems, insider access to voting equipment, and disruption of election-office IT have all happened (🟢). Altering votes in a real election has not been shown, and no source shows AI enabling any attack on election infrastructure.

**Necessary security failure (in scope?):** In. Every path runs through confidentiality, integrity, availability, authentication, authorization, or system control.

## Path A: intrusion into voter registration and results-reporting systems

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | Get into internet-facing election IT (voter registration databases, results-reporting sites) | 🟢 | Illinois voter registration database, 2016 (SQL injection) [\[212\]](../Sources.md#^s212). An Iranian actor "successfully obtained voter registration data in at least one state," 2020 [\[213\]](../Sources.md#^s213). CISA, 2026: "Hackers have attempted to breach voter registration systems in all 50 states, with confirmed success in at least 20 states" (p. 7) [\[214\]](../Sources.md#^s214). |
| 2 | Read or take voter data | 🟢 | Illinois: up to about 200,000 voter records accessed (SSCI pp. 22–24) [\[212\]](../Sources.md#^s212). Iran: data used in a propaganda video [\[213\]](../Sources.md#^s213). |
| 3 | Change voter records | 🔴 | SSCI: the Illinois intruders "were in a position to delete or change voter data, but the Committee is not aware of any evidence that they did so" [\[212\]](../Sources.md#^s212). |

## Path B: access to voting equipment and altering votes

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | Get access to voting equipment or its software | 🟢 (insider route) | Mesa County, Colorado, 2021: the Secretary of State found hard-drive images of election servers and BIOS passwords posted online; "The only method to make such copies is to physically access the machines" [\[215\]](../Sources.md#^s215). Former clerk Tina Peters was convicted on 7 counts (Aug 2024); the convictions were affirmed on appeal, and the sentence was reversed and remanded because it relied in part on protected speech (People v. Peters, 2026 COA 24, Apr 2, 2026) [\[216\]](../Sources.md#^s216). Coffee County, Georgia, 2021: the Secretary of State found former officials "allowed the unauthorized access" and replaced the county's equipment [\[217\]](../Sources.md#^s217); two defendants pleaded guilty (First Offender pleas, so not convictions) to misdemeanor conspiracy to interfere with election duties (Oct 2023) [\[218\]](../Sources.md#^s218). No external hack of vote-casting or counting equipment is documented. |
| 2 | Exploit a vulnerability in vote-casting equipment to change votes | 🟡 | CISA confirmed nine vulnerabilities in Dominion ImageCast X (CVE-2022-1739 to 1747) and has "no evidence that these vulnerabilities have been exploited in any elections"; exploitation "would require physical access" [\[219\]](../Sources.md#^s219). Halderman and Springall (expert report, unsealed 2023): "Attackers can alter the QR codes on printed ballots to modify voters' selections" (lab) [\[220\]](../Sources.md#^s220). The court found Halderman's testing showed "the practical feasibility through a cyber attack of causing the swapping or deletion of specific votes cast" (Curling v. Raffensperger, Oct 2020) [\[221\]](../Sources.md#^s221). MITRE's review (funded by Dominion) rated the six scenarios "Operationally Infeasible" under normal controls and did not test them itself [\[222\]](../Sources.md#^s222). DEF CON 27 Voting Village found issues in every device tested, mostly with physical access [\[223\]](../Sources.md#^s223). |
| 3 | The change survives voter checks, testing and audits | 🟡 | Voters rarely catch a ballot-marking device (BMD) error: in a mock election 7.8% noticed and 6.6% reported an altered race [\[224\]](../Sources.md#^s224). Audits check the paper, so "no audit can ensure that the votes on paper are the ones expressed by the voter on a touchscreen" [\[225\]](../Sources.md#^s225). Halderman showed malware evading logic-and-accuracy testing in the lab [\[220\]](../Sources.md#^s220). About 96% of registered voters vote on paper (69.5% hand-marked, 26.5% via BMDs; 2026, Verified Voting figures as reported by SciLine) [\[226\]](../Sources.md#^s226). |
| 4 | Votes are changed in a real election | 🔴 | 2016: SSCI "has seen no evidence that any votes were changed or that any voting machines were manipulated" [\[212\]](../Sources.md#^s212). 2020: "no evidence that any voting system deleted or lost votes, changed votes, or was in any way compromised" (EI-GCC/SCC) [\[227\]](../Sources.md#^s227); ODNI found "no indications that any foreign actor attempted to alter any technical aspect of the voting process" [\[228\]](../Sources.md#^s228). 2018–2022: CISA found "no evidence that malicious actors changed, altered, or deleted votes" [\[229\]](../Sources.md#^s229). 2024: "no evidence of any malicious activity that had a material impact" [\[230\]](../Sources.md#^s230). |

## Path C: disruption

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | Disrupt election-office IT or public election websites | 🟢 | Mississippi Secretary of State, 2022: DDoS made public sites "periodically inaccessible"; "Our election system was not compromised" [\[231\]](../Sources.md#^s231). Ransomware hit county IT in Fulton County, GA (2024): "a ransomware incident" by "financially motivated" actors, with "no evidence or reason to believe that this incident is related to the election process" [\[232\]](../Sources.md#^s232). Hall County, GA (2020) is known only through press quoting the county. |
| 2 | Voting or counting is disrupted | 🔴 | In every case found, officials reported no effect on vote counts [\[231\]](../Sources.md#^s231)[\[232\]](../Sources.md#^s232). |

## AI's contribution (applies to all paths)

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | AI materially enables the attack | 🔴 | No official source reports AI used in an intrusion into, or disruption of, election infrastructure. CISA: generative AI "will likely not introduce new risks, but they may amplify existing risks" [\[233\]](../Sources.md#^s233). ODNI, Sep 2024: AI has not "revolutionize[d]" foreign influence operations; the discussion covers influence content only [\[234\]](../Sources.md#^s234). FBI/CISA, Oct 2026, warn that AI lets attackers "create language that appears genuine" in phishing against election officials, but name no AI-enabled incident [\[235\]](../Sources.md#^s235). The one adjudicated AI election case, the 2024 New Hampshire deepfake robocalls, targeted voters, not systems (see [[G45 Information integrity - dis- and misinformation\|G45]]). |

## Also on record

- **Real counting errors, caught by audits.** Georgia's 2020 hand count confirmed the outcome but found counties that "failed to upload all memory cards" [\[236\]](../Sources.md#^s236). Antrim County, Michigan's wrong unofficial 2020 results came from "human error and lack of training," per the Michigan Senate Oversight Committee, which found no evidence of hacking [\[237\]](../Sources.md#^s237).
- **Known flaws left unpatched.** The EAC "certified fixes for the vulnerabilities identified in the report" [\[238\]](../Sources.md#^s238); a Georgia State Election Board resolution (Sep 2026) says Georgia "has not updated the software" [\[239\]](../Sources.md#^s239). CISA (2026): certification constraints "limit vendors' ability to release patches and prevent system owners from applying them quickly," and election infrastructure is often reachable from general office networks (p. 7) [\[214\]](../Sources.md#^s214).
- **How the court cases ended.** Curling v. Raffensperger was dismissed in Mar 2025 for lack of standing, without a ruling on the merits; the court noted "substantial concerns" about security [\[240\]](../Sources.md#^s240). The Fulton County charges against the remaining Coffee County defendants were dropped in Nov 2025 without any finding on the conduct (via press). Colorado's governor commuted Peters's sentence in May 2026 (via press).
- **Breaches went unnoticed for a time.** Mesa County surfaced months later, when passwords appeared online [\[215\]](../Sources.md#^s215); Coffee County became public through litigation. GBI interview summaries describe the Coffee County system image being "uploaded to a file share site on the internet" and shared with several named people; they do not establish wide public distribution [\[241\]](../Sources.md#^s241).
- UK National Risk Register 2026 adds threats to democracy, including interference [\[209\]](../Sources.md#^s209).

## Allegations (not counted toward any light)

- The Netyksho indictment (2018) on GRU intrusions into a state board of elections and a voting-software vendor, and the Kazemi indictment (2021) on Iranian access to state voter websites. Neither was tried.
- Michigan's 2023 charges over tabulators taken from clerks. Felony counts against two defendants were dismissed in Apr 2026; others are unresolved.
- Claims that the Mesa County images showed election fraud. No court or agency finding supports them.

## Not publicly knowable / not verified

- Read only via press or mirrors: the Peters appeal opinion (counselstack mirror), the Hall County statement, the Georgia SEB resolution's adoption, the Fulton County dismissal order (Nov 2025), and the 2026 Verified Voting figures.
- CISA's "at least 20 states" figure cites CISA's own products ("Recognizing and Addressing Threats to Statewide Voter Registration Databases" and "Vulnerabilities in Electronic Voting and Ballot-Counting Systems," 2026), which give no underlying list or data.
- The 2026 midterm (Nov 3) had not happened at the time of research.

## Sources

All sources are listed in [[Sources]]; citations here use its numbers.
