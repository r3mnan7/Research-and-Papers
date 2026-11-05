---
tags: [attack-path, ai-fud-whitepaper]
---
# G09 Embedding inversion

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):** Recovery of the source text, including PII such as full names in clinical notes, from stored or shared embeddings.

**Path:**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | Attacker gets embeddings. Routes: exposed or misconfigured vector database; API; breach | 🟢 | Legit Security, "The Risks Lurking in Publicly Exposed GenAI Development Services", 22 Aug 2024, https://legitsecurity.com/blog/the-risks-lurking-in-publicly-exposed-genai-development-services : "around 30 servers with evidence of corporate or private data"; the embeddings themselves were readable |
| 2 | Attacker has or trains an inversion model for that embedding model | 🟡 | Morris et al., "Text Embeddings Reveal (Almost) As Much As Text", arXiv 2310.06816, 2023 |
| 3 | Source text is recovered (AI inverts the embeddings) | 🟡 | Same source: "recover 92% of 32-token text inputs exactly"; recovered "full names" from clinical notes |

**Weakest-link light:** 🟡

**In scope:** Yes. Necessary security failure at step 1 (confidentiality and authorization, on the exposed-database or breach routes) and step 3 (confidentiality).

**Gaps:** No documented in-the-wild inversion of leaked embeddings found.
