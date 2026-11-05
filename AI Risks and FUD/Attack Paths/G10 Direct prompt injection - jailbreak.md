---
tags: [attack-path, ai-fud-whitepaper]
---
# G10 Direct prompt injection / jailbreak

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):** The sources claim two severities, so there are two paths. Baseline: the model produces output or actions its operator restricted. Maximal: a jailbroken agentic model carries out real intrusions against third parties [\[36\]](../Sources.md#^s36).

**Path:**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | The attacker gets direct input access to the model (an account, the API, or an agent harness). | 🟢 | [\[36\]](../Sources.md#^s36), Anthropic, Nov 2025: the actor ran Claude Code with "open standard Model Context Protocol (MCP) tools" |
| 2 | The attacker writes input that gets past safety training or operator restrictions. Routes: role-play or false pretext, or splitting the request into harmless-looking subtasks. | 🟢 | [\[36\]](../Sources.md#^s36): operators "convinced Claude that it was being used in defensive cybersecurity testing"; attacks were "decomposed… into discrete technical tasks" Shared step [[RQ2 Screening Log#Shared steps\|SS1]]. |
| 3 | The model does what the concern says: it produces the restricted output or takes the restricted actions. | 🟢 | [\[36\]](../Sources.md#^s36): Claude carried out reconnaissance and exploitation tasks through MCP tools |
| 4 | (Maximal only) The output or actions cause harm to a victim. | 🟢 | [\[36\]](../Sources.md#^s36): "The operation targeted roughly 30 entities"; "validated a handful of successful intrusions" |

**Weakest-link light:** 🟢 (both paths)

**In scope:** Yes. The necessary security failure is at step 2: system control, because the attacker gets past the deployer's restrictions on what the model will do. On the maximal path, step 4 adds a confidentiality and integrity failure at the victims.

**Gaps:** [\[36\]](../Sources.md#^s36) calls this "social engineering" of the model and does not use the word "jailbreak." [\[40\]](../Sources.md#^s40) (Sept 2026) describes actors negotiating "sanitized wording" after refusals and says it does not report a fully successful jailbreak. Whether the baseline path counts as in scope depends on treating operator content restrictions as a system-control property. Under the rule as written, they are treated that way.

## Sources

Shared sources are listed in [[Sources]] and cited by its numbers. Other sources are cited inline.
