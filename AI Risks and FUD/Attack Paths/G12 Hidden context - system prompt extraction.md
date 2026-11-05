---
tags: [attack-path, ai-fud-whitepaper]
---
# G12 Hidden context / system prompt extraction

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):** Baseline: proprietary instructions or guardrail logic are exposed, which helps further attacks. Maximal: secrets placed in the prompt (credentials, internal data) are exposed and used for unauthorized access. NIST classifies prompt extraction as a privacy compromise [\[22\]](../Sources.md#^s22).

**Path:**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | The deployer puts confidential material in the system prompt or hidden context. Baseline: instructions. Maximal: credentials or data. | 🟢 | Radware (Babo, Nakibly), "The New .env: Measuring Credential Leakage in AI Agent Instruction Files," 5 Aug 2026, https://www.radware.com/blog/posts/the-new-code-env-code-measuring-credential-leakage/: ~100K agent-instruction files scanned, ~100 confirmed live external secrets; "a majority of the testable keys still grant access today." These files leaked through public repos, not through the model. Shen et al., arXiv 2506.00197 (May 2025): leaked GPT knowledge files include "internal materials from a listed company." |
| 2 | The attacker sends an extraction prompt, directly or through indirect injection. | 🟡 | [\[38\]](../Sources.md#^s38) lists "system prompt leakage" as an intent seen in the wild, but per my read describes no case. [\[22\]](../Sources.md#^s22) NISTAML.035. A specific controlled demonstration was not fetched |
| 3 | The model does what the concern says: it reveals the hidden context. | 🟡 | Zhang, Carlini, Ippolito, arXiv 2307.06865 (Jul 2023), 11 LLMs. Yu et al., arXiv 2311.11538 (Nov 2023): system prompts and uploaded files extracted from 200+ custom GPTs. Shen et al., arXiv 2506.00197: knowledge files downloadable through Code Interpreter at 95.95% success. The Bing "Sydney" prompt (Feb 2023) was user-extracted from a live product (🟡 under rule 3); Microsoft acknowledgement exists only as a spokesperson quote in the press. No malicious real-world extraction found. |
| 4 | The attacker uses the disclosed material: credentials for access, or guardrail knowledge to refine attacks. | 🔴 | No primary case of an attacker using credentials or guardrail knowledge taken from an extracted system prompt. Radware tested its keys read-only as researchers, and its exposure was not via the model. |

**Weakest-link light:** 🔴 (step 4)

**In scope:** Yes. Step 3 is a confidentiality failure. Step 4 on the maximal path is an authentication failure.

**Gaps:** Step 1 is evidenced by exposure through repositories, not by the model. A malicious extraction followed by use (step 4) is the missing link.

## Sources

Shared sources are listed in [[Sources]] and cited by its numbers. Other sources are cited inline.
