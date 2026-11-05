---
tags: [catastrophe-pathway, ai-fud-whitepaper]
---
# S02 Bio/chemical: AI enables a mass-casualty weapon

Back to [[RQ2 Screening Log]] · [[Catastrophe Pathways]]

> [!info] Method
> Map the attack path, then light each step by evidence: 🟢 happened in the real world · 🟡 shown only in a lab or evaluation · 🔴 never shown. The scenario is only as real as its weakest step. Quotes came through automated extraction; verify before citing.

**Weakest-link light:** 🔴 Speculative

**Necessary security failure (in scope?):** In. Defeating DNA-synthesis screening or model safeguards (including weight theft) is a security failure; only those routes are analyzed. Outside scope: open-weight models and non-cyber acquisition, which bypass those steps.

## Attack path

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | AI gives meaningful planning or knowledge uplift | 🟡 | Controlled human trials found no statistically significant uplift (RAND [\[137\]](../Sources.md#^s137); OpenAI: "at most a mild uplift," not significant [\[138\]](../Sources.md#^s138)). Benchmark: o3 outperforms 94% of expert virologists on Q&A [\[139\]](../Sources.md#^s139). Labs raised safeguards as a precaution without confirming the threshold [\[140\]](../Sources.md#^s140)[\[141\]](../Sources.md#^s141). No post-2024 controlled uplift trial is public. |
| 2 | Get the capability past model safeguards (jailbreak or weight theft) (shared step [[RQ2 Screening Log#Shared steps\|SS2]]) | 🟡 | Classifiers: no universal jailbreak found in ~198,000 attempts, but "no AI systems currently on the market have perfectly robust defenses" [\[142\]](../Sources.md#^s142). Weight theft by top state actors: RAND says "Achieving SL5 is currently not possible" [\[143\]](../Sources.md#^s143); no frontier-weight theft documented. Open models stripped of safeguards exist ([[RQ2 Screening Log#Shared steps\|SS3]]), but have not shown the uplift in step 1. |
| 3 | Overcome tacit knowledge and wet-lab skill | 🔴 | OpenAI: "information access alone is insufficient"; its evaluation "does not test for success in the physical construction" [\[138\]](../Sources.md#^s138). |
| 4 | Acquire materials and evade synthesis screening and export controls | 🟡 | AI-designed protein variants evaded screening software in a 2025 study; patched before publication (Science, Oct 2025; quotes not retrieved) [\[144\]](../Sources.md#^s144). International AI Safety Report: hard to assess how far material barriers still constrain actors [\[109\]](../Sources.md#^s109). |
| 5 | Scale up and deliver at mass-casualty scale | 🔴 | No AI evaluation addresses production scale or delivery. |

## Also on record

- Real-world misuse: Anthropic's Sept 2026 report covers biological misuse cases; press reports no weapon, agent, or casualty resulted (details secondary) [\[40\]](../Sources.md#^s40). No government enforcement action found.

## Not publicly knowable / not verified

- Lab-internal uplift trial numbers (e.g., Claude Opus 4 system card §7.2.4.1) not retrieved.
- No literature on cyber intrusion into DNA-synthesis screening systems; the documented weakness is algorithmic evasion.
- Classifier robustness figures are vendor self-reported.

## Sources

All sources are listed in [[Sources]]; citations here use its numbers.
