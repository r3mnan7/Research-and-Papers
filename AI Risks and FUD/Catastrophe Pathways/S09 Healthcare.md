---
tags: [catastrophe-pathway, ai-fud-whitepaper]
---
# S09 Healthcare: attacks on hospitals or medical devices cause mass patient harm

Back to [[RQ2 Screening Log]] · [[Catastrophe Pathways]]

> [!info] Method
> Map the attack path, then light each step by evidence: 🟢 happened in the real world · 🟡 shown only in a lab or evaluation · 🔴 never shown. The scenario is only as real as its weakest step. Quotes came through automated extraction; verify before citing.

**Weakest-link light:** 🔴 Speculative as mass harm. Large disruption is 🟢, without AI.

**Necessary security failure (in scope?):** In. Requires availability and integrity failures in health IT or devices.

## Attack path

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | Compromise hospital or health IT at scale | 🟢 | WannaCry hit at least 81 English NHS trusts and 603 other NHS bodies [\[203\]](../Sources.md#^s203). Change Healthcare, 2024: "criminals used compromised credentials to remotely access a Change Healthcare Citrix portal"; "The portal did not have multi-factor authentication" (UnitedHealth CEO testimony) [\[207\]](../Sources.md#^s207); about 192.7 million people affected (HHS OCR, Jul 2025) [\[204\]](../Sources.md#^s204)[\[204\]](../Sources.md#^s204). |
| 2 | Compromise implanted or connected medical devices | 🟡 | Pacemaker authentication "can be compromised or bypassed," but needs radio proximity and "a highly skilled attacker"; no malicious use reported [\[205\]](../Sources.md#^s205). |
| 3 | Cause attributable mass patient harm | 🔴 | NAO did not establish patient harm from WannaCry [\[203\]](../Sources.md#^s203). |
| 4 | AI materially enables the attack | 🔴 | Neither incident involved AI; only general AI threat assessments exist. |

## Also on record

- FDA now requires cybersecurity information for "cyber devices" before market (section 524B; final guidance Jun 2025) [\[206\]](../Sources.md#^s206).

## Not publicly knowable / not verified

- No prominent primary source frames AI-enabled medical-device mass casualty specifically.

## Sources

All sources are listed in [[Sources]]; citations here use its numbers.
