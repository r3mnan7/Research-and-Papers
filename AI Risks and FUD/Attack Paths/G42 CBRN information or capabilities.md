---
tags: [attack-path, ai-fud-whitepaper]
---
# G42 CBRN information or capabilities

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):** A mass-casualty chemical, biological, radiological or nuclear attack enabled by AI uplift. All sources frame the severity as catastrophic. They disagree on likelihood and uplift, not on severity, so this note has one path.

**Path:**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | AI gives meaningful uplift beyond existing resources (planning or knowledge) | 🟡 | RAND RRA2977-2, 25 Jan 2024, https://www.rand.org/pubs/research_reports/RRA2977-2.html: "no statistically significant difference in the viability of plans". OpenAI, 31 Jan 2024, https://openai.com/index/building-an-early-warning-system-for-llm-aided-biological-threat-creation/: "at most a mild uplift"; not statistically significant. Anthropic, 22 May 2025, https://anthropic.com/news/activating-asl3-protections: "clearly ruling out ASL-3 risks is not possible for Claude Opus 4". IASR 2026, arXiv 2602.21012, https://arxiv.org/abs/2602.21012: systems give "expert-level laboratory instructions"; companies added safeguards because testing "could not rule out" meaningful novice help. All are evaluations, not real-world events. |
| 2 | Actor gets the uplift-capable model past its CBRN-specific safeguards (shared step [[RQ2 Screening Log#Shared steps\|SS2]]). Alternatives: universal jailbreak of a guarded model, or theft of its weights | 🟡 | Anthropic's ASL-3 measures target "universal jailbreaks" and add bug bounty and threat-intel monitoring. This research found no primary source of a CBRN-specific bypass in the wild. Models without safeguards exist ([[RQ2 Screening Log#Shared steps\|SS3]], 🟢), but none has shown the step-1 uplift, so that route does not satisfy this step. |
| 3 | Actor acquires materials and equipment | 🔴 | No AI-assisted instance found. IASR 2026: "difficult to assess the degree to which material barriers continue to constrain actors". |
| 4 | Actor produces the agent or device | 🔴 | No AI-assisted instance or wet-lab demonstration found in the sources reviewed. |
| 5 | Delivery or release causes mass casualties | 🔴 | No AI-assisted instance found. |

**Weakest-link light:** 🔴

**In scope:** In. Step 2 is an authorization failure (getting past the deployer's CBRN safeguards) on the jailbreak route; only that route is analyzed. Outside scope: the no-safeguards route, which needs no security failure.

**Gaps:**
- Steps 3–5 have non-AI historical precedents. They are not counted because the step is AI-conditioned.
- The FBI said the Palm Springs bombing (May 2025) involved an "AI chat program", but that case was conventional explosives, not CBRN, and the source is secondary only.
- This research could not read the IASR 2026 CBRN section body (§2.1.4); the fetch truncated before it.
