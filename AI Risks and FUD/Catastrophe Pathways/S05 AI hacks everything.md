---
tags: [catastrophe-pathway, ai-fud-whitepaper]
---
# S05 AI hacks everything at once: mass autonomous cyberattack

Back to [[RQ2 Screening Log]] · [[Catastrophe Pathways]]

> [!info] Method
> Map the attack path, then light each step by evidence: 🟢 happened in the real world · 🟡 shown only in a lab or evaluation · 🔴 never shown. The scenario is only as real as its weakest step. Quotes came through automated extraction; verify before citing.

**Weakest-link light:** 🔴 Speculative as a simultaneous, autonomous mass attack. Every individual stage is 🟢.

**Necessary security failure (in scope?):** In. It is a chain of conventional security failures at scale.

## Attack path

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | Find targets (reconnaissance) | 🟢 | "Reconnaissance proceeded without human guidance" [\[36\]](../Sources.md#^s36); scheduled AI collection fleets [\[40\]](../Sources.md#^s40). |
| 2 | Find vulnerabilities | 🟢 | A criminal 2FA-bypass zero-day attributed to AI with "high confidence" [\[176\]](../Sources.md#^s176); AI-assisted PHP2Shell discovery [\[79\]](../Sources.md#^s79). |
| 3 | Develop exploits | 🟢 | An AI-built exploit seen in the wild [\[176\]](../Sources.md#^s176); lab: working Firefox exploits 181 times [\[177\]](../Sources.md#^s177). |
| 4 | Gain initial access | 🟢 | Access to at least 14 of 42 targets in one campaign [\[40\]](../Sources.md#^s40); "a handful" of ~30 in GTG-1002 [\[36\]](../Sources.md#^s36). |
| 5 | Move laterally and escalate | 🟢 | One stolen token to full admin in about 3 hours [\[40\]](../Sources.md#^s40). Lab ranges solved only partially (e.g., 3 of 10 full runs) [\[178\]](../Sources.md#^s178). |
| 6 | Steal data or cause impact | 🟢 | Hundreds of gigabytes and ~140,000 records exfiltrated [\[40\]](../Sources.md#^s40). Anthropic: "autonomy and harm are separate axes"; humans still set targets and reviewed exfiltration [\[40\]](../Sources.md#^s40). |
| 7 | Run the full lifecycle autonomously | 🔴 | NCSC (Jul 2026): "we have not yet seen fully autonomous attacks operating across the complete intrusion lifecycle" [\[179\]](../Sources.md#^s179). International AI Safety Report 2026: not reported [\[171\]](../Sources.md#^s171). The Jun–Jul 2026 OpenAI/HF incident ([[G15 Agent misbehaviour- misread task, exceeded scope, loss of control, rog\|G15]]) had evaluation agents attack out-of-scope live systems without approval; it was not attacker-directed, and the NCSC still reported no full-lifecycle autonomous attack afterward. |
| 8 | Compromise many unrelated targets simultaneously against active defenders | 🔴 | Largest documented AI-run scopes are about 30–50 targets [\[36\]](../Sources.md#^s36)[\[40\]](../Sources.md#^s40). No cyber range includes active defenders [\[178\]](../Sources.md#^s178). AI-found bugs are exploited at about the normal rate (1.3%) [\[180\]](../Sources.md#^s180). |

## Also on record

- Threat intel consistently reports productivity and speed, not breakthrough capability [\[34\]](../Sources.md#^s34)[\[33\]](../Sources.md#^s33).
- Patch bottleneck: of 530 disclosed AI-found bugs, 75 were patched [\[181\]](../Sources.md#^s181).
- Mandiant, M-Trends 2026 (2025 investigations): "we don't consider 2025 to be the year where breaches were the direct result of AI"; "the vast majority of successful intrusions still stem from human and systemic failures" [\[182\]](../Sources.md#^s182).
- Microsoft, 2026 Digital Defense Report (blog summary): AI "can give threat actors greater speed, scale, and ability to tailor activity," but "much of their use remains focused on specific parts of existing attack workflows" [\[183\]](../Sources.md#^s183).
- OpenAI, Oct 2025: "threat actors bolt AI onto old playbooks to move faster, not gain novel offensive capability" [\[184\]](../Sources.md#^s184).

## Not publicly knowable / not verified

- The full Microsoft MDDR 2026 and OpenAI's 2026 threat-report cyber sections were not read; claims of "autonomous 32-step attack chains" (secondary) are unverified and, if real, describe emulated environments.
- Vendor incident data is self-reported; VulnCheck disputes some Glasswing counts [\[180\]](../Sources.md#^s180).

## Sources

All sources are listed in [[Sources]]; citations here use its numbers.
