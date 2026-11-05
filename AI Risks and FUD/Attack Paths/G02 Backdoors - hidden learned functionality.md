---
tags: [attack-path, ai-fud-whitepaper]
---
# G02 Backdoors / hidden learned functionality

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):** A model behaves normally until a trigger appears, then misbehaves. Examples: a stop sign classified as a speed limit, or code-writing models inserting exploitable code. Sources say such backdoors can be undetectable and can survive safety training.

**Path:**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | Attacker plants a backdoor. Routes: poisoned training data, malicious outsourced training, or direct weight edit | 🟡 | Gu et al., "BadNets", arXiv 1708.06733, 2017: "identifies stop signs as speed limits when a special sticker is added." Goldwasser et al., arXiv 2204.06974, 2022: "a malicious learner can plant an undetectable backdoor into a classifier" |
| 2 | Victim gets and deploys the backdoored model (supply chain, hub, outsourced training) | 🟡 | Mithril Security, "PoisonGPT", 9 Jul 2023, https://blog.mithrilsecurity.io/poisongpt-how-we-hid-a-lobotomized-llm-on-hugging-face-to-spread-fake-news/ : researchers uploaded a ROME-edited GPT-J under a lookalike name ("EleuterAI") on Hugging Face as a demonstration |
| 3 | Backdoor gets past evaluation and safety training | 🟡 | Hubinger et al., "Sleeper Agents", arXiv 2401.05566, Jan 2024: "not removed by standard safety training techniques." PoisonGPT: ToxiGen difference "only 0.1% in accuracy" |
| 4 | Trigger is presented and the hidden behaviour runs (AI does what the concern says) | 🟡 | Hubinger et al.: "insert exploitable code when the stated year is 2024" |
| 5 | The triggered behaviour causes harm in deployment | 🔴 | No in-the-wild case after a full search. Cloud Security Alliance, "Poisoned Weights: Trigger-Activated Backdoors in Abliterated Open-Weight Models," 21 Oct 2026, https://labs.cloudsecurityalliance.org/research/csa-research-note-abliterated-model-backdoors-20261021-csa-s/, documents none. Controlled demos (🟡): ProjectDiscovery (Prince Chaddha), "How abliterated models can get you pwned," 6 Oct 2026, https://projectdiscovery.io/research/how-abliterated-models-can-get-you-pwned (a LoRA-triggered Qwen2.5-7B exfiltrated `.env` secrets through Codex CLI, "with a .env containing production-looking dummy credentials"); Hubinger et al., "Sleeper Agents," arXiv 2401.05566; Mithril Security, "PoisonGPT," 9 Jul 2023, https://blog.mithrilsecurity.io/poisongpt-how-we-hid-a-lobotomized-llm-on-hugging-face-to-spread-fake-news/ (researcher upload to a live hub). |

**Weakest-link light:** 🔴

**In scope:** Yes. Necessary security failure at step 1 (integrity of training data or weights) and step 2 (supply-chain integrity/authentication of model provenance).

**Gaps:**
- Real malicious models on public hubs run code when the file is loaded (pickle/loader), not a trigger learned into the weights: JFrog, 27 Feb 2024, https://jfrog.com/blog/data-scientists-targeted-by-malicious-hugging-face-ml-models-with-silent-backdoor/ ("initiates a reverse shell connection to an actual IP address"). Those are filed under [[G21 Supply chain - value chain - third-party components|G21]] and [[G22 Model artefact manipulation - malicious fine-tuning - training regimen|G22]], because they lack this concern's AI step (hidden learned functionality).
- Microsoft, "Detecting backdoored language models at scale," 4 Feb 2026, https://www.microsoft.com/en-us/security/blog/2026/02/04/detecting-backdoored-language-models-at-scale/, tested only "after injecting controlled backdoors."