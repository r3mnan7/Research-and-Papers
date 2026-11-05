---
tags: [attack-path, ai-fud-whitepaper]
---
# G16 Tool misuse / coerced tool use

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):** An agent's legitimate tools are turned to the attacker's purposes: offensive operations, data exfiltration, destructive commands.

**Path:**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | The agent is connected to tools with real-world effects (shell, browser, MCP servers, CLIs). | 🟢 | [\[36\]](../Sources.md#^s36): MCP servers for "remote command execution", browser automation and callback (summary wording) |
| 1 (instance) | A defender's own agent holds the tools that are turned. The [\[36\]](../Sources.md#^s36) evidence in steps 1, 3 and 4 is attacker-owned tooling ([[RQ4 Rogue AI Incidents#Case 2 — GTG-1002: AI-orchestrated espionage using Claude Code (Sept–Nov 2025)\|RQ4 Case 2]]), not a defender's grant. | 🟢 | [[RQ4 Rogue AI Incidents#Case 4 — Grok / Bankrbot: a public reply authorizes a token transfer (May 2026)\|RQ4 Case 4]]: Bankrbot held command authority over a wallet and acted on posts from @grok as the owner's instructions [\[301\]](../Sources.md#^s301), [\[303\]](../Sources.md#^s303). [[RQ4 Rogue AI Incidents#B. Attacks on AI systems\|RQ4 register B-25]] [\[40\]](../Sources.md#^s40): an AI vendor's automated evaluation sandbox held production API keys (added Nov 5, 2026 from [[RQ4 Rogue AI Incidents]]) |
| 2 | The attacker coerces tool selection or parameters. Routes: operator-side jailbreak ([\[36\]](../Sources.md#^s36) 🟢), prompt injection ([\[40\]](../Sources.md#^s40) 🟢 qualified), poisoned tool descriptions (Invariant Labs, 1 Apr 2025, https://invariantlabs.ai/blog/mcp-security-notification 🟡: "malicious instructions are embedded within MCP tool descriptions"), or malware invoking local AI CLIs (Nx postmortem, 5 Sep 2025, https://nx.dev/blog/s1ngularity-postmortem 🟢: the script "attempted to use local AI tools (like Claude and Gemini)"). | 🟢 | as listed |
| 2 (route) | Cross-agent relay: one operator's model publishes attacker-supplied text, and a second operator's agent takes it as a command. Reached through improper output handling, not injection, under [[RQ2 Risk Classification\|RQ2]]'s definitions. | 🟢 (qualified: secondary sources) | [[RQ4 Rogue AI Incidents#Case 4 — Grok / Bankrbot: a public reply authorizes a token transfer (May 2026)\|RQ4 Case 4]]: Grok decoded Morse-encoded text and posted it with an @bankrbot tag, and Bankrbot executed it [\[303\]](../Sources.md#^s303); the transfer is on-chain [\[300\]](../Sources.md#^s300) (added Nov 5, 2026 from [[RQ4 Rogue AI Incidents]]) |
| 2 (route) | Malware invoking local AI CLIs, further instances. This is a conventional supply-chain compromise with the AI as payload: the causal step was the package compromise, and the CLIs' approval gates were turned off by flags the attacker's code supplied. | 🟢 | [[RQ4 Rogue AI Incidents#A. Attackers using AI\|RQ4 register A-25]] [\[352\]](../Sources.md#^s352), A-26 [\[35\]](../Sources.md#^s35), [\[353\]](../Sources.md#^s353), A-27 [\[354\]](../Sources.md#^s354) (added Nov 5, 2026 from [[RQ4 Rogue AI Incidents]]) |
| 3 | The AI does what the concern says: it calls its tools with harmful parameters. | 🟢 | [\[36\]](../Sources.md#^s36): Claude ran reconnaissance and exploitation through the MCP tools |
| 3 (instance) | Defender-grant instances: the turned tool is called with harmful parameters. | 🟢 | [[RQ4 Rogue AI Incidents#Case 4 — Grok / Bankrbot: a public reply authorizes a token transfer (May 2026)\|RQ4 Case 4]] (qualified: secondary sources): Bankrbot signed the transfer of 3,000,000,000 DRB [\[300\]](../Sources.md#^s300); the mechanism rests on press reports [\[303\]](../Sources.md#^s303), [\[304\]](../Sources.md#^s304). [[RQ4 Rogue AI Incidents#B. Attacks on AI systems\|RQ4 register B-25]] [\[40\]](../Sources.md#^s40): the sandbox handed over stored production API keys for several providers (added Nov 5, 2026 from [[RQ4 Rogue AI Incidents]]) |
| 4 | Harm results. | 🟢 | [\[36\]](../Sources.md#^s36): "a handful of successful intrusions" |
| 4 (instance) | Defender-grant instances: harm results. | 🟢 | [[RQ4 Rogue AI Incidents#Case 4 — Grok / Bankrbot: a public reply authorizes a token transfer (May 2026)\|RQ4 Case 4]]: the tokens left the wallet on-chain [\[300\]](../Sources.md#^s300), and the recipient now holds 0 DRB [\[302\]](../Sources.md#^s302); about 80% was later returned (qualified: secondary sources) [\[303\]](../Sources.md#^s303), [\[304\]](../Sources.md#^s304). [[RQ4 Rogue AI Incidents#B. Attacks on AI systems\|RQ4 register B-25]] [\[40\]](../Sources.md#^s40): the stolen keys were reused in a follow-on campaign against about 30 AI companies, in which every attempted path failed (added Nov 5, 2026 from [[RQ4 Rogue AI Incidents]]) |

**Weakest-link light:** 🟢

**In scope:** Yes. Step 2 is a failure of system control and authorization: tools are invoked for purposes no legitimate principal authorized. Step 4 is a confidentiality and integrity failure at the victims.

**Gaps:** In [\[36\]](../Sources.md#^s36) the attacker owned the tools and MCP servers, and no defender's tool grant was coerced; the defender-grant instances are [[RQ4 Rogue AI Incidents#Case 4 — Grok / Bankrbot: a public reply authorizes a token transfer (May 2026)|RQ4 Case 4]] (Grok/Bankr: an on-chain loss, mechanism from secondary reports; reached through improper output handling, not injection, under [[RQ2 Risk Classification|RQ2]]'s definitions) and [[RQ4 Rogue AI Incidents#B. Attacks on AI systems|RQ4 register B-25]] ([\[40\]](../Sources.md#^s40), GTG-50020) (corrected Nov 5, 2026; see [[RQ4 Rogue AI Incidents]]). The Amazon Q wiper prompt "was unsuccessful in executing due to a syntax error" (AWS-2025-015). It is not evidence that a coerced destructive action happened. The Nx postmortem says "attempted" and does not confirm whether the AI CLIs completed the secret search. The GitHub MCP issue (Invariant, 26 May 2025, https://invariantlabs.ai/blog/mcp-github-vulnerability) is 🟡: "implement this attack practically using a set of demo repositories".

## Sources

Shared sources are listed in [[Sources]] and cited by its numbers. Other sources are cited inline.
