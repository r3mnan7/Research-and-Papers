---
tags: [attack-path, ai-fud-whitepaper]
---
# G21 Supply chain / value chain / third-party components

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):**
- **Baseline:** A malicious or compromised third-party AI component runs attacker code or leaks data inside the organisation that adopts it. The component can be a model file, an AI library, or an MCP server.
- **Maximal:** A backdoored upstream model, poorly vetted at the scale it ships, behaves maliciously in downstream deployments. NIST AI 600-1 §2.12 describes weakly vetted components causing "diminished transparency or accountability for downstream users."

**Path A (baseline):**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | An attacker publishes or hijacks an AI component. Routes: (a) a malicious model on Hugging Face; (b) a hijacked package release; (c) a malicious MCP server. | 🟢 | LiteLLM, "Security Update: Suspected Supply Chain Incident," BerriAI, 24 Mar 2026, https://docs.litellm.ai/blog/security-update-march-2026. Versions 1.82.7 and 1.82.8 contained "a credential stealer"; they were live about 40 minutes. JFrog, "Data Scientists Targeted by Malicious Hugging Face ML Models with Silent Backdoor," 27 Feb 2024, https://jfrog.com/blog/data-scientists-targeted-by-malicious-hugging-face-ml-models-with-silent-backdoor/. JFrog found "around 100 instances" of malicious models. |
| 2 | The adopter installs or loads the component without catching it. | 🟢 | JFrog, same post: users reporting a "dangerously malicious payload" indicated they were victims. postmark-mcp had 1,643 downloads [via secondary: The Hacker News, 29 Sep 2025, https://thehackernews.com/2025/09/first-malicious-mcp-server-found.html; Koi's original post now redirects and could not be fetched]. |
| 3 | The component runs malicious logic with the adopter's privileges. Routes: pickle code running on model load; a credential stealer; BCC-copying of emails. | 🟢 | JFrog: "pickle files can also contain arbitrary code that is executed when the file is loaded." LiteLLM: the payload sent harvested secrets to `models.litellm.cloud`, "not an official BerriAI / LiteLLM domain." The 🟢 rests on the package route (LiteLLM). The model-file (pickle) route on its own has no documented victim compromise and is 🟡 (see [[G22 Model artefact manipulation - malicious fine-tuning - training regimen\|G22]] Path A). |
| 4 | The attacker receives the data or access. | 🟢 | Koi, quoted in The Hacker News, 29 Sep 2025: "quietly copying every email to the developer's personal server" [via secondary]. GTIG, 11 May 2026 (URL under [[G33 AI-accelerated vulnerability discovery & exploitation\|G33]]): the LiteLLM compromise "could lead to considerable exposure of AI API secrets." |

**Path B (maximal, backdoored weights):**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | An attacker plants a trigger-conditioned backdoor in an upstream model's weights or training data. | 🟡 | Hubinger et al., "Sleeper Agents," arXiv:2401.05566, Jan 2024, https://arxiv.org/abs/2401.05566. This is a lab construction. |
| 2 | The backdoor survives the downstream adopter's vetting and safety training. | 🟡 | Same paper: the backdoor "can be made persistent, so that it is not removed by standard safety training techniques." |
| 3 | The backdoored model is adopted in production. | 🔴 | No documented production adoption of a trigger-conditioned model after a full search. CSA, "Model Hub Typosquatting," 12 May 2026, https://labs.cloudsecurityalliance.org/research-rb/csa-research-note-huggingface-model-supply-chain-attack-2026/: a typosquatted repo reached 244,000 downloads, but its `loader.py` ran credential-stealing code (a Path A route, not a learned trigger). Closest controlled case: PoisonGPT on a live hub (🟡; see [[G02 Backdoors - hidden learned functionality\|G02]]). |
| 4 | The trigger fires and causes harmful behaviour in a deployment. | 🔴 | None found. |

**Weakest-link light:** Path A 🟢. Path B 🔴.

**In scope:** Yes. Necessary security failure at step 1 (integrity of the component), step 3 (system control) and step 4 (confidentiality).

**Gaps:**
- No primary source gives victim counts for LiteLLM.
- The Koi primary post for postmark-mcp could not be fetched.
- The authors of the JFrog models may have been researchers (JFrog leaves this unresolved).