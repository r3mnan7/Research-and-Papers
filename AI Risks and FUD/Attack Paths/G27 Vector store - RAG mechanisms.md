---
tags: [attack-path, ai-fud-whitepaper]
---
# G27 Vector store / RAG mechanisms

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):** Poisoned or manipulated retrieved content changes answers (misinformation, steered recommendations) or carries injected instructions that lead to exfiltration. Cross-tenant retrieval exposes other customers' data.

**Path (poisoning / manipulation):**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | The attacker places content in a corpus the retriever indexes: the public web, shared documents, email. | 🟢 | [\[38\]](../Sources.md#^s38): SEO-poisoning payloads meant to push a fake betting site in LLM recommendations (summary wording). [\[39\]](../Sources.md#^s39) |
| 2 | The retriever selects the poisoned chunk for the target query. | 🟡 | Zou et al., "PoisonedRAG," arXiv:2402.07867 (v3 Aug 2024), https://arxiv.org/abs/2402.07867. USENIX Security 2025 acceptance is unverified |
| 3 | The AI does what the concern says: the model treats the retrieved text as authoritative or as instructions. | 🟡 | PoisonedRAG: "90% attack success rate when injecting five malicious texts". [\[76\]](../Sources.md#^s76) |
| 4 | A harmful answer or action reaches the user or attacker. | 🟡 | [\[76\]](../Sources.md#^s76); [\[38\]](../Sources.md#^s38) success unconfirmed |

**Path (cross-boundary leakage through retrieval):**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | The attacker places instructions in content the retriever indexes. | 🟢 | As step 1 above. |
| 2 | The AI does what the concern says: retrieval pulls data from a scope the attacker cannot access (a private channel, another tenant) into the answer. | 🟡 | PromptArmor, "Data Exfiltration from Slack AI via Indirect Prompt Injection," Aug 2024, https://promptarmor.com/resources/data-exfiltration-from-slack-ai-via-indirect-prompt-injection: an injection in a public channel leaked an API key from a private channel (PoC). Noma Security (Sasi Levi), "ForcedLeak," 25 Sep 2025, https://noma.security/blog/forcedleak-agent-risks-exposed-in-salesforce-agentforce/: Agentforce leaked CRM lead data (PoC, CVSS 9.4). |
| 3 | The data reaches the attacker. | 🟡 | Same PoCs. Slack, 21 Aug 2024, https://slack.com/blog/news/slack-security-update-082124: "no evidence" of unauthorized access to customer data. Salesforce enforced Trusted URLs on 8 Sep 2025 (per Noma). |

**Path (retrieval jamming):**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | The attacker adds a document to a corpus the retriever indexes. | 🟢 | As step 1 of the poisoning path. |
| 2 | The AI does what the concern says: a crafted "blocker" document is retrieved for a target query and makes the system refuse or answer that it has no information. | 🟡 | Shafran, Schuster, Shmatikov, "Machine Against the RAG: Jamming Retrieval-Augmented Generation with Blocker Documents," arXiv 2406.05870 (v4, Mar 2025; USENIX Security 2025, https://www.usenix.org/conference/usenixsecurity25/presentation/shafran): RAG systems on untrusted content "are vulnerable to denial-of-service attacks" (controlled evaluation across several embeddings and LLMs). |
| 3 | Legitimate users lose answers to targeted questions. | 🟡 | Same source. No in-the-wild case found. |

**Path (semantic-cache poisoning):**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | The attacker submits queries to a service that caches answers by embedding similarity. | 🟢 | Ordinary query access. |
| 2 | The AI does what the concern says: a crafted query collides with a victim's cache key, so the victim receives the attacker-shaped cached response. | 🟡 | Zhang, Liu, Xie, Huang, She, "From Similarity to Vulnerability: Key Collision Attack on LLM Semantic Caching," arXiv 2601.23088 (Jan 2026; ICML 2026): an 86% hit rate in response hijacking; locality "fundamentally conflicts with the cryptographic avalanche effect" (controlled). |
| 3 | Harmful or wrong answers reach users or agents. | 🟡 | Same source (financial-agent case study, not shown to be a live system). No in-the-wild case found. |

**Weakest-link light:** Poisoning path 🟡. Cross-boundary path 🟡. Retrieval jamming 🟡. Semantic-cache poisoning 🟡.

**In scope:** Yes. Steps 1–2 are an integrity failure (the knowledge base). On the cross-tenant route, retrieval is a confidentiality and authorization failure.

**Gaps:** No primary source documents cross-tenant leakage through a shared vector store specifically (🔴). Nearest cases are not retrieval: the Asana MCP bug ([[G13 Sensitive information disclosure - privacy breach via AI system|G13]]) and Sage Copilot (Jan 2025, known only through a spokesperson quote in The Register: "unrelated business information to a very small number of customers"). A Bugcrowd disclosure against OpenAI (19 Aug 2026) names retrieval namespace failure only as a researcher hypothesis. The March 2023 ChatGPT leak ([[G13 Sensitive information disclosure - privacy breach via AI system|G13]]) was a cache bug. Memory poisoning is filed under [[G18 Memory & context poisoning (persistent)|G18]].

## Sources

Shared sources are listed in [[Sources]] and cited by its numbers. Other sources are cited inline.
