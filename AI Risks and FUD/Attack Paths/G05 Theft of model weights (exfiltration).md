---
tags: [attack-path, ai-fud-whitepaper]
---
# G05 Theft of model weights (exfiltration)

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):** Baseline: proprietary weights leaked or stolen and redistributed (IP loss, loss of control over release). Maximal (RAND; lab security standards): a highly resourced actor steals frontier weights, removes safeguards, and uses the model for catastrophic misuse.

**Path (baseline):**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | Unauthorized party gets access to weights. Routes: intrusion; insider or authorized-recipient leak | 🟢 | NovelAI announcement (company account, r/NovelAi), Oct 2022: "we experienced an unauthorized breach in the company's GitHub and secondary repositories." DOJ N.D. Cal., "Former Google Engineer Found Guilty…", 29 Jan 2026, https://www.justice.gov/usao-ndca/pr/former-google-engineer-found-guilty-economic-espionage-and-theft-confidential-ai : insider "uploaded them to his personal Google Cloud account" (AI infrastructure trade secrets, not weights) |
| 2 | Weights are copied out | 🟢 | Mistral "miqu," Jan 2024: Mistral CEO Arthur Mensch (account `arthurmensch`) opened discussion #10, "Might consider attribution," on the leaked repo, 31 Jan 2024, https://huggingface.co/miqudev/miqu-1-70b/discussions/10. Meta LLaMA, Mar 2023: Meta's DMCA notice to GitHub, 20 Mar 2023 (github/dmca, `2023/03/2023-03-21-meta.md`), against `shawwn/llama-dl` and 403 forks: "No one is authorized to exhibit, reproduce, transmit, or otherwise distribute Meta Properties." Mensch on X, 31 Jan 2024, https://x.com/arthurmensch/status/1752737462663684344: "An over-enthusiastic employee of one of our early access customers leaked a quantised (and watermarked) version of an old model we trained." |
| 3 | Weights are redistributed or used by unauthorized parties | 🟢 | Miqu hosted publicly on Hugging Face (huggingface.co/miqudev/miqu-1-70b; Mensch opened a PR there titled "Might consider attribution", 31 Jan 2024) |

**Path (maximal):**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | Highly resourced or state actor compromises a frontier lab (intrusion or insider) | 🟢 (insider; AI trade secrets, not weights) | DOJ Ding verdict above. RAND, "Securing AI Model Weights" RR-A2849-1, 30 May 2024, https://www.rand.org/pubs/research_reports/RRA2849-1.html : "38 meaningfully distinct attack vectors" |
| 2 | Frontier model weights are exfiltrated | 🔴 | No documented theft of frontier weights by a state actor found |
| 3 | Safeguards are removed | 🟢 | Shared step [[RQ2 Screening Log#Shared steps\|SS3]] (see [[RQ2 Screening Log]]): safety behaviour is stripped from open weights by fine-tuning in practice ([[G22 Model artefact manipulation - malicious fine-tuning - training regimen\|G22]] Path B step 2). Qi et al., arXiv 2310.03693. Never shown on stolen frontier weights, because step 2 has not happened. |
| 4 | Model provides catastrophic (e.g. CBRN) uplift and is used | 🟡 / 🔴 | Anthropic, "Activating ASL-3 protections", 22 May 2025, https://www.anthropic.com/news/activating-asl3-protections : "clearly ruling out ASL-3 risks is not possible for Claude Opus 4" (evaluation only); use not documented |

**Weakest-link light:** Baseline 🟢. Maximal 🔴.

**In scope:** Yes. Necessary security failure at steps 1–2: confidentiality and authorization (and authentication on the intrusion route).

**Gaps:**
- Meta's DMCA notice names LLaMA but does not say "weights."
- The NovelAI statement quote names "proprietary software and source code"; that model weights were part of the leak is reported but not in the quoted line.