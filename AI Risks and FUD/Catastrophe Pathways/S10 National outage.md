---
tags: [catastrophe-pathway, ai-fud-whitepaper]
---
# S10 National digital or telecom outage

Back to [[RQ2 Screening Log]] · [[Catastrophe Pathways]]

> [!info] Method
> Map the attack path, then light each step by evidence: 🟢 happened in the real world · 🟡 shown only in a lab or evaluation · 🔴 never shown. The scenario is only as real as its weakest step. Quotes came through automated extraction; verify before citing.

**Weakest-link light:** 🔴 Speculative as a deliberate national outage. Accidental mass outage is 🟢.

**Necessary security failure (in scope?):** In. Requires availability or integrity failure at a shared dependency or backbone.

## Attack path

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | A single point of failure takes down systems at mass scale | 🟢 | Accidental: the July 2024 CrowdStrike update hit 8.5 million Windows devices [\[208\]](../Sources.md#^s208). |
| 2 | Adversary presence in telecom backbones | 🟢 | Salt Typhoon: the actors "focus on large backbone routers of major telecommunications providers" and "often modify routers to maintain persistent, long-term access," for espionage (NSA/CISA/FBI and allies, AA25-239A, Aug 2025) [\[211\]](../Sources.md#^s211). The advisory describes no destructive or outage capability. |
| 3 | Deliberately cause a national-scale outage | 🔴 | Not documented. Using Salt Typhoon-style access to cause an outage is an extrapolation; no source shows that capability or intent. |
| 4 | AI materially enables the attack | 🔴 | Only general statements that AI "offers new ways" to attack [\[209\]](../Sources.md#^s209). |

## Also on record

- UK National Risk Register 2026 adds national data-infrastructure disruption and digital resilience failure [\[210\]](../Sources.md#^s210).

## Not publicly knowable / not verified

- Telecom regulator controls and the Dec 2024 CISA hardening guidance not retrieved.
- NRR likelihood figures are from secondary coverage.

## Sources

All sources are listed in [[Sources]]; citations here use its numbers.
