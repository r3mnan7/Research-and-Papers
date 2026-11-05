---
tags: [attack-path, ai-fud-whitepaper]
---
# G22 Model artefact manipulation / malicious fine-tuning / training regimen / quantisation

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):** This concern covers different harms, so it has three paths: (A) malicious model files run code when loaded; (B) fine-tuning strips safety training so the model produces harmful output; (C) the training regimen is sabotaged or altered.

**Path A (malicious model file):**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | Attacker builds a model file with an executable payload (pickle) | 🟢 | JFrog, "Data Scientists Targeted by Malicious Hugging Face ML Models with Silent Backdoor", 27 Feb 2024, https://jfrog.com/blog/data-scientists-targeted-by-malicious-hugging-face-ml-models-with-silent-backdoor/ : "around 100 instances"; "reverse shell connection to an actual IP address" |
| 2 | File is published on a public hub and gets past scanning | 🟢 | ReversingLabs, "nullifAI", Feb 2025, https://www.reversinglabs.com/blog/rl-identifies-malware-ml-model-hosted-on-hugging-face : evaded Picklescan. RL says they "look more like a proof-of-concept"; JFrog notes a possible researcher origin (KREOnet IP) |
| 3 | Victim downloads and loads the model | 🟡 | Only researcher loading documented; no victim compromise found |
| 4 | Payload runs and compromises the host | 🟡 | Same sources |

**Path B (safety-stripping fine-tune):**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | Attacker gets fine-tunable weights or a fine-tuning API | 🟢 | Open-weight releases; leaked weights ([[G05 Theft of model weights (exfiltration)\|G05]]) |
| 2 | Fine-tuning removes safety behaviour (AI drops its safeguards) | 🟢 | Cisco Talos, "Cybercriminal abuse of large language models", 25 Jun 2025, https://blog.talosintelligence.com/cybercriminal-abuse-of-large-language-models : uncensored model WhiteRabbitNeo "will happily write offensive security tools." Qi et al., arXiv 2310.03693, 2023: "only 10 such examples," "less than $0.20" (🟡) Shared step [[RQ2 Screening Log#Shared steps\|SS3]]. |
| 3 | Stripped model's output is used to cause harm | 🔴 | Talos documents no attack carried out with these tools; FraudGPT turned out to be a scam on buyers |

**Path C (altered training regimen / quantisation):**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | Insider or supplier with access to the training pipeline. Alternatively, an attacker publishes a model built to turn malicious when quantised | 🟢 (insider) / 🟡 (quantisation) | ByteDance statement of 19 Oct 2024, reported by Yicai Global 21 Oct 2024, https://www2.yicaiglobal.com/news/fact-check-bytedance-confirms-intern-disrupted-ai-model-training-with-malware (primary statement not retrieved). Egashira et al., "Exploiting LLM Quantization", arXiv 2405.18137 |
| 2 | Training code or regimen is altered | 🟢 / 🟡 | ByteDance: "The intern interfered with the AI model training task." Egashira: "benign behavior in full precision but when quantized, it follows the adversarial behavior" |
| 3 | Training disrupted, or the deployed model behaves maliciously | 🟢 (disruption) / 🟡 (malicious behaviour) | Same sources |

**Weakest-link light:** Path A 🟡. Path B 🔴. Path C 🟢 (insider sabotage route).

**In scope:** Yes.
- Path A: step 4 is a system-control/integrity failure (code execution); step 2 is supply-chain integrity.
- Path C: step 2 is integrity and authorization.
- Path B: no step requires a security failure when the weights were obtained legitimately. Only the leaked-weights route involves one (confidentiality, via [[G05 Theft of model weights (exfiltration)|G05]]), so only that route of Path B is analyzed; safety-stripping of legitimately obtained weights is outside scope.

**Gaps:**
- No primary ByteDance statement retrieved.
- No documented victim infected by a hub model. CSA (12 May 2026, see [[G21 Supply chain - value chain - third-party components|G21]]) reports a typosquatted repo with 244,000 downloads whose loader ran a credential stealer, but no documented compromise of a downloader.