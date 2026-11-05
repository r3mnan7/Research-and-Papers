---
tags: [attack-path, ai-fud-whitepaper]
---
# G18 Memory & context poisoning (persistent)

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):** The sources claim two severities. Baseline: an assistant's memory is seeded so that later recommendations are biased (Microsoft, Feb 2026). Maximal: a persistent instruction exfiltrates all of a user's future conversations (SpAIware).

**Path:**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | Attacker content reaches the assistant through a link with a prefilled prompt, a web page or a document. | 🟢 | Microsoft Security, "AI Recommendation Poisoning," 10 Feb 2026, https://www.microsoft.com/en-us/security/blog/2026/02/10/ai-recommendation-poisoning/: "50 distinct examples of prompt‑based attempts" from 31 companies |
| 2 | The AI does what the concern says: it writes the attacker's instruction or false fact into persistent memory. | 🟡 | Rehberger, "SpAIware," 20 Sep 2024, https://embracethered.com/blog/posts/2024/chatgpt-macos-app-persistent-data-exfiltration/: "long-term persistent spyware into ChatGPT's memory". Rehberger, Gemini, 10 Feb 2025, https://embracethered.com/blog/posts/2025/gemini-memory-persistence-prompt-injection/. Microsoft: "effectiveness and persistence… varied" |
| 3 | The poisoned memory is retrieved in a later session and changes behaviour. | 🟡 | SpAIware: exfiltration continues into future chats |
| 4 | Harm: biased recommendations (baseline) or ongoing exfiltration (maximal). | 🟡 | SpAIware: "continuous data exfiltration of any information the user typed" (researcher demo). OpenAI fixed the macOS exfiltration vector in Sept 2024 |

**Weakest-link light:** 🟡 (both paths)

**In scope:** Yes. Step 2 is an integrity failure (the persistent memory store). On the maximal path, step 4 is a confidentiality failure.

**Gaps:** Microsoft recorded real-world attempts but no count of users whose memory was actually poisoned. Google rated the Gemini issue "low likelihood and low impact." [\[40\]](../Sources.md#^s40) mentions "persistent campaign memory" for GTG-10007, but that is the attacker's own memory, not poisoning.

## Sources

Shared sources are listed in [[Sources]] and cited by its numbers. Other sources are cited inline.
