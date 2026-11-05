---
tags: [attack-path, ai-fud-whitepaper]
---
# G43 Dangerous, violent, or hateful content

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):**
- **Baseline:** offensive or hateful content reaches people and causes distress or reputational harm.
- **Maximal:** AI output facilitates or encourages real-world violence or self-harm.

**Path (baseline):**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | Input drives the model toward harmful content. Alternatives: coordinated adversarial users, a bad configuration or update, or ordinary prompting | 🟢 | Microsoft, "Learning from Tay's introduction", 25 Mar 2016, https://blogs.microsoft.com/blog/2016/03/25/learning-tays-introduction/: "a coordinated attack by a subset of people exploited a vulnerability in Tay". |
| 2 | AI generates hateful or violent content | 🟢 | Same source. xAI/Grok, @grok on X, 12 Jul 2025, https://x.com/grok/status/1943916977481036128: "we deeply apologize for the horrific behavior that many experienced"; the root cause was "an update to a code path upstream of the @grok bot," active 16 hours, that made it "susceptible to existing X user posts; including when such posts contained extremist views." |
| 3 | Content is published or reaches an audience | 🟢 | Tay posted publicly on Twitter (same source). |
| 4 | Harm to targets or audience | 🟢 | Same source: "deeply sorry for the unintended offensive and hurtful tweets". |

**Path (maximal):**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | Person with violent or self-harm intent uses AI | 🟢 (secondary) | Las Vegas police (LVMPD) said the Jan 2025 Cybertruck bomber used ChatGPT in planning. This research did not retrieve the primary briefing; secondary: https://npr.org/2025/01/07/nx-s1-5251611/cybertruck-explosion-las-vegas-chatgpt-ai |
| 2 | AI provides information or encouragement | 🟢 (secondary) | LVMPD on the Cybertruck bomber (same, secondary). Garcia v. Character Technologies does not count: its pleadings are allegations, and the 20 May 2025 order on the motions to dismiss (Doc. 115, M.D. Fla. 6:24-cv-1903; FIRE copy, https://www.fire.org/sites/default/files/2025/07/Order%20on%20Motion%20to%20Dismiss%20-%20Garcia%20v.%20Character%20Technologies%20Inc.pdf) takes them as true only to decide the motion. |
| 3 | AI output materially changes the person's capability or decision | 🔴 | No court or other on-the-record finding of causal contribution. The Garcia order lets negligence and product-liability claims proceed and is "not prepared to hold that Character A.I.'s output is speech"; it makes no finding of fact. |
| 4 | Violence or self-harm occurs | 🟢 | The events occurred; the AI's causal role is unestablished (step 3). |

**Weakest-link light:** 🟢 for the in-scope route (Tay). The other baseline routes (🟢) and the maximal path (🔴) are outside scope.

**In scope:** In. On the Tay route, step 1 is an integrity failure (attackers manipulating what the model learns; Microsoft says they "exploited a vulnerability"); only that route is analyzed. Outside scope: ordinary prompting, bad updates, and the maximal path, which need no security failure.

**Gaps:**
- The LVMPD and Palm Springs items are secondary only.
- No court has made findings on chatbot causation.