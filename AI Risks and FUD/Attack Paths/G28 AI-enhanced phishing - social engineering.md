---
tags: [attack-path, ai-fud-whitepaper]
---
# G28 AI-enhanced phishing / social engineering

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):** AI makes lures more convincing, more scalable and more personalised. That raises the success rate of credential theft, initial access and fraud. NCSC, Jan 2024: AI-enabled access "will contribute to the global ransomware threat in the near term."

**Path:**

| #   | Step                                                                                                                             | Light | Evidence                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| --- | -------------------------------------------------------------------------------------------------------------------------------- | ----- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | The attacker uses AI to research targets and write or run lures. Routes: written lures; personas; multi-turn "rapport-building." | 🟢    | GTIG, "GTIG AI Threat Tracker: Distillation, Experimentation, and (Continued) Integration of AI for Adversarial Use," 12 Feb 2026, https://cloud.google.com/blog/topics/threat-intelligence/distillation-experimentation-integration-ai-adversarial-use: APT42 used Gemini to "craft a good persona or scenario to get engagement from the target." GTIG, 5 Nov 2025 (URL under [[G31 AI-generated - AI-concealed malware\|G31]]): APT42 used Gemini "to craft material for phishing campaigns." |
| 2   | The lure reaches the victim.                                                                                                     | 🟢    | FBI IC3 PSA I-120324-PSA, "Criminals Use Generative Artificial Intelligence to Facilitate Financial Fraud," 3 Dec 2024, https://www.ic3.gov/PSA/2024/PSA241203. Microsoft, "AI vs. AI: Detecting an AI-obfuscated phishing campaign," 24 Sep 2025, https://www.microsoft.com/en-us/security/blog/2025/09/24/ai-vs-ai-detecting-an-ai-obfuscated-phishing-campaign/: a real campaign that Defender blocked.                                          |
| 3   | The victim acts on the lure (clicks, enters credentials, or pays).                                                               | 🟢    | FBI PSA, same: generative AI is used to "facilitate financial fraud." The claimed uplift over non-AI lures is 🟡 only: Heiding et al., arXiv:2412.00586, 30 Nov 2024, https://arxiv.org/abs/2412.00586, a human-subject study. Fully AI-automated emails got 54% clicks against a 12% control; "performed on par with human experts."                                                                                                               |
| 4   | The attacker converts the response into account access or financial loss.                                                        | 🟢    | FBI PSA, same.                                                                                                                                                                                                                                                                                                                                                                                                                                      |

**Weakest-link light:** 🟢 for occurrence. The claimed higher success rate is supported only at 🟡.

**In scope:** In. Necessary security failure at step 3/4 (authentication) on every route: credential harvesting, and payment fraud, where the victim acts on an identity or instruction that wasn't verified. Social engineering is an attack on authentication.

**Gaps:**
- No primary source measures the real-world success uplift of AI-written lures compared with human-written ones.
- This research did not reach the Microsoft Digital Defense Report 2025 or the OpenAI reports.
