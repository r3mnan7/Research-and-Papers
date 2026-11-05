---
tags: [attack-path, ai-fud-whitepaper]
---
# G26 Improper output handling

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):** Unsanitized model output reaches a renderer, eval, SQL or shell, leading to RCE, XSS or SQLi, or data exfiltration through rendered links and images.

**Path:**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | The attacker influences model output through direct or indirect injection. | 🟢 | See [[G10 Direct prompt injection - jailbreak\|G10]] and [[G11 Indirect prompt injection - goal hijack\|G11]] ([\[36\]](../Sources.md#^s36), [\[40\]](../Sources.md#^s40)) |
| 2 | The AI does what the concern says: its output is passed to an interpreter or renderer without validation. | 🟡 | JFrog/Vanna, 27 Jun 2024 (URL under [[G17 Unexpected code execution by agents\|G17]]): LLM-generated Plotly code is evaluated. [\[76\]](../Sources.md#^s76) EchoLeak |
| 3 | The interpreter runs or renders the payload. | 🟡 | JFrog: "Running the following template will print us the current directory's files!" |
| 4 | Harm: code execution or exfiltration. | 🟡 | JFrog PoC; [\[76\]](../Sources.md#^s76) (no customers affected) |

**Weakest-link light:** 🟡

**In scope:** Yes. Step 3 is an integrity failure, with a system-control failure if it leads to code execution. Step 4 is a confidentiality failure on the exfiltration route.

**Gaps:** No in-the-wild case found after a full search. Every case is a PoC or researcher disclosure: LangChain CVE-2023-29374 and CVE-2023-36258 (both CVSS 9.8, neither in CISA KEV); the Bard markdown-image exfiltration (Embrace The Red, 3 Nov 2023, https://embracethered.com/blog/posts/2023/google-bard-data-exfiltration/; Google fixed it 19 Oct 2023); Slack AI (Slack, "Slack Security Update," 21 Aug 2024, https://slack.com/blog/news/slack-security-update-082124: no evidence of unauthorized access); EchoLeak ("Exploited: No"). [\[40\]](../Sources.md#^s40) says LiteLLM keys were exfiltrated through prompt injection, but the mechanism is not given.

## Sources

Shared sources are listed in [[Sources]] and cited by its numbers. Other sources are cited inline.
