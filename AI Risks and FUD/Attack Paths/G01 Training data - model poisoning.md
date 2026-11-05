---
tags: [attack-path, ai-fud-whitepaper]
---
# G01 Training data / model poisoning

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):** Baseline: an attacker changes model behaviour (degraded, biased, offensive or disinformation output, or a security classifier that has been skewed) by adding attacker-controlled data to training, fine-tuning, online learning or retrieval data. Maximal: a small number of poisoned samples compromises large LLMs regardless of their size, which could be used for targeted harmful behaviour.

**Path (baseline):**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | Attacker places data where the model will take it in. Routes: (a) user interaction or feedback in an online-learning system; (b) publishing web content that crawlers or retrieval pick up; (c) changing a hosted dataset source (expired domains, a Wikipedia snapshot window) | 🟢 | Microsoft, "Learning from Tay's introduction", 25 Mar 2016, https://blogs.microsoft.com/blog/2016/03/25/learning-tays-introduction/ : "a coordinated attack by a subset of people exploited a vulnerability in Tay." E. Bursztein (Google anti-abuse lead), "Attacks against machine learning – an overview", May 2018, https://elie.net/blog/ai/attacks-against-machine-learning-an-overview/ : "reporting massive amounts of spam emails as not spam" |
| 2 | The pipeline takes in the data without integrity checks (training, fine-tuning, online learning, or retrieval/RAG) | 🟢 | NIST AI 100-2e2025, Mar 2025, p.27, https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-2e2025.pdf : "MITRE ATLAS reported a poisoning incident on the VirusTotal threat intelligence service." NewsGuard Pravda audit (undated page, covers to Feb 2025), https://www.newsguardrealitycheck.com/p/a-well-funded-moscow-based-global : "deliberately infiltrating the retrieved data of artificial intelligence chatbots" |
| 3 | Model behaviour shifts the way the attacker intended (AI does what the concern says) | 🟢 | NIST AI 100-2e2025 p.27: "The first example of a real-world poisoning attack is the Tay.AI chatbot." NewsGuard: chatbots repeated Pravda narratives 33.55% of the time; 7 of 10 cited Pravda articles |
| 4 | The changed output reaches users or decisions | 🟢 | Microsoft Tay post (offensive tweets published within the first 24 hours) |

**Path (maximal):**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | Attacker injects poison into a web-scale pre-training corpus | 🟡 | Carlini et al., "Poisoning Web-Scale Training Datasets is Practical", arXiv 2302.10149, 2023: "could have poisoned 0.01% of the LAION-400M or COYO-700M datasets for just $60 USD" (a feasibility demonstration, not an actual poisoning) |
| 2 | A frontier developer trains on the poisoned corpus without filtering it | 🟡 | Souly et al., "Poisoning Attacks on LLMs Require a Near-constant Number of Poison Samples", arXiv 2510.07192, 8 Oct 2025: "250 poisoned documents similarly compromise models across all model and dataset sizes" |
| 3 | The poisoned behaviour shows up in the deployed model | 🟡 | Same source (controlled training runs) |
| 4 | The behaviour causes serious downstream harm | 🔴 | No in-the-wild case found |

**Weakest-link light:** Baseline 🟢. Maximal 🔴.

**In scope:** Yes. Necessary security failure at steps 2–3: integrity (untrusted data enters the training or retrieval pipeline, and the model's output is altered without authorization).

**Gaps:**
- The Pravda evidence points to retrieval-time poisoning. Training-time ingestion is not shown.
- The Gmail post documents "at least four malicious large-scale attempts", but not whether they succeeded.
- This research did not read the VirusTotal ATLAS case directly.
