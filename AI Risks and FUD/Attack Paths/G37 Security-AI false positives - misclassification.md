---
tags: [attack-path, ai-fud-whitepaper]
---
# G37 Security-AI false positives / misclassification

Back to [[RQ2 Screening Log]]

Path, lights, and scope call produced with AI assistance under the fixed method in the screening log. Quotes came through automated extraction; verify before citing.

**Harm (as claimed):** An AI security or surveillance control misclassifies. A false positive leads to wrongful accusation, search, exclusion or police contact. A false negative lets a threat through and causes physical harm.

**Path:**

| # | Step | Light | Evidence |
| --- | --- | --- | --- |
| 1 | An AI classifier is deployed as a security control (facial recognition for loss prevention; AI weapons screening) | 🟢 | FTC, Rite Aid press release, 19 Dec 2023 (archived copy, https://data.aclum.org/storage/2025/01/FTC_www_ftc_gov_news-events_news_press-releases_2023_12_rite-aid-banned-using-ai-facial-recognition-after-ftc-says-retailer-deployed-technology-without.pdf); FTC, Evolv press release, 26 Nov 2024, https://www.ftc.gov/news-events/news/press-releases/2024/11/ftc-takes-action-against-evolv-technologies-deceiving-users-about-its-ai-powered-security-screening. Deployment itself is not contested; both orders regulate it. |
| 2 | Misclassification. Alternatives: (a) benign person or item flagged; (b) real threat missed | 🔴 (allegation only) | Rite Aid: "thousands of false-positive matches." Evolv: "a 50% false alarm rate"; "failed to detect a seven-inch knife brought into a school in October 2022." All are FTC complaint allegations resolved by consent order without findings. |
| 3 | The output is acted on without effective human verification | 🔴 (allegation only) | Rite Aid: employees "followed consumers around its stores, searched them, ordered them to leave" (FTC allegation). Shared step SS10. |
| 4 | Harm: wrongful accusation or detention, or an attack that succeeds | 🔴 (allegation only) | Rite Aid: staff "called the police to confront or remove consumers." Evolv: the missed knife "was used to stab a student." Both as alleged by the FTC. Williams v. City of Detroit (facial-recognition wrongful arrest) settled in Jun 2024 with policy terms (ACLU one-pager, https://assets.aclu.org/live/uploads/2024/06/williams_settlement_one-pager_june_24-1.pdf); a settlement is not a finding. |

**Weakest-link light:** 🔴 (steps 2–4 rest on allegations)

**In scope:** Yes. A security failure is necessary at step 2, where an identification or detection control fails. For false positives this is an authentication/identification error that denies access to legitimate people; for false negatives it is an authorization/access-control failure that admits a weapon.

**Gaps:** Every harm source found is an allegation (FTC complaints, a civil suit) resolved by consent order or settlement. An on-the-record finding of an AI security control misclassifying and causing harm would move this concern. This research found no primary source for SOC/EDR alert-fatigue harms.