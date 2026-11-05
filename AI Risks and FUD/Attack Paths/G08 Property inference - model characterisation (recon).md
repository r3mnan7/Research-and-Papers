---
tags: [attack-path, ai-fud-whitepaper]
---
# G08 Property inference / model characterisation (recon)

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):** Two versions. Property inference: disclosure of aggregate properties of the training data. Model characterisation: learning a model's architecture or hidden parameters to plan follow-on attacks.

**Path:**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | Attacker gets query or white-box access | 🟢 | Routine (GTIG Feb 2026, "legitimate access") |
| 2 | Attacker infers dataset properties or characterises the model (AI's outputs or parameters reveal it) | 🟢 | Characterisation route, in the wild: GreyNoise, "Threat Actors Actively Targeting LLMs," 8 Jan 2026, https://www.greynoise.io/blog/threat-actors-actively-targeting-llms: 80,469 sessions probing 73+ model endpoints, with prompts likely meant to "fingerprint which model actually responds." Zenity Labs, "Scanning for AI," 30 Jun 2026, https://labs.zenity.io/p/scanning-for-ai-live-campaigns-mapping-the-internet-s-exposed-llm-backends: ~446 requests asked models to name themselves; Zenity notes intent is unverified. Property-inference route is 🟡: Ganju et al., CCS 2018, https://doi.org/10.1145/3243734.3243834: "the model consumer can infer other properties of the training data the model producer did not intend to share" (abstract via OpenAlex). Carlini et al., arXiv 2403.06634: "the exact hidden dimension of the gpt-3.5-turbo model." |
| 3 | Inferred information is disclosed harmfully or used for a follow-on attack | 🟡 | Carlini et al. 2024 used the characterisation to extract the projection matrix (controlled). GreyNoise and Zenity record scanning, but no follow-on attack that used the fingerprint was documented. |

**Weakest-link light:** 🟡 (step 3)

**In scope:** In. Step 2 is a confidentiality failure when confidential dataset properties or secret parameters are revealed; only that route is analyzed. Outside scope: characterising behaviour the model is permitted to show, which requires no security failure.

**Gaps:** No in-the-wild property inference on training data was found. Reconnaissance is documented; its use in a follow-on attack is not.