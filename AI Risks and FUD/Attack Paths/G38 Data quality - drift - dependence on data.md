---
tags: [attack-path, ai-fud-whitepaper]
---
# G38 Data quality / drift / dependence on data

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):** A model trained on unrepresentative or outdated data degrades in deployment. People act on wrong outputs, causing missed clinical diagnoses or financial loss.

**Path:**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | The deployment data diverges from the training data (site shift, population change, market regime change) or is poor quality | 🟢 | Finlayson et al., "The Clinician and Dataset Shift in AI," NEJM 385(3), 15 Jul 2021, DOI 10.1056/NEJMc2104626 (author copy https://samfinlayson.com/assets/dataset_shift/Finlayson_Dataset_Shift_NEJM.pdf): "changes in patients' demographic characteristics associated with the coronavirus disease 2019 pandemic." |
| 2 | Model performance degrades | 🟢 | Wong et al., JAMA Intern Med 181(8), 21 Jun 2021, https://jamanetwork.com/journals/jamainternalmedicine/fullarticle/2781313: Epic Sepsis Model AUC was 0.63, against the 0.76–0.83 Epic reported, and it missed 67% of sepsis cases (paraphrase). Finlayson: "the model had to be deactivated because of spurious alerting." |
| 3 | Decisions are made on the degraded outputs | 🟢 | Zillow Q3 2021 letter (SEC 8-K Ex. 99.1), 2 Nov 2021, https://www.sec.gov/Archives/edgar/data/1617640/000161764021000085/q32021991.htm: "the unpredictability in forecasting home prices far exceeds what we anticipated." Homes were bought above their estimated resale prices. |
| 4 | Harm: financial loss or missed or burdensome clinical care | 🟢 | Zillow: "a write-down of inventory of approximately $304 million," plus a ~25% workforce cut. Wong: alerts fired on 18% of all patients. Patient injury itself is not documented. |

**Path B (tampered data; the in-scope route):**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | An attacker alters data that a deployed model relies on (user feedback, user input, or shared intelligence data) | 🟢 | [\[247\]](../Sources.md#^s247): "we regularly see some of the most advanced spammer groups trying to throw the Gmail filter off-track" by "reporting massive amounts of spam emails as not spam," with "at least four malicious large-scale attempts to skew our classifier" between late Nov 2017 and early 2018. Microsoft, "Learning from Tay's introduction," 25 Mar 2016, https://blogs.microsoft.com/blog/2016/03/25/learning-tays-introduction/: "a coordinated attack by a subset of people exploited a vulnerability in Tay." |
| 2 | The system takes in the altered data without effective integrity checks | 🟢 | Tay learned from the coordinated input (same source). [\[247\]](../Sources.md#^s247) reports the Gmail attempts, not whether any succeeded. |
| 3 | Decisions or outputs degrade the way the attacker intended | 🟢 | Tay produced the offensive output its attackers steered it toward (same source). |
| 4 | Harm: wrong decisions or harmful output reach users | 🟢 | Tay's offensive tweets were published within its first day (same source). |

**Weakest-link light:** Path B (tampered data, in scope) 🟢. The natural-drift path above is 🟢 and outside scope.

**In scope:** In. Only Path B, tampered data, requires a security failure (integrity: data altered without authorization at step 1). Outside scope: natural drift and poor-quality data, which degrade outputs with no security failure; the first path's evidence is for these.

**Gaps:** Zillow's letter does not call the pricing model "ML" or "AI" in the quoted text. The Epic finding shows a site-level shift and spurious alerting, not documented patient deaths. Data poisoning is probably covered by a separate concern.
