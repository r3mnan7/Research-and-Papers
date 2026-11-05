---
tags: [attack-path, ai-fud-whitepaper]
---
# G34 Credential attacks amplified (passwords, brute force, credential stuffing)

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):** AI makes password guessing, cracking and credential stuffing faster or more effective, leading to account takeover.

**Path:**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | The attacker obtains credential material (dumps, hashes, or harvested credentials). | 🟢 | Anthropic, Nov 2025 (URL under [[G30 Autonomous - automated attack tooling\|G30]]): "Claude executed systematic credential collection across targeted networks." |
| 2 | AI generates guesses or automates testing and stuffing. Routes: (a) GAN or ML guess generation; (b) an AI agent testing harvested credentials across systems; (c) AI-built stuffing tools. | 🟢 (via route b) | Anthropic, Nov 2025: Claude tested harvested credentials against other systems and mapped access levels without human direction [paraphrase]. Route (a) is 🟡 only: Hitaj et al., "PassGAN," arXiv:1709.00440, https://arxiv.org/abs/1709.00440, where PassGAN combined with HashCat matched 51–73% more passwords than HashCat alone. Route (c): Anthropic, Apr 2025, https://anthropic.com/news/detecting-and-countering-malicious-uses-of-claude-march-2025, describes an actor building tools for leaked IoT-camera credentials, but Anthropic "has not confirmed" deployment. |
| 3 | The credentials succeed against real accounts or systems. | 🟢 | Anthropic, Nov 2025 (intrusions validated). |
| 4 | Account or system takeover. | 🟢 | Same. |

**Weakest-link light:** 🟢 (via the agentic credential-reuse route). The guessing/cracking-uplift route is 🟡.

**In scope:** Yes. Necessary security failure at steps 3–4 (authentication).

**Gaps:**
- This research found no primary source showing AI-generated password guessing or AI-amplified internet-scale stuffing in the wild. The search budget was exhausted before this research could check the OpenAI and Microsoft Digital Defense Report sources.
- GTIG, 11 May 2026: PROMPTSPY replays captured PINs and lock patterns. That is credential capture and replay, not guessing.
