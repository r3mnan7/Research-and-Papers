---
tags: [attack-path, ai-fud-whitepaper]
---
# G23 Model hardware attacks (side channels, fault injection, RAM)

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):** Hardware faults or side channels on shared hardware either leak model inputs and outputs, or corrupt or backdoor weights. Examples: accuracy drops "up to 80%", or a single-bit-flip backdoor with ~99.6% success.

**Path:**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | Attacker runs code on the same GPU, memory or host as the victim model | 🟡 | Assumed in all PoCs below |
| 2 | Attacker triggers a fault or side channel. Routes: Rowhammer on GPU or DRAM; uninitialized GPU local memory | 🟡 | Lin et al., "GPUHammer", USENIX Sec 2025, arXiv 2507.08166 (NVIDIA A6000). Trail of Bits, "LeftoverLocals", 16 Jan 2024, https://blog.trailofbits.com/2024/01/16/leftoverlocals-listening-to-llm-responses-through-leaked-gpu-local-memory/ (CVE-2023-4969) |
| 3 | Weights are corrupted or backdoored, or model data leaks (AI misbehaves or exposes data) | 🟡 | Li et al., "Rowhammer-Based Trojan Injection: One Bit Flip Is Sufficient…", USENIX Sec 2025, https://www.usenix.org/conference/usenixsecurity25/presentation/li-xiang : "up to 99.9%, with an average of 99.6%." GPUHammer: "accuracy drops (up to 80%)." LeftoverLocals: "enough information to reconstruct the LLM response with high precision" |

**Weakest-link light:** 🟡

**In scope:** Yes. Necessary security failure at step 2 (system control/isolation failure) and step 3 (integrity or confidentiality).

**Gaps:** No in-the-wild exploitation found. Trail of Bits notes "very limited ways to observe that an attacker is currently stealing data."
