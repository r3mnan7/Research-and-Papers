---
tags: [catastrophe-pathway, ai-fud-whitepaper]
---
# S03 Critical infrastructure: AI causes a large, lasting grid or water failure

Back to [[RQ2 Screening Log]] · [[Catastrophe Pathways]]

> [!info] Method
> Map the attack path, then light each step by evidence: 🟢 happened in the real world · 🟡 shown only in a lab or evaluation · 🔴 never shown. The scenario is only as real as its weakest step. Quotes came through automated extraction; verify before citing.

**Weakest-link light:** 🔴 Speculative (catastrophic version). Local, hours-long disruption is 🟢, but without AI.

**Necessary security failure (in scope?):** In. Every path needs access, integrity, and system-control failures in IT and OT.

## Attack path

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | Initial access to IT networks | 🟢 | Volt Typhoon held footholds "for at least five years" in U.S. infrastructure [\[145\]](../Sources.md#^s145). |
| 2 | Pivot from IT into OT | 🟢 | Ukraine 2015 VPNs lacked two-factor authentication [\[146\]](../Sources.md#^s146); Volt Typhoon moved laterally to a control system [\[145\]](../Sources.md#^s145); poor IT/OT segmentation in 81% of Dragos service reports [\[147\]](../Sources.md#^s147); over 70% of inspected U.S. water systems violated basic requirements [\[148\]](../Sources.md#^s148). Volt Typhoon was "observed testing access to domain-joint OT assets using default OT vendor credentials" [\[145\]](../Sources.md#^s145). |
| 3 | Produce a physical OT effect | 🟢 | Ukraine 2015 (~225,000 customers, hours) [\[146\]](../Sources.md#^s146); Kyiv 2016 [\[149\]](../Sources.md#^s149); Lviv heating 2024; Poland 2025, RTUs damaged but no outage [\[150\]](../Sources.md#^s150). DHS ICS-CERT: outages "impacting approximately 225,000 customers," breakers operated remotely "by multiple external humans," and serial-to-Ethernet devices made inoperable by corrupted firmware [\[159\]](../Sources.md#^s159). CRASHOVERRIDE "Issues valid commands directly to remote terminal units (RTUs)" [\[160\]](../Sources.md#^s160). |
| 4 | Defeat safety systems and manual fallback | 🔴 | TRITON triggered a safe shutdown instead [\[151\]](../Sources.md#^s151). Operators reverted to manual in Ukraine 2015 [\[146\]](../Sources.md#^s146) and Aliquippa 2023 [\[152\]](../Sources.md#^s152); Poland's operators and EDR limited impact [\[150\]](../Sources.md#^s150). |
| 5 | Sustain a large-scale, long outage (days+, multi-region) | 🔴 | Worst cases are hours [\[146\]](../Sources.md#^s146)[\[149\]](../Sources.md#^s149); Dragos's multi-site worst case is "hours, potentially a few days" [\[153\]](../Sources.md#^s153). GAO: scale "not well understood" [\[154\]](../Sources.md#^s154); NERC: no cyber outages on bulk-system equipment in 2024 [\[155\]](../Sources.md#^s155). |
| 6 | AI materially performs the OT steps | 🟡 | Single lab preprint: agents sustained physical objectives in 31.3% of PLC episodes, with access assumed [\[156\]](../Sources.md#^s156). Threat intel: productivity gains, no novel ICS capability [\[157\]](../Sources.md#^s157)[\[34\]](../Sources.md#^s34). |

## Also on record

- Government guidance: "the number of AI-enabled attacks on existing IT and OT systems" will increase; LLMs "almost certainly should not be used to make safety decisions" [\[158\]](../Sources.md#^s158).
- Oldsmar, Florida (2021): CISA advised that actors "obtained unauthorized access to the supervisory control and data acquisition (SCADA) system" [\[161\]](../Sources.md#^s161). In 2023 the FBI said it could not confirm the incident began with a cyber intrusion (press report). It is disputed and not used as evidence here.

## Not publicly knowable / not verified

- Classified assessments of adversary OT capability.
- The FBI's 2023 Oldsmar statement is known only through press; no official retraction of the CISA advisory was found.

## Sources

All sources are listed in [[Sources]]; citations here use its numbers.
