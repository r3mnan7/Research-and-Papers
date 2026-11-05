---
tags: [attack-path, ai-fud-whitepaper]
---
# G63 Financial-market and economic instability

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):** Baseline: algorithmic trading causes flash crashes. Maximal: widespread AI trading herds or colludes, amplifying shocks into systemic instability.

**Path (baseline, algorithmic, not AI):**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | An automated algorithm executes large orders | 🟢 | CFTC–SEC, *Findings Regarding the Market Events of May 6, 2010* (30 Sep 2010), https://www.sec.gov/files/marketevents-report.pdf: "automated execution algorithm" |
| 2 | The algorithm acts without regard to market conditions | 🟢 | Same: targeted 9% of volume "without regard to price or time" |
| 3 | Liquidity collapses and prices crash | 🟢 | Same (Flash Crash). Knight Capital $460M (SEC 2013) is a related operational case. |

**Path (AI-specific / maximal):**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | Similar autonomous AI trading models are widely deployed | 🔴 | Bank of England FPC, *Financial Stability in Focus: AI in the financial system* (Apr 2025), https://www.bankofengland.co.uk/-/media/boe/files/financial-stability-in-focus/2025/financial-stability-in-focus-artificial-intelligence-in-the-financial-system: "autonomous AI-based trading models do not yet appear to be in widespread production" |
| 2 | Models herd, correlate or collude. Alternatives: herding; tacit collusion; third-party or provider concentration failure | 🟡 | Dou, Goldstein, Ji, NBER WP 34054 (Jul 2025), https://econpapers.repec.org/paper/nbrnberwo/34054.htm: RL traders "autonomously sustain collusive supra-competitive profits" (simulation). FSB (14 Nov 2024), https://www.fsb.org/2024/11/fsb-assesses-the-financial-stability-implications-of-artificial-intelligence lists "third-party dependencies," "market correlations," "cyber risks" |
| 3 | Shocks are amplified into systemic instability | 🔴 | BoE: risk "acting in a similar way during a stress, thereby amplifying shocks"; "the practical implications are uncertain." No observed instance. |

**Weakest-link light:** Baseline 🟢 (but not AI); AI-specific / maximal 🔴

**In scope:** In. Only the third-party-concentration and cyber alternative in step 2 requires a security failure (availability); only that route is analyzed. Outside scope: the herding and collusion routes and the baseline crash route.

**Gaps:** The documented crashes involve simple rule-based algorithms, not AI or ML, so AI is not shown to be necessary for the baseline harm.
