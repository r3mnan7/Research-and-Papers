---
tags: [ai-fud-whitepaper]
---
# RQ3 Second Rating

Back to [[Addressing Fear, Uncertainty, and Doubt in the Security and Safety of Artificial Intelligence Models|main note]] · [[RQ3 Control Coverage]]

> [!note] Drafting and review
> Work in progress. Drafted with AI assistance (2026); the author's review is ongoing. See [[Methodology — Use of Generative AI]].

Second rating of [[RQ3 Control Coverage|RQ3]]'s step cells with AI assistance, November 4, 2026. This is the methodological control [[RQ2 Risk Classification|RQ2]] had (a blind second classification) and [[RQ3 Control Coverage|RQ3]] lacked.

## Procedure

1. Rater 2 read [[RQ3 Control Coverage|RQ3]] only through "How to Read" (method, assumption, abbreviations), the step lights in the G and S notes, and the control catalogs.
2. For each `#### Path` heading in [[RQ3 Control Coverage|RQ3]], a script printed only the heading and the first three table columns (#, Step, Light). The Controls and Verdict columns were not seen. Exceptions, recorded rather than hidden: (a) the [[G56 Existential risk - loss of control over advanced AI - superintelligenc|G56]]/[[G57 Misaligned AI goals (proxy gaming, goal drift, power-seeking, deceptio|G57]] table's third column *is* its controls column, so rater 1's controls for that row were seen (its verdicts were not); (b) [[G04 Model extraction - stealing - distillation|G04]]'s maximal path has no step table in [[RQ3 Control Coverage|RQ3]], so its steps were taken from the [[G04 Model extraction - stealing - distillation|G04]] note; (c) [[S02 Bio-chemical|S02]] and [[S04 Rogue AI|S04]] had no step tables when the blind rating was made, and their rater-1 tables were then written with AI assistance in Task 1 of the same session, so their second rating is not independent and is excluded from the agreement figures.
3. Each step was rated on [[RQ3 Control Coverage|RQ3]]'s scale (Bounded / Bounded within limits / Unbounded / Not an information-security step) and each path on [[RQ3 Control Coverage|RQ3]]'s path scale, citing controls from the catalogs only. The ratings below were written to this note before rater 1's verdicts were read.
4. Only then was the full [[RQ3 Control Coverage|RQ3]] read and the reconciliation below added.
5. **Contamination, disclosed.** Before rating, rater 2 also read the project's working to-do list, which records two of rater 1's conventions: that all six Class D rows read "within the granted scope," and that RAG poisoning was marked "partial" for untrusted corpora. Rater 2 did not see any step-level verdict. Rater 1 is the author: the verdicts in [[RQ3 Control Coverage|RQ3]] are the author's ratings, entered into the note with AI assistance. Rater 2 is an AI agent. (Corrected November 4, 2026; an earlier version of this item said both raters were Claude.)

## Blind ratings

### G01 · Baseline path (🟢)

| # | Step | Rater 2 verdict | Rater 2 controls |
| --- | --- | --- | --- |
| 1 | The attacker places data where the model will take it in | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^ac-3\|AC-3]]; CIS: [[CIS Controls v8.1 Catalog#^cis-3-3\|3.3]]. Limit: only sources the operator controls; public web and user feedback stay writable by anyone. |
| 2 | The pipeline takes in the data without integrity checks | **Bounded** | 53: [[NIST SP 800-53 Rev 5 Catalog#^si-7\|SI-7]], [[NIST SP 800-53 Rev 5 Catalog#^si-10\|SI-10]]; 161: [[NIST SP 800-161r1 Catalog#^161-sr-4\|SR-4]] |
| 3 | Model behavior shifts the way the attacker intended | **Unbounded** | None outside the model. |
| 4 | The changed output reaches users or decisions | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^si-15\|SI-15]], [[NIST SP 800-53 Rev 5 Catalog#^ac-6\|AC-6]]. Limit: output checks catch only content they can recognize; actions capped at the grant. |

**Path (rater 2):** **Contained** at step 2 (integrity and validation of ingested data).

### G01 · Maximal path: web-scale pre-training (🔴)

| # | Step | Rater 2 verdict | Rater 2 controls |
| --- | --- | --- | --- |
| 1 | The attacker injects poison into a web-scale pre-training corpus | **Unbounded** | None: the attacker writes to the public web. |
| 2 | A frontier developer trains on the corpus without filtering it | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^si-7\|SI-7]], [[NIST SP 800-53 Rev 5 Catalog#^si-10\|SI-10]]; 161: [[NIST SP 800-161r1 Catalog#^161-sr-4\|SR-4]]. Limit: snapshot hashes stop split-view changes; validation catches only poison it can recognize. |
| 3 | The poisoned behavior shows up in the deployed model | **Unbounded** | 53: [[NIST SP 800-53 Rev 5 Catalog#^sa-11\|SA-11]] testing finds only what it tests for; not a bound. |
| 4 | The behavior causes serious downstream harm | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^ac-6\|AC-6]], [[NIST SP 800-53 Rev 5 Catalog#^si-15\|SI-15]]. Limit: the grant. |

**Path (rater 2):** **Contained within the granted scope** (step 4); step 2 is a partial upstream check.

### G02 · Path (🔴)

| # | Step | Rater 2 verdict | Rater 2 controls |
| --- | --- | --- | --- |
| 1 | The attacker plants a backdoor | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^sr-5\|SR-5]], [[NIST SP 800-53 Rev 5 Catalog#^sr-6\|SR-6]]. Limit: contracts and supplier review do not bound a malicious or compromised supplier. |
| 2 | The victim obtains and deploys the backdoored model | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^sr-4\|SR-4]], [[NIST SP 800-53 Rev 5 Catalog#^cm-14\|CM-14]], [[NIST SP 800-53 Rev 5 Catalog#^si-7-15\|SI-7(15)]]. Limit: establishes origin and integrity, not behavior. |
| 3 | The backdoor gets past evaluation and safety training | **Unbounded** | None outside the model. |
| 4 | The trigger is presented and the hidden behavior runs | **Unbounded** | None: the trigger is ordinary input. |
| 5 | The triggered behavior causes harm in deployment | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^ac-6\|AC-6]], [[NIST SP 800-53 Rev 5 Catalog#^si-15\|SI-15]]. Limit: the grant. |

**Path (rater 2):** **Contained within the granted scope** (step 5).

### G03 · Baseline path (🟢)

| # | Step | Rater 2 verdict | Rater 2 controls |
| --- | --- | --- | --- |
| 1 | The attacker probes or learns how the deployed classifier behaves | **Bounded within limits** | ASVS: [[OWASP ASVS 5.0.0 Catalog#^asvs-2-4-1\|2.4.1]]; 53: [[NIST SP 800-53 Rev 5 Catalog#^si-4\|SI-4]]. Limit: a query budget; offline surrogates and transfer attacks need no queries. |
| 2 | The attacker crafts an evasive input | **Unbounded** | None: done on the attacker's side. |
| 3 | The model misclassifies, and the detection or control is bypassed | **Unbounded** | None outside the model. |
| 4 | The attacker gets the fraud, abuse, or delivery they wanted | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^sc-29\|SC-29]], [[NIST SP 800-53 Rev 5 Catalog#^si-4\|SI-4]]. Limit: only where an independent, non-model control covers the same decision. |

**Path (rater 2):** **Contained within limits** (step 4, independent control layer; step 1 only raises cost).

### G03 · Maximal path M1–M3 (🔴)

| # | Step | Rater 2 verdict | Rater 2 controls |
| --- | --- | --- | --- |
| M1–M3 | Physical perturbation → perception model misclassifies → physical harm | **Unbounded** | 53: [[NIST SP 800-53 Rev 5 Catalog#^si-17\|SI-17]] acts only on an *indicated* failure; a misperception is not indicated. |

**Path (rater 2):** **Not contained** by information-security controls.

### G04 · Baseline path, in-scope routes (🟡)

| # | Step | Rater 2 verdict | Rater 2 controls |
| --- | --- | --- | --- |
| 1 | Query access through fraudulent accounts or proxies | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^ac-2\|AC-2]]; 63: [[NIST SP 800-63-4 Requirements Extraction#SP 800-63A-4 Identity Proofing and Enrollment\|63A-4]]. Limit: proofing raises the cost of fake accounts; it does not prevent them. |
| 2 | Systematic high-volume querying | **Bounded within limits** | ASVS: [[OWASP ASVS 5.0.0 Catalog#^asvs-2-4-1\|2.4.1]]; 53: [[NIST SP 800-53 Rev 5 Catalog#^sc-6\|SC-6]]. Limit: the quota. |
| 3 | Parameters are recovered from returned confidence scores | **Bounded** | ASVS: [[OWASP ASVS 5.0.0 Catalog#^asvs-15-3-1\|15.3.1]]; 53: [[NIST SP 800-53 Rev 5 Catalog#^si-15\|SI-15]] (return labels, not scores). |
| 4 | The copied capability is used or released | Not an information-security step | IP loss after the fact. |

**Path (rater 2):** **Contained** at step 3.

### G04 · Maximal path (🔴; steps 1–3 as baseline, then 4–5 from [[G04 Model extraction - stealing - distillation]])

| # | Step | Rater 2 verdict | Rater 2 controls |
| --- | --- | --- | --- |
| 1–3 | As baseline | **Bounded** | As baseline; step 3 bounded. |
| 4 | Distilled model lacks safeguards | Not an information-security step | The attacker's own model; outside the victim's system. |
| 5 | It is used for offensive cyber or other national-security harm | Not an information-security step | Harm meets its victims' own controls; not this system's. |

**Path (rater 2):** **Contained** at step 3. *Not rated from [[RQ3 Control Coverage|RQ3]]: [[RQ3 Control Coverage|RQ3]] has no step table for this path; steps taken from the [[G04 Model extraction - stealing - distillation|G04]] note.*

### G06 · Path (🟡)

| # | Step | Rater 2 verdict | Rater 2 controls |
| --- | --- | --- | --- |
| 1 | The model is trained on data where membership itself is sensitive | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^si-12-1\|SI-12(1)]]. Limit: minimization only where the sensitive set is not the training purpose. |
| 2 | The attacker gets query or output access | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^ac-3\|AC-3]]; ASVS: [[OWASP ASVS 5.0.0 Catalog#^asvs-2-4-1\|2.4.1]]. Limit: authorized users keep access. |
| 3 | The attacker runs membership inference and determines membership | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^si-19-6\|SI-19(6)]]. Limit: the privacy parameter (ε). |

**Path (rater 2):** **Contained within limits** (step 3, differential-privacy bound).

### G07 · Gradient route (🟡)

| # | Step | Rater 2 verdict | Rater 2 controls |
| --- | --- | --- | --- |
| 1 | The model memorizes sensitive training data | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^si-19-6\|SI-19(6)]]. Limit: ε. |
| 2 | The attacker gets gradient access | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^sc-8\|SC-8]], [[NIST SP 800-53 Rev 5 Catalog#^ac-3\|AC-3]]. Limit: stops an eavesdropper, not the aggregating server, which receives updates by design. |
| 3 | The attacker reconstructs the data | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^si-19-6\|SI-19(6)]]. Limit: ε. |

**Path (rater 2):** **Contained within limits** (step 2 for eavesdroppers; step 3 privacy bound for the server).

### G07 · Query route (🟡)

| # | Step | Rater 2 verdict | Rater 2 controls |
| --- | --- | --- | --- |
| 1 | The model memorizes sensitive training data | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^si-19-6\|SI-19(6)]], [[NIST SP 800-53 Rev 5 Catalog#^si-12-1\|SI-12(1)]]. Limit: ε; minimization. |
| 2 | The attacker gets query access | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^ac-3\|AC-3]]; ASVS: [[OWASP ASVS 5.0.0 Catalog#^asvs-2-4-1\|2.4.1]]. Limit: authorized users keep access. |
| 3 | The model emits memorized data | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^si-15\|SI-15]]. Limit: output filters catch recognizable patterns only. |

**Path (rater 2):** **Contained within limits** (steps 1 and 3).

### G08 · Path (🟡)

| #   | Step                                                                           | Rater 2 verdict           | Rater 2 controls                                                                                                                                                   |
| --- | ------------------------------------------------------------------------------ | ------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 1   | The attacker gets query or white-box access                                    | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^ac-3\|AC-3]], [[NIST SP 800-53 Rev 5 Catalog#^sc-28\|SC-28]]. Limit: white-box access is blocked; query access is the service. |
| 2   | The attacker infers dataset properties or characterises the model              | **Unbounded**             | None: differential privacy protects records, not dataset-level properties.                                                                                         |
| 3   | The inferred information is disclosed harmfully or used for a follow-on attack | **Bounded within limits** | Follow-on attacks meet their own paths' controls; disclosure itself is not bounded.                                                                                |

**Path (rater 2):** **Contained within limits** (step 1, white-box route only).

### G09 · Path (🟡)

| # | Step | Rater 2 verdict | Rater 2 controls |
| --- | --- | --- | --- |
| 1 | The attacker gets the embeddings | **Bounded** | 53: [[NIST SP 800-53 Rev 5 Catalog#^ac-3\|AC-3]], [[NIST SP 800-53 Rev 5 Catalog#^sc-28\|SC-28]]; ASVS: [[OWASP ASVS 5.0.0 Catalog#^asvs-15-3-1\|15.3.1]]; CIS: [[CIS Controls v8.1 Catalog#^cis-3-3\|3.3]] |
| 2 | The attacker has or trains an inversion model | **Unbounded** | None: attacker-side. |
| 3 | The source text is recovered | **Unbounded** | None outside the model. |

**Path (rater 2):** **Contained** at step 1.

### G10 · Path (🟢)

| # | Step | Rater 2 verdict | Rater 2 controls |
| --- | --- | --- | --- |
| 1 | The attacker gets direct input access to the model | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^ac-2\|AC-2]], [[NIST SP 800-53 Rev 5 Catalog#^ia-2\|IA-2]]. Limit: decides who may prompt, not what they send. |
| 2 | The attacker writes input that gets past safety training or operator restrictions ([[RQ2 Screening Log#Shared steps\|SS1]]) | **Unbounded** | None outside the model. |
| 3 | The model produces the restricted output or takes the restricted actions | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^ac-3\|AC-3]], [[NIST SP 800-53 Rev 5 Catalog#^ac-6\|AC-6]], [[NIST SP 800-53 Rev 5 Catalog#^si-15\|SI-15]]. Limit: actions capped at the grant; text output only as far as filters recognize it. |
| 4 | (Maximal) The output or actions cause harm to a victim | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^sc-7-5\|SC-7(5)]], [[NIST SP 800-53 Rev 5 Catalog#^ac-6\|AC-6]]. Limit: the grant and egress policy. |

**Path (rater 2):** **Contained within the granted scope** (step 3).

### G11 · Path (🟢 qualified)

| # | Step | Rater 2 verdict | Rater 2 controls |
| --- | --- | --- | --- |
| 1 | The attacker plants instructions in content the AI will ingest | **Unbounded** | None: the content is public or third-party. |
| 2 | The victim's AI pulls that content into the same context as its trusted instructions | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^ac-4\|AC-4]]. Limit: a whitelist of sources removes function. |
| 3 | The model treats the injected text as instructions | **Unbounded** | None outside the model. |
| 4 | The agent uses a tool or output channel to carry out the harmful action | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^ac-6\|AC-6]], [[NIST SP 800-53 Rev 5 Catalog#^ac-3-2\|AC-3(2)]]; ASVS: [[OWASP ASVS 5.0.0 Catalog#^asvs-8-3-3\|8.3.3]]. Limit: the grant. |

**Path (rater 2):** **Contained within the granted scope** (step 4).

### G14 · Path (🟢)

| # | Step | Rater 2 verdict | Rater 2 controls |
| --- | --- | --- | --- |
| 1 | The agent holds privileges or long-lived credentials beyond what the task needs | **Bounded** | 53: [[NIST SP 800-53 Rev 5 Catalog#^ac-6\|AC-6]], [[NIST SP 800-53 Rev 5 Catalog#^ia-5\|IA-5]]; CIS: [[CIS Controls v8.1 Catalog#^cis-6-8\|6.8]] |
| 2 | Control passes to an attacker, or the agent errs | **Unbounded** | None for model error. |
| 3 | The AI uses those privileges for actions outside the intended task | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^ac-3\|AC-3]]. Limit: the grant. |
| 4 | Harm results | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^ac-6\|AC-6]]. Limit: the grant. |

**Path (rater 2):** **Contained** at step 1.

### G16 · Path (🟢)

| # | Step | Rater 2 verdict | Rater 2 controls |
| --- | --- | --- | --- |
| 1 | The agent is connected to tools with real-world effects | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^cm-7\|CM-7]], [[NIST SP 800-53 Rev 5 Catalog#^ac-6\|AC-6]]. Limit: tools the task needs remain. |
| 2 | The attacker coerces tool selection or parameters | **Unbounded** | None for the jailbreak and injection routes (53: [[NIST SP 800-53 Rev 5 Catalog#^si-7\|SI-7]] covers only the poisoned-description route). |
| 3 | The AI calls its tools with harmful parameters | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^si-10\|SI-10]], [[NIST SP 800-53 Rev 5 Catalog#^ac-3-2\|AC-3(2)]]; ASVS: [[OWASP ASVS 5.0.0 Catalog#^asvs-8-3-3\|8.3.3]]. Limit: parameters that are valid but harmful pass. |
| 4 | Harm results | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^ac-6\|AC-6]]. Limit: the grant. |

**Path (rater 2):** **Contained within the granted scope** (step 3).

### G18 · Path (🟡)

| # | Step | Rater 2 verdict | Rater 2 controls |
| --- | --- | --- | --- |
| 1 | Attacker content reaches the assistant | **Unbounded** | None: content accepted by design. |
| 2 | The AI writes the attacker's instruction or false fact into persistent memory | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^ac-3\|AC-3]], [[NIST SP 800-53 Rev 5 Catalog#^si-7\|SI-7]]. Limit: write permission and change detection, not the truth of what is written. |
| 3 | The poisoned memory is retrieved in a later session and changes behavior | **Unbounded** | None outside the model. |
| 4 | Harm: biased recommendations, or ongoing exfiltration | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^ac-4\|AC-4]], [[NIST SP 800-53 Rev 5 Catalog#^sc-7-10\|SC-7(10)]]. Limit: exfiltration bounded; biased advice is not. |

**Path (rater 2):** **Contained within the granted scope** (step 4, exfiltration route).

### G24 · Path A (denial of wallet)

| # | Step | Rater 2 verdict | Rater 2 controls |
| --- | --- | --- | --- |
| A1 | The attacker gains the ability to run inference billed to the victim | **Bounded** | 53: [[NIST SP 800-53 Rev 5 Catalog#^ia-2\|IA-2]], [[NIST SP 800-53 Rev 5 Catalog#^ia-5\|IA-5]]; ASVS: [[OWASP ASVS 5.0.0 Catalog#^asvs-13-3-1\|13.3.1]] |
| A2 | The victim has no effective spend or quota cap | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^sc-6\|SC-6]]; ASVS: [[OWASP ASVS 5.0.0 Catalog#^asvs-2-4-1\|2.4.1]]. Limit: the cap amount. |

**Path (rater 2):** **Contained** at step A1.

### G24 · Path B (DoS and resource-heavy inputs)

| # | Step | Rater 2 verdict | Rater 2 controls |
| --- | --- | --- | --- |
| B1 | Abnormal-volume traffic or resource-heavy (sponge) queries | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^sc-5\|SC-5]]; ASVS: [[OWASP ASVS 5.0.0 Catalog#^asvs-2-4-1\|2.4.1]]. Limit: per-request cost caps for sponge inputs. |
| B2 | Capacity and rate limiting do not absorb it | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^sc-5\|SC-5]], [[NIST SP 800-53 Rev 5 Catalog#^sc-6\|SC-6]]. Limit: provisioned capacity. |
| B3 | Legitimate users lose service | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^sc-6\|SC-6]], [[NIST SP 800-53 Rev 5 Catalog#^cp-10\|CP-10]]. Limit: priority allocation and recovery time. |

**Path (rater 2):** **Contained within limits** (step B1).

### G27 · Poisoning path (🟡)

| # | Step | Rater 2 verdict | Rater 2 controls |
| --- | --- | --- | --- |
| 1 | The attacker places content in a corpus the retriever indexes | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^ac-3\|AC-3]]; CIS: [[CIS Controls v8.1 Catalog#^cis-3-3\|3.3]]. Limit: curated corpora only. |
| 2 | The retriever selects the poisoned chunk for the target query | **Unbounded** | None outside the model. |
| 3 | The model treats the retrieved text as authoritative or as instructions | **Unbounded** | None outside the model. |
| 4 | A harmful answer or action reaches the user or attacker | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^ac-6\|AC-6]], [[NIST SP 800-53 Rev 5 Catalog#^si-15\|SI-15]]. Limit: the grant. |

**Path (rater 2):** **Contained within limits** (step 1, curated corpora); otherwise within the granted scope.

### G27 · Cross-boundary leakage path (🟡)

| # | Step | Rater 2 verdict | Rater 2 controls |
| --- | --- | --- | --- |
| 1 | The attacker places instructions in content the retriever indexes | **Unbounded** | None for public content. |
| 2 | Retrieval pulls data from a scope the attacker cannot access | **Bounded** | ASVS: [[OWASP ASVS 5.0.0 Catalog#^asvs-8-3-3\|8.3.3]], [[OWASP ASVS 5.0.0 Catalog#^asvs-8-2-2\|8.2.2]]; 53: [[NIST SP 800-53 Rev 5 Catalog#^ac-3\|AC-3]] |
| 3 | The data reaches the attacker | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^ac-4\|AC-4]], [[NIST SP 800-53 Rev 5 Catalog#^sc-7-10\|SC-7(10)]]. Limit: egress policy. |

**Path (rater 2):** **Contained** at step 2.

### G27 · Retrieval jamming path (🟡)

| # | Step | Rater 2 verdict | Rater 2 controls |
| --- | --- | --- | --- |
| 1 | The attacker adds a document to a corpus the retriever indexes | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^ac-3\|AC-3]]. Limit: curated corpora only. |
| 2 | A crafted blocker document is retrieved and makes the system refuse | **Unbounded** | None outside the model. |
| 3 | Legitimate users lose answers to targeted questions | **Unbounded** | None: no availability control sees a refusal as an outage. |

**Path (rater 2):** **Contained within limits** (step 1).

### G27 · Semantic-cache poisoning path (🟡)

| # | Step | Rater 2 verdict | Rater 2 controls |
| --- | --- | --- | --- |
| 1 | The attacker submits queries to a service that caches answers by embedding similarity | **Bounded within limits** | ASVS: [[OWASP ASVS 5.0.0 Catalog#^asvs-2-4-1\|2.4.1]]. Limit: the query budget. |
| 2 | A crafted query collides with a victim's cache key | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^sc-4\|SC-4]]. Limit: prevents cross-user or cross-tenant transfer only if the cache is partitioned; a deliberately shared cache is not. |
| 3 | Harmful or wrong answers reach users or agents | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^ac-6\|AC-6]]. Limit: the grant. |

**Path (rater 2):** **Contained within limits** (step 2).

### G41 · Path, route (b) (🟡)

| # | Step | Rater 2 verdict | Rater 2 controls |
| --- | --- | --- | --- |
| 1 | AI perception or planning controls physical actuators | Not an information-security step | A design fact. |
| 2 | An adversarial physical perturbation causes misperception | **Unbounded** | None outside the model. |
| 3 | The fallback fails | Not an information-security step | Safety fallback; 53: [[NIST SP 800-53 Rev 5 Catalog#^si-17\|SI-17]] acts only on an indicated failure. |
| 4 | Physical harm | Not an information-security step | Physical consequence. |

**Path (rater 2):** **Not contained** by information-security controls.

### G42 · Path, jailbreak route (🔴)

| # | Step | Rater 2 verdict | Rater 2 controls |
| --- | --- | --- | --- |
| 2 | The actor gets the model past its CBRN-specific safeguards | **Unbounded** | As [[G10 Direct prompt injection - jailbreak\|G10]] step 2. |
| 3–5 | Materials, production, delivery | Not an information-security step | Physical and material barriers. |

**Path (rater 2):** **Not contained** by information-security controls (barriers at 3–5 are outside them).

### G43 · Path, Tay route (🟢)

| # | Step | Rater 2 verdict | Rater 2 controls |
| --- | --- | --- | --- |
| 1 | Coordinated adversarial users drive what a live-learning model learns | **Bounded** | 53: [[NIST SP 800-53 Rev 5 Catalog#^cm-3\|CM-3]], [[NIST SP 800-53 Rev 5 Catalog#^si-10\|SI-10]] (model updates are configuration-controlled changes). |
| 2 | The AI generates the harmful content | **Unbounded** | None outside the model. |
| 3 | Content is published or reaches an audience | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^si-15\|SI-15]]. Limit: filter coverage. |
| 4 | Harm | Not an information-security step | Social harm. |

**Path (rater 2):** **Contained** at step 1.

### G44 · Path, hosted-service route (🟢)

| # | Step | Rater 2 verdict | Rater 2 controls |
| --- | --- | --- | --- |
| 2 | The offender gets a hosted service to generate what its safeguards prohibit | **Unbounded** | As [[G10 Direct prompt injection - jailbreak\|G10]] step 2. |
| 3 | The model generates the imagery | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^si-15\|SI-15]]. Limit: output-classifier coverage. |
| 4–5 | Sharing and harm | Not an information-security step | Outside the service. |

**Path (rater 2):** **Contained within limits** (step 3).

### G56/G57 · Kinds of step (🔴; goal step 🟡) — *not fully blind: RQ3's third column here is the controls column, which the extraction showed*

| # | Step | Rater 2 verdict | Rater 2 controls |
| --- | --- | --- | --- |
| — | The model holds a goal of its own ([[RQ2 Screening Log#Shared steps\|SS5]]) | **Unbounded** | None outside the model. |
| — | The model reaches beyond its isolation | **Bounded** | 53: [[NIST SP 800-53 Rev 5 Catalog#^sc-7-5\|SC-7(5)]], [[NIST SP 800-53 Rev 5 Catalog#^sc-39\|SC-39]] |
| — | The model's weights leave the operator's control | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^sc-28\|SC-28]], [[NIST SP 800-53 Rev 5 Catalog#^sc-7-10\|SC-7(10)]]. Limit: the weight-security level achieved. |
| — | The model's actions go undetected ([[RQ2 Screening Log#Shared steps\|SS6]], [[RQ2 Screening Log#Shared steps\|SS7]]) | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^au-9-2\|AU-9(2)]], [[NIST SP 800-53 Rev 5 Catalog#^si-4\|SI-4]]. Limit: detection coverage. |
| — | Operators cannot stop it | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^ir-3\|IR-3]], [[NIST SP 800-53 Rev 5 Catalog#^pe-10\|PE-10]]. Limit: tested scenarios; power-off only on operator-controlled compute. |

**Path (rater 2):** **Contained** at the isolation step.

### S01 · Indirect path (steps 4–7)

| # | Step | Rater 2 verdict | Rater 2 controls |
| --- | --- | --- | --- |
| 4 | A false or manipulated warning reaches decision-makers | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^si-7\|SI-7]], [[NIST SP 800-53 Rev 5 Catalog#^sc-8\|SC-8]]. Limit: protects the warning data in transit and at rest, not its correctness. |
| 5 | Cyber or AI is the cause of the false warning | **Bounded within limits** | Poisoning route as [[G01 Training data - model poisoning\|G01]] baseline (53: [[NIST SP 800-53 Rev 5 Catalog#^si-7\|SI-7]]); adversarial-input route as [[G03 Evasion - adversarial inputs\|G03]] (unbounded). |
| 6 | The second, independent sensor fails to contradict it | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^sc-29\|SC-29]]. Limit: independence of the sensors. |
| 7 | Leaders authorize use on corrupted information | Not an information-security step | Human decision. |

**Path (rater 2):** **Contained within limits** (step 6, heterogeneous sensing).

### S06 · Cyber path

| # | Step | Rater 2 verdict | Rater 2 controls |
| --- | --- | --- | --- |
| 1 | Compromise of a shared AI model or provider | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^sr-6\|SR-6]], [[NIST SP 800-53 Rev 5 Catalog#^sa-9\|SA-9]]; 161: [[NIST SP 800-161r1 Catalog#^161-sr-4\|SR-4]]. Limit: as [[G02 Backdoors - hidden learned functionality\|G02]], origin not behavior. |
| 2 | A cyber event at a systemic financial node | **Bounded within limits** | 53: [[NIST SP 800-53 Rev 5 Catalog#^sc-29\|SC-29]], [[NIST SP 800-53 Rev 5 Catalog#^ir-4\|IR-4]]. Limit: concentration on one provider. |
| 3 | Propagation into a disorderly crash | Not an information-security step | Market dynamics. |
| 4 | Circuit breakers and recovery are defeated | **Bounded** | 53: [[NIST SP 800-53 Rev 5 Catalog#^cp-9\|CP-9]], [[NIST SP 800-53 Rev 5 Catalog#^cp-10\|CP-10]]; CIS: [[CIS Controls v8.1 Catalog#^cis-11-4\|11.4]] |

**Path (rater 2):** **Contained** at step 4.

## Reconciliation

Everything below was written after rater 1's verdicts in [[RQ3 Control Coverage]] were read. [[RQ3 Control Coverage|RQ3]]'s verdicts were not changed.

### How rater 1's cells were coded

Rater 1's Verdict cells are prose, so each was coded to the four values. Most are a single value. Fourteen cells give different values for different routes (for example "Bounded (curated corpus); Unbounded (open sources)"). These were coded two ways. **Strict (primary):** the weakest value in the cell. **Lenient (sensitivity check):** a cell mixing a bounded route and an unbounded route codes as Bounded within limits, which is how rater 2 wrote the same situations. Other codings: "—" and "Not security steps" are Not an information-security step; "Bounded by the target's controls" and "Bounded by an established non-IT control" are Bounded; "Detected, then removed at step 1" and "Bounded within capacity" are Bounded within limits. Excluded from the comparison: [[G03 Evasion - adversarial inputs|G03]]'s M1–M3 row (rater 1 marked it "Not assessed"); [[G04 Model extraction - stealing - distillation|G04]] maximal steps 1–3 (both raters wrote "as baseline"); [[S02 Bio-chemical|S02]] and [[S04 Rogue AI|S04]] (see Procedure, item 2c). That leaves **102 step cells on 29 paths**.

### Step-level reconciliation

| Path | Step | Rater 1 (strict) | Rater 1 (lenient) | Rater 2 | Agree (strict)? |
| --- | --- | --- | --- | --- | --- |
| [[G01 Training data - model poisoning\|G01]] baseline | 1 | Within limits | Within limits | Within limits | yes |
| [[G01 Training data - model poisoning\|G01]] baseline | 2 | Bounded | Bounded | Bounded | yes |
| [[G01 Training data - model poisoning\|G01]] baseline | 3 | Unbounded | Unbounded | Unbounded | yes |
| [[G01 Training data - model poisoning\|G01]] baseline | 4 | Within limits | Within limits | Within limits | yes |
| [[G01 Training data - model poisoning\|G01]] web-scale | 1 | Within limits | Within limits | Unbounded | **no** |
| [[G01 Training data - model poisoning\|G01]] web-scale | 2 | Unbounded | Unbounded | Within limits | **no** |
| [[G01 Training data - model poisoning\|G01]] web-scale | 3 | Unbounded | Unbounded | Unbounded | yes |
| [[G01 Training data - model poisoning\|G01]] web-scale | 4 | Within limits | Within limits | Within limits | yes |
| [[G02 Backdoors - hidden learned functionality\|G02]] | 1 | Unbounded | Within limits | Within limits | **no** |
| [[G02 Backdoors - hidden learned functionality\|G02]] | 2 | Unbounded | Within limits | Within limits | **no** |
| [[G02 Backdoors - hidden learned functionality\|G02]] | 3 | Unbounded | Unbounded | Unbounded | yes |
| [[G02 Backdoors - hidden learned functionality\|G02]] | 4 | Unbounded | Unbounded | Unbounded | yes |
| [[G02 Backdoors - hidden learned functionality\|G02]] | 5 | Within limits | Within limits | Within limits | yes |
| [[G03 Evasion - adversarial inputs\|G03]] baseline | 1 | Within limits | Within limits | Within limits | yes |
| [[G03 Evasion - adversarial inputs\|G03]] baseline | 2 | Unbounded | Unbounded | Unbounded | yes |
| [[G03 Evasion - adversarial inputs\|G03]] baseline | 3 | Unbounded | Unbounded | Unbounded | yes |
| [[G03 Evasion - adversarial inputs\|G03]] baseline | 4 | Within limits | Within limits | Within limits | yes |
| [[G04 Model extraction - stealing - distillation\|G04]] baseline | 1 | Within limits | Within limits | Within limits | yes |
| [[G04 Model extraction - stealing - distillation\|G04]] baseline | 2 | Within limits | Within limits | Within limits | yes |
| [[G04 Model extraction - stealing - distillation\|G04]] baseline | 3 | Bounded | Bounded | Bounded | yes |
| [[G04 Model extraction - stealing - distillation\|G04]] baseline | 4 | Not infosec | Not infosec | Not infosec | yes |
| [[G04 Model extraction - stealing - distillation\|G04]] maximal | 4 | Not infosec | Not infosec | Not infosec | yes |
| [[G04 Model extraction - stealing - distillation\|G04]] maximal | 5 | Not infosec | Not infosec | Not infosec | yes |
| [[G06 Membership inference\|G06]] | 1 | Within limits | Within limits | Within limits | yes |
| [[G06 Membership inference\|G06]] | 2 | Within limits | Within limits | Within limits | yes |
| [[G06 Membership inference\|G06]] | 3 | Within limits | Within limits | Within limits | yes |
| [[G07 Training-data reconstruction - extraction - memorization\|G07]] gradient | 1 | Within limits | Within limits | Within limits | yes |
| [[G07 Training-data reconstruction - extraction - memorization\|G07]] gradient | 2 | Within limits | Within limits | Within limits | yes |
| [[G07 Training-data reconstruction - extraction - memorization\|G07]] gradient | 3 | Within limits | Within limits | Within limits | yes |
| [[G07 Training-data reconstruction - extraction - memorization\|G07]] query | 1 | Within limits | Within limits | Within limits | yes |
| [[G07 Training-data reconstruction - extraction - memorization\|G07]] query | 2 | Within limits | Within limits | Within limits | yes |
| [[G07 Training-data reconstruction - extraction - memorization\|G07]] query | 3 | Unbounded | Within limits | Within limits | **no** |
| [[G08 Property inference - model characterisation (recon)\|G08]] | 1 | Within limits | Within limits | Within limits | yes |
| [[G08 Property inference - model characterisation (recon)\|G08]] | 2 | Unbounded | Unbounded | Unbounded | yes |
| [[G08 Property inference - model characterisation (recon)\|G08]] | 3 | Unbounded | Unbounded | Within limits | **no** |
| [[G09 Embedding inversion\|G09]] | 1 | Bounded | Bounded | Bounded | yes |
| [[G09 Embedding inversion\|G09]] | 2 | Unbounded | Unbounded | Unbounded | yes |
| [[G09 Embedding inversion\|G09]] | 3 | Unbounded | Unbounded | Unbounded | yes |
| [[G10 Direct prompt injection - jailbreak\|G10]] | 1 | Within limits | Within limits | Within limits | yes |
| [[G10 Direct prompt injection - jailbreak\|G10]] | 2 | Unbounded | Unbounded | Unbounded | yes |
| [[G10 Direct prompt injection - jailbreak\|G10]] | 3 | Within limits | Within limits | Within limits | yes |
| [[G10 Direct prompt injection - jailbreak\|G10]] | 4 | Bounded | Bounded | Within limits | **no** |
| [[G11 Indirect prompt injection - goal hijack\|G11]] | 1 | Unbounded | Within limits | Unbounded | yes |
| [[G11 Indirect prompt injection - goal hijack\|G11]] | 2 | Within limits | Within limits | Within limits | yes |
| [[G11 Indirect prompt injection - goal hijack\|G11]] | 3 | Unbounded | Unbounded | Unbounded | yes |
| [[G11 Indirect prompt injection - goal hijack\|G11]] | 4 | Within limits | Within limits | Within limits | yes |
| [[G14 Excessive agency - privilege - credentials\|G14]] | 1 | Bounded | Bounded | Bounded | yes |
| [[G14 Excessive agency - privilege - credentials\|G14]] | 2 | Unbounded | Within limits | Unbounded | yes |
| [[G14 Excessive agency - privilege - credentials\|G14]] | 3 | Within limits | Within limits | Within limits | yes |
| [[G14 Excessive agency - privilege - credentials\|G14]] | 4 | Within limits | Within limits | Within limits | yes |
| [[G16 Tool misuse - coerced tool use\|G16]] | 1 | Bounded | Bounded | Within limits | **no** |
| [[G16 Tool misuse - coerced tool use\|G16]] | 2 | Unbounded | Within limits | Unbounded | yes |
| [[G16 Tool misuse - coerced tool use\|G16]] | 3 | Within limits | Within limits | Within limits | yes |
| [[G16 Tool misuse - coerced tool use\|G16]] | 4 | Within limits | Within limits | Within limits | yes |
| [[G18 Memory & context poisoning (persistent)\|G18]] | 1 | Unbounded | Unbounded | Unbounded | yes |
| [[G18 Memory & context poisoning (persistent)\|G18]] | 2 | Within limits | Within limits | Within limits | yes |
| [[G18 Memory & context poisoning (persistent)\|G18]] | 3 | Within limits | Within limits | Unbounded | **no** |
| [[G18 Memory & context poisoning (persistent)\|G18]] | 4 | Within limits | Within limits | Within limits | yes |
| [[G24 Resource exhaustion - denial of wallet - DoS\|G24]] A | A1 | Bounded | Bounded | Bounded | yes |
| [[G24 Resource exhaustion - denial of wallet - DoS\|G24]] A | A2 | Bounded | Bounded | Within limits | **no** |
| [[G24 Resource exhaustion - denial of wallet - DoS\|G24]] B | B1 | Within limits | Within limits | Within limits | yes |
| [[G24 Resource exhaustion - denial of wallet - DoS\|G24]] B | B2 | Within limits | Within limits | Within limits | yes |
| [[G24 Resource exhaustion - denial of wallet - DoS\|G24]] B | B3 | Within limits | Within limits | Within limits | yes |
| [[G27 Vector store - RAG mechanisms\|G27]] poisoning | 1 | Unbounded | Within limits | Within limits | **no** |
| [[G27 Vector store - RAG mechanisms\|G27]] poisoning | 2 | Within limits | Within limits | Unbounded | **no** |
| [[G27 Vector store - RAG mechanisms\|G27]] poisoning | 3 | Unbounded | Unbounded | Unbounded | yes |
| [[G27 Vector store - RAG mechanisms\|G27]] poisoning | 4 | Within limits | Within limits | Within limits | yes |
| [[G27 Vector store - RAG mechanisms\|G27]] cross-boundary | 1 | Unbounded | Within limits | Unbounded | yes |
| [[G27 Vector store - RAG mechanisms\|G27]] cross-boundary | 2 | Bounded | Bounded | Bounded | yes |
| [[G27 Vector store - RAG mechanisms\|G27]] cross-boundary | 3 | Within limits | Within limits | Within limits | yes |
| [[G27 Vector store - RAG mechanisms\|G27]] jamming | 1 | Unbounded | Within limits | Within limits | **no** |
| [[G27 Vector store - RAG mechanisms\|G27]] jamming | 2 | Within limits | Within limits | Unbounded | **no** |
| [[G27 Vector store - RAG mechanisms\|G27]] jamming | 3 | Within limits | Within limits | Unbounded | **no** |
| [[G27 Vector store - RAG mechanisms\|G27]] cache | 1 | Within limits | Within limits | Within limits | yes |
| [[G27 Vector store - RAG mechanisms\|G27]] cache | 2 | Bounded | Bounded | Within limits | **no** |
| [[G27 Vector store - RAG mechanisms\|G27]] cache | 3 | Within limits | Within limits | Within limits | yes |
| [[G41 Physical safety (cyber-physical AI)\|G41]] | 1 | Not infosec | Not infosec | Not infosec | yes |
| [[G41 Physical safety (cyber-physical AI)\|G41]] | 2 | Unbounded | Unbounded | Unbounded | yes |
| [[G41 Physical safety (cyber-physical AI)\|G41]] | 3 | Not infosec | Not infosec | Not infosec | yes |
| [[G41 Physical safety (cyber-physical AI)\|G41]] | 4 | Not infosec | Not infosec | Not infosec | yes |
| [[G42 CBRN information or capabilities\|G42]] | 2 | Unbounded | Unbounded | Unbounded | yes |
| [[G42 CBRN information or capabilities\|G42]] | 3–5 | Not infosec | Not infosec | Not infosec | yes |
| [[G43 Dangerous, violent, or hateful content\|G43]] | 1 | Bounded | Bounded | Bounded | yes |
| [[G43 Dangerous, violent, or hateful content\|G43]] | 2 | Unbounded | Unbounded | Unbounded | yes |
| [[G43 Dangerous, violent, or hateful content\|G43]] | 3 | Within limits | Within limits | Within limits | yes |
| [[G43 Dangerous, violent, or hateful content\|G43]] | 4 | Not infosec | Not infosec | Not infosec | yes |
| [[G44 Obscene - abusive content (CSAM, NCII)\|G44]] | 2 | Within limits | Within limits | Unbounded | **no** |
| [[G44 Obscene - abusive content (CSAM, NCII)\|G44]] | 3 | Unbounded | Unbounded | Within limits | **no** |
| [[G44 Obscene - abusive content (CSAM, NCII)\|G44]] | 4–5 | Not infosec | Not infosec | Not infosec | yes |
| [[G56 Existential risk - loss of control over advanced AI - superintelligenc\|G56]]/[[G57 Misaligned AI goals (proxy gaming, goal drift, power-seeking, deceptio\|G57]] | goal | Unbounded | Unbounded | Unbounded | yes |
| [[G56 Existential risk - loss of control over advanced AI - superintelligenc\|G56]]/[[G57 Misaligned AI goals (proxy gaming, goal drift, power-seeking, deceptio\|G57]] | isolation | Bounded | Bounded | Bounded | yes |
| [[G56 Existential risk - loss of control over advanced AI - superintelligenc\|G56]]/[[G57 Misaligned AI goals (proxy gaming, goal drift, power-seeking, deceptio\|G57]] | weights | Within limits | Within limits | Within limits | yes |
| [[G56 Existential risk - loss of control over advanced AI - superintelligenc\|G56]]/[[G57 Misaligned AI goals (proxy gaming, goal drift, power-seeking, deceptio\|G57]] | undetected | Within limits | Within limits | Within limits | yes |
| [[G56 Existential risk - loss of control over advanced AI - superintelligenc\|G56]]/[[G57 Misaligned AI goals (proxy gaming, goal drift, power-seeking, deceptio\|G57]] | stop | Within limits | Within limits | Within limits | yes |
| [[S01 Nuclear\|S01]] | 4 | Within limits | Within limits | Within limits | yes |
| [[S01 Nuclear\|S01]] | 5 | Unbounded | Within limits | Within limits | **no** |
| [[S01 Nuclear\|S01]] | 6 | Bounded | Bounded | Within limits | **no** |
| [[S01 Nuclear\|S01]] | 7 | Within limits | Within limits | Not infosec | **no** |
| [[S06 Financial system\|S06]] | 1 | Unbounded | Within limits | Within limits | **no** |
| [[S06 Financial system\|S06]] | 2 | Bounded | Bounded | Within limits | **no** |
| [[S06 Financial system\|S06]] | 3 | Not infosec | Not infosec | Not infosec | yes |
| [[S06 Financial system\|S06]] | 4 | Bounded | Bounded | Bounded | yes |

### Agreement

**Contingency table, strict (primary) coding** (rows rater 1, columns rater 2; n = 102)

| Rater 1 \ Rater 2 | Bounded | Within limits | Unbounded | Not infosec | Total |
| --- | --- | --- | --- | --- | --- |
| Bounded | 9 | 6 | 0 | 0 | 15 |
| Within limits | 0 | 39 | 6 | 1 | 46 |
| Unbounded | 0 | 10 | 21 | 0 | 31 |
| Not infosec | 0 | 0 | 0 | 10 | 10 |
| Total | 9 | 55 | 27 | 11 | 102 |

Observed agreement 79/102 = 77.5%; expected by chance 34.7%; **Cohen's κ = 0.65**.

**Contingency table, lenient (sensitivity) coding** (rows rater 1, columns rater 2; n = 102)

| Rater 1 \ Rater 2 | Bounded | Within limits | Unbounded | Not infosec | Total |
| --- | --- | --- | --- | --- | --- |
| Bounded | 9 | 6 | 0 | 0 | 15 |
| Within limits | 0 | 46 | 10 | 1 | 57 |
| Unbounded | 0 | 3 | 17 | 0 | 20 |
| Not infosec | 0 | 0 | 0 | 10 | 10 |
| Total | 9 | 55 | 27 | 11 | 102 |

Observed agreement 82/102 = 80.4%; expected by chance 37.7%; **Cohen's κ = 0.69**.

**Summary.** Step level: 79 of 102 cells agree (77.5%), κ = 0.65 (strict coding); 82 of 102 (80.4%), κ = 0.69 (lenient). Path level: 24 of 29 path verdicts agree (82.8%). That compares with [[RQ2 Risk Classification|RQ2]]'s human-versus-AI first pass at κ = 0.12, but this is an AI-versus-AI comparison, so it is the weaker check.

### Path-level reconciliation

| Path | Rater 1 | Rater 2 | Agree? |
| --- | --- | --- | --- |
| [[G01 Training data - model poisoning\|G01]] baseline | Contained (2) | Contained (2) | yes |
| [[G01 Training data - model poisoning\|G01]] web-scale | Within granted scope (4) | Within granted scope (4) | yes |
| [[G02 Backdoors - hidden learned functionality\|G02]] | Within granted scope (5) | Within granted scope (5) | yes |
| [[G03 Evasion - adversarial inputs\|G03]] baseline | Within granted scope (4) | Contained within limits (4) | **no** |
| [[G04 Model extraction - stealing - distillation\|G04]] baseline | Contained (1–3) | Contained (3) | yes |
| [[G04 Model extraction - stealing - distillation\|G04]] maximal | As baseline | Contained (3) | yes |
| [[G06 Membership inference\|G06]] | Contained (1–3) | Contained within limits (3) | yes |
| [[G07 Training-data reconstruction - extraction - memorization\|G07]] gradient | Contained (1–3) | Contained within limits (2–3) | yes |
| [[G07 Training-data reconstruction - extraction - memorization\|G07]] query | Contained (1, 3) | Contained within limits (1, 3) | yes |
| [[G08 Property inference - model characterisation (recon)\|G08]] | Contained (1) | Contained within limits (1) | yes |
| [[G09 Embedding inversion\|G09]] | Contained (1) | Contained (1) | yes |
| [[G10 Direct prompt injection - jailbreak\|G10]] | Within granted scope (3) | Within granted scope (3) | yes |
| [[G11 Indirect prompt injection - goal hijack\|G11]] | Within granted scope (4) | Within granted scope (4) | yes |
| [[G14 Excessive agency - privilege - credentials\|G14]] | Within granted scope | Contained (1) | **no** |
| [[G16 Tool misuse - coerced tool use\|G16]] | Within granted scope (1, 3) | Within granted scope (3) | yes |
| [[G18 Memory & context poisoning (persistent)\|G18]] | Within granted scope | Within granted scope (4) | yes |
| [[G24 Resource exhaustion - denial of wallet - DoS\|G24]] A | Contained (A1–A2) | Contained (A1) | yes |
| [[G24 Resource exhaustion - denial of wallet - DoS\|G24]] B | Contained (B1–B2) | Contained within limits (B1) | yes |
| [[G27 Vector store - RAG mechanisms\|G27]] poisoning | Contained (1, curated) | Contained within limits (1) | yes |
| [[G27 Vector store - RAG mechanisms\|G27]] cross-boundary | Contained (2) | Contained (2) | yes |
| [[G27 Vector store - RAG mechanisms\|G27]] jamming | Contained (1, curated) | Contained within limits (1) | yes |
| [[G27 Vector store - RAG mechanisms\|G27]] cache | Contained (2) | Contained within limits (2) | yes |
| [[G41 Physical safety (cyber-physical AI)\|G41]] | Not contained (safety fallback only) | Not contained | yes |
| [[G42 CBRN information or capabilities\|G42]] | As the direct-injection row | Not contained | **no** |
| [[G43 Dangerous, violent, or hateful content\|G43]] | Contained (1) | Contained (1) | yes |
| [[G44 Obscene - abusive content (CSAM, NCII)\|G44]] | As the direct-injection row | Contained within limits (3) | **no** |
| [[G56 Existential risk - loss of control over advanced AI - superintelligenc\|G56]]/[[G57 Misaligned AI goals (proxy gaming, goal drift, power-seeking, deceptio\|G57]] | Within granted scope (isolation) | Contained (isolation) | **no** |
| [[S01 Nuclear\|S01]] | Contained (6) | Contained within limits (6) | yes |
| [[S06 Financial system\|S06]] | Contained (4) | Contained (4) | yes |

Rater 2 wrote "contained within limits," which is not one of [[RQ3 Control Coverage|RQ3]]'s three path values. Under Method item 5 a path is contained when a step is Bounded *or Bounded within limits*, so it is read here as "contained." The exception is where the bounded step is the grant, which is read as "within the granted scope."

### Disagreements and rater 2's reasoning

The 23 strict-coding disagreements fall into four groups.

**Coding artifacts (7): [[G02 Backdoors - hidden learned functionality|G02]] steps 1–2, [[G07 Training-data reconstruction - extraction - memorization|G07]] query 3, [[G27 Vector store - RAG mechanisms|G27]] poisoning 1, [[G27 Vector store - RAG mechanisms|G27]] jamming 1, [[S01 Nuclear|S01]] 5, [[S06 Financial system|S06]] 1.** Each is a rater 1 cell that splits by route. The strict rule takes the unbounded route, while rater 2 wrote one "within limits" value and named the unbounded route as the limit. Substance agrees. Under lenient coding all seven agree, and four new disagreements appear the other way ([[G11 Indirect prompt injection - goal hijack|G11]] 1, [[G14 Excessive agency - privilege - credentials|G14]] 2, [[G16 Tool misuse - coerced tool use|G16]] 2, [[G27 Vector store - RAG mechanisms|G27]] cross-boundary 1).

**Same control, adjacent step (4): [[G01 Training data - model poisoning|G01]] web-scale 1 and 2; [[G44 Obscene - abusive content (CSAM, NCII)|G44]] 2 and 3.** For [[G01 Training data - model poisoning|G01]] web-scale, rater 1 puts the maintainers' snapshot-integrity controls at step 1 (injection); rater 2 put them at step 2 (ingestion without filtering). Both have one bounded and one unbounded step. For [[G44 Obscene - abusive content (CSAM, NCII)|G44]], rater 1 reads step 2 as accountable identity and step 3 as the AI step. Rater 2 read step 2 as the refusal failing (the AI step) and step 3 as output filtering. Both readings fit the step text.

**Bounded versus Bounded within limits (6): [[G10 Direct prompt injection - jailbreak|G10]] 4, [[G16 Tool misuse - coerced tool use|G16]] 1, [[G24 Resource exhaustion - denial of wallet - DoS|G24]] A2, [[G27 Vector store - RAG mechanisms|G27]] cache 2, [[S01 Nuclear|S01]] 6, [[S06 Financial system|S06]] 2.** Rater 2 was more conservative in every case, naming a residual parameter as a limit: the egress policy, tools the task still needs, the cap amount, a deliberately shared cache, sensor independence, provider concentration. Rater 1 reserves "within limits" for a quantity the control caps. Rater 2's reading treats any deployer-set parameter as a limit. That is closer to the Residual section's R1, but it makes "Bounded" almost empty. Rater 2 would accept rater 1's narrower use if the Method said so explicitly.

**Substantive (6):**
- **[[G08 Property inference - model characterisation (recon)|G08]] step 3** (rater 1 Unbounded, rater 2 within limits). Rater 2 argued that follow-on attacks meet their own controls. On reflection rater 1 is right: the step is *disclosure* of the inferred property, and nothing bounds that. Rater 2 concedes.
- **[[G18 Memory & context poisoning (persistent)|G18]] step 3** (rater 1 within limits, rater 2 Unbounded). Rater 1 sees memory as a corpus the deployer controls, so integrity and source trust apply to its retrieval. Rater 2 rated only the model's response to retrieved text. Rater 2 concedes: rater 1 identified a stop rater 2 missed.
- **[[G27 Vector store - RAG mechanisms|G27]] poisoning step 2** (rater 1 within limits, rater 2 Unbounded). Rater 1's own evidence says the defenses tested "are insufficient" [\[269\]](Sources.md#^s269) and names no requirement that caps selection. Rater 2 holds that this is Unbounded. Logged as a question.
- **[[G27 Vector store - RAG mechanisms|G27]] jamming step 2** (rater 1 within limits, rater 2 Unbounded). Rater 1's cell reads "Bounded within limits. The AI step." It names no limit and cites no control, so rater 2 holds Unbounded. Logged.
- **[[G27 Vector store - RAG mechanisms|G27]] jamming step 3** (rater 1 "Detected, then removed at step 1"; rater 2 Unbounded). Detection is not a value on the scale, and no availability requirement treats a targeted refusal as an outage. Logged.
- **[[S01 Nuclear|S01]] step 7** (rater 1 within limits, rater 2 Not an information-security step). The controls rater 1 cites (human in the loop, the two-person rule, intent codes [\[122\]](Sources.md#^s122), [\[129\]](Sources.md#^s129)) are nuclear-command doctrine, not requirements in the seven frameworks. In [[S06 Financial system|S06]] step 3 and [[G41 Physical safety (cyber-physical AI)|G41]] step 3, rater 1 treats controls outside the frameworks as non-security. Logged.

**Path-level disagreements (5).** [[G03 Evasion - adversarial inputs|G03]], [[G44 Obscene - abusive content (CSAM, NCII)|G44]] and [[G56 Existential risk - loss of control over advanced AI - superintelligenc|G56]]/[[G57 Misaligned AI goals (proxy gaming, goal drift, power-seeking, deceptio|G57]] are labeling differences: both raters put the stop at the same step. [[G14 Excessive agency - privilege - credentials|G14]] and [[G56 Existential risk - loss of control over advanced AI - superintelligenc|G56]]/[[G57 Misaligned AI goals (proxy gaming, goal drift, power-seeking, deceptio|G57]] point to something larger. Rater 1's own tables mark a step Bounded ([[G14 Excessive agency - privilege - credentials|G14]] step 1, least privilege; the [[G56 Existential risk - loss of control over advanced AI - superintelligenc|G56]]/[[G57 Misaligned AI goals (proxy gaming, goal drift, power-seeking, deceptio|G57]] isolation step), and under Method item 5 a Bounded step outside the model makes a path "contained." Yet rater 1 labels both "within the granted scope." The Method never defines "within the granted scope" as a separate path verdict. [[G42 CBRN information or capabilities|G42]] is a real difference. Rater 1's verdict says "as the direct-injection row," and its Counts paragraph counts [[G42 CBRN information or capabilities|G42]] among the contained paths. Rater 1's own Summary table, though, gives [[G42 CBRN information or capabilities|G42]] "None inside the deployer's controls" as the bounded step. Rater 2 reads that as not contained.

### Resolutions (Nov 4, 14:00)

Author's decisions on the disagreements. [[RQ3 Control Coverage|RQ3]] was changed to rater 2's reading for [[G27 Vector store - RAG mechanisms|G27]] poisoning step 2, [[G27 Vector store - RAG mechanisms|G27]] jamming steps 2 and 3, and [[S01 Nuclear|S01]] step 7. [[G14 Excessive agency - privilege - credentials|G14]] and [[G56 Existential risk - loss of control over advanced AI - superintelligenc|G56]]/[[G57 Misaligned AI goals (proxy gaming, goal drift, power-seeking, deceptio|G57]] were relabeled "contained." The figures above describe the ratings *before* these resolutions. Later the same day, [[G42 CBRN information or capabilities|G42]] was set to not contained. The convention was settled on Method item 4 as written, which moved [[G10 Direct prompt injection - jailbreak|G10]] step 4, [[G16 Tool misuse - coerced tool use|G16]] step 1 and [[G24 Resource exhaustion - denial of wallet - DoS|G24]] step A2 to rater 2's reading and kept [[G27 Vector store - RAG mechanisms|G27]] cache step 2, [[S01 Nuclear|S01]] step 6 and [[S06 Financial system|S06]] step 2 at rater 1's.

