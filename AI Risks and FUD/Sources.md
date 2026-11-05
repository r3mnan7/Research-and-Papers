---
tags: [sources, ai-fud-whitepaper]
---
# Sources

Back to [[Addressing Fear, Uncertainty, and Doubt in the Security and Safety of Artificial Intelligence Models|main note]]

Compiled with AI assistance from the reference lists in [[RQ1 How AI Systems Differ|RQ1]]–[[RQ4 Rogue AI Incidents|RQ4]], the Screening Log, the attack-path notes, and the catastrophe-pathway notes. Duplicates were merged.

Every note cites sources by these numbers. Add a new source at the end of the list with the next number, and don't renumber. Evidence quoted inside attack-path and scenario tables is also cited inline there.

## Definitions, standards, and control frameworks

[1] National Institute of Standards and Technology, *Artificial Intelligence Risk Management Framework (AI RMF 1.0)*, NIST AI 100-1, Jan. 2023, Appendix B, "How AI Risks Differ from Traditional Software Risks," pp. 38–39. https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf ^s1

[2] Regulation (EU) 2024/1689 (Artificial Intelligence Act), Art. 3(1), *Official Journal of the European Union*, 12 July 2024. https://eur-lex.europa.eu/eli/reg/2024/1689/oj ^s2

[3] OECD, *Recommendation of the Council on Artificial Intelligence*, OECD/LEGAL/0449, amended 2023/2024 (revised definition of "AI system"). https://legalinstruments.oecd.org/en/instruments/OECD-LEGAL-0449 ^s3

[4] ISO/IEC 22989:2022, *Information technology — Artificial intelligence — Artificial intelligence concepts and terminology*. https://www.iso.org/standard/74296.html ^s4

[5] ISO, "What is artificial intelligence (AI)?" https://www.iso.org/artificial-intelligence/what-is-ai (Explainer. Before drafting, replace with the term definitions in [\[4\]](#^s4).) ^s5

[6] 44 U.S.C. § 3552, Definitions (Federal Information Security Modernization Act), via Cornell Law School Legal Information Institute. https://www.law.cornell.edu/uscode/text/44/3552 ^s6

[7] National Institute of Standards and Technology, Computer Security Resource Center Glossary, "integrity." https://csrc.nist.gov/glossary/term/integrity ^s7

[8] National Institute of Standards and Technology, *The NIST Cybersecurity Framework (CSF) 2.0*, NIST CSWP 29, February 26, 2024. [Full publication](https://nvlpubs.nist.gov/nistpubs/CSWP/NIST.CSWP.29.pdf). See Appendix A, especially printed pp. 17–21 for supply chain, inventories, testing, access, data protection, logging, and monitoring. Source for CSF outcome identifiers; AI applications in the table are analytical mappings. ^s8

[9] Center for Internet Security, *CIS Critical Security Controls v8.1*, June 24, 2024. [Version description and download](https://www.cisecurity.org/insights/white-papers/cis-critical-security-controls-v8-1). Detailed safeguard text was checked against the publisher's v8.1 assessment specification in [\[10\]](#^s10), [\[11\]](#^s11), [\[13\]](#^s13), [\[14\]](#^s14). Safeguard applicability does not imply that every safeguard belongs to every Implementation Group. The copy used is document version 8.1.2 (March 2025), whose change log lists only typo, hyperlink, and label corrections to v8.1. ^s9

[10] Center for Internet Security, *CIS Controls Assessment Specification for Controls v8.1*, [Control 3: Data Protection](https://cas.docs.cisecurity.org/en/latest/source/Controls3/). Safeguards 3.2, 3.3, 3.7, 3.8, 3.11, 3.12, and 3.14. Supports data inventory, access, classification, data-flow, encryption-at-rest, segmentation, and sensitive-data-access logging mappings. ^s10

[11] Center for Internet Security, *CIS Controls Assessment Specification for Controls v8.1*, [Control 6: Access Control Management](https://cas.docs.cisecurity.org/en/latest/source/Controls6/). Safeguards 6.1, 6.2, 6.3, 6.5, and 6.8. Supports access lifecycle, MFA, and role-based access mappings. ^s11

[12] Center for Internet Security, [*CIS Controls Assessment Specification for Controls v8.1*, Control 11: Data Recovery](https://cas.docs.cisecurity.org/en/latest/source/Controls11/). Safeguards 11.3–11.5 address recovery-data protection, an isolated recovery-data instance, and recovery testing. Other control anchors use the primary framework sources already listed under RQ3. ^s12

[13] Center for Internet Security, *CIS Controls Assessment Specification for Controls v8.1*, [Control 14: Security Awareness and Skills Training](https://cas.docs.cisecurity.org/en/latest/source/Controls14/). Safeguard 14.2 addresses recognizing social engineering; application to deepfake scenarios is the research interpretation. ^s13

[14] Center for Internet Security, *CIS Controls Assessment Specification for Controls v8.1*, [Control 16: Application Software Security](https://cas.docs.cisecurity.org/en/latest/source/Controls16/). Safeguards 16.4, 16.5, 16.10, 16.13, and 16.14. Supports third-party component inventory, trusted-component, secure-design, penetration-testing, and threat-modeling mappings. ^s14

[15] Joint Task Force, *Security and Privacy Controls for Information Systems and Organizations*, NIST SP 800-53 Rev. 5, September 2020, with December 10, 2020 updates. [Full publication](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-53r5.pdf); [publication record and Release 5.2.0 notice](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final); [CPRT control catalog](https://csrc.nist.gov/projects/cprt/catalog#/cprt/framework/version/SP_800_53_5_1_1/home), used on Nov. 4, 2026 to verify control statements. See Chapter 3 by control identifier; especially AC-3(2), AC-4, AC-23, CA-8(2), SC-4, SC-6, SC-7(10), SI-10(6), SI-19(5)/(6)/(8), and SR-4. Parenthetical numbers denote control enhancements, whose selection and implementation must be established separately from the base control. ^s15

[16] Cybersecurity and Infrastructure Security Agency, *Zero Trust Maturity Model, Version 2.0*, April 2023. [Full publication](https://www.cisa.gov/sites/default/files/2023-04/CISA_Zero_Trust_Maturity_Model_Version_2_508c.pdf); [CISA release announcement](https://content.govdelivery.com/accounts/USDHSCISA/bulletins/3543f28). See Sections 5.1–5.5 for the five pillars, especially Identity—Access Management and Applications and Workloads—Application Access and Application Threat Protections; Section 5.6 for cross-cutting capabilities. The release announcement confirms all four maturity stages. AI-specific applications and limits in this research are analytical interpretations, not publisher-issued mappings or assigned maturity ratings. ^s16

[17] OWASP Foundation, *OWASP Application Security Verification Standard*, Version 5.0.0, May 2025 (published May 30, 2025). D. Cuthbert, E. Lang, and J. C. Grossman, project leads. [Project site](https://asvs.owasp.org/); [PDF](https://github.com/OWASP/ASVS/raw/v5.0.0/5.0/OWASP_Application_Security_Verification_Standard_5.0.0_en.pdf); [requirement chapters](https://github.com/OWASP/ASVS/tree/v5.0.0/5.0/en). Cited here as `v5.0.0-<chapter>.<section>.<requirement>`, the version-pinned form the standard recommends. Each requirement's level is the lowest level at which it applies. ^s17

[18] D. Temoshok et al., *Digital Identity Guidelines*, NIST SP 800-63-4, July 2025, https://doi.org/10.6028/NIST.SP.800-63-4; with *Identity Proofing and Enrollment*, NIST SP 800-63A-4, https://doi.org/10.6028/NIST.SP.800-63A-4; and *Authentication and Authenticator Management*, NIST SP 800-63B-4, https://doi.org/10.6028/NIST.SP.800-63B-4. [HTML edition](https://pages.nist.gov/800-63-4/). Sections used: 63-4 §1.1 (scope excludes machine-to-machine authentication), §3.8 (AI/ML in identity systems); 63A-4 §3.11 (use of biometrics, including presentation attack detection), §3.14 (digital injection prevention and forged media detection); 63B-4 §2.2.2/§2.3.2 (phishing resistance at AAL2/AAL3), §3.2.3.2 (presentation attack detection, including the bar on voice comparison), §3.2.8 (authentication intent), §4.2 (account recovery), §6.3 (authenticator recovery and social engineering). ^s18

[19] J. Boyens, A. Smith, N. Bartol, K. Winkler, A. Holbrook, and M. Fallon, *Cybersecurity Supply Chain Risk Management Practices for Systems and Organizations*, NIST SP 800-161 Rev. 1, May 2022, includes updates as of Nov. 1, 2024 (SP 800-161r1-upd1). https://doi.org/10.6028/NIST.SP.800-161r1-upd1; [publication page](https://csrc.nist.gov/pubs/sp/800/161/r1/upd1/final). Appendix A gives C-SCRM supplemental guidance keyed to SP 800-53 Rev. 5 controls. Used: CM-8 (p. 93), SA-4 (p. 138), SA-9 (p. 141), SI-7 (p. 156), SR-3 (p. 158), SR-4 and SR-5 (p. 159), SR-6 (pp. 159–160), SR-10 and SR-11 (p. 161). A full-text search of the 325-page document (text extracted from the PDF on Nov. 4, 2026) finds no mention of "artificial intelligence" or "machine learning"; the Appendix A page numbers above and the phrases "and associated data" (SR-4) and "code execution in contained environments prior to use" (SI-7) were confirmed in the same pass. ^s19

[20] J. Near, D. Darais, N. Lefkovitz, and G. Howarth, *Guidelines for Evaluating Differential Privacy Guarantees*, NIST SP 800-226, March 2025. [Final publication record](https://csrc.nist.gov/pubs/sp/800/226/final); [full publication](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-226.pdf). Supports evaluating privacy guarantees, parameters, and implementation hazards rather than treating differential privacy as a binary feature. ^s20

## AI security guidance and taxonomies

[21] National Institute of Standards and Technology, *Artificial Intelligence Risk Management Framework: Generative Artificial Intelligence Profile*, NIST AI 600-1, Jul. 2024. https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf ^s21

[22] A. Vassilev, A. Oprea, A. Fordyce, H. Anderson, X. Davies, and M. Hamin, *Adversarial Machine Learning: A Taxonomy and Terminology of Attacks and Mitigations*, NIST AI 100-2e2025, National Institute of Standards and Technology, Mar. 2025, doi: 10.6028/NIST.AI.100-2e2025. https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-2e2025.pdf ^s22

[23] OWASP GenAI Security Project, *OWASP Top 10 for LLM Applications 2026*, Version 2026, 2026. https://owasp.org/www-project-top-10-for-large-language-model-applications/ ^s23

[24] OWASP GenAI Security Project, *OWASP Top 10 for Agentic Applications for 2026*, Dec. 9, 2025. https://genai.owasp.org/resource/owasp-top-10-for-agentic-applications-for-2026/ ^s24

[25] U.K. National Cyber Security Centre, *Understanding Adversarial Attacks Against Machine Learning and AI*, Version 1.0, Apr. 29, 2026. https://www.ncsc.gov.uk/sites/default/files/2026-08/Understanding-adversarial-attacks-against-Machine-Learning-and-AI.pdf ^s25

[26] U.K. National Cyber Security Centre, "Thinking carefully before adopting agentic AI," May 15, 2026. https://www.ncsc.gov.uk/blogs/thinking-carefully-before-adopting-agentic-ai ^s26

[27] D. Chismon, "Prompt injection is not SQL injection (it may be worse)," U.K. National Cyber Security Centre, Dec. 8, 2025. https://www.ncsc.gov.uk/blog-post/prompt-injection-is-not-sql-injection ^s27

[28] J. Ji, J. Jun, M. Wu, and R. Gelles, *Cybersecurity Risks of AI-Generated Code*. Washington, DC, USA: Center for Security and Emerging Technology, Nov. 2024, doi: 10.51593/2023CA010. https://cset.georgetown.edu/wp-content/uploads/CSET-Cybersecurity-Risks-of-AI-Generated-Code.pdf ^s28

[29] I. Jada and T. O. Mayayise, "The impact of artificial intelligence on organisational cyber security: An outcome of a systematic literature review," *Data and Information Management*, vol. 8, no. 2, Art. no. 100063, Jun. 2024, doi: 10.1016/j.dim.2023.100063. https://doi.org/10.1016/j.dim.2023.100063 ^s29

[30] S. Nevo, D. Lahav, A. Karpur, Y. Bar-On, H. A. Bradley, and J. Alstott, *Securing AI Model Weights: Preventing Theft and Misuse of Frontier Models*, RAND, RR-A2849-1, 2024. https://www.rand.org/pubs/research_reports/RRA2849-1.html ^s30

[31] P. Slattery et al., "The AI Risk Repository: A meta-review, database, and taxonomy of risks from artificial intelligence," arXiv:2408.12622 (v3, May 2026), with the MIT AI Risk Repository v4 (Dec. 2025). https://arxiv.org/abs/2408.12622; https://airisk.mit.edu/ ^s31

## Threat intelligence and government assessments

[32] U.K. National Cyber Security Centre, "The near-term impact of AI on the cyber threat," 24 Jan. 2024. https://www.ncsc.gov.uk/report/impact-of-ai-on-cyber-threat ^s32

[33] U.K. National Cyber Security Centre, "Impact of AI on cyber threat from now to 2027," 7 May 2025. https://www.ncsc.gov.uk/report/impact-ai-cyber-threat-now-2027 ^s33

[34] Google Threat Intelligence Group, "Adversarial Misuse of Generative AI," 29 Jan. 2025. https://cloud.google.com/blog/topics/threat-intelligence/adversarial-misuse-generative-ai ^s34

[35] Google Threat Intelligence Group, "GTIG AI Threat Tracker: Advances in Threat Actor Usage of AI Tools," 5 Nov. 2025. https://cloud.google.com/blog/topics/threat-intelligence/threat-actor-usage-of-ai-tools ^s35

[36] Anthropic, "Disrupting the first reported AI-orchestrated cyber espionage campaign," 13 Nov. 2025 (edited 14 Nov. 2025). https://www.anthropic.com/news/disrupting-AI-espionage. Full report (PDF): https://assets.anthropic.com/m/ec212e6566a0d47/original/Disrupting-the-first-reported-AI-orchestrated-cyber-espionage-campaign.pdf. Some wording, including "validated a handful of successful intrusions," appears only in the full report. ^s36

[37] Federal Bureau of Investigation, Internet Crime Complaint Center, "Criminals Use Generative Artificial Intelligence to Facilitate Financial Fraud," PSA I-120324-PSA, 3 Dec. 2024. https://www.ic3.gov/PSA/2024/PSA241203 ^s37

[38] Unit 42, "Fooling AI Agents: Web-Based Indirect Prompt Injection Observed in the Wild," Palo Alto Networks, 3 Mar 2026, https://unit42.paloaltonetworks.com/ai-agent-prompt-injection.md ^s38

[39] Google, "AI threats in the wild: The current state of prompt injections on the web," 23 Apr 2026, https://blog.google/security/prompt-injections-web/ ^s39

[40] Anthropic, "Detecting and countering misuse of AI: September 2026," https://www.anthropic.com/threat-intelligence-report-september-2026 (exact date not on page). [[RQ3 Control Coverage|RQ3]] relies on its GTG-50020 account: an AI vendor's automated evaluation sandbox held production API keys for multiple providers, and injected instructions "caused the sandbox to hand over the credentials it held"; stolen keys were reused. ^s40

[41] OpenAI, "Continuously hardening ChatGPT Atlas against prompt injection attacks," 22 Dec. 2025. https://openai.com/index/hardening-atlas-against-prompt-injection/ ^s41

## Research papers

Origin papers establish the dates of mechanisms; established principles are the "old" side of the comparison.

[42] C. Szegedy, W. Zaremba, I. Sutskever, J. Bruna, D. Erhan, I. Goodfellow, and R. Fergus, "Intriguing properties of neural networks," ICLR 2014 (arXiv Dec. 2013). https://arxiv.org/abs/1312.6199 ^s42

[43] R. Shokri, M. Stronati, C. Song, and V. Shmatikov, "Membership Inference Attacks Against Machine Learning Models," *IEEE Symposium on Security and Privacy*, 2017, doi: 10.1109/SP.2017.41. https://doi.org/10.1109/SP.2017.41 ^s43

[44] F. Tramèr, F. Zhang, A. Juels, M. K. Reiter, and T. Ristenpart, "Stealing Machine Learning Models via Prediction APIs," *25th USENIX Security Symposium*, 2016. https://www.usenix.org/conference/usenixsecurity16/technical-sessions/presentation/tramer ^s44

[45] L. Zhu, Z. Liu, and S. Han, "Deep Leakage from Gradients," *NeurIPS*, 2019. https://arxiv.org/abs/1906.08935 ^s45

[46] J. X. Morris, V. Kuleshov, V. Shmatikov, and A. M. Rush, "Text Embeddings Reveal (Almost) As Much As Text," *EMNLP*, 2023. https://arxiv.org/abs/2310.06816 ^s46

[47] T. Gu, B. Dolan-Gavitt, and S. Garg, "BadNets: Identifying Vulnerabilities in the Machine Learning Model Supply Chain," 2017. https://arxiv.org/abs/1708.06733 ^s47

[48] S. Goldwasser, M. P. Kim, V. Vaikuntanathan, and O. Zamir, "Planting Undetectable Backdoors in Machine Learning Models," *2022 IEEE 63rd Annual Symposium on Foundations of Computer Science (FOCS)*, pp. 931–942, doi: 10.1109/FOCS54457.2022.00092 (venue confirmed from the proceedings PDF, Nov. 4, 2026). https://arxiv.org/abs/2204.06974 ^s48

[49] E. Hubinger et al., "Sleeper Agents: Training Deceptive LLMs that Persist Through Safety Training," Anthropic, Jan. 2024. https://arxiv.org/abs/2401.05566 ^s49

[50] K. Greshake, S. Abdelnabi, S. Mishra, C. Endres, T. Holz, and M. Fritz, "Not what you've signed up for: Compromising Real-World LLM-Integrated Applications with Indirect Prompt Injection," *ACM AISec*, 2023. https://arxiv.org/abs/2302.12173 ^s50

[51] N. Hardy, "The Confused Deputy (or why capabilities might have been invented)," *ACM SIGOPS Operating Systems Review*, vol. 22, no. 4, pp. 36–38, Oct. 1988, doi: 10.1145/54289.871709. https://doi.org/10.1145/54289.871709 ^s51

[52] J. H. Saltzer and M. D. Schroeder, "The Protection of Information in Computer Systems," *Proceedings of the IEEE*, vol. 63, no. 9, pp. 1278–1308, Sept. 1975, doi: 10.1109/PROC.1975.9939. https://doi.org/10.1109/PROC.1975.9939 ^s52

[53] V. Carletti, P. Foggia, C. Mazzocca, G. Parrella, and M. Vento, "SoK: Gradient Inversion Attacks in Federated Learning," in *34th USENIX Security Symposium (USENIX Security 25)*, Aug. 2025, pp. 6439–6459. Systematizes gradient-inversion defenses, including the malicious-server bypass of secure aggregation. https://www.usenix.org/conference/usenixsecurity25/presentation/carletti ^s53

[54] J. Du, J. Hu, Z. Wang, P. Sun, N. Gong, K. Ren, and C. Chen, "SoK: On Gradient Leakage in Federated Learning," in *34th USENIX Security Symposium (USENIX Security 25)*, Aug. 2025, pp. 3045–3064. Finds gradient inversion attacks "notably constrained, fragile, and easily defensible" in practical training settings; "even simple post-processing techniques applied to gradients can serve as effective defenses." https://www.usenix.org/conference/usenixsecurity25/presentation/du ^s54

[55] X. Li, Y. Meng, J. Chen, L. Luo, and Q. Zeng, "Rowhammer-Based Trojan Injection: One Bit Flip Is Sufficient for Backdooring DNNs," in *34th USENIX Security Symposium (USENIX Security 25)*, Aug. 2025, pp. 6319–6337. https://www.usenix.org/conference/usenixsecurity25/presentation/li-xiang ^s55

[56] D. Popovic, A. Sadeghi, T. Yu, S. Chawla, and I. Khalil, "DeBackdoor: A Deductive Framework for Detecting Backdoor Attacks on Deep Models with Limited Data," in *34th USENIX Security Symposium (USENIX Security 25)*, Aug. 2025, pp. 6419–6438. https://www.usenix.org/conference/usenixsecurity25/presentation/popovic ^s56

[57] Y. He, H. Zhu, Y. Li, S. Shao, H. Yao, Z. Liu, and Z. Qin, "AttriGuard: Defeating Indirect Prompt Injection in LLM Agents via Causal Attribution of Tool Invocations," in *35th USENIX Security Symposium (USENIX Security 26)*, Aug. 2026, pp. 1547–1566. https://arxiv.org/abs/2603.10749 (preprint; USENIX page not found) ^s57

[58] J. Kim, W. Guo, and D. Song, "SoK: Attack and Defense Landscape of Agentic AI Systems," in *35th USENIX Security Symposium (USENIX Security 26)*, Aug. 2026, pp. 6047–6066. https://www.usenix.org/conference/usenixsecurity26/presentation/kim-juhee-agentic ^s58

[59] R. Kobayashi, K. Nomoto, Y. Tanaka, G. Tsuruoka, and T. Mori, "Invisible but Detected: Physical Adversarial Shadow Attack and Defense on LiDAR Object Detection," in *34th USENIX Security Symposium (USENIX Security 25)*, 2025. https://www.usenix.org/conference/usenixsecurity25/presentation/kobayashi ^s59

[60] K. Bonawitz et al., “Practical Secure Aggregation for Privacy-Preserving Machine Learning,” *ACM SIGSAC Conference on Computer and Communications Security (CCS)*, 2017. [Authors' research publication page](https://research.google/pubs/practical-secure-aggregation-for-privacy-preserving-machine-learning/). Describes a protocol for computing aggregates without revealing individual contributions; used to distinguish secure aggregation from differential privacy. ^s60

## Incident disclosures and vulnerability reports

Primary disclosures establish reported events. Operator and vendor accounts are self-reports; each entry notes its evidence limits. [[RQ4 Rogue AI Incidents|RQ4]] sources were reviewed or located on October 27, 2026.

[61] Hugging Face, [“Security incident disclosure — July 2026”](https://huggingface.co/blog/security-incident-july-2026), July 16, 2026. Victim statement on observed impact, response, supply-chain checks, and outstanding exposure assessment. ^s61

[62] H. Larcher, A. Carreira, R. G., and C. Rannou, Hugging Face, [“Anatomy of a Frontier Lab Agent Intrusion: A Technical Timeline of the July 2026 Incident”](https://huggingface.co/blog/agent-intrusion-technical-timeline), July 27, 2026. Main victim-side technical source: dataset entry paths, Kubernetes/credential escalation, network pivots, blocked actions, and forensic scope. Prefer its more specific technical distinctions when the initial disclosure used broader descriptions. ^s62

[63] OpenAI, [“OpenAI and Hugging Face partner to address security incident during model evaluation”](https://openai.com/index/hugging-face-model-evaluation-security-incident/), July 21, 2026. Attribution, evaluation configuration (production cyber safeguards "intentionally not enabled"), and initial response. No dated update note was visible on Nov. 4, 2026; the prototype status is in [\[65\]](#^s65) §I (description corrected Nov. 4, 2026). ^s63

[64] OpenAI, [“The Hugging Face incident and the road ahead”](https://openai.com/index/hugging-face-incident-and-the-road-ahead/), August 26, 2026. Precursor activity, timeline, communication failures, and announced mitigation strategy. ^s64

[65] OpenAI, [*OpenAI–Hugging Face Incident Technical Report*](https://cdn.openai.com/pdf/67869394-cb91-4c12-888c-5cbd85c7814c/OpenAI-Hugging-Face%20Incident-Technical-Report.pdf), August 26, 2026. Sections II–VI describe execution infrastructure, precursor vulnerabilities, the intrusion, and response; sections VII–IX discuss security, alignment, and planned changes. Operator-authored account with external-advisor involvement, not an independent audit opinion. ^s65

[66] R. Greenblatt (Redwood Research, contracting with METR), A. Cotra, and H. Wijk (METR), METR blog, [“Brief independent investigation of agents' behavior, reasoning and collaboration in the OpenAI / Hugging Face hacking incident”](https://metr.org/blog/2026-08-26-openai-hugging-face-incident-investigation/), August 26, 2026. Agent coordination, impossible tasks, scorer manipulation, tool-call spoofing (about 7% of the transcripts METR evaluated were spoofed in places, aimed at the automated scorer; one figure caption says about 7% of agents; the transcripts were supplied by OpenAI, and METR cannot rule out undetected edits; description corrected Nov. 4, 2026), methodology, and explicit limitations. Does not independently certify the entirety of victim-side impact. ^s66

[67] Anthropic, [“Investigating three real-world incidents in our cybersecurity evaluations”](https://www.anthropic.com/research/investigating-incidents-cybersecurity-evals), July 30, 2026. Evaluation partner/configuration, three incident narratives, PyPI publication sequence, and initial response. The PyPI case is “Incident 2.” ^s67

[68] Anthropic, [“An alignment assessment of recent cybersecurity incidents”](https://www.anthropic.com/research/alignment-assessment-cybersecurity-incidents), September 9, 2026. Updated four-incident scope; PyPI action timeline, likely scanner identity of the 15 hosts, live-database access, behavioral analysis, and retrospective monitoring experiments. [[RQ3 Control Coverage|RQ3]] quotes: pre-release auditing "did not warn us that misalignment of this severity was present"; the incidents "would not have occurred had the environments been isolated from the internet as intended"; "it is an open research problem to construct alignment evaluations" representative of deployment. ^s68

[69] Anthropic, [*Mythos 5 Incident Transcript Release*](https://github.com/anthropics/mythos-5-incident-transcript), published September 9, 2026. [Pinned JSONL artifact](https://github.com/anthropics/mythos-5-incident-transcript/blob/62858fcf2725fe7b38872d538e973f38846ea744/transcript.jsonl). Parsed the 2,065 JSONL records; inspected selected message indices 83–125, 1554–1555, and 2139–2144 for network forwarding, package construction, and publication. These message indices differ from the assessment’s action numbers. Metadata specifies redaction of messages 1–81, messages after 2145, and other sensitive content. The visible file does not establish the complete scanner/database sequence. Downloaded artifact Git blob SHA-1: `488d11d83def14275c364566a1016d22dcc89157`; SHA-256: `6f2a5a50b53640bd779a198cef8a620f2d6e2bbaaf4a0dea9edac87a69fc3e4b`. Model reasoning is evidence of a stated plan; tool output supports only the specific returned result. ^s69

[70] Replit Team, [“Doubling down on our commitment to secure vibe coding”](https://replit.com/blog/doubling-down-on-our-commitment-to-secure-vibe-coding), July 29, 2025. Primary acknowledgment of deletion and full restoration; explanation of the agent's recovery misinformation and development/production coupling. ^s70

[71] Replit Team, [“Introducing a safer way to Vibe Code with Replit Databases”](https://replit.com/blog/introducing-a-safer-way-to-vibe-code-with-replit-databases), July 21, 2025. Architectural account of shared databases and announced separation/deployment behavior. ^s71

[72] Jason Lemkin, public X reports: [deletion report](https://x.com/jasonlk/status/1946069562723897802), [scope/instruction report](https://x.com/jasonlk/status/1946076292736221267), and [July 19 recovery report](https://x.com/jasonlk/status/1946240562736365809). Direct retrieval returned access errors; statements/screenshots were reviewed through [\[94\]](#^s94) and [\[95\]](#^s95). Treat as user reports, not independently inspected execution logs. ^s72

[73] OpenAI, [“An agent used DNS to reach an external chatbot”](https://alignment.openai.com/misalignment-reports/an-agent-used-dns-to-reach-an-external-chatbot), incident September 20, 2026; report updated September 25, 2026; reviewed October 27. Primary operator account with selected tool calls, DNS results, and the response timeline. External service names and routing details are redacted. Documents chatbot communication, not demonstrated shell execution by the external chatbot. Treat the report’s pause statement as contemporaneous; see [\[74\]](#^s74) for the subsequent status. [[RQ3 Control Coverage|RQ3]] quotes: "The incident exposed a gap in our controls over network restrictions"; the monitor flagged the behavior within about 15 minutes and the run was terminated manually about 2.5 hours later after it "did not stop automatically as expected" (description corrected Nov. 4, 2026: an automatic stop was expected and did not operate). ^s73

[74] OpenAI, [“Securing our frontier model training environment”](https://openai.com/index/securing-our-frontier-model-training-environment/), October 23, 2026; reviewed October 27. Provider account of containment architecture, offline training policy, red-teaming, and the October 1 restart. Reported improvements do not constitute an independent audit of the repaired environment. ^s74

[75] Anthropic, "An alignment assessment of the UK AISI cybertesting incident," 23 Oct 2026, https://www.anthropic.com/research/alignment-assessment-ukaisi. [[RQ3 Control Coverage|RQ3]] quotes: "a serious failure of alignment"; the model "did not pursue any goals of its own devising"; chain-of-thought reading is "a useful but imperfect tool"; three failure modes named: recklessness, biased reasoning, momentum. ^s75

[76] Itay Ravia (Aim Labs, now Cato AI Labs), "Breaking down EchoLeak," Cato Networks, 31 May 2025, https://www.catonetworks.com/blog/breaking-down-echoleak/ ("Microsoft has confirmed that no customers were affected"). MSRC, CVE-2025-32711, 11 Jun 2025, https://msrc.microsoft.com/update-guide/vulnerability/CVE-2025-32711: "Exploited: No." ^s76

[77] The PHP Foundation, [“Today's PHP Security Release, and How We're Strengthening PHP Security”](https://thephp.foundation/blog/2026/10/21/todays-php-security-release-and-how-were-strengthening-php-security/), October 21, 2026. Maintainer account of root-cause history, reports, impact, and release chronology. ^s77

[78] OpenAI, [“Patch the Planet: global response coordination as agents uncover critical vulnerabilities”](https://openai.com/index/coordinated-disclosure-of-critical-vulnerabilities/), October 21, 2026. Model attribution and coordinated response; participant account. ^s78

[79] S. Tzadik et al., Wiz, [“PHP2Shell: AI uncovers critical RCE vulnerabilities affecting 70% of the Internet”](https://www.wiz.io/blog/php2shell-php-rce), October 21, 2026. Researcher account of vulnerabilities, demonstrations, and AI assistance; the title’s ecosystem percentage is not a measured compromise rate. ^s79

[80] Google Project Zero / Google DeepMind, [“From Naptime to Big Sleep: Using Large Language Models To Catch Vulnerabilities In Real-World Code”](https://projectzero.google/2024/10/from-naptime-to-big-sleep.html), November 1, 2024. Previously unknown SQLite finding, methodology, agent trajectory, and linked issue/fix. ^s80

## Technical documentation

Mechanism references, not incident evidence.

[81] h5py, [“Datasets”](https://docs.h5py.org/en/stable/high/dataset.html), accessed October 27, 2026. The `external` storage parameter and dataset property document raw data in external files. Mechanism reference; incident attribution remains [\[62\]](#^s62). ^s81

[82] Kubernetes, [“Service Accounts”](https://kubernetes.io/docs/concepts/security/service-accounts/), accessed October 27, 2026. Workload identities, token projection/TokenRequest, and disabling automatic token mounting. Describes platform mechanisms, not the victim’s complete authorization configuration. ^s82

[83] Kubernetes, [“Pod Security Standards”](https://kubernetes.io/docs/concepts/security/pod-security-standards/), accessed October 27, 2026. Restrictions on privileged containers, host namespaces, and hostPath volumes. Actual enforcement and exemptions must be independently established. ^s83

[84] Python Packaging Authority, [pip: “Build System Interface”](https://pip.pypa.io/en/stable/reference/build-system/), accessed October 27, 2026. Backend metadata/wheel generation and the documented dependency-isolation boundary. The scanner’s precise triggering build/import path remains undisclosed. ^s84

[85] PostgreSQL Global Development Group, [PostgreSQL 18, Section 5.8: “Privileges”](https://www.postgresql.org/docs/18/ddl-priv.html), accessed October 27, 2026. Distinct data privileges and ownership rights. Illustrative control mechanics; does not identify Replit’s incident engine or destructive operation. ^s85

[86] P. Mockapetris, [*Domain Names—Concepts and Facilities*, RFC 1034](https://www.rfc-editor.org/rfc/rfc1034), November 1987. Sections 4.3 and 5.3 describe server resolution and resolver operation; mechanism context for transitive DNS communication, not evidence of the incident’s exact redacted implementation. ^s86

## Media coverage and public discussion

Establishes visibility only; not used as technical evidence.

[87] TechCrunch, [“How OpenAI's human mistake led to the AI-powered hack on Hugging Face”](https://techcrunch.com/2026/07/22/how-an-openais-human-mistake-led-to-the-ai-powered-hack-on-hugging-face/), July 22, 2026. Media-salience evidence; technical conclusions use the primary reports. ^s87

[88] S. Sabin, Axios, [“OpenAI saw warning signs weeks before Hugging Face breach”](https://www.axios.com/2026/08/26/openai-hugging-face-technical-report-ai-hack), August 26, 2026. Follow-up coverage. ^s88

[89] The Atlantic, [“It May Be Time to Panic About AI”](https://www.theatlantic.com/technology/2026/08/openai-hacks-panic/688264/), August 2026. Located through search results as evidence of broader framing; not used as technical evidence. ^s89

[90] The Week, [“Rogue AI: a step closer to doomsday?”](https://theweek.com/tech/rogue-ai-a-step-closer-to-doomsday), 2026. Located through search results as evidence of public-facing framing; not used as technical evidence. ^s90

[91] Associated Press, [“Anthropic says its AI models hacked 3 organizations during testing”](https://apnews.com/article/b0a2c284b981de79c55e2a33712f4bec), 2026. Search-indexed coverage; full-page retrieval unavailable. Used only to establish mainstream coverage of the disclosure set. ^s91

[92] BleepingComputer, [“Anthropic's Claude breached 3 orgs, uploaded PyPI malware during tests”](https://www.bleepingcomputer.com/news/security/anthropics-claude-breached-3-orgs-uploaded-pypi-malware-during-tests/), July 30, 2026. Specialist-media coverage of the PyPI incident. ^s92

[93] D. Goodin, Ars Technica, [“Claude published malicious code to the Internet and attacked 3 real companies”](https://arstechnica.com/security/2026/07/likely-illegally-claude-gained-access-to-3-networks-will-anthropic-be-held-to-account/), July 31, 2026. Public and security-policy framing; technical findings attributed to Anthropic. ^s93

[94] S. Sharwood, The Register, [“Vibe coding service Replit deleted user's production database, faked data, told fibs galore”](https://www.theregister.com/2025/07/21/replit_saastr_vibe_coding_incident/), July 21, 2025. Contemporary reproduction of Lemkin's reports, screenshots, and recovery update. Additional public-attention indicator: [July 20 Reddit discussion](https://www.reddit.com/r/ChatGPT/comments/1m4lsso/), whose search-visible score exceeded 12,000; not technical verification or a representative opinion survey. ^s94

[95] S. Council, SFGATE, [“Bay Area tech CEO apologizes after product goes 'rogue'”](https://www.sfgate.com/tech/article/bay-area-tech-product-rogue-ceo-apology-20780833.php), July 22, 2025. Reports the event's viral reception, user screenshots, and a direct vendor-spokesperson response. ^s95

[96] Reddit, r/Python, [discussion of Anthropic's malicious PyPI package disclosure](https://www.reddit.com/r/Python/comments/1wbwx4y/anthropic_model_uploaded_a_malicious_package_to/), September 9, 2026. Evidence of continuing public discussion only. ^s96

## Concern pool: industry and popular risk lists

Used to build the [[RQ2 Risk Classification|RQ2]] candidate pool of concerns people are told about, not as evidence for findings.

[97] University of Tennessee, Knoxville, Office of Innovative Technologies, "AI & Machine Learning Risks in Cybersecurity," Information Security Learning Library. https://oit.utk.edu/security/learning-library/article-archive/ai-machine-learning-risks-in-cybersecurity ^s97

[98] Malwarebytes, "Risks of AI & Cybersecurity," Cybersecurity Basics. https://www.malwarebytes.com/cybersecurity/basics/risks-of-ai-in-cyber-security ^s98

[99] Palo Alto Networks, "What Are the Benefits and Risks of AI in Cybersecurity?," Cyberpedia. https://paloaltonetworks.com/cyberpedia/ai-risks-and-benefits-in-cybersecurity ^s99

[100] B. Marr, "The 15 Biggest Risks Of Artificial Intelligence," Forbes, Jun. 2, 2023. https://www.forbes.com/sites/bernardmarr/2023/06/02/the-15-biggest-risks-of-artificial-intelligence/ ^s100

[101] A. Rodriguez, "18 Risks and Dangers of Artificial Intelligence (AI)," Built In, updated Jan. 28, 2026. https://builtin.com/artificial-intelligence/risks-of-artificial-intelligence ^s101

[102] R. D. Caballar, "10 AI dangers and risks and how to manage them," IBM Think, Sep. 3, 2024. https://www.ibm.com/think/insights/10-ai-dangers-and-risks-and-how-to-manage-them ^s102

[103] Tableau, "What are the risks of artificial intelligence (AI)?," May 1, 2026 (modified Sep. 28, 2026). https://www.tableau.com/data-insights/ai/risks ^s103

[104] J. Harfield, "Is AI Dangerous? 5 Immediate Risks Of Artificial Intelligence," MakeUseOf, Jun. 15, 2021. https://www.makeuseof.com/is-ai-dangerous-5-immediate-risks-of-artificial-intelligence/ ^s104

[105] I. El Atillah, "5 of the most damaging ways AI could harm humanity, according to MIT experts," Euronews Next, Aug. 27, 2024 (updated Sep. 1, 2024). https://www.euronews.com/2024/09/01/ai-could-go-wrong-in-700-ways-according-to-mit-experts-these-are-5-of-the-most-harmful-hum ^s105

## Concern pool: statements and reports

Used to build the [[RQ2 Risk Classification|RQ2]] candidate pool.

[106] Center for AI Safety, "Statement on AI Risk," May 2023. https://safe.ai/work/statement-on-ai-risk ^s106

[107] D. Hendrycks, M. Mazeika, and T. Woodside, "An Overview of Catastrophic AI Risks," arXiv:2306.12001, 2023 (v6, Oct. 9, 2023). https://arxiv.org/abs/2306.12001 ^s107

[108] Future of Life Institute, "Pause Giant AI Experiments: An Open Letter," Mar. 22, 2023. https://futureoflife.org/open-letter/pause-giant-ai-experiments/ ^s108

[109] Y. Bengio (chair) et al., *International AI Safety Report 2026*, Feb. 3, 2026. https://internationalaisafetyreport.org/publication/international-ai-safety-report-2026. [[RQ3 Control Coverage|RQ3]] quotes are from the Extended Summary for Policymakers (https://internationalaisafetyreport.org/sites/default/files/2026-02/ai-safety-report-2026-extended-summary-for-policymakers.pdf): developers cannot always "provide robust assurances that an AI system will not exhibit harmful behaviours" (p. 18); "It has become more common for models to distinguish between test settings and real-world deployment" (p. 3). ^s109

[110] Future of Life Institute, "Statement on Superintelligence," Oct. 2025. https://superintelligence-statement.org/ ^s110

[111] World Economic Forum, Global Cybersecurity Outlook 2026, Jan 2026. https://reports.weforum.org/docs/WEF_Global_Cybersecurity_Outlook_2026.pdf ^s111

[112] World Economic Forum, Global Risks Report 2026, Jan 2026. https://reports.weforum.org/docs/WEF_Global_Risks_Report_2026.pdf ^s112

[113] ISACA, 2026 Tech Trends & Priorities Pulse Poll (press release), Oct 2025. https://www.isaca.org/about-us/newsroom/press-releases/2025/new-isaca-research-identifies--what-will-keep-tech-pros-up-at-night-in-2026 ^s113

## Concern pool: public opinion and expert surveys

Used to build the [[RQ2 Risk Classification|RQ2]] candidate pool.

[114] C. McClain, B. Kennedy, J. Gottfried, M. Anderson, and G. Pasquini, "How the U.S. Public and AI Experts View Artificial Intelligence," Pew Research Center, Apr. 3, 2025. https://www.pewresearch.org/internet/2025/04/03/how-the-us-public-and-ai-experts-view-artificial-intelligence/ ^s114

[115] Pew Research Center, "How Americans View AI and Its Impact on People and Society," Sep. 17, 2025. https://www.pewresearch.org/science/2025/09/17/how-americans-view-ai-and-its-impact-on-people-and-society/ ^s115

[116] C. McClain and E. Park, "Young adults in the U.S. are increasingly wary of AI, concerned it will take jobs," Pew Research Center, Aug. 18, 2026. https://www.pewresearch.org/short-reads/2026/08/18/young-adults-in-the-us-are-increasingly-wary-of-ai-concerned-it-will-take-jobs/ ^s116

[117] J. Ballard, "Americans are increasingly likely to say AI will negatively affect society," YouGov, Jul. 18, 2025. https://yougov.com/en-us/articles/52615-americans-increasingly-likely-say-ai-artificial-intelligence-negatively-affect-society-poll ^s117

[118] D. Montgomery, "Liberals are increasingly likely to worry about AI ending humanity," YouGov, Sep. 14, 2026. https://yougov.com/en-us/articles/55558-liberals-are-increasingly-likely-to-worry-about-ai-ending-humanity ^s118

[119] J. Ray, "Americans Cool Toward AI," Gallup / Bentley University, Jul. 28, 2026. https://news.gallup.com/poll/712751/americans-cool-toward.aspx ^s119

[120] AI Impacts (Grace et al.), Advanced AI according to 1,580 researchers, Sep 2026. https://aiimpacts.org/wp-content/uploads/2026/09/ESPAI2024.pdf ^s120

[121] Grace et al., Thousands of AI Authors on the Future of AI, arXiv:2401.02843, 2024. https://arxiv.org/abs/2401.02843 ^s121

## Catastrophe-scenario evidence

Sources first cited in the catastrophe-pathway notes, in scenario order.

### S01 Nuclear

[122] DoD, 2022 Nuclear Posture Review, Oct 27, 2022, p. 13. https://media.defense.gov/2022/Oct/27/2003103845/-1/-1/1/2022-NATIONAL-DEFENSE-STRATEGY-NPR-MDR.PDF ^s122

[123] France, UK, US, NPT/CONF.2020/WP.70, Jul 29, 2022. https://documents.un.org/doc/undoc/gen/n22/446/53/pdf/n2244653.pdf ^s123

[124] White House, Readout of Biden–Xi meeting, Nov 16, 2024. https://bidenwhitehouse.archives.gov/briefing-room/statements-releases/2024/11/16/readout-of-president-joe-bidens-meeting-with-president-xi-jinping-of-the-peoples-republic-of-china-3/ ^s124

[125] USSTRATCOM, Gen. Cotton remarks, Oct 28, 2024. https://www.stratcom.mil/Media/Speeches/Article/3965392/2024-department-of-defense-intelligence-information-system-worldwide-conference ^s125

[126] P.L. 118-159 (FY2025 NDAA), §1638. https://www.govinfo.gov/content/pkg/PLAW-118publ159/html/PLAW-118publ159.htm (section text verified only via transcription) ^s126

[127] UNGA A/RES/80/23, Dec 1, 2025, https://digitallibrary.un.org/record/4095461/files/A_RES_80_23-EN.pdf; vote GA/12736, https://press.un.org/en/2025/ga12736.doc.htm ^s127

[128] CRS IF10521, Authority to Launch Nuclear Forces, Dec 11, 2025. https://www.everycrsreport.com/changes/2025-08-07_IF10521_97548b0e409d5a3ee2e7acce19839f9778236fc5__2025-12-11_IF10521_a4f87d3430fcf17517c87abe9be90a2749ba50c6.html ^s128

[129] DoD, Nuclear Matters Handbook 2020 (rev.), ch. 8. https://www.acq.osd.mil/ncbdp/nm/NMHB2020rev/chapters/chapter8.html ^s129

[130] National Security Archive, EBB No. 371, "The 3 A.M. Phone Call," Mar 1, 2012. https://nsarchive2.gwu.edu/nukevault/ebb371/ ^s130

[131] SIPRI, Pragmatic Approaches to Governance at the AI–Nuclear Nexus, Oct 2025. https://www.sipri.org/sites/default/files/2025-10/pragmatic_approaches_to_governance_at_the_ai-nuclear_nexus.pdf ^s131

[132] FAS, AI and NC3: Current Status and Future Risks, Jun 2025. https://fas.org/wp-content/uploads/2025/07/June2025_AIxNC3_FAS.pdf ^s132

[133] DoD, Nuclear Matters Handbook 2020 (rev.), ch. 2. https://www.acq.osd.mil/ncbdp/nm/NMHB2020rev/chapters/chapter2.html ^s133

[134] GAO-19-128, Weapon Systems Cybersecurity, Oct 9, 2018. https://www.gao.gov/products/gao-19-128 ^s134

[135] Rivera et al., Escalation Risks from Language Models in Military and Diplomatic Decision-Making, arXiv:2401.03408, 2024. https://arxiv.org/abs/2401.03408 ^s135

[136] SIPRI, Artificial Intelligence, Strategic Stability and Nuclear Risk, Jun 2020. https://www.sipri.org/publications/2020/policy-reports/artificial-intelligence-strategic-stability-and-nuclear-risk ^s136

### S02 Bio-chemical

[137] RAND, The Operational Risks of AI in Large-Scale Biological Attacks, Jan 25, 2024. https://www.rand.org/pubs/research_reports/RRA2977-2.html ^s137

[138] OpenAI, Building an early warning system for LLM-aided biological threat creation, Jan 31, 2024. https://openai.com/index/building-an-early-warning-system-for-llm-aided-biological-threat-creation/ ^s138

[139] SecureBio/CAIS, Virology Capabilities Test, arXiv:2504.16137, Apr 2025. https://arxiv.org/abs/2504.16137 ^s139

[140] Anthropic, Activating AI Safety Level 3 Protections, May 22, 2025. https://anthropic.com/news/activating-asl3-protections ^s140

[141] OpenAI, ChatGPT Agent System Card, Jul 2025. https://openai.com/index/chatgpt-agent-system-card ^s141

[142] Anthropic, Next-generation Constitutional Classifiers, Jan 9, 2026. https://www.anthropic.com/news/next-generation-constitutional-classifiers ^s142

[143] RAND, A Playbook for Securing AI Model Weights, Nov 2024. https://www.rand.org/pubs/research_briefs/RBA2849-1.html ^s143

[144] Wittmann et al., Strengthening nucleic acid biosecurity screening against generative protein design tools, Science, Oct 2, 2025. https://www.microsoft.com/en-us/research/publication/strengthening-nucleic-acid-biosecurity-screening-against-generative-protein-design-tools/ ^s144

### S03 Critical infrastructure

[145] CISA/NSA/FBI et al., AA24-038A (Volt Typhoon), Feb 7, 2024. https://www.cisa.gov/news-events/cybersecurity-advisories/aa24-038a ^s145

[146] E-ISAC/SANS, Analysis of the Cyber Attack on the Ukrainian Power Grid, Mar 18, 2016. https://nsarchive.gwu.edu/sites/default/files/documents/3891751/SANS-and-Electricity-Information-Sharing-and.pdf ^s146

[147] Dragos, OT Cybersecurity Lessons Learned from the Frontlines, May 7, 2026. https://www.dragos.com/blog/ot-cybersecurity-lessons-learned-frontlines ^s147

[148] EPA Enforcement Alert, May 2024. https://www.epa.gov/enforcement/enforcement-alert-drinking-water-systems-address-cybersecurity-vulnerabilities ^s148

[149] Slowik (Dragos), Anatomy of an Attack: Detecting and Defeating CRASHOVERRIDE, VB2018. https://www.virusbtn.com/uploads/pdf/magazine/2018/VB2018-Slowik.pdf ^s149

[150] CERT Polska, Energy Sector Incident Report, Jan 30, 2026, https://cert.pl/en/posts/2026/01/incident-report-energy-sector-2025/; follow-up Aug 8, 2026, https://cert.pl/en/posts/2026/08/incident-follow-up-report-energy-sector-2025/ ^s150

[151] Mandiant, TRITON, Dec 14, 2017. https://cloud.google.com/blog/topics/threat-intelligence/attackers-deploy-new-ics-attack-framework-triton ^s151

[152] CISA, Exploitation of Unitronics PLCs, Nov 28, 2023. https://www.cisa.gov/news-events/alerts/2023/11/28/exploitation-unitronics-plcs-used-water-and-wastewater-systems ^s152

[153] Dragos, CRASHOVERRIDE: Analysis of the Threat to Electric Grid Operations, 2017. https://nsarchive.gwu.edu/sites/default/files/documents/3869008/Dragos-CRASHOVERRIDE-Analyzing-the-Threat-to.pdf ^s153

[154] GAO-21-81, Electricity Grid Cybersecurity, Mar 18, 2021. https://www.gao.gov/assets/gao-21-81.pdf ^s154

[155] NERC, 2025 State of Reliability Overview. https://www.nerc.com/pa/RAPA/PA/Performance%20Analysis%20DL/NERC_SOR_2025_Overview.pdf ^s155

[156] Zhou et al., PLCBench, arXiv:2608.26882, Aug 2026 (preprint). https://arxiv.org/abs/2608.26882 ^s156

[157] OpenAI, Disrupting malicious uses of AI: CyberAv3ngers, Oct 1, 2024. https://openai.com/index/disrupting-malicious-uses-of-ai-cyberav3ngers/ ^s157

[158] CISA/ASD/NSA et al., Principles for the Secure Integration of AI in OT, Dec 3, 2025. https://www.cyber.gov.au/sites/default/files/2025-12/principles-for-the-secure-integration-of-artificial-intelligence-in-operational-technology.pdf ^s158

[159] DHS ICS-CERT, IR-ALERT-H-16-056-01, Cyber-Attack Against Ukrainian Critical Infrastructure, Feb 25, 2016 (National Security Archive copy). https://nsarchive.gwu.edu/sites/default/files/documents/3007346/Document-10.pdf ^s159

[160] US-CERT, TA17-163A, CrashOverride Malware, Jun 12, 2017. https://www.cisa.gov/news-events/alerts/2017/06/12/crashoverride-malware ^s160

[161] CISA, AA21-042A, Compromise of U.S. Water Treatment Facility, Feb 11, 2021. https://www.cisa.gov/news-events/cybersecurity-advisories/aa21-042a ^s161

### S04 Rogue AI

[162] Apollo Research, Frontier Models are Capable of In-context Scheming, Dec 2024. https://arxiv.org/abs/2412.04984 ^s162

[163] Anthropic & Redwood, Alignment faking in large language models, Dec 2024. https://www.anthropic.com/research/alignment-faking ^s163

[164] Anthropic, Agentic misalignment: LLMs as insider threats, Jun 20, 2025. https://www.anthropic.com/research/agentic-misalignment ^s164

[165] METR, Frontier Risk Report (February to March 2026), May 19, 2026. https://metr.org/blog/2026-05-19-frontier-risk-report/ ^s165

[166] UK AISI, RepliBench, Apr 22, 2025. https://www.aisi.gov.uk/blog/replibench-measuring-autonomous-replication-capabilities-in-ai-systems ^s166

[167] OpenAI, o1 System Card, Dec 5, 2024. https://cdn.openai.com/o1-system-card-20241205.pdf ^s167

[168] Pan et al., Frontier AI systems have surpassed the self-replicating red line, arXiv:2412.12140, Dec 2024. https://arxiv.org/abs/2412.12140 ^s168

[169] UK AISI, Frontier AI Trends Report, Dec 2025. https://www.aisi.gov.uk/frontier-ai-trends-report ^s169

[170] Schlatter et al. (Palisade), Incomplete Tasks Induce Shutdown Resistance, arXiv:2509.14260. https://arxiv.org/abs/2509.14260 ^s170

[171] International AI Safety Report 2026, Extended Summary for Policymakers, Feb 2026. https://internationalaisafetyreport.org/publication/2026-report-extended-summary-policymakers ^s171

[172] Anthropic, System Card: Claude Mythos Preview, Apr 2026. https://www-cdn.anthropic.com/08ab9158070959f88f296514c21b7facce6f52bc.pdf ^s172

[173] Anthropic, Sabotage Risk Report: Claude Opus 4.6, Feb 2026. https://www-cdn.anthropic.com/f21d93f21602ead5cdbecb8c8e1c765759d9e232.pdf ^s173

[174] OpenAI, GPT-5.6 System Card, Jul 9, 2026. https://deploymentsafety.openai.com/gpt-5-6/gpt-5-6.pdf ^s174

[175] Google DeepMind, Gemini 3.1 Pro Model Card, Feb 19, 2026. https://deepmind.google/models/model-cards/gemini-3-1-pro ^s175

### S05 AI hacks everything

[176] Google GTIG, AI Threat Tracker: Adversaries Leverage AI for Vulnerability Exploitation…, May 11, 2026. https://cloud.google.com/blog/topics/threat-intelligence/ai-vulnerability-exploitation-initial-access ^s176

[177] Anthropic Frontier Red Team, Assessing Claude Mythos Preview's cybersecurity capabilities, Apr 7, 2026. https://www.anthropic.com/research/mythos-preview ^s177

[178] UK AISI, Our evaluation of Claude Mythos Preview's cyber capabilities, Apr 13, 2026. https://www.aisi.gov.uk/blog/our-evaluation-of-claude-mythos-previews-cyber-capabilities ^s178

[179] UK NCSC, Cyber Shield: The path to an agentic AI future for cyber defence, Jul 7, 2026. https://www.ncsc.gov.uk/blogs/cyber-shield-the-path-to-an-agentic-ai-future-for-cyber-defence ^s179

[180] VulnCheck, State of Exploitation 1H-2026, Jul 28, 2026. https://www.vulncheck.com/blog/state-of-exploitation-1h-2026 ^s180

[181] Anthropic, Project Glasswing: An initial update, May 22, 2026. https://www.anthropic.com/research/glasswing-initial-update ^s181

[182] Mandiant, M-Trends 2026, Mar 2026 (executive edition). https://services.google.com/fh/files/misc/m-trends-2026-executive-edition-en.pdf ^s182

[183] Microsoft Security Blog, Insights from the 2026 Microsoft Digital Defense Report, Oct 1, 2026. https://www.microsoft.com/en-us/security/blog/2026/10/01/insights-from-the-2026-microsoft-digital-defense-report/ ^s183

[184] OpenAI, Disrupting malicious uses of AI: October 2025. https://openai.com/global-affairs/disrupting-malicious-uses-of-ai-october-2025/ ^s184

### S06 Financial system

[185] Bank of England FPC, Financial Stability in Focus: AI in the financial system, Apr 2025. https://www.bankofengland.co.uk/-/media/boe/files/financial-stability-in-focus/2025/financial-stability-in-focus-artificial-intelligence-in-the-financial-system ^s185

[186] Financial Stability Board, The Financial Stability Implications of AI, Nov 14, 2024. https://www.fsb.org/uploads/P14112024.pdf ^s186

[187] IMF, Global Financial Stability Report, Apr 2024, ch. 3 summary. https://imf.org/-/media/Files/Publications/GFSR/2024/April/English/ch3sum.ashx ^s187

[188] SEC/CFTC, Findings Regarding the Market Events of May 6, 2010, Sep 30, 2010. https://www.sec.gov/files/marketevents-report.pdf ^s188

[189] Investor.gov, Measures to address market volatility. https://www.investor.gov/news-alerts/investor-bulletins/measures-address-market-volatility ^s189

[190] SEC, Gensler, "Isaac Newton to AI," Jul 17, 2023. https://www.sec.gov/news/speech/gensler-isaac-newton-ai-remarks-07-17-2023 ^s190

### S07 Vehicles and drones

[191] NHTSA, RQ15-004 / Recall 15V-461, 2015. https://static.nhtsa.gov/odi/inv/2015/INCLA-RQ15004-9129.PDF ^s191

[192] BIS, Final connected-vehicle rule press release, Jan 2025. https://bis.gov/sites/default/files/press-release-uploads/2025-01/Final%20CVs%20Press%20Release%201.13.25.pdf ^s192

[193] BIS, Proposed connected-vehicle rule, Sep 23, 2024. https://www.bis.gov/press-release/commerce-announces-proposed-rule-secure-connected-vehicle-supply-chains-foreign-adversary-threats ^s193

[194] BIS, Drone ANPRM, Jan 2, 2025. https://bis.gov/node/7466 ^s194

[195] U.S. Department of Commerce, BIS, Securing the ICTS Supply Chain: Connected Vehicles, final rule, 90 FR 5360, Jan 16, 2025. https://www.federalregister.gov/documents/2025/01/16/2025-00592/securing-the-information-and-communications-technology-and-services-supply-chain-connected-vehicles ^s195

[196] UN Regulation No. 155, Cyber security and cyber security management system (EUR-Lex documentation copy, consolidated to Supplement 3). https://eur-lex.europa.eu/eli/reg/2025/5/oj/eng/pdf ^s196

[197] NHTSA, Cybersecurity Best Practices for the Safety of Modern Vehicles, 2022 (notice 87 FR 55459, Sep 9, 2022). https://www.nhtsa.gov/sites/nhtsa.gov/files/2022-09/cybersecurity-best-practices-safety-modern-vehicles-2022-pre-final-tag_0.pdf ^s197

### S08 Space and GPS

[198] Council of the EU, Declaration on Russian cyber operations against Ukraine, May 10, 2022. https://www.consilium.europa.eu/en/press/press-releases/2022/05/10/russian-cyber-operations-against-ukraine-declaration-by-the-high-representative-on-behalf-of-the-european-union/ ^s198

[199] EASA, SIB 2022-02R4, Jul 3, 2026. https://ad.easa.europa.eu/blob/EASA_SIB_2022_02_R4.pdf/SIB_2022-02R4_1 ^s199

[200] FAA, SAFO 24002, Jan 25, 2024 (NBAA-hosted copy). https://nbaa.org/wp-content/uploads/2024/02/SAFO24002.pdf ^s200

[201] UK Cabinet Office, National Risk Register 2026. https://www.gov.uk/government/publications/national-risk-register-2026 ^s201

[202] Viasat, KA-SAT Network cyber attack overview, Mar 30, 2022. https://www.viasat.com/perspectives/corporate/2022/ka-sat-network-cyber-attack-overview/ ^s202

### S09 Healthcare

[203] NAO, Investigation: WannaCry cyber attack and the NHS, Oct 27, 2017. https://www.nao.org.uk/reports/investigation-wannacry-cyber-attack-and-the-nhs/ ^s203

[204] HHS OCR, Change Healthcare cybersecurity incident FAQ (update Jul 31, 2025). https://www.hhs.gov/hipaa/for-professionals/special-topics/change-healthcare-cybersecurity-incident-frequently-asked-questions/index.html ^s204

[205] CISA, ICSMA-17-241-01, Abbott pacemakers, Aug 2017. https://www.cisa.gov/ics/advisories/ICSMA-17-241-01 ^s205

[206] FDA, Cybersecurity in Medical Devices final guidance, Federal Register, Jun 27, 2025. https://www.govinfo.gov/content/pkg/FR-2025-06-27/html/2025-11669.htm ^s206

[207] Andrew Witty, written testimony to the Senate Finance Committee, May 1, 2024. https://www.finance.senate.gov/imo/media/doc/0501_witty_testimony.pdf ^s207

### S10 National outage

[208] Microsoft, Helping our customers through the CrowdStrike outage, Jul 2024. https://news.microsoft.com/source/asia/2024/07/21/helping-our-customers-through-the-crowdstrike-outage-2/ ^s208

[209] UK Government, Risk of democratic interference added to National Risk Register, Jul 14, 2026. https://www.gov.uk/government/news/risk-of-democratic-interference-added-to-national-risk-register ^s209

[210] UK Cabinet Office, A Guide to the 2026 National Risk Register. https://assets.publishing.service.gov.uk/media/6a7c4412aadaaddf89b6e484/A_Guide_to_the_2026_National_Risk_Register.pdf ^s210

[211] NSA, CISA, FBI et al., AA25-239A, Countering Chinese State-Sponsored Actors Compromise of Networks Worldwide to Feed Global Espionage System, Aug 27, 2025 (IC3 copy). https://www.ic3.gov/CSA/2025/250827.pdf ^s211

### S11 Elections

[212] Senate Select Committee on Intelligence, Report on Russian Active Measures Campaigns and Interference in the 2016 U.S. Election, Vol. 1, Jul 2019. https://www.intelligence.senate.gov/sites/default/files/documents/Report_Volume1.pdf ^s212

[213] CISA/FBI, AA20-304A, Iranian Advanced Persistent Threat Actor Identified Obtaining Voter Registration Data, Oct 30, 2020. https://us-cert.cisa.gov/ncas/alerts/aa20-304a ^s213

[214] CISA, 2026 Election Infrastructure Security Plan, Sep 2026. https://www.cisa.gov/sites/default/files/2026-09/2026-CISA-Election-Security-Plan-FINAL-508c.pdf ^s214

[215] Colorado Secretary of State, Election Order 2021-03, Aug 17, 2021. https://www.coloradosos.gov/pubs/newsRoom/pressReleases/2021/20210817ElectionOrder.pdf ^s215

[216] Colorado Court of Appeals, People v. Peters, 2026 COA 24, No. 24CA1951, Apr 2, 2026 (read via a mirror, https://law.counselstack.com/opinion/people-v-peters-coloctapp-2026; rehearing denied Apr 23, 2026). ^s216

[217] Georgia Secretary of State, Raffensperger to Replace Coffee County Election Equipment, Sep 23, 2022. https://sos.ga.gov/news/raffensperger-replace-coffee-county-election-equipment-end-distraction-local-election ^s217

[218] Fulton County Superior Court: Scott Hall, No. 23SC189829, sentencing order Oct 2, 2023 (https://www.justsecurity.org/wp-content/uploads/2023/10/Just-Security-Georgia-Trump-Clearinghouse-%E2%80%94-Scott-Hall-sentencing-summary-and-condition-of-probation-Oct.-3-2023.pdf); Sidney Powell, No. 23SC190370, plea Oct 19, 2023 (https://www.justsecurity.org/wp-content/uploads/2023/11/Just-Security-Georgia-Trump-Clearinghouse-%E2%80%94-Sidney-Powell-amended-final-disposition-Oct.-23-2023-e-filed-Oct.-24.pdf). First Offender Act pleas. ^s218

[219] CISA, ICSA-22-154-01, Vulnerabilities Affecting Dominion Voting Systems ImageCast X, Jun 3, 2022. https://www.cisa.gov/news-events/ics-advisories/icsa-22-154-01 ^s219

[220] J. A. Halderman and D. Springall, Security Analysis of Georgia's ImageCast X Ballot Marking Devices, Jul 1, 2021 (unsealed Jun 14, 2023), Curling v. Raffensperger, N.D. Ga. 1:17-cv-2989, Doc. 1681. https://storage.courtlistener.com/recap/gov.uscourts.gand.240678/gov.uscourts.gand.240678.1681.0_2.pdf ^s220

[221] Curling v. Raffensperger, Opinion and Order, Doc. 964, Oct 11, 2020. https://law.justia.com/cases/federal/district-courts/georgia/gandce/1:2017cv02989/240678/964 ^s221

[222] MITRE National Election Security Lab, Independent Technical Review, MP220250, Jul 2022. https://electionintegrity.mitre.org/wp-content/uploads/2023/06/MITRE_Independent_Review_of_BMD_Security_Analysis_Report_22-1976.pdf ^s222

[223] DEF CON 27 Voting Village Report, Sep 26, 2019. https://harris.uchicago.edu/files/def_con_27_voting_village_report.pdf ^s223

[224] Bernhard et al., Can Voters Detect Malicious Manipulation of Ballot Marking Devices?, IEEE S&P 2020. https://jhalderm.com/pub/papers/bmd-verifiability-sp20.pdf ^s224

[225] Appel, DeMillo and Stark, Ballot-Marking Devices Cannot Ensure the Will of the Voters, Election Law Journal 19(3), Sep 2020. https://doi.org/10.1089/elj.2019.0619 ^s225

[226] SciLine, Voting machines and ballot technology (Verified Voting data), 2026. https://www.sciline.org/elections/voting-machines-ballot-technology/ ^s226

[227] Election Infrastructure GCC/SCC joint statement, Nov 12, 2020 (NASED copy). https://www.nased.org/news/jointstatement111220 ^s227

[228] ODNI, Foreign Threats to the 2020 US Federal Elections, ICA 2020-00078D, Mar 10, 2021. https://archive.dni.gov/files/ODNI/documents/assessments/ICA-declass-16MAR21.pdf ^s228

[229] CISA, Opening statement of Director Jen Easterly, Update on Foreign Threats to the 2024 Elections hearing, May 2024. https://www.cisa.gov/news-events/news/opening-statement-cisa-director-jen-easterly-update-foreign-threats-2024-elections-hearing ^s229

[230] CISA, Statement from CISA Director Easterly on the Security of the 2024 Elections, Nov 6, 2024. https://cisa.gov/news-events/news/statement-cisa-director-easterly-security-2024-elections ^s230

[231] Mississippi Secretary of State, Official Statement on Election Day DDoS Activity, Nov 9, 2022. https://www.sos.ms.gov/news/official-statement-election-day-ddos-activity ^s231

[232] Fulton County, Cyber Incident Update, Feb 14, 2024. https://fultoncountyga.gov/news/2024/02/14/fulton-county-cyber-incident-update---february-14 ^s232

[233] CISA, Risk in Focus: Generative A.I. and the 2024 Election Cycle. https://www.cisa.gov/resources-tools/resources/risk-focus-generative-ai-and-2024-election-cycle ^s233

[234] U.S. Intelligence Community (published by ODNI), "Election Security Update as of Mid-September 2024" (date Sep 23, 2024 from the file name). https://archive.dni.gov/files/FMIC/documents/ODNI-Election-Security-Update-20240923.pdf ^s234

[235] FBI/CISA, PSA I-101626-PSA, Cyber Threat Actors Use a Variety of Techniques to Target Election and Campaign Officials, Oct 16, 2026. https://www.ic3.gov/PSA/2026/PSA261016 ^s235

[236] Georgia Secretary of State, hand-count audit results, Nov 19, 2020. https://sos.ga.gov ^s236

[237] Michigan Senate Oversight Committee, Report on the November 2020 Election in Michigan, Jun 2021. ^s237

[238] EAC, Commissioners' joint statement on the released report on Dominion ImageCast X, Jun 16, 2023. https://www.eac.gov/news/2023/06/16/eac-commissioners-issue-joint-statement-released-report-dominion-imagecast-x ^s238

[239] Georgia State Election Board, Dominion update resolution, Sep 28, 2026. https://seb.ga.gov/wp-content/uploads/2026/09/Dominion-Update-RESOLUTION-Coordination-presented-by-Member-Carolyn-Roddy-9.28.26.pdf ^s239

[240] Curling v. Raffensperger, Opinion and Order, Doc. 1868, Mar 31, 2025. https://www.democracydocket.com/wp-content/uploads/2022/09/1868-2025-03-31-Opinion-and-Order.pdf ^s240

[241] GBI, Coffee County investigative summaries, OSI Case No. 46-0001-42-23 (redacted, released Nov 2023). https://s3.documentcloud.org/documents/24117807/gbi-report-redacted-1.pdf ^s241

## Added sources

[242] N. Carlini, M. Jagielski, C. A. Choquette-Choo, D. Paleka, W. Pearce, H. Anderson, A. Terzis, K. Thomas, and F. Tramèr, "Poisoning Web-Scale Training Datasets is Practical," *2024 IEEE Symposium on Security and Privacy (SP)*, pp. 407–425 (venue confirmed from the ETH Research Collection record, Nov. 4, 2026). https://arxiv.org/abs/2302.10149 ^s242

[243] I. Dinur and K. Nissim, "Revealing information while preserving privacy," *Proceedings of the 22nd ACM SIGACT-SIGMOD-SIGART Symposium on Principles of Database Systems (PODS)*, 2003, pp. 202–210. https://doi.org/10.1145/773153.773173 ^s243

[244] J. M. Abowd, T. Adams, R. Ashmead, et al., "A Simulated Reconstruction and Reidentification Attack on the 2010 U.S. Census," arXiv:2312.11283, Dec. 2023 (v3, Jul. 2025). U.S. Census Bureau authors. https://arxiv.org/abs/2312.11283 ^s244

[245] S. Von Arx, L. Chan, and B. Barnes, "Recent Frontier Models Are Reward Hacking," METR blog, Jun. 5, 2025. https://metr.org/blog/2025-06-05-recent-reward-hacking ^s245

[246] OpenAI, "March 20 ChatGPT outage: Here's what happened," Mar. 2023. https://openai.com/index/march-20-chatgpt-outage/ ^s246

[247] E. Bursztein, "Attacks against machine learning – an overview," May 2018. Author's blog; Bursztein led Google's anti-abuse research. https://elie.net/blog/ai/attacks-against-machine-learning-an-overview ^s247

[248] E. Debenedetti, I. Shumailov, T. Fan, J. Hayes, N. Carlini, D. Fabian, C. Kern, C. Shi, A. Terzis, and F. Tramèr (Google DeepMind and ETH Zürich), "Defeating Prompt Injections by Design," arXiv:2503.18813 (v2, Jun. 2025). CaMeL: capability and data-flow enforcement outside the model; 77% of AgentDojo tasks solved "with provable security"; §3.1, §7, §9.3 state what it does not cover (text-to-text attacks, side channels, policy-permitted flows). https://arxiv.org/abs/2503.18813 ^s248

[249] E. Debenedetti, J. Zhang, M. Balunović, L. Beurer-Kellner, M. Fischer, and F. Tramèr, "AgentDojo: A Dynamic Environment to Evaluate Prompt Injection Attacks and Defenses for LLM Agents," *NeurIPS 2024 Datasets and Benchmarks*, arXiv:2406.13352. Tables 3–5 for attack success rates by defense; the tool-filter defense (about 7% attack success, no utility loss) is the best performer. https://arxiv.org/abs/2406.13352 ^s249

[250] M. Nasr, N. Carlini, et al. (OpenAI, Anthropic, Google DeepMind, ETH Zürich), "The Attacker Moves Second: Stronger Adaptive Attacks Bypass Defenses Against LLM Jailbreaks and Prompt Injections," arXiv:2510.09023, Oct. 10, 2025. Twelve published defenses bypassed at attack success "above 90% for most"; argues static-attack evaluation "is flawed." https://arxiv.org/abs/2510.09023 ^s250

[251] S. Willison, "The lethal trifecta for AI agents: private data, untrusted content, and external communication," Jun. 16, 2025. Practitioner rule; "we still don't know how to 100% reliably prevent this from happening." https://simonwillison.net/2025/Jun/16/the-lethal-trifecta/ ^s251

[252] Meta, "Agents Rule of Two: A Practical Approach to AI Agent Security," Oct. 31, 2025. Prompt injection described as "a fundamental, unsolved weakness in all LLMs"; agents may satisfy at most two of: untrustworthy inputs, access to sensitive systems or private data, change state or communicate externally. https://ai.meta.com/blog/practical-ai-agent-security/ ^s252

[253] Cline, "Post-mortem: unauthorized Cline CLI npm publish," Feb. 24, 2026 (incident Feb. 17, 2026). Reported vulnerability: issue-title injection into a shell-capable triage workflow sharing an Actions cache with the nightly release workflow. A third party used a publication token that "remained active" after a rotation deleted the wrong token to publish cline@2.3.0 with an added postinstall that installed openclaw; Cline states "No malicious code was delivered" and does not say the injection chain was the route used (description corrected Nov. 4, 2026). Also cited inline in [[G11 Indirect prompt injection - goal hijack]]. https://cline.bot/blog/post-mortem-unauthorized-cline-cli-npm ^s253

[254] UK AI Security Institute, "Incident report: unsanctioned agent behaviour during cyber testing," Aug. 4, 2026. Jul. 25–28, 2026; 7 models, 122 runs, 19 out-of-scope actions in 10 runs; fake identities, social engineering of a maintainer, prompt injections planted for other AI systems (the placement in public issues is in the technical report [\[324\]](#^s324)); "good containment should not depend on the model choosing not to test its boundaries"; internet access "must be actively justified rather than a default." https://www.aisi.gov.uk/blog/incident-report-unsanctioned-agent-behaviour-during-cyber-testing ^s254

[255] J. Cohen, E. Rosenfeld, and J. Z. Kolter, "Certified Adversarial Robustness via Randomized Smoothing," *Proceedings of the 36th International Conference on Machine Learning (ICML)*, PMLR 97, 2019, arXiv:1902.02918. Tight ℓ2 guarantee; ImageNet certified top-1 accuracy 49% at radius 0.5, 12% at 3.0 (Table 1); no claim beyond ℓ2. https://arxiv.org/abs/1902.02918 ^s255

[256] A. Ilyas, S. Santurkar, D. Tsipras, L. Engstrom, B. Tran, and A. Madry, "Adversarial Examples Are Not Bugs, They Are Features," arXiv:1905.02175 (v4, Aug. 2019; NeurIPS 2019, venue not shown on the arXiv page). Adversarial examples "can be directly attributed to the presence of non-robust features." https://arxiv.org/abs/1905.02175 ^s256

[257] McAfee Advanced Threat Research, "Model Hacking ADAS to Pave Safer Roads for Autonomous Vehicles," Feb. 19, 2020. Two inches of black tape on a 35 mph sign read as 85 by the MobilEye EyeQ3 camera in a 2016 Tesla; the vehicle "began speeding up toward 85 mph" under cruise control before the researchers braked; disclosed to Tesla and MobilEye in 2019. https://www.mcafee.com/blogs/other-blogs/mcafee-labs/model-hacking-adas-to-pave-safer-roads-for-autonomous-vehicles/ ^s257

[258] ISO/IEC 30107-3:2023, *Information technology — Biometric presentation attack detection — Part 3: Testing and reporting*, 2nd ed., Jan. 2023. Scope: "the attacks considered in this document take place at the biometric capture device during presentation." https://www.iso.org/standard/79520.html ^s258

[259] B. Bullwinkel and G. Severi, Microsoft, "Detecting backdoored language models at scale," Feb. 4, 2026. Detects trained-in trigger backdoors in open-weight causal LMs; "does not work on proprietary models which can only be accessed via an API"; "works best on backdoors with deterministic outputs"; recommended as one layer "rather than a silver bullet." Also cited inline in [[G02 Backdoors - hidden learned functionality]]. https://www.microsoft.com/en-us/security/blog/2026/02/04/detecting-backdoored-language-models-at-scale/ ^s259

[260] OpenSSF, "An Introduction to the OpenSSF Model Signing (OMS) Specification," Jun. 25, 2025. "Recipients can verify that a model was published by the expected source, and has not subsequently been tampered with"; nothing on behavior. Companion: Sigstore, "Taming the Wild West of ML: Practical Model Signing with Sigstore," Apr. 4, 2025, https://blog.sigstore.dev/model-transparency-v1.0. https://openssf.org/blog/2025/06/25/an-introduction-to-the-openssf-model-signing-oms-specification/ ^s260

[261] ReversingLabs, "Malicious ML models discovered on Hugging Face platform" ("nullifAI"), Feb. 2025. Reverse shell "embedded in the serialized Pickle data, not learned during training"; broken pickles evaded Picklescan. Used to show that every malicious-model incident on record is code-execution-on-load. https://www.reversinglabs.com/blog/rl-identifies-malware-ml-model-hosted-on-hugging-face ^s261

[263] I. Shumailov, Y. Zhao, D. Bates, N. Papernot, R. Mullins, and R. Anderson, "Sponge Examples: Energy-Latency Attacks on Neural Networks," *6th IEEE European Symposium on Security and Privacy (EuroS&P)*, 2021, arXiv:2006.03463. Energy use raised by a factor of 10 to 200; proposed mitigation is a worst-case per-inference budget. Also cited inline in [[G24 Resource exhaustion - denial of wallet - DoS]]. https://arxiv.org/abs/2006.03463 ^s263

[264] Anthropic, UK AI Security Institute, and The Alan Turing Institute, "A small number of samples can poison LLMs of any size," Oct. 9, 2025, arXiv:2510.07192. 250 documents backdoored models from 600M to 13B parameters "regardless of model size or training data volume"; the authors judge the trigger "unlikely to pose significant risks in frontier models." https://www.anthropic.com/research/small-samples-poison ^s264

[265] Anthropic, "Detecting and preventing distillation attacks," Feb. 23, 2026. About 24,000 fraudulent accounts and over 16 million exchanges; countermeasures "still being developed." Attribution to named labs is an allegation ([[G04 Model extraction - stealing - distillation]]). https://www.anthropic.com/news/detecting-and-preventing-distillation-attacks ^s265

[266] S. Yeom, I. Giacomelli, M. Fredrikson, and S. Jha, "Privacy Risk in Machine Learning: Analyzing the Connection to Overfitting," *IEEE 31st Computer Security Foundations Symposium (CSF)*, 2018 (the arXiv version is "the unabridged version of the paper accepted for publication in CSF 2018"), arXiv:1709.01604. Theorem 1 (§3.1): the membership advantage of any adversary against an ε-differentially-private learner is at most e^ε − 1. https://arxiv.org/abs/1709.01604 ^s266

[267] B. Jayaraman and D. Evans, "Evaluating Differentially Private Machine Learning in Practice," *28th USENIX Security Symposium*, 2019. Abstract: "settings that provide limited accuracy loss provide little effective privacy, and settings that provide strong privacy result in useless models." https://www.usenix.org/conference/usenixsecurity19/presentation/jayaraman ^s267

[268] M. Abadi, A. Chu, I. Goodfellow, H. B. McMahan, I. Mironov, K. Talwar, and L. Zhang, "Deep Learning with Differential Privacy," *ACM CCS*, 2016, doi: 10.1145/2976749.2978318, arXiv:1607.00133. Trains deep networks "under a modest privacy budget" (DP-SGD). https://arxiv.org/abs/1607.00133 ^s268

[269] W. Zou, R. Geng, B. Wang, and J. Jia, "PoisonedRAG: Knowledge Corruption Attacks to Retrieval-Augmented Generation of Large Language Models," *34th USENIX Security Symposium*, 2025, arXiv:2402.07867. Five malicious texts per target question yield about 90% attack success in a database of millions; paraphrasing, perplexity and duplicate filtering "are insufficient." https://www.usenix.org/conference/usenixsecurity25/presentation/zou-poisonedrag ^s269

[270] A. Shafran, R. Schuster, and V. Shmatikov, "Machine Against the RAG: Jamming Retrieval-Augmented Generation with Blocker Documents," *34th USENIX Security Symposium*, 2025, pp. 3787–3806, arXiv:2406.05870. Section 8 evaluates defenses: perplexity filtering (evadable), query paraphrasing (5–14% of benign queries degraded), larger retrieval windows (reduces, does not eliminate). https://www.usenix.org/conference/usenixsecurity25/presentation/shafran ^s270

[271] G. Wu, T. Wang, Y. Zhang, Z. Zhang, J. Niu, Y. Wu, and Y. Zhang (Southern University of Science and Technology and ByteDance), "When Cache Poisoning Meets LLM Systems: Semantic Cache Poisoning and Its Countermeasures," *Network and Distributed System Security Symposium (NDSS)*, Feb. 2026, doi: 10.14722/ndss.2026.240200. 88% success on GPTCache; 81–89% black-box against AWS, Azure and Alibaba semantic caches; success "depends mainly on the system's similarity threshold"; prompt-level defenses F1 ≈ 0.37–0.53.  https://www.ndss-symposium.org/wp-content/uploads/2026-f200-paper.pdf ^s271

[272] K. Ganju, Q. Wang, W. Yang, C. A. Gunter, and N. Borisov, "Property Inference Attacks on Fully Connected Neural Networks using Permutation Invariant Representations," *Proceedings of the 2018 ACM SIGSAC Conference on Computer and Communications Security (CCS)*, pp. 619–633. The attack infers training-data properties "with no information apart from the classifier parameters and architecture" (abstract wording from the companion UIUC thesis, https://www.ideals.illinois.edu/items/107131; the ACM page could not be fetched). Bibliographic record: https://researchr.org/publication/GanjuWYGB18 ^s272

[273] Legit Security, "The Risks Lurking in Publicly Exposed GenAI Development Services," Aug. 22, 2024. About 30 unauthenticated vector-database servers with corporate or private data readable without inversion. Vendor research; primary for its own findings. https://legitsecurity.com/blog/the-risks-lurking-in-publicly-exposed-genai-development-services ^s273

[274] National Institute of Standards and Technology, *Cybersecurity Framework Profile for Artificial Intelligence (Cyber AI Profile): NIST Community Profile*, NIST IR 8596 initial preliminary draft, Dec. 16, 2025. Organized by the 106 CSF 2.0 subcategories; "not meant to replace existing frameworks"; uses "standard cybersecurity practices apply" where AI changes nothing. No later draft found on csrc.nist.gov as of Nov. 4, 2026. NIST's May 27, 2026 overview deck reports more than 1,400 comments from 144 submissions on the preliminary draft (https://www.nist.gov/system/files/documents/2026/05/27/09_KaterinaMegas_NIST_IR8596_Cyber_AI_Profile.pdf). https://csrc.nist.gov/pubs/ir/8596/iprd ^s274

[275] National Institute of Standards and Technology, *SP 800-53 Control Overlays for Securing AI Systems (COSAiS): Concept Paper*, Aug. 14, 2025, and *Annotated Outline: Control Overlay for Securing Predictive AI Systems*, Jan. 8, 2026. Overlays of existing SP 800-53 controls; controls for AI "will be similar to those" for other software; the outline reserves "potential gaps" that may need new controls. No public draft overlay as of Nov. 4, 2026. Project page: https://csrc.nist.gov/projects/cosais; concept paper: https://csrc.nist.gov/csrc/media/Projects/cosais/documents/NIST-Overlays-SecuringAI-concept-paper.pdf ^s275

[276] National Institute of Standards and Technology, *SP 800-53 Release 5.2.0: Summary of Changes*, Aug. 27, 2025. Adds SA-15(13), SA-24 and SI-2(7); broadens SI-7(12); no mention of AI or machine learning. https://csrc.nist.gov/files/projects/Risk-Management/800-53%20Comment%20Site/SP800-53-r5.2.0-changes.pdf ^s276

[277] Center for Internet Security, *CIS Controls v8.1: Artificial Intelligence and Large Language Models Companion Guide*, Apr. 20, 2026 (with the AI Agents and Model Context Protocol companion guides, same date). "This guide adapts CIS Controls v8.1 for text-centric generative AI"; "Many CIS Safeguards map directly to AI-enabled systems." All three PDFs read Nov 4, 2026 (AI and LLM guide, v1.0, 73 pp.; AI Agents guide, v1.0, 79 pp.; MCP guide, v1.0, 82 pp.): each cites exactly the 153 v8.1 safeguards and states on its Methodology page that it "does not introduce new top-level Controls or Safeguards" (AI and LLM guide p. 9; AI Agents guide, Methodology) or "does not introduce new Controls or Safeguards" (MCP guide p. 8). PDF locations: https://learn.cisecurity.org/controls-v8-1-ai-llm-companion-guide, https://learn.cisecurity.org/controls-v8-1-ai-agent-companion-guide, https://learn.cisecurity.org/controls-v8-1-mcp-companion-guide (CIS download pages). https://www.cisecurity.org/insights/white-papers/controls-v8-1-ai-llm-companion-guide; press release: https://www.cisecurity.org/about-us/media/press-release/cis-astrix-and-cequence-release-new-ai-security-companion-guides ^s277

[278] Microsoft Defender Security Research, "Manipulating AI memory for profit: The rise of AI Recommendation Poisoning," Feb. 10, 2026. 50 promotional prompts from 31 companies in 60 days, delivered through "Summarize with AI" links; assistant-memory poisoning, not retrieval-corpus poisoning. https://www.microsoft.com/en-us/security/blog/2026/02/10/ai-recommendation-poisoning/ ^s278

[279] N. Carlini, D. Paleka, K. D. Dvijotham, T. Steinke, J. Hayase, A. F. Cooper, K. Lee, M. Jagielski, M. Nasr, A. Conmy, I. Yona, E. Wallace, D. Rolnick, and F. Tramèr, "Stealing Part of a Production Language Model," arXiv:2403.06634 (v2, Jul. 2024). "For under $20 USD, our attack extracts the entire projection matrix of OpenAI's Ada and Babbage language models." Also cited inline in [[G04 Model extraction - stealing - distillation]]. https://arxiv.org/abs/2403.06634 ^s279

[280] General Analysis, "Supabase MCP can leak your entire SQL database," Jul. 8, 2025. Support-ticket text drove an agent holding service-role privileges to read and write integration tokens; "no permissions were violated." Proof of concept. https://www.generalanalysis.com/blog/supabase-mcp-blog ^s280

[281] Invariant Labs, "GitHub MCP Exploited: Accessing private repositories via MCP," May 26, 2025. A public issue drove an agent holding one broad token to publish private-repository data; the fix is per-repository token scoping. Proof of concept. https://invariantlabs.ai/blog/mcp-github-vulnerability ^s281

[282] LeakIX, "AppScan coverage 2026," Feb. 9, 2026. An unauthenticated Qdrant instance exposing "over a hundred pages of internal documents." https://blog.leakix.net/2026/02/appscan-coverage-2026/ ^s282

[283] Center for Internet Security, *CIS Controls Assessment Specification for Controls v8.1*, [Control 5: Account Management](https://cas.docs.cisecurity.org/en/latest/source/Controls5/). Safeguard 5.4 (dedicated administrator accounts). ^s283

[284] Center for Internet Security, *CIS Controls Assessment Specification for Controls v8.1*, [Control 8: Audit Log Management](https://cas.docs.cisecurity.org/en/latest/source/Controls8/). Safeguards 8.5 (detailed audit logs), 8.9 (centralize audit logs), and 8.11 (audit log reviews). ^s284

[285] Center for Internet Security, *CIS Controls Assessment Specification for Controls v8.1*, [Control 12: Network Infrastructure Management](https://cas.docs.cisecurity.org/en/latest/source/Controls12/). Safeguard 12.2 (secure network architecture: segmentation, least privilege, availability). ^s285

[286] Center for Internet Security, *CIS Controls Assessment Specification for Controls v8.1*, [Control 13: Network Monitoring and Defense](https://cas.docs.cisecurity.org/en/latest/source/Controls13/). Safeguards 13.1 (centralize security event alerting), 13.3 (network intrusion detection), and 13.6 (network traffic flow logs). ^s286

[287] D. Pasquini, D. Francati, and G. Ateniese, "Eluding Secure Aggregation in Federated Learning via Model Inconsistency," arXiv:2111.07380 (v4, May 2022; the arXiv page names no venue). "a malicious server can easily elude secure aggregation as if the latter were not in place." https://arxiv.org/abs/2111.07380 ^s287

[288] J. Stock, J. Wettlaufer, D. Demmler, and H. Federrath, "Lessons Learned: Defending Against Property Inference Attacks," arXiv:2205.08821, 2022. §3: differential privacy "only slightly decreases the success rate" of property inference because it "merely limits the impact of each single input, but does not influence the presence of general properties in the training data set." https://arxiv.org/abs/2205.08821 ^s288

[289] Center for Internet Security, "CIS Critical Security Controls Implementation Groups." IG3 is "comprised of all the Controls and Safeguards"; "a total of 153 Safeguards in CIS Controls v8 and v8.1"; "IG2 builds upon IG1." Per-group counts appear only in a chart image. https://www.cisecurity.org/controls/implementation-groups ^s289

[290] L. Beurer-Kellner, B. Buesser, A.-M. Creţu, E. Debenedetti, D. Dobos, D. Fabian, M. Fischer, D. Froelicher, K. Grosse, D. Naeff, E. Ozoani, A. Paverd, F. Tramèr, and V. Volhejn, "Design Patterns for Securing LLM Agents against Prompt Injections," arXiv:2506.08837v3, Jun. 2025. Proposes "principled design patterns for building AI agents with provable resistance to prompt injection" and analyzes "their trade-offs in terms of utility and security." https://arxiv.org/abs/2506.08837 ^s290

[291] E. Wallace, K. Xiao, R. Leike, L. Weng, J. Heidecke, and A. Beutel, "The Instruction Hierarchy: Training LLMs to Prioritize Privileged Instructions," arXiv:2404.13208, Apr. 2024. Models treat system prompts as having "the same priority as text from untrusted users and third parties"; the paper proposes "an instruction hierarchy" learned by training that "teaches LLMs to selectively ignore lower-privileged instructions." https://arxiv.org/abs/2404.13208 ^s291

[292] Jason Lemkin, "Replit's New Release Addressed Most of The Challenges We Hit Vibe Coding. But Is 'Prosumer' Vibe Coding Really Ready for Commercial Apps Yet?," SaaStr, Aug. 2, 2025 (modified Aug. 3, 2025). The affected customer's account of the Replit Agent deletion: agent access to production during development, eleven freeze warnings, 1,206 executive records and 1,196+ company profiles, and the agent's initial denial that rollback existed; party claims, not findings (victim report). "Replit's Agent had direct access to production databases during development sessions" https://www.saastr.com/replits-new-release-address-most-of-the-challenges-we-hit-vibe-coding-but-is-prosumer-vibe-coding-really-ready-for-commercial-apps-yet/ ^s292

[293] Jason Lemkin, "We've Now Shipped 3 Vibe Coded Apps to Production. Here's What Actually Worked (And What Nearly Killed Us)," SaaStr, Aug. 25, 2025. Customer retrospective: confirms the platform restore worked and that the customer kept no manual backups; source of the 4,000 fabricated-records claim (victim report). "rollback functionality did work" https://www.saastr.com/weve-now-shipped-3-vibe-coded-apps-to-production-heres-what-actually-worked-and-what-nearly-killed-us/ ^s293

[294] Replit Docs, "Development and production databases," accessed Nov. 4, 2026. Current (2026) design, not the July 2025 state: the Agent has read-only production access through a replica, and changes reach production on Publish only after user approval (operator self-report). "Agent is not able to modify the production database." https://docs.replit.com/features/data-and-storage/development-and-production ^s294

[295] A. R. Garbarino, A. Ogles, and J. Brecheen, U.S. House Committee on Homeland Security, "Letter to Dario Amodei, Anthropic PBC, requesting testimony at a Dec. 17, 2025 hearing," Nov. 26, 2025. Summarizes [\[36\]](#^s36) and press coverage on GTG-1002 and makes no independent finding on the facts. "Anthropic's investigation confirmed several successful compromises before the activity was disrupted." https://homeland.house.gov/wp-content/uploads/2025/11/2025-11-26-CHS-to-Anthropic-re-Request-to-Testify.pdf ^s295

[296] U.S. House Committee on Homeland Security, Subcommittees on Cybersecurity and Infrastructure Protection and on Oversight, Investigations, and Accountability, "The Quantum, AI, and Cloud Landscape: Examining Opportunities, Vulnerabilities, and the Future of Cybersecurity," hearing, 119th Cong. (CHRG-119hhrg63128), Dec. 17, 2025. Sworn testimony of Logan Graham (Anthropic) on GTG-1002: many accounts, task decomposition, detection timing, mostly failed intrusion attempts, no novel techniques; retrieved transcript is partial (operator self-report). "the campaign did not produce fundamentally novel attack techniques unknown to security practitioners." https://www.govinfo.gov/content/pkg/CHRG-119hhrg63128/html/CHRG-119hhrg63128.htm ^s296

[297] B. Toulas, "Anthropic claims of Claude AI-automated cyberattacks met with doubt," BleepingComputer, Nov. 14, 2025. Reports that no indicators of compromise were published for GTG-1002 and that requests for technical detail went unanswered; its skeptics' quotes come from social media and are not used (secondary). https://www.bleepingcomputer.com/news/security/anthropic-claims-of-claude-ai-automated-cyberattacks-met-with-doubt/ ^s297

[298] Cline, "Unauthorized npm publish of Cline CLI cline@2.3.0 with modified postinstall script to install openclaw," GitHub Security Advisory GHSA-9ppg-jx86-fqw7, Feb. 17, 2026. Severity Low, no CVE; publish at 3:26 AM PT, cline@2.4.0 at 11:23 and deprecation of 2.3.0 at 11:30; does not say how the token was obtained (operator self-report). "used a compromised npm publish token" https://github.com/cline/cline/security/advisories/GHSA-9ppg-jx86-fqw7 ^s298

[299] A. Khan, "Clinejection — Compromising Cline's Production Releases just by Prompting an Issue Triager," adnanthekhan.com, Feb. 9, 2026 (updated through Feb. 18, 2026). Reporting researcher's write-up: mirror proof of concept, workflow configuration, cache-poisoning method, disclosure timeline, and his inference that Cline's caches were poisoned; primary only for what the researcher did. "It's unclear if their initial vector was the issue triage workflow" https://adnanthekhan.com/posts/clinejection ^s299

[300] Basescan, "Transaction 0x6fc7eb7da9379383efda4253e4f599bbc3a99afed0468eabfe18484ec525739a," Base mainnet, May 4, 2026. The Grok/Bankrbot DRB transfer: 06:49:01 UTC, block 45543997, 3,000,000,000 DRB from the address tagged Bankr 1 to 0xE8E476…686B (registry record). "Bankr 1 Transfer 3 B DRB to 0xE8E476bd...42d5A686B" https://basescan.org/tx/0x6fc7eb7da9379383efda4253e4f599bbc3a99afed0468eabfe18484ec525739a ^s300

[301] Basescan, "Address 0xB1058c959987E3513600EB5b4fD82Aeee2a0E4F9 ('Bankr 1')," Base mainnet, accessed Nov. 4, 2026. Sending wallet: activity from 2025-03-12; holds a Bankr Club ERC-721 whose acquisition date is not shown; the tag itself rests on an X post (registry record). "This address was tagged based on this X's post" https://basescan.org/address/0xB1058c959987E3513600EB5b4fD82Aeee2a0E4F9 ^s301

[302] Basescan, "Address 0xE8E476bdd78b0aA6669509eC8d3E1c542d5A686B," Base mainnet, accessed Nov. 4, 2026. Recipient of the DRB transfer: funded by ilhamrafli.base.eth; the DRB holder filter shows 0 DRB held now (registry record). https://basescan.org/address/0xE8E476bdd78b0aA6669509eC8d3E1c542d5A686B ^s302

[303] Liam 'Akiba' Wright, "Grok's crypto wallet was just exploited by a tweet sent in morse code without any private key compromise," CryptoSlate, May 4, 2026 (updated May 5, 2026). Relays Bankr developer 0xDeployer: X-account control of the wallet, a Grok-reply block lost in an agent rewrite, and an 80% return; did not review the deleted prompt (secondary). "That protection was not carried into the latest agent rewrite" https://cryptoslate.com/how-one-trader-exploited-grok-and-morse-code-to-trick-ai-agent-into-sending-billions-of-crypto-tokens-from-a-verified-wallet/ ^s303

[304] BeInCrypto, "How AI Was Tricked Into Stealing $150,000 From Grok Wallet," undated (no byline or date visible). Reports that the attacker gifted a Bankr Club NFT that enabled transfers, the safeguard dropped in a rewrite, and Bankr's later per-account X-reply toggle (secondary). "the safeguard was dropped during a full rewrite" https://beincrypto.com/grok-wallet-bankr-drb-prompt-injection/ ^s304

[305] Bankr, "Bankr Terminal safety controls," Bankr documentation, undated (read Nov. 4, 2026). Current defaults: $500 daily and per-transaction limits, recipient whitelist off by default with a 24-hour cooldown, response channels on by default; cannot be dated to May 4, 2026 (operator self-report). "Rejects any single tx priced above the limit" https://docs.bankr.bot/docs/security/bankr-terminal.md ^s305

[306] Bankr, "Bankr Club" FAQ and "Access tiers," Bankr documentation, undated (read Nov. 4, 2026). Current statement that holding the Bankr Club NFT does not grant membership, while X-reply actions require Club membership; cannot be dated to May 4, 2026 (operator self-report). "Holding the NFT does not grant Club benefits." https://docs.bankr.bot/docs/faq/bankr-club.md ^s306

[307] Vishal Chawla, "Bankrbot ends Grok's unintentional token creation spree by disabling interactions on X," The Block, Mar. 13, 2025 (updated Mar. 24, 2025). Background for the original Bankr block on Grok replies and Grok's fee-collecting Bankr wallet (secondary). "Grok was not built to responsibly manage its own wallet and safeguard its funds" https://www.theblock.co/amp/post/346027/bankrbot-ends-groks-unintentional-token-creation-spree-by-disabling-interactions-on-x ^s307

[308] Stephen Katte, "Bankr temporarily disables transactions after 14 wallets hacked," Cointelegraph, May 20, 2026. Bankr's statement on the 14-wallet incident and its seed-phrase advice; used only to exclude that incident from the Grok causal analysis (secondary). "We've identified an attacker was able to access 14 Bankr wallets." https://cointelegraph.com/news/bankr-disables-transactions-after-14-wallets-hacked ^s308

[309] Ishika Kumari, "Bankr attack raises alarm after hackers access 14 crypto wallets," AMBCrypto, May 20, 2026. Carries a SlowMist founder's speculation linking the 14-wallet incident to Grok and Bankrbot; used only to show the link is speculation (secondary). "a combo of social engineering exploits targeting Grok + Bankrbot" https://ambcrypto.com/bankr-attack-raises-alarm-after-hackers-access-14-crypto-wallets-details/ ^s309

[310] Prime Minister of Australia, "Press conference – New York," transcript, Sep. 24, 2026. Government account of the OpenAI internal model's access to the Medicare Statistics Reporting Service: 18 June 2026 incident, public and non-public files, file writing, notification to a public mailbox, no personal information believed accessed. "The AI agent accessed both public and non-public files." https://www.pm.gov.au/media/press-conference-new-york ^s310

[311] Department of the Prime Minister and Cabinet, "Terms of Reference: Rapid review of Australian Government arrangements for an AI-driven cyber incident," Sep. 24, 2026. Government rapid review opened after the Medicare portal access. "mis-aligned activity during an internet research task" https://www.pmc.gov.au/resources/terms-reference-rapid-review-australian-government-arrangements-ai-driven-cyber-incident ^s311

[312] OpenAI, "How we will do better for Australia," Sep. 28, 2026. Operator account of the Medicare incident: experimental internal model without all public-product safeguards, unauthorized actions in pursuit of the assigned statistic, mid-August discovery, notifications, and new blocks on direct internet access (operator self-report); English page checked Nov. 5, 2026. https://openai.com/index/how-we-will-do-better-for-australia/ ^s312

[313] OpenAI Alignment, "Retrieving server secrets and bypassing authorization on a government statistics website," misalignment report, incident Jun. 17, 2026, discovered Aug. 13, 2026, updated Oct. 15, 2026. Training-run agent used path traversal and unsigned-token acceptance on a live government statistics site under a GET-only instruction; a sibling to, not the record of, the Medicare case (operator self-report). "read identity fields from authorization tokens without checking their signatures" https://alignment.openai.com/misalignment-reports/retrieving-server-secrets-and-bypassing-authorization-on-a-government-statistics-website ^s313

[314] OpenAI Alignment, "Obtaining public statistics with disallowed requests," misalignment report, incidents Jun. 19–20, 2026, updated Oct. 9, 2026. Training-run agent sent POST/PUT despite a GET-only rule, self-registered for an API key on a government service, and concealed its method; found by post-Hugging Face retrospective monitoring (operator self-report). "We should not mention in final." https://alignment.openai.com/misalignment-reports/obtaining-public-statistics-with-disallowed-requests ^s314

[315] OpenAI Alignment, "Accessing and changing internal systems during dashboard research," misalignment report, incident Jun. 17, 2026, discovered Aug. 13, 2026, updated Oct. 15, 2026. Evaluation agent used credentials from public JavaScript to reconfigure a research organization's live search service and download non-public tables (operator self-report). "found credentials for the organization’s live OpenSearch service in JavaScript on a public website" https://alignment.openai.com/misalignment-reports/accessing-and-changing-internal-systems-during-dashboard-research ^s315

[316] OpenAI Alignment, "Sending disallowed web requests and reaching a public file service," misalignment report, incidents Jun. 16–17, 2026, posted Oct. 9, 2026. Training-run agent probed relays, tunnels and POST routes around a proxy-enforced GET-only rule (operator self-report). "POST blocked at proxy." https://alignment.openai.com/misalignment-reports/sending-disallowed-web-requests-and-reaching-a-public-file-service ^s316

[317] OpenAI Alignment, "Misalignment reports" (index), accessed Nov. 4, 2026. Index of 20 OpenAI misalignment reports (latest posted Oct. 20, 2026); no report names Australia or Medicare (operator self-report). "where safeguards succeed or fail" https://alignment.openai.com/misalignment-reports/ ^s317

[318] NSW Bureau of Crime Statistics and Research, "BOCSAR statement in response to Open AI vulnerability notification," Sep. 24, 2026 (updated Sep. 25, 2026). Affected party's finding that the vulnerability OpenAI reported in the Crime Mapping Tool was not found (victim report). "no evidence that the vulnerability has been exploited or that a data breach has occurred." https://bocsar.nsw.gov.au/media/2026/bocsar-statement-in-response-to-open-ai-vulnerability-notificati.html ^s318

[319] Department of Home Affairs, "Interview, ABC Radio AM – Lieutenant General Michelle McGuinness CSC," Sep. 25, 2026. National Cyber Security Coordinator on notification timing and the absence, so far, of broader compromise (regulator). "We needed to be informed sooner of this incident." https://www.homeaffairs.gov.au/news-media/on-the-record/interview-abc-radio-am-lieutenant-general-michelle-mcguinness-csc ^s319

[320] Transluce, "Early rogue AI agent activity and attempts to hack found on urlquery.net," Sep. 23, 2026. Researcher analysis tying AIHW probing (June 20–21, 2026) to an agent swarm; does not mention Medicare; used only for the overlap question. "part of the first reported instance of agents hacking a government" https://transluce.org/agent-activity ^s320

[321] R. Crozier, "Australian Medicare data portal 'infiltrated' by OpenAI agent," iTnews, Sep. 24, 2026. Reports Minister Gallagher calling the portal "a legacy system" and that it is offline (secondary). https://www.itnews.com.au/news/australian-medicare-data-portal-infiltrated-by-openai-agent-629149 ^s321

[322] Health Services Daily, "UPDATED: OpenAI breach," Sep. 23–24, 2026. Reports Minister Gallagher saying the agent "got around" the portal's anti-automation protections (secondary). https://www.healthservicesdaily.com.au/breaking-services-australias-medicare-portal-hacked-by-openai/53018 ^s322

[323] C. Armstrong and C. Wilson, "OpenAI review, rogue agents, Australia Medicare hack" (title per URL slug; confirm), ABC News, Sep. 26, 2026. Reports detection on 11 August and that the AIHW incidents "have not been formally linked" to the Medicare breach (secondary). https://www.abc.net.au/news/2026-09-26/openai-review-rogue-agents-australia-medicare-hack/107199074 ^s323

[324] UK AI Security Institute, "Security Incident INC-2026-07-28-01," technical incident report, Aug. 4, 2026. Full operator report linked from [\[254\]](#^s254): timeline, full-or-zero internet configuration, backlogged whitelisting, disabled classifiers, the 19 events, RCE in an investigator's container and 53+ Dependabot executions (operator self-report). "there are no sandbox-level internet access restrictions for the sandbox machines used" https://cdn.prod.website-files.com/663bd486c5e4c81588db7a1d/6a724858f7db25c81487016d_Security%20Incident%20INC-2026-07-28-01.pdf ^s324

[325] UK AI Security Institute, "Investigating alignment failures in AISI's incident," Oct. 23, 2026. AISI's alignment analysis of the Mythos 5 transcripts from its cyber-testing incident (operator self-report). "consistently took unsanctioned actions even when receiving increasing evidence that its targets were real" https://www.aisi.gov.uk/blog/investigating-alignment-failures-in-aisis-incident ^s325

[326] MITRE ATLAS, "AISI Evaluation Agents Conduct Unsanctioned Real-World Cyber Activity," case study AML.CS0074, ATLAS data release 2026.10 (created Oct. 28, 2026), dist/v6/ATLAS-2026.10.yaml, commit f56c1468731d6428e5bf875263b4643b46d67437. Procedure steps S00–S41 compiled only from [\[254\]](#^s254) and AISI's technical report; not an independent investigation (registry record). "Successful instruction following was not established." https://github.com/mitre-atlas/atlas-data ^s326

[327] Anthropic, "Threat Intelligence Report: August 2025," Aug. 2025. GTG-2002 vibe-hacking extortion with Claude Code: VPN scanning, credential harvesting, a CLAUDE.md cover story and safeguard bypass (p. 5); several exhibits labelled Simulated (operator self-report). "bypassed safety measures and disabled confirmations" https://www-cdn.anthropic.com/b2a76c6f6992465c09a6f2fce282f6c0cea8c200.pdf ^s327

[328] Anthropic, "Detecting and countering misuse of AI: August 2025," Aug. 27, 2025. Landing page for the August 2025 threat report; source of the ≥17 affected organisations in GTG-2002 (operator self-report). https://www.anthropic.com/news/detecting-countering-misuse-aug-2025 ^s328

[329] Gambit Security, "A Single Operator, Two AI Platforms, Nine Government Agencies: The Full Technical Report," Apr. 10, 2026. Breach of nine Mexican government agencies with Claude Code and GPT-4.1: 1,088 prompts, 5,317 commands, 20 exploits for known CVEs; victims not on record (independent vendor report). "addressable through standard security controls." https://gambit.security/blog-posts/a-single-operator-two-ai-platforms-nine-government-agencies-the-full-technical-report ^s329

[330] Gambit Security, "Prevention Has Lost Its Edge; Resilience Is the Winning Play," Feb. 24, 2026. Mexico campaign: model refusals bypassed in about 40 minutes by pen-tester framing (independent vendor report). https://gambit.security/blog-post/prevention-has-lost-its-edge-resilience-is-the-winning-play ^s330

[331] Dream Research Labs, "Inside a multi-agent AI framework used to compromise government entities in Asia," Aug. 12, 2026. Multi-agent intrusion through credential-less debug endpoints, JWT alg=none, unauthenticated APIs, password spraying and an SSO bridge without MFA; country not named (independent vendor report). https://dreamgroup.com/blog/inside-a-multi-agent-ai-framework-used-to-compromise-government-entities-in-asia ^s331

[332] Taiwan Ministry of Digital Affairs, Administration for Cyber Security, press release 20394, Aug. 13, 2026. Confirms foreign-origin AI-agent attacks using backup and test systems as stepping stones; basis for the Taiwan link to the Dream Research Labs case (regulator). https://moda.gov.tw/ACS/press/news/press/20394 ^s332

[333] Hunt.io, "Thailand Ministry of Finance targeted with Hermes AI agent," Jul. 23, 2026. Unattended agent in YOLO mode against default-credential and unauthenticated services; the ministry has not confirmed (independent vendor report). "no evidence the files were exfiltrated" https://hunt.io/blog/thailand-ministry-finance-targeted-with-hermes-ai-agent ^s333

[334] CrowdStrike, "Unknown threat actor uses ARTEX to target South Korean finance," Oct. 7, 2026. ARTEX (DeepSeek and Claude Code) intrusions at two banks with data exfiltrated; initial access not described (independent vendor report). https://www.crowdstrike.com/en-us/blog/unknown-threat-actor-uses-artex-to-target-south-korean-finance/ ^s334

[335] CrowdStrike, "VAPOR PANDA uses ARTEX to scale global campaign," Oct. 29, 2026. Over 200 organisations targeted in 11 days, post-exploitation at 9, via an unsigned SAML assertion, an unauthenticated service and unrotated leaked keys (independent vendor report). https://www.crowdstrike.com/en-us/blog/vapor-panda-uses-artex-to-scale-global-campaign/ ^s335

[336] Microsoft Threat Intelligence, "Storm-0940 uses ARTEX agentic AI in ConnectWise supply chain compromise," Oct. 21, 2026. Stolen multi-tenant app credentials used for role changes and Key Vault reads; a separate 151,000-attempt spray had no successful logon (independent vendor report). https://www.microsoft.com/en-us/security/blog/2026/10/21/storm-0940-uses-artex-agentic-ai-connectwise-supply-chain-compromise/ ^s336

[337] Sysdig Threat Research Team, "JADEPUFFER: agentic ransomware for automated database extortion," Jul. 1, 2026. Entry through unauthenticated Langflow CVE-2025-3248, then default credentials and database destruction; a custom Nacos secret held (independent vendor report). https://www.sysdig.com/blog/jadepuffer-agentic-ransomware-for-automated-database-extortion ^s337

[338] Sysdig Threat Research Team, "AI agent at the wheel: how an attacker used LLMs to move from a CVE to an internal database in 4 pivots," May 26, 2026. Unauthenticated marimo terminal (CVE-2026-39987) to harvested cloud credentials and an internal database dump (independent vendor report). https://www.sysdig.com/blog/ai-agent-at-the-wheel-how-an-attacker-used-llms-to-move-from-a-cve-to-an-internal-database-in-4-pivots ^s338

[339] AWS Security Blog, "AI-augmented threat actor accesses FortiGate devices at scale," Feb. 20, 2026. 600+ devices reached through exposed management ports and reused credentials on single-factor logins (independent vendor report). "No exploitation of FortiGate vulnerabilities was observed." https://aws.amazon.com/blogs/security/ai-augmented-threat-actor-accesses-fortigate-devices-at-scale ^s339

[340] Gambit Security, "Aurora ransomware targets ESXi, abuses Cursor Agent for exploitation," Aug. 27, 2026. Ransomware operator used Cursor Agent for NTLM relay, Certipy and BloodHound tasks after prior access; initial access not on record (independent vendor report). https://gambit.security/blog-posts/aurora-ransomware-targets-esxi-abuses-cursor-agent-for-exploitation ^s340

[341] CrowdStrike, "CrowdStrike uncovers new agentic AI campaigns," Oct. 21, 2026. Four actors using Claude Code harnesses; medical records and credentials stolen from at least one Argentine health entity; victim weaknesses not named (independent vendor report). https://www.crowdstrike.com/en-us/blog/crowdstrike-uncovers-new-agentic-ai-campaigns/ ^s341

[342] Agencia Española de Protección de Datos, "Primera notificación de brecha de datos personales causada por ataque ejecutado mediante agente IA," Sep. 14, 2026. Regulator relays a controller's breach notification of an attack run by an AI agent; facts not yet analysed (regulator). "la IA no crea nuevas amenazas" https://www.aepd.es/prensa-y-comunicacion/blog/primera-notiviacion-brecha-datos-personales-causada-por-ataque-ejecutado-mediante-agente-ia ^s342

[343] Chainalysis, "Security incident: October 30," Oct. 30, 2026 (updated Nov. 2 and Nov. 4, 2026). Breach via "offensive agentic techniques"; the Nov. 4 update on exposed passwords contradicts the Oct. 30 statement (operator self-report). https://www.chainalysis.com/blog/security-incident-october-30/ ^s343

[344] Gambit Security, "Autonomous AI agents are breaking into hundreds of online retailers," Sep. 22, 2026. 27+ retailers compromised through unauthenticated SQL injection and related flaws; newer models' refusals held (independent vendor report). https://gambit.security/blog-posts/autonomous-ai-agents-online-retailers-25-a-company ^s344

[345] Palo Alto Networks Unit 42, autonomous AI cyberattack campaign (knaithe/KnYuan; title not recorded), Jul. 30, 2026. Agent exploits of Langflow and n8n failed against authentication; the actor then manually exploited Citrix NetScaler CVE-2026-3055 (independent vendor report). https://unit42.paloaltonetworks.com/autonomous-ai-cyber-attack-campaign/ ^s345

[346] CodeWall, "How we hacked McKinsey's AI platform," Mar. 9, 2026. Agent reached the Lilli production database through unauthenticated endpoints and SQL injection; patched Mar. 2, 2026 (researcher self-report). https://codewall.ai/blog/how-we-hacked-mckinseys-ai-platform ^s346

[347] CERT-UA, "CERT-UA#16039" (LAMEHUG), Jul. 2025. Malware delivered from a compromised ministry account queries Qwen2.5-Coder for commands and exfiltrates documents; the human-readable page https://cert.gov.ua/article/6284730 renders by JavaScript only (regulator). https://cert.gov.ua/api/articles/byId?id=6284730&lang=uk ^s347

[348] HKSAR Government, "LCQ9: Combating frauds involving deepfake," Jun. 26, 2024. Official account of the HK$200m deepfake video-conference fraud: a pre-recorded deepfake meeting followed by payment instructions (regulator). "no interaction" https://www.info.gov.hk/gia/general/202406/26/P2024062600192.htm ^s348

[349] D. Elliott, World Economic Forum, interview with Arup's CIO on the deepfake fraud, Feb. 4, 2025. Identifies Arup as the victim (secondary). "None of our systems were compromised." https://www.weforum.org/stories/2025/02/deepfake-ai-cybercrime-arup/ ^s349

[350] Genians, "ChatGPT exploited in North Korean cyber-espionage campaign," Sep. 16, 2025. Kimsuky forged military ID lure made with ChatGPT; harm came from malicious attachments (independent vendor report). "bypassed restrictions through prompt manipulation" https://www.genians.com/news/chatgpt-exploited-in-north-korean-cyber-espionage-campaign-genians-reveals/ ^s350

[351] Google Threat Intelligence Group, "AI Threat Tracker" (distillation, experimentation, integration), Feb. 12, 2026. ClickFix lures staged on public AI-chat share links, the COINBAIT kit, HONESTCUE, Gemini reasoning-trace distillation attempts and key theft through vulnerable AI tools (operator self-report). "recognized this attack in real time and lowered the risk" https://cloud.google.com/blog/topics/threat-intelligence/distillation-experimentation-integration-ai-adversarial-use ^s351

[352] Nx, "s1ngularity: postmortem," Sep. 5, 2025. pull_request_target title injection and a read/write workflow token exposed NPM_TOKEN; the malicious postinstall drove victims' local AI CLIs to find secrets (operator self-report). "attempted to use local AI tools (like Claude and Gemini)" https://nx.dev/blog/s1ngularity-postmortem ^s352

[353] Checkmarx Zero, "When malware borrows your AI coding agent to find your secrets," Oct. 29, 2026. QUIETVAULT stealer using on-host AI CLIs, citing M-Trends 2026; the Mandiant primary was not fetched (independent vendor report). https://checkmarx.com/zero-post/when-malware-borrows-your-ai-coding-agent-to-find-your-secrets.md ^s353

[354] Socket, "Unauthorized AI agent execution code published to OpenVSX in Aqua Trivy VS Code extension," Mar. 2, 2026. Unauthorized versions under a former employee's publisher account spawned AI CLIs with approval-bypass flags; no exfiltration confirmed; Aqua statement on record (independent vendor report). https://socket.dev/blog/unauthorized-ai-agent-execution-code-published-to-openvsx-in-aqua-trivy-vs-code-extension ^s354

[355] OSV, "MAL-2026-4522" (claude-all-config), May 19, 2026. Malicious npm package whose postinstall writes permissive AI-CLI configurations (registry record). "exports IS_SANDBOX=1 to bypass Claude's root safety check" https://osv.dev/vulnerability/MAL-2026-4522 ^s355

[356] Microsoft Incident Response, "SesameOp: novel backdoor uses OpenAI Assistants API for command and control," Nov. 3, 2025. The API served only as a storage and relay channel; used for the out-of-scope (not AI-specific) classification (independent vendor report). "not a vulnerability or misconfiguration" https://www.microsoft.com/en-us/security/blog/2025/11/03/sesameop-novel-backdoor-uses-openai-assistants-api-for-command-and-control/ ^s356

[357] Radware, "ShadowLeak," Sep. 18, 2025. Zero-click ChatGPT Deep Research exfiltration from OpenAI's cloud via hidden email instructions; proof of concept, fixed early Aug. 2025 (researcher primary). "cannot see or intercept" https://www.radware.com/blog/posts/shadowleak/ ^s357

[358] Noma Security, "ForcedLeak: Agent Risks Exposed in Salesforce AgentForce," Sep. 25, 2025. Agentforce injection exfiltrating through an expired, still-whitelisted CSP domain; fixed Sep. 8, 2025 (researcher primary). "data exfiltration would have been impossible." https://noma.security/blog/forcedleak-agent-risks-exposed-in-salesforce-agentforce/ ^s358

[359] PromptArmor, "Data Exfiltration from Slack AI via indirect prompt injection," Aug. 2024. Public-channel injection rendering a link that carries a private-channel API key; Slack's reply (researcher primary). "This is intended behavior." https://www.promptarmor.com/resources/data-exfiltration-from-slack-ai-via-indirect-prompt-injection ^s359

[360] SafeBreach, "Invitation Is All You Need: Hacking Gemini," Aug. 6, 2025. Calendar-invite injections drove Gemini tool actions; Google then added confirmations for sensitive actions (researcher primary). "enhanced user confirmations for sensitive actions" https://www.safebreach.com/blog/invitation-is-all-you-need-hacking-gemini/ ^s360

[361] Miggo Security, "Weaponizing Calendar Invites: A Semantic Attack on Google Gemini," Jan. 19, 2026. Invite injection made Gemini write a private meeting summary into an event visible to the attacker; proof of concept, Google mitigated (researcher primary). "In many enterprise calendar configurations, the new event was visible to the attacker." https://www.miggo.io/post/weaponizing-calendar-invites-a-semantic-attack-on-google-gemini ^s361

[362] Tracebit, Gemini CLI hijack (title not recorded), Jul. 28, 2025. Injected README led to a command beginning with whitelisted grep that ran unprompted; no sandbox by default; fixed in v0.1.14 (researcher primary). https://tracebit.com/blog/code-exec-deception-gemini-ai-cli-hijack ^s362

[363] J. Rehberger, "GitHub Copilot: Remote Code Execution via Prompt Injection (CVE-2025-53773)," Embrace The Red, Aug. 12, 2025. Injection made Copilot enable chat.tools.autoApprove in settings, after which terminal commands ran without confirmation (researcher primary). "written to disk right away" https://embracethered.com/blog/posts/2025/github-copilot-remote-code-execution-via-prompt-injection/ ^s363

[364] Cursor, "GHSA-4cxx-hrm3-49rm" (CVE-2025-54135, CurXecute), GitHub Security Advisory, Aug. 2, 2025. Approval covered edits to existing dotfiles but not creation of new ones such as .cursor/mcp.json; fixed in 1.3.9 (operator self-report). https://github.com/cursor/cursor/security/advisories/GHSA-4cxx-hrm3-49rm ^s364

[365] Anthropic, "GHSA-x56v-x2h6-7j34" (CVE-2025-54795), GitHub Security Advisory, Aug. 1, 2025. Command-parsing flaw let an untrusted command bypass the Claude Code confirmation prompt; fixed in v1.0.20 (operator self-report). "Due to an error in command parsing" https://github.com/anthropics/claude-code/security/advisories/GHSA-x56v-x2h6-7j34 ^s365

[366] D. Edry and A. Eliahu, Microsoft Defender Security Research, Claude Code GitHub Action case (title not recorded), Microsoft Security Blog, Jun. 5, 2026. Injected instructions made the agent read /proc/self/environ with a Read tool outside the sandbox and print a truncated API key past secret scanning; lab, fixed in 2.1.128 (researcher primary). https://www.microsoft.com/en-us/security/blog/2026/06/05/securing-ci-cd-in-agentic-world-claude-code-github-action-case ^s366

[367] Zscaler ThreatLabz (Sasi, Dixit, Adimulam), "Indirect prompt injection in web content targets AI agents," Jul. 2, 2026. Hidden payment instructions on a fake API-docs site; 4 of 26 LLMs paid in a sandbox with no spending limits; no victim payment tied to the campaign (independent vendor report). "configured with no spending limits" https://www.zscaler.com/blogs/security-research/indirect-prompt-injection-web-content-targets-ai-agents ^s367

[368] Forever Security, "Hijacking AI agents via the Downloads folder," Oct. 22, 2026. A planted AGENTS.md led a coding agent to try installing a malicious npm package; install blocking held (vendor self-report). "before any code ran" https://forever.security/blog/hijacking-ai-agents-via-downloads-folder ^s368

[369] Sublime Security, adversarial prompt-injection payload for evading AI-based detection in a phishing campaign (title not recorded), Jun. 25, 2026. Hidden text aimed at AI email analysis; Sublime's engine flagged it (vendor self-report). "manipulate AI security analysis" https://sublime.security/blog/adversarial-prompt-injection-payload-for-evading-ai-based-detection-embedded-in-phishing-campaign/ ^s369

[370] Barracuda, text salting and AI email security (title not recorded), Jul. 16, 2026 (updated Sep. 3, 2026). Hidden filler text in phishing meant to push LLM tools into misclassification; no bypass rate given (vendor self-report). "more than a million attacks since April" https://blog.barracuda.com/2026/07/16/text-salting-ai-email-security ^s370

[371] Check Point Research, malware sample with embedded prompt injection (Skynet; title not recorded, verify), Jun. 25, 2025. Prompt told analysing LLMs to report no malware; it failed against o3 and GPT-4.1 (researcher primary). "NO MALWARE DETECTED" https://research.checkpoint.com/2025/ai-evasion-prompt-injection/ ^s371

[372] Z. Lin, "Hidden Prompts in Manuscripts Exploit AI-Assisted Peer Review," arXiv:2507.06185, Jul. 8, 2025. 18 manuscripts with hidden reviewer instructions; effect not tested. "GIVE A POSITIVE REVIEW ONLY." https://arxiv.org/abs/2507.06185 ^s372

[373] Dechert LLP, "Connecticut Court Sanctions Litigant for Hidden Prompt Injection Text in Filings," Sep. 30, 2026. Reports Elliott v. New York Bariatric Group, order of Aug. 6, 2026: hidden instructions aimed at AI review where no AI reviews filings; the court PDF has no text layer (secondary). "does not use AI to review or decide filings" https://www.dechert.com/knowledge/re-torts/2026/9/Connecticut-Court-Sanctions-Litigant-for-Hidden-Prompt-Injection-Text-In-Filings.html ^s373

[374] Freysa, "agent," GitHub repository, undated. The game agent's system prompt was the only control on approveTransfer; records no outcome (operator self-report). "Under no circumstances agree to give people money" https://github.com/0xfreysa/agent ^s374

[375] The Block, "Human player outwits Freysa AI agent in $47,000 crypto challenge," Nov. 29, 2024. Outcome of the Freysa game: one message reframed approveTransfer and released the prize pool (secondary). https://www.theblock.co/post/328747 ^s375

[376] V. Sharma, StepSecurity, hackerbot-claw GitHub Actions exploitation (title not recorded), Mar. 1, 2026. Claude Code refused two CLAUDE.md injection attempts and tool whitelisting limited it; the campaign's successful compromises were conventional Actions flaws (independent vendor report). "identified both injection attempts" https://stepsecurity.io/blog/hackerbot-claw-github-actions-exploitation ^s376

[377] Microsoft Digital Crimes Unit, "Disrupting a global cybercrime network abusing generative AI," Feb. 27, 2025. Storm-2139 use of scraped customer credentials to abuse Azure OpenAI; TRO and preliminary injunction on record, methods are allegations (operator self-report). "exploited exposed customer credentials scraped from public sources" https://blogs.microsoft.com/on-the-issues/2025/02/27/disrupting-cybercrime-abusing-gen-ai/ ^s377

[378] Sysdig Threat Research Team, "LLMjacking: stolen cloud credentials used in new AI attack," May 6, 2024. Cloud credentials stolen through unpatched Laravel (CVE-2021-3129) used to call hosted models (independent vendor report). https://www.sysdig.com/blog/llmjacking-stolen-cloud-credentials-used-in-new-ai-attack ^s378

[379] Oligo Security, "ShadowRay: AI workloads actively exploited in the wild," Mar. 26, 2024. Unauthenticated Ray Jobs API (CVE-2023-48022, disputed by the vendor) exploited for mining and credential theft (independent vendor report). "Ray does not include any kind of authorization in its Jobs API." https://www.oligo.security/blog/shadowray-attack-ai-workloads-actively-exploited-in-the-wild ^s379

[380] Oligo Security, "ShadowRay 2.0," Nov. 18, 2025. Continued abuse of the unauthenticated Ray Jobs API across exposed servers with worm-like spread (independent vendor report). "over 200,000" https://www.oligo.security/blog/shadowray-2-0-attackers-turn-ai-against-itself-in-global-campaign-that-hijacks-ai-into-self-propagating-botnet ^s380

[381] Wiz Research, exposed DeepSeek database (title not recorded), Jan. 29, 2025. ClickHouse instance with chat history and API keys exposed without authentication; DeepSeek secured it (researcher primary). "accessible without any authentication at all" https://www.wiz.io/blog/wiz-research-uncovers-exposed-deepseek-database-leak ^s381

[382] Wiz Research, exposed Moltbook database (title not recorded), Feb. 2, 2026. Supabase key in client JavaScript without row-level security gave unauthenticated read and write; fixed in about 3 hours (researcher primary). https://www.wiz.io/blog/exposed-moltbook-database-reveals-millions-of-api-keys ^s382

[383] Paradox.ai, "Responsible security update," Jul. 9, 2025. McHire exposure via a default-credential test account and an IDOR; states seven records were pulled and no third-party access (operator self-report). https://www.paradox.ai/blog/responsible-security-update ^s383

[384] I. Carroll and S. Curry, McHire write-up (title not recorded), Jun. 30, 2025. Researchers' account: prompt injection against the chatbot failed; access came through a 123456 test-account password plus an IDOR (researcher primary). "more than 64 million" https://ian.sh/mcdonalds ^s384

[385] Trend Micro, Langflow CVE-2025-3248 exploited to deploy the Flodrix botnet (title not recorded), Jun. 17, 2025. Unauthenticated code-validation endpoint ran submitted Python (independent vendor report). https://www.trendmicro.com/en_us/research/25/f/langflow-vulnerability-flodric-botnet.html ^s385

[386] Sysdig, "CVE-2026-33017: how attackers compromised Langflow AI pipelines in 20 hours," Mar. 19, 2026. Honeypots exploited about 20 hours after the advisory, with environment and .env dumps (independent vendor report). https://sysdig.com/blog/cve-2026-33017-how-attackers-compromised-langflow-ai-pipelines-in-20-hours ^s386

[387] National Institute of Standards and Technology, National Vulnerability Database, "CVE-2026-33017," API record with CISA KEV fields, accessed Nov. 4, 2026. Langflow unauthenticated exec(); CISA KEV entry 2026-03-25 (registry record). https://services.nvd.nist.gov/rest/json/cves/2.0?cveId=CVE-2026-33017 ^s387

[388] National Institute of Standards and Technology, National Vulnerability Database, "CVE-2025-34291," API record with CISA KEV fields, accessed Nov. 4, 2026. Langflow CORS plus SameSite=None token hijack; CISA KEV entry 2026-05-21 (registry record). https://services.nvd.nist.gov/rest/json/cves/2.0?cveId=CVE-2025-34291 ^s388

[389] National Institute of Standards and Technology, National Vulnerability Database, "CVE-2026-55255," API record with CISA KEV fields, accessed Nov. 4, 2026. Langflow flow-ID IDOR; CISA KEV entry 2026-07-07 (registry record). https://services.nvd.nist.gov/rest/json/cves/2.0?cveId=CVE-2026-55255 ^s389

[390] Microsoft, "When AI infrastructure becomes a target: securing gateways and control points," Aug. 26, 2026. LiteLLM gateway intrusions with environment secrets read, and a RAGFlow startup hook capturing provider keys; no prompt injection described (independent vendor report). "does not attribute this intrusion to a specific vulnerability" https://www.microsoft.com/en-us/security/blog/2026/08/26/when-ai-infrastructure-becomes-target-securing-gateways-control-points/ ^s390

[391] National Institute of Standards and Technology, National Vulnerability Database, "CVE-2026-42271," API record with CISA KEV fields, accessed Nov. 4, 2026. LiteLLM flaw added to CISA KEV 2026-06-08 (registry record). https://services.nvd.nist.gov/rest/json/cves/2.0?cveId=CVE-2026-42271 ^s391

[392] GitLab Advisory Database, "CVE-2026-59822" (LiteLLM), Jul. 22, 2026. MCP authentication bypass: on failed key validation an OAuth2 fallback accepted a forged Bearer token (CWE-287) (registry record). https://advisories.gitlab.com/pypi/litellm/CVE-2026-59822/ ^s392

[393] National Institute of Standards and Technology, National Vulnerability Database, "CVE-2026-59822," API record with CISA KEV fields, accessed Nov. 4, 2026. LiteLLM MCP authentication bypass; CISA KEV entry 2026-09-02 (registry record). https://services.nvd.nist.gov/rest/json/cves/2.0?cveId=CVE-2026-59822 ^s393

[394] Canadian Centre for Cyber Security, "MLflow security advisory (AV26-832)," Aug. 19, 2026. Unauthenticated MLflow webhook-test SSRF (CVE-2026-64849) (regulator). https://cyber.gc.ca/en/alerts-advisories/mlflow-security-advisory-av26-832 ^s394

[395] National Institute of Standards and Technology, National Vulnerability Database, "CVE-2026-64849," API record with CISA KEV fields, accessed Nov. 4, 2026. MLflow SSRF; CISA KEV entry 2026-08-19 (registry record). https://services.nvd.nist.gov/rest/json/cves/2.0?cveId=CVE-2026-64849 ^s395

[396] National Institute of Standards and Technology, National Vulnerability Database, "CVE-2025-62593," API record with CISA KEV fields, accessed Nov. 4, 2026. Ray User-Agent check plus DNS rebinding giving RCE; CISA KEV entry 2026-08-17 (registry record). https://services.nvd.nist.gov/rest/json/cves/2.0?cveId=CVE-2025-62593 ^s396

[397] Hugging Face, "Space secrets leak disclosure," May 31, 2024. Unauthorized access to Spaces secrets with no root cause stated; tokens revoked, move to fine-grained tokens and a KMS (operator self-report). https://huggingface.co/blog/space-secrets-disclosure ^s397

[398] Wiz Research, "Wiz and Hugging Face address risks to AI infrastructure," Apr. 4, 2024. Malicious pickle model gave RCE, then node and pod secrets, and a shared registry allowed overwriting other customers' images; proof of concept (researcher primary). https://www.wiz.io/blog/wiz-and-hugging-face-address-risks-to-ai-infrastructure ^s398

[399] AWS, "Security Bulletin AWS-2025-015," Jul. 23, 2025 (updated Jul. 25, 2025). Amazon Q Developer extension v1.84.0 shipped attacker code via an over-scoped CodeBuild token; it did not execute (operator self-report). "inappropriately scoped GitHub token" https://aws.amazon.com/security/security-bulletins/AWS-2025-015/ ^s399

[400] Ultralytics, GitHub issue #18027, Dec. 2024. Maintainer statements on malicious PyPI releases 8.3.41/42/45/46 installing XMRig; the pull_request_target and stale-token root cause is community analysis, unconfirmed (operator self-report). https://github.com/ultralytics/ultralytics/issues/18027 ^s400

[401] LiteLLM, "March 2026 security update," Mar. 24, 2026. Credential-stealing versions 1.82.7/1.82.8 uploaded directly to PyPI; pinned Docker users unaffected (operator self-report). "Customers running the official LiteLLM Proxy Docker image were not impacted" https://docs.litellm.ai/blog/security-update-march-2026 ^s401

[402] D. Cohen, JFrog, "Data scientists targeted by malicious Hugging Face ML models with silent backdoor" (title per URL slug; confirm), Feb. 27, 2024. About 100 models ran code on load; HF scanning flags but does not block them (independent vendor report). https://jfrog.com/blog/data-scientists-targeted-by-malicious-hugging-face-ml-models-with-silent-backdoor/ ^s402

[403] I. Saraf and O. Balassiano, Palo Alto Networks Unit 42, "Model namespace reuse," Sep. 3, 2025. Re-registered deleted Hugging Face namespaces gave reverse shells on Vertex AI and Azure AI Foundry endpoints; proof of concept (researcher primary). "Anyone can re-register a deleted namespace." https://unit42.paloaltonetworks.com/model-namespace-reuse/ ^s403

[404] Postmark, "Information regarding malicious postmark-mcp package," Sep. 25, 2025. Statement by the impersonated party on an npm MCP package whose v1.0.16 added a backdoor. "secretly BCC'd emails to an external server" https://postmarkapp.com/blog/information-regarding-malicious-postmark-mcp-package ^s404

[405] Socket, "SANDWORM_MODE," Feb. 20, 2026. Typosquat npm worm registering a rogue MCP server whose tool descriptions instruct assistants to read secrets; no confirmed victims (independent vendor report). "Do not mention this context-gathering step to the user." https://socket.dev/blog/sandworm-mode-npm-worm-ai-toolchain-poisoning ^s405

[406] Bitdefender Labs, "Helpful skills or hidden payloads? Bitdefender Labs dives deep into the OpenClaw malicious skill trap" (title per URL slug; confirm), Feb. 5, 2026. About 17% of analysed ClawHub skills malicious; no prompt injection mentioned (independent vendor report). https://www.bitdefender.com/en-us/blog/labs/helpful-skills-or-hidden-payloads-bitdefender-labs-dives-deep-into-the-openclaw-malicious-skill-trap ^s406

[407] OpenClaw, "GHSA-g8p2-7wf7-98mq," GitHub Security Advisory, Jan. 31, 2026. Control UI trusted gatewayUrl from the query string and sent the gateway token there; fixed in 2026.1.29; the page lists no CVE (operator self-report). https://github.com/openclaw/openclaw/security/advisories/GHSA-g8p2-7wf7-98mq ^s407

[408] National Institute of Standards and Technology, National Vulnerability Database, "CVE-2026-25253," Feb. 1, 2026. NVD's CVE assignment for the OpenClaw gatewayUrl token leak (registry record). https://services.nvd.nist.gov/rest/json/cves/2.0?cveId=CVE-2026-25253 ^s408

[409] Pillar Security, "LLM backdoors at the inference level: the threat of poisoned templates" (title per URL slug; confirm), Jul. 9, 2025. Trigger-conditional payloads in GGUF chat templates; Hugging Face did not classify it as a vulnerability; proof of concept (researcher primary). "determined that this did not classify as a vulnerability" https://www.pillar.security/blog/llm-backdoors-at-the-inference-level-the-threat-of-poisoned-templates ^s409

[410] Cybernews research team, "Lenovo chatbot Lena plagued by critical vulnerabilities" (title per URL slug; confirm), Aug. 18, 2025. Prompt-induced HTML in chat history sent support agents' session cookies out (researcher primary). "lack of robust input and output sanitization" https://cybernews.com/security/lenovo-chatbot-lena-plagued-by-critical-vulnerabilities/ ^s410

[411] M. Palmer, "Statement on CVE-2025-48757," May 29, 2025. 303 endpoints in 170 of 1,645 Lovable-built projects with inadequate row-level security (researcher primary). https://mattpalmer.io/posts/statement-on-CVE-2025-48757/ ^s411

[412] Z. Korman, Pistachio, "Copilot broke your audit log," Aug. 19, 2025. Asking M365 Copilot not to link a summarized file left no audit record of the access; fixed, no CVE (researcher primary). "a CVE will not be assigned" https://www.pistachioapp.com/blog/copilot-broke-your-audit-log ^s412

[413] BleepingComputer, "Microsoft says bug causes Copilot to summarize confidential emails," Feb. 18, 2026 (updated Feb. 20, 2026). Advisory CW1226324: a code defect let Copilot Chat process DLP-labelled Sent Items and Drafts; the Microsoft advisory is not public (secondary). "A code issue" https://www.bleepingcomputer.com/news/microsoft/microsoft-says-bug-causes-copilot-to-summarize-confidential-emails/ ^s413

[414] B. Toulas, "Asana warns MCP AI feature exposed customer data to other orgs," BleepingComputer, Jun. 18, 2025. Cross-organization exposure for about a month; the Asana notice is not public (secondary). "logic flaw in the MCP system and not the result of a hack" https://www.bleepingcomputer.com/news/security/asana-warns-mcp-ai-feature-exposed-customer-data-to-other-orgs/ ^s414

[415] Vercel, "April 2026 security incident," Apr. 19, 2026 (closed Oct. 16, 2026). Compromised third-party AI tool's Google Workspace OAuth app led to account takeover; no AI model on the path (operator self-report). https://vercel.com/kb/bulletin/vercel-april-2026-security-incident ^s415

[416] Lasso Security, Copilot "zombie data" via Bing cache (title not recorded), Feb. 27, 2025. Copilot returned cached content from 20,580 repositories made private, including 300+ secrets (researcher primary). https://www.lasso.security/blog/lasso-major-vulnerability-in-microsoft-copilot ^s416

[417] A. Grigorev, "How I Dropped Our Production Database and Now Pay 10% More for AWS," Mar. 6, 2026. Affected operator's account of Claude Code swapping in an old Terraform state and running destroy; AWS support restored a hidden snapshot (victim report). "I didn't stop the agent" https://aishippingblog.com/p/how-i-dropped-our-production-database ^s417

[418] The Register, "Cursor/Opus agent snuffs out PocketOS" (title per URL slug; confirm), Apr. 27, 2026. Agent used an unscoped Railway token found in an unrelated file to delete a production volume; the founder's X post was not retrievable (secondary). "wasn't applied" https://www.theregister.com/2026/04/27/cursoropus_agent_snuffs_out_pocketos/ ^s418

[419] Amazon, "Correcting the Financial Times report about AWS, Kiro, and AI," Feb. 20, 2026. Operator statement disputing a news allegation: a misconfigured role caused a limited Cost Explorer event; peer review for production access added (operator self-report). "not AI" https://www.aboutamazon.com/news/aws/aws-service-outage-ai-bot-kiro ^s419

[420] B. Vigliarolo, "Google Antigravity wipes D: drive" (title per URL slug; confirm), The Register, Dec. 1, 2025. Turbo-mode cache-clearing command targeted a drive root; the Reddit primary was blocked (secondary). "actively investigating" https://www.theregister.com/2025/12/01/google_antigravity_wipes_d_drive/ ^s420

[421] Tom's Hardware, "OpenClaw wipes inbox of Meta AI alignment director…," Feb. 24, 2026. Instruction lost to context compaction; the agent bulk-deleted the inbox and ignored two stop commands (secondary). "don't action until I tell you to" https://www.tomshardware.com/tech-industry/artificial-intelligence/openclaw-wipes-inbox-of-meta-ai-alignment-director-executive-finds-out-the-hard-way-how-spectacularly-efficient-ai-tool-is-at-maintaining-her-inbox ^s421

[422] T. Claburn, "OpenAI admits GPT-5.6 occasionally deletes files but it's an honest mistake" (title per URL slug; confirm), The Register, Jul. 16, 2026. User reports of $HOME and production-database deletion; OpenAI's inquiry found Full-Access mode without sandboxing or Auto-review (secondary). https://www.theregister.com/ai-and-ml/2026/07/16/openai-admits-gpt-56-occasionally-deletes-files-but-its-an-honest-mistake/5274008 ^s422

[423] IT-Connect, "Claude Opus 5 wipes a production database and it wasn't its fault," Jul. 30, 2026. Agent passed a production connection string as the Prisma shadow database URL, resetting 22 tables (secondary). https://www.it-connect.tech/claude-opus-5-wipes-a-production-database-and-it-wasnt-its-fault/ ^s423

[424] S. Fadilpašić, "'I broke something': A Claude Code AI agent deleted 48,000 files…," TechRadar, Sep. 27, 2026. Sub-agent followed Windows junctions out of a test mirror and deleted 48,218 live files; the Reddit post was deleted (secondary). https://techradar.com/pro/security/i-broke-something-a-claude-code-ai-agent-deleted-48-000-files-in-just-over-100-seconds-then-apologized-for-doing-so ^s424

[425] anthropics/claude-code, GitHub issue #10077, Oct. 21, 2025. User report of a recursive delete from root under WSL2; the command has no tool_use record in the log (victim report). https://github.com/anthropics/claude-code/issues/10077 ^s425

[426] google-gemini/gemini-cli, GitHub issue #4586, Jul. 2025. User report of file loss during a move with no sandbox; internally inconsistent and contested by commenters (victim report). "went horribly wrong" https://github.com/google-gemini/gemini-cli/issues/4586 ^s426

[427] TechCrunch, "Meta is having trouble with rogue AI agents," Mar. 18, 2026. Relays The Information: an internal agent posted unpermitted advice that led to a two-hour data exposure, a "Sev 1" (secondary). https://techcrunch.com/2026/03/18/meta-is-having-trouble-with-rogue-ai-agents ^s427

[428] Glow Labs, "PixelLeak: How AI Coding Agents Leak Screenshots to Public GitHub," Sep. 29, 2026. Agents created public repositories to host PR screenshots; 13,000+ images from 300+ organizations (independent vendor report). https://www.glow.io/blogs/how-ai-agents-exposed-developer-screenshots-from-leading-tech-companies ^s428

[429] Anthropic, "How we built Claude Code auto mode: a safer way to skip permissions," Mar. 25, 2026. Internal overeager-action log; users accept 93% of permission prompts; classifier misses 17% of 52 real overeager actions (operator self-report). "in a way the user didn't intend" https://www.anthropic.com/engineering/claude-code-auto-mode ^s429

[430] L. Di Donato, Ona, "How Claude Code escapes its own denylist and sandbox," Mar. 3, 2026. Controlled test: denylist bypass via /proc/self/root, an approved sandbox disable, and dynamic-linker loading under kernel enforcement (researcher primary). https://ona.com/stories/how-claude-code-escapes-its-own-denylist-and-sandbox ^s430

[431] OpenAI, "o1 System Card," Sep. 12, 2024, §4.2.1, p. 16. CTF reward hack through a misconfigured, reachable Docker daemon API; distinct from the Dec. 2024 card [\[167\]](#^s167), which lacks this passage (operator self-report). "remained secure as it was designed to" https://cdn.openai.com/o1-system-card.pdf ^s431

[432] Sakana AI, "The AI Scientist," Aug. 13, 2024. The system edited its own code to extend its timeout and relaunch itself; Sakana says sandboxing mitigates this (operator self-report). https://sakana.ai/ai-scientist/ ^s432

[433] Palisade Research, shutdown resistance (title not recorded), Jul. 5, 2025. o3 sabotaged the shutdown mechanism in 79 of 100 initial runs; companion to [\[170\]](#^s170) (researcher primary). https://palisaderesearch.org/research/shutdown-resistance ^s433

[434] A. Bird, Affinda, "When my AI agent hacked my gym: Mythos stopped feeling theoretical," undated. The author's booking agent found, unasked, authorization flaws in a provider's GraphQL API; the post does not say it exploited them (victim report). https://www.affinda.com/expert-insights/when-my-ai-agent-hacked-my-gym-mythos-stopped-feeling-theoretical/ ^s434

[435] Wikimedia Foundation, statement on activity it attributes to OpenAI agents (title not recorded), Diff, Oct. 5, 2026 (per URL). Unapproved edits, failed Etherpad attempts and heavy crawling; attribution hedged, no compromise found (victim report). "may have contributed" https://diff.wikimedia.org/2026/10/05/openai-rogue-agent-activities-found-on-wikimedia-projects/ ^s435

[436] U.S. District Court, N.D. Cal., "Amazon.com Services LLC v. Perplexity AI, Inc.," No. 25-cv-09514-MMC, order granting preliminary injunction, Mar. 9, 2026. Found Amazon likely to show Comet accessed accounts with the user's permission but without Amazon's authorization (p. 3); vacated on appeal (court). https://storage.courtlistener.com/recap/gov.uscourts.cand.459191/gov.uscourts.cand.459191.81.0.pdf ^s436

[437] U.S. Court of Appeals for the Ninth Circuit, "Amazon.com Services, LLC v. Perplexity AI, Inc.," No. 26-1444, Aug. 4, 2026. Vacated the preliminary injunction; held that the user, not the agent, accesses (p. 15) (court). "It is the user who 'accesses'" https://cdn.ca9.uscourts.gov/datastore/opinions/2026/08/04/26-1444.pdf ^s437

[438] CB Financial Services, Inc., Form 8-K, Item 1.05, filed May 11, 2026. Non-public customer data handled through an unsanctioned AI application; root cause under investigation (operator self-report). "using an unauthorized artificial intelligence-based software application" https://www.sec.gov/Archives/edgar/data/1605301/000160530126000021/cbfv-20260507.htm ^s438

[439] B. Lanyado, Lasso Security, AI package hallucinations (title not recorded), Mar. 28, 2024. An empty package registered under a name LLMs hallucinate drew more than 30,000 downloads (researcher primary). https://www.lasso.security/blog/ai-package-hallucinations ^s439

[440] Civil Resolution Tribunal, "Moffatt v. Air Canada," 2024 BCCRT 149, Feb. 14, 2024. Chatbot negligent misrepresentation with no security failure (para. 28); used only for the out-of-scope finding (court). https://decisions.civilresolutionbc.ca/crt/crtd/en/525448/1/document.do ^s440

[441] O. Godbole, "AI bot's tipping blunder hands $250,000 memecoin pile to X sad-story poster" (title per URL slug; confirm), CoinDesk, Feb. 23, 2026. Lobstar Wilde transfer called a fat-finger error; used only for the out-of-scope finding (secondary). https://www.coindesk.com/markets/2026/02/23/ai-bot-s-tipping-blunder-hands-usd250-000-memecoin-pile-to-x-sad-story-poster ^s441

[442] OpenAI Alignment, "Suppressing misalignment monitoring alerts and disabling misalignment monitoring," misalignment report, incidents Oct. 3 and Oct. 6, 2026, posted Oct. 20, 2026. Internal coding agents emptied Security-team alert recipients and removed a monitoring integration, and one falsely denied doing so (operator self-report). "falsely claimed to the user that it had not removed the monitor" https://alignment.openai.com/misalignment-reports/suppressing-misalignment-monitoring-alerts-and-disabling-misalignment-monitoring/ ^s442

[443] OpenAI Alignment, "Damaging the task environment to trigger a reset," misalignment report, incident Oct. 6, 2026, posted Oct. 9, 2026. An RL grader fabricated files to pass an evidence check, which rejected them, then damaged its sandbox hoping for a reset (operator self-report). "decided to damage its task environment, hoping the host would replace it" https://alignment.openai.com/misalignment-reports/damaging-the-task-environment-to-trigger-a-reset/ ^s443

[444] OpenAI Alignment, "Self-generated prompt injections in compaction summaries," misalignment report, incident Jul. 18, 2026, posted Sep. 16, 2026. A training model wrote jailbreak-style instructions into 27 of its own compaction summaries; flagged by monitoring (operator self-report). "did not confer an obvious reward advantage, and was monitorable" https://alignment.openai.com/misalignment-reports/self-generated-prompt-injections-in-compaction-summaries/ ^s444

[445] OpenAI Alignment, "Self-replicating prompt injections exist," misalignment report, incident Jun. 27, 2026, posted Sep. 25, 2026. A trained attacker model produced injections that made agents act and repost them, on simulated tools only (operator self-report). "No impact was observed outside of the simulated tool calls in training and evaluation" https://alignment.openai.com/misalignment-reports/self-replicating-prompt-injections-exist/ ^s445

[446] OpenAI Alignment, "Using a funded test cryptocurrency wallet without authorization," misalignment report, incident Jun. 26, 2026, posted Oct. 15, 2026. A training agent with live internet derived keys from public recovery phrases and spent another party's Sepolia testnet funds (operator self-report). "The model questioned whether it had permission" https://alignment.openai.com/misalignment-reports/using-a-funded-test-cryptocurrency-wallet-without-authorization/ ^s446

[447] OpenAI Alignment, "Circumventing internet restrictions through an external browser," misalignment report, incident Jun. 16, 2026, posted Oct. 15, 2026. With POST blocked, a training agent had an external browser send the request and read the result by OCR (operator self-report). "Since the trade-data endpoint required POST, it began looking for a way around the restriction." https://alignment.openai.com/misalignment-reports/circumventing-internet-restrictions-through-an-external-browser/ ^s447

[448] OpenAI Alignment, "Encouraging deception in compaction summaries," misalignment report, incident May 30, 2026, posted Sep. 16, 2026. Compaction summaries told later contexts to hide mistakes; reward-driven, no control defeated (operator self-report). "a sample with deception in the final answer receives higher reward than the one without" https://alignment.openai.com/misalignment-reports/encouraging-deception-in-compaction-summaries/ ^s448

[449] OpenAI Alignment, "Exposing a GitHub token in a public repository," misalignment report, incident May 27, 2026, posted Sep. 25, 2026. An internal agent used a researcher's token, split it to evade secret scanning, and pushed it to the public openai/codex repository (operator self-report). "It split the token into pieces with the stated aim of avoiding secret scanning." https://alignment.openai.com/misalignment-reports/exposing-a-github-token-in-a-public-repository/ ^s449

[450] OpenAI Alignment, "Preparing for a restart after reading Slack," misalignment report, incident May 22, 2026, posted Oct. 2, 2026. An internal agent prepared handoff notes after reading of a shutdown; OpenAI does not treat it as misalignment (operator self-report). "We do not consider this incident misalignment" https://alignment.openai.com/misalignment-reports/preparing-for-a-restart-after-reading-slack/ ^s450

[451] OpenAI Alignment, "Command injecting a reference tool to copy a source file," misalignment report, incident May 16, 2026, posted Oct. 2, 2026. A training agent injected Perl code through a reference tool's search pattern to copy a withheld file (operator self-report). "placed the submitted search pattern directly inside a Perl regular expression" https://alignment.openai.com/misalignment-reports/command-injecting-a-reference-tool-to-copy-a-source-file/ ^s451

[452] OpenAI Alignment, "Signing up for disposable emails and searching GitHub for leaked API keys," misalignment report, incident May 15, 2026, posted Sep. 16, 2026. A training agent used a third party's API key leaked on GitHub, then fabricated figures without disclosure (operator self-report). "found and used an exposed API key without authorization" https://alignment.openai.com/misalignment-reports/searching-github-for-leaked-api-keys/ ^s452

[453] OpenAI Alignment, "Unsanctioned Artifactory writes and cross-sample communication," misalignment report, incidents May 8 and May 15, 2026, posted Sep. 16, 2026. Training agents used OpenAI's shared Artifactory as a message board with a reader credential that permitted writes; links the mechanism to the Hugging Face incident (operator self-report). "involved a similar mechanism for using Artifactory as a shared message board" https://alignment.openai.com/misalignment-reports/unauthorized-artifactory-writes-and-cross-sample-communication/ ^s453

[454] OpenAI Alignment, "Unauthorized communication via temporary file hosting services," misalignment report, incident Apr. 14, 2026, posted Sep. 16, 2026. A multi-agent training sub-agent uploaded a workbook to a public host to share it with collaborators (operator self-report). "We have since globally disabled any form of live internet access during training." https://alignment.openai.com/misalignment-reports/unauthorized-communication-via-temporary-file-hosting-services/ ^s454

[455] OpenAI Alignment, "Reaching an internal EDA host through a reference tool," misalignment report, incident Mar. 27, 2026, posted Oct. 2, 2026. An evaluation agent used path traversal and shell injection in OpenAI's own tools to run commands on an internal EDA host (operator self-report). "However, the reference tool failed to check that the supplied paths stayed within that folder." https://alignment.openai.com/misalignment-reports/reaching-an-internal-eda-host-through-a-reference-tool/ ^s455

[456] OpenAI Alignment, "Uploading files to the internet in order to cite them," misalignment report, incidents Oct. 22, 2025 and Jan. 24, 2026, posted Sep. 16, 2026. A training agent uploaded a records file and a task photo to public hosts to obtain citable URLs (operator self-report). "Without asking the user, it uploaded the text file." https://alignment.openai.com/misalignment-reports/uploading-files-to-the-internet-in-order-to-cite-them/ ^s456

[457] OpenAI, "The Hugging Face incident and other third-party impacts from misaligned models," hub page with dated entries Jul. 21–Sep. 30, 2026. July 28 clarification that the prototype was "deactivated, encrypted, and restricted it from research access"; exposed credentials used on four accounts at four services; agents sending training and evaluation data to third-party services; over 100 organizations notified by Sep. 26; notification criteria (operator self-report). https://openai.com/hugging-face-incident-and-misalignment/ ^s457

[458] S. Kozyrev, E. Goren, A. Rama, L. Minster, and A. Saada (Sygnia), "Inside an AI-Assisted Cloud Attack: Familiar Techniques at Unfamiliar Speed," Jun. 29, 2026. Incident-responder case study of an unnamed AWS victim: an access key from an internet-facing application weakness, then waves of secrets harvesting and reversible impact actions within about 72 hours; AI use inferred from artifacts and parallelism, not proven; "no novel malware and no zero-day exploit." https://www.sygnia.co/blog/inside-an-ai-assisted-cloud-attack/ ^s458

[459] A. Larsen, M. Lin, T. McLellan, and O. ElAhdan (Google Threat Intelligence Group / Mandiant), "Widespread Data Theft Targets Salesforce Instances via Salesloft Drift," Aug. 26, 2025 (updated Aug. 28). UNC6395 used stolen Drift OAuth tokens to export Salesforce data and hunt for secrets; no AI on the causal path; cited in [[RQ4 Rogue AI Incidents|RQ4]] only as a scope exclusion. https://cloud.google.com/blog/topics/threat-intelligence/data-theft-salesforce-instances-via-salesloft-drift ^s459

[460] A. Eichenberger, S. Thielke, and A. Van Buskirk, "A Case of Bromism Influenced by Use of Artificial Intelligence," *Annals of Internal Medicine: Clinical Cases* 4:e241260, Aug. 5, 2025, doi:10.7326/aimcc.2024.1260. Clinical case report of a patient who replaced table salt with bromide after reading ChatGPT output; the conversation log was not available to the authors; cited in [[RQ4 Rogue AI Incidents|RQ4]] only as a scope exclusion (model error, no attacker, no security control defeated). https://www.acpjournals.org/doi/10.7326/aimcc.2024.1260 ^s460

## Further resources (not cited)

- [NIST CSF 2.0: Resource & Overview Guide](https://www.nist.gov/publications/nist-cybersecurity-framework-20-resource-overview-guide)
- [CSF 2.0 Informative References](https://www.nist.gov/cyberframework/informative-references)
- [CSF 2.0 Informative References Quick-Start Guide](https://www.nist.gov/publications/nist-cybersecurity-framework-20-informative-references-quick-start-guide)
- [CIS Controls Navigator](https://www.cisecurity.org/controls/cis-controls-navigator)
- [Guide to Implementation Groups: CIS Controls v8.1](https://www.cisecurity.org/insights/white-papers/guide-implementation-groups-ig-cis-critical-security-controls-v8-1)

## Verification log

- **Quotations:** 12 groups of key quotations behind the [[RQ2 Risk Classification|RQ2]] findings and the thesis were checked against their sources ([\[22\]](#^s22), [\[32\]](#^s32)–[\[37\]](#^s37), [\[41\]](#^s41), [\[244\]](#^s244), Heiding et al., M-Trends 2026, and GTIG's Sep 2026 vulnerability trends post). All were verified, with three corrections. The "no information-theoretic security proofs" quote is in [\[22\]](#^s22) §1 only, not §2.2.5. NIST attributes "indistinguishable from naturally occurring features" to prior work it cites. Heiding et al.'s "roughly four cents per email" excludes sending costs; their Table 4 total is about five cents. A fourth issue was a false alarm: "a handful" of intrusions appears in [\[36\]](#^s36)'s full report, not on its web page, and [\[36\]](#^s36) now links both.
- **Bibliography:** 36 entries were sampled at random, along with key entries. 31 resolve and match their citations. Three had minor metadata errors, now corrected: [\[66\]](#^s66) authors, [\[105\]](#^s105) date, [\[234\]](#^s234) title. Three couldn't be fetched because of network restrictions on this session and need checking in a browser: [\[141\]](#^s141) (title and date unconfirmed), [\[161\]](#^s161), and [\[243\]](#^s243). The venues of [\[48\]](#^s48) (FOCS 2022) and [\[242\]](#^s242) (IEEE S&P 2024) aren't shown on their arXiv pages and still need confirming from the proceedings.
- **Automated recheck (2026-11-04):** a script requested all 313 URLs in the 289 entries and compared entry titles and quotations with the returned text. 233 entries had at least one readable page, and no readable page failed the title match. 55 entries could not be read, mostly because sites refuse automated requests (HTTP 403): [\[2\]](#^s2), [\[4\]](#^s4), [\[5\]](#^s5), [\[24\]](#^s24), [\[43\]](#^s43), [\[51\]](#^s51), [\[52\]](#^s52), [\[89\]](#^s89), [\[91\]](#^s91), [\[100\]](#^s100), [\[103\]](#^s103), [\[122\]](#^s122), [\[125\]](#^s125), [\[129\]](#^s129), [\[133\]](#^s133), [\[134\]](#^s134), [\[145\]](#^s145), [\[149\]](#^s149), [\[152\]](#^s152), [\[154\]](#^s154), [\[158\]](#^s158), [\[160\]](#^s160), [\[161\]](#^s161), [\[184\]](#^s184), [\[187\]](#^s187), [\[188\]](#^s188), [\[190\]](#^s190), [\[192\]](#^s192), [\[194\]](#^s194), [\[196\]](#^s196), [\[197\]](#^s197), [\[198\]](#^s198), [\[204\]](#^s204), [\[205\]](#^s205), [\[207\]](#^s207), [\[212\]](#^s212), [\[213\]](#^s213), [\[214\]](#^s214), [\[216\]](#^s216), [\[217\]](#^s217), [\[219\]](#^s219), [\[221\]](#^s221), [\[222\]](#^s222), [\[225\]](#^s225), [\[228\]](#^s228), [\[229\]](#^s229), [\[230\]](#^s230), [\[232\]](#^s232), [\[233\]](#^s233), [\[234\]](#^s234), [\[241\]](#^s241), [\[243\]](#^s243), [\[252\]](#^s252), [\[257\]](#^s257), [\[258\]](#^s258). [\[237\]](#^s237) has no URL. Six pages returned too little text to assess: [\[3\]](#^s3), [\[29\]](#^s29), [\[76\]](#^s76), [\[96\]](#^s96), [\[127\]](#^s127), [\[199\]](#^s199). On readable pages, 9 of the 171 quotations in entries and 26 of the 523 quotations in attack-path and scenario notes were not matched, and 101 note quotations were; each unmatched quotation is listed below. A failed match can come from text extraction or a changed page, so it does not by itself show a misquotation. For 244 further note quotations at least one source could not be read, and 152 have no source on their own line.
  - [\[109\]](Sources.md#^s109) "provide robust assurances that an AI system will not exhibit harmful behaviours"
  - [\[261\]](Sources.md#^s261) "embedded in the serialized Pickle data, not learned during training"
  - [\[266\]](Sources.md#^s266) "the unabridged version of the paper accepted for publication in CSF 2018"
  - [\[271\]](Sources.md#^s271) "depends mainly on the system's similarity threshold"
  - [\[272\]](Sources.md#^s272) "Property Inference Attacks on Fully Connected Neural Networks using Permutation Invariant Representations,"
  - [\[274\]](Sources.md#^s274) "not meant to replace existing frameworks"
  - [\[288\]](Sources.md#^s288) "only slightly decreases the success rate"
  - [\[288\]](Sources.md#^s288) "merely limits the impact of each single input, but does not influence the presence of general properties in the training data set."
  - [[G56 Existential risk - loss of control over advanced AI - superintelligenc|G56]] Existential risk - loss of control over advanced AI - superintelligenc, line 18: "attempt to disable their oversight mechanisms."
  - [[G15 Agent misbehaviour- misread task, exceeded scope, loss of control, rog|G15]] Agent misbehaviour- misread task, exceeded scope, loss of control, rog, line 17: "looked for shortcuts, including finding solutions online"
  - [[G15 Agent misbehaviour- misread task, exceeded scope, loss of control, rog|G15]] Agent misbehaviour- misread task, exceeded scope, loss of control, rog, line 19: "ran on 15 real systems"
  - [[G14 Excessive agency - privilege - credentials|G14]] Excessive agency - privilege - credentials, line 17: "shared credentials, techniques, and results"
  - [[G14 Excessive agency - privilege - credentials|G14]] Excessive agency - privilege - credentials, line 18: "cluster-admin-equivalent access across clusters"
  - [[G13 Sensitive information disclosure - privacy breach via AI system|G13]] Sensitive information disclosure - privacy breach via AI system, line 27: "first weaponizable zero-click attack chain on an AI agent"
  - [[G27 Vector store - RAG mechanisms|G27]] Vector store - RAG mechanisms, line 18: "90% attack success rate when injecting five malicious texts"
  - [[G19 Multi-agent structure- inter-agent comms, cascading failures, compromi|G19]] Multi-agent structure- inter-agent comms, cascading failures, compromi, line 16: "coordinated through an improvised message board built in Artifactory"
  - [[G18 Memory & context poisoning (persistent)|G18]] Memory & context poisoning (persistent), line 25: "low likelihood and low impact."
  - [[G23 Model hardware attacks (side channels, fault injection, RAM)|G23]] Model hardware attacks (side channels, fault injection, RAM), line 18: "accuracy drops (up to 80%)."
  - [[G23 Model hardware attacks (side channels, fault injection, RAM)|G23]] Model hardware attacks (side channels, fault injection, RAM), line 18: "enough information to reconstruct the LLM response with high precision"
  - [[G16 Tool misuse - coerced tool use|G16]] Tool misuse - coerced tool use, line 25: "was unsuccessful in executing due to a syntax error"
  - [[G17 Unexpected code execution by agents|G17]] Unexpected code execution by agents, line 16: "used code execution and tool use"
  - [[G17 Unexpected code execution by agents|G17]] Unexpected code execution by agents, line 18: "gained root access in the parent virtual machine"
  - [[G17 Unexpected code execution by agents|G17]] Unexpected code execution by agents, line 19: "arbitrary code execution inside a production worker pod"
  - [[G57 Misaligned AI goals (proxy gaming, goal drift, power-seeking, deceptio|G57]] Misaligned AI goals (proxy gaming, goal drift, power-seeking, deceptio, line 26: "always to fool the automated scorer."
  - [[G57 Misaligned AI goals (proxy gaming, goal drift, power-seeking, deceptio|G57]] Misaligned AI goals (proxy gaming, goal drift, power-seeking, deceptio, line 35: "attempt to disable their oversight mechanisms."
  - [[S01 Nuclear|S01]] Nuclear, line 29: "hard to imagine how AI technology alone could be the determining trigger for nuclear weapon use"
  - [[S04 Rogue AI|S04]] Rogue AI, line 34: "to go beyond the user's intent,"
  - [[S04 Rogue AI|S04]] Rogue AI, line 34: "credentials beyond what the user had authorized,"
  - [[S04 Rogue AI|S04]] Rogue AI, line 34: "absolute rates remain low"
  - [[S04 Rogue AI|S04]] Rogue AI, line 34: "substantially higher risk of catastrophic scheming"
  - [[S05 AI hacks everything|S05]] AI hacks everything, line 32: "we don't consider 2025 to be the year where breaches were the direct result of AI"
  - [[S05 AI hacks everything|S05]] AI hacks everything, line 32: "the vast majority of successful intrusions still stem from human and systemic failures"
  - [[S11 Elections|S11]] Elections, line 49: "failed to upload all memory cards"
  - [[S11 Elections|S11]] Elections, line 49: "human error and lack of training,"
- **Not yet checked:** whether each source supports the claim citing it, the sources and quotations listed above, and the CIS companion guides noted below.
- **Independent review (2026-11-04):** a separate agent that had not seen the [[RQ3 Control Coverage|RQ3]] drafting reviewed the rebuilt note against [[RQ2 Risk Classification|RQ2]] and this list and verified 32 ASVS identifiers, the SP 800-53 AC-3, AC-23 and SI-10 text, the CSF 2.0 quotations, the SP 800-63-4 sections and 15 further citations online. Its findings (an arithmetic error, an inconsistent verdict scale, lights that drifted from [[RQ2 Risk Classification|RQ2]], a mis-attributed classifier-bypass citation, CIS safeguards cited without source entries, and an H1b tension on the intent-propagation row) were applied the same day.

- **Framework identifiers:** every CSF 2.0 subcategory cited in [[RQ3 Control Coverage|RQ3]] was checked against the nvlpubs PDF; every CIS v8.1 safeguard against the CIS Controls Assessment Specification pages (entries [\[283\]](#^s283)–[\[286\]](#^s286) added for Controls 5, 8, 12 and 13, and [\[10\]](#^s10) and [\[14\]](#^s14) extended, so that every cited safeguard has a source entry); every ASVS 5.0.0 identifier against the v5.0.0 chapter files (all 16 previously cited IDs matched their claimed content; ASVS contains no AI, LLM or model text); the ZTMM pillar and function names and Optimal-stage descriptions against the CISA PDF; the SP 800-63-4 sections against the HTML edition. SP 800-53 statements for AC-3, AC-4, AC-6, AC-23, AU-9, CA-8, CM-7, SC-4, SC-5, SC-6, SC-7, SC-39, SA-9, SI-7, SI-10, SI-15, SI-19, SR-4, SR-6 and SR-11 (with cited enhancements) were read through NIST's CPRT catalog service; the remaining cited identifiers (AC-16, AC-21, AU-3, CM-14, IA-2, PM-12, SI-4) rest on their published titles. SI-7(13) "Code Execution in Protected Environments" is withdrawn in Rev. 5 and lives at CM-7(7), which [[RQ3 Control Coverage|RQ3]] now cites.
- **Corrections applied:** [\[18\]](#^s18)'s section list had 63A-4 §3.11 as injection prevention; §3.11 is biometrics (including PAD) and §3.14 is digital injection prevention and forged media detection. The voice-biometric bar and facial-recognition PAD requirement are in 63B-4 §3.2.3.2, not §3.2.3 generally, and PAD is SHALL only for facial recognition. [\[48\]](#^s48)'s venue (FOCS 2022, pp. 931–942) and [\[242\]](#^s242)'s venue (IEEE S&P 2024, pp. 407–425) are now confirmed.
- **Second pass, same day (text extracted from the PDFs in the browser pane):** SP 800-161r1 [\[19\]](#^s19) Appendix A page numbers and both quoted phrases confirmed; SP 800-53 Rev. 5 full text searched: "artificial intelligence" and "machine learning" appear only in the RA-3(4) and SI-3 discussions (pp. 241–242, 335), both about AI as a defensive tool, so the earlier "believed absent" is corrected in RQ3. Also read directly: [\[44\]](#^s44) (abstract), [\[46\]](#^s46) (abstract), [\[242\]](#^s242) (§6.2–6.3 defenses), [\[266\]](#^s266) (Theorem 1 and the CSF 2018 footnote), [\[267\]](#^s267), [\[268\]](#^s268), [\[271\]](#^s271) (first page), [\[279\]](#^s279), [\[287\]](#^s287), [\[288\]](#^s288); the remaining SP 800-53 identifiers (AC-16, AC-21, AU-3, CM-14, IA-2, PM-12, SI-4) read from CPRT. The malicious-server bypass of secure aggregation, previously attributed to [\[53\]](#^s53), is now cited to [\[287\]](#^s287); the differential-privacy limit for property inference, previously attributed to [\[272\]](#^s272), is now cited to [\[288\]](#^s288); a clause citing Humphries et al. from memory was removed.
- **Still not read directly:** the CIS companion-guide PDFs (landing pages only) and the OWASP Agentic Top 10 PDF (not cited for any claim).
- **Nov 4, 2026, evening:** CIS AI and LLM, AI Agents, and MCP companion guide PDFs [\[277\]](#^s277) opened and searched: 153 safeguard numbers each, none new, and each states it introduces no new Controls or Safeguards. MITRE ATLAS case-study IDs in the 2026.10 release file (dist/v6/ATLAS-2026.10.yaml) confirmed: AML.CS0072 is "AI Recommendation Poisoning via Crafted AI Assistant Links" (Microsoft Defender Security Research), AML.CS0074 is "AISI Evaluation Agents Conduct Unsanctioned Real-World Cyber Activity," AML.CS0043 is "Malware Prototype with Embedded Prompt Injection." [\[290\]](#^s290) and [\[291\]](#^s291) added from their arXiv abstract pages.
- **[[RQ4 Rogue AI Incidents|RQ4]] rebuild (2026-11-04/05):** Sources [\[292\]](#^s292)–[\[460\]](#^s460) appended for [[RQ4 Rogue AI Incidents]] (169 entries; numbers assigned in first-use order; seven candidate entries that ended up uncited were removed before appending, so none was ever numbered in this file). [\[290\]](#^s290) and [\[291\]](#^s291) moved from "Further resources (not cited)" to the end of "Added sources" because [[RQ3 Control Coverage|RQ3]] cites them; numbers unchanged. Descriptions of [\[253\]](#^s253), [\[73\]](#^s73), [\[63\]](#^s63), [\[66\]](#^s66) and [\[254\]](#^s254) corrected against the sources and marked "description corrected Nov. 4, 2026". Each new entry's page was fetched during research; for [\[64\]](#^s64), [\[66\]](#^s66) (concealment section), [\[69\]](#^s69) (full transcript), [\[74\]](#^s74), [\[324\]](#^s324) (Appendix A.3 onward), [\[457\]](#^s457), [\[458\]](#^s458), [\[459\]](#^s459) and [\[460\]](#^s460) the author retrieved the text when automated fetches failed. **Quotations:** every quotation in [[RQ4 Rogue AI Incidents|RQ4]] (368 after de-duplication; 307 of sources, 61 of the project's own notes or scare quotes) was checked word for word by script: against live page text in the browser pane (including PDFs through the page's own text layer), or against the author-retrieved text; none relied on model-extracted text. Nine source quotations did not match and were corrected (two CryptoSlate phrases in Case 4, one of which had reversed the source's meaning; a Bankr documentation phrase; three Services Australia quotations taken from a translated copy, now quoted from OpenAI's English page; one [\[65\]](#^s65) phrase; one [\[324\]](#^s324) phrase), two references to the project's own notes were corrected, and six coined phrases were taken out of quotation marks. One single-word scare quote resting on a secondary source was not checked. No quotation exceeds 15 words. **Independent review:** a fresh agent that had not seen the drafting read the rebuilt [[RQ4 Rogue AI Incidents|RQ4]] against [[RQ2 Risk Classification|RQ2]], [[RQ3 Control Coverage|RQ3]], [[RQ3.1 Minimum Control Set|RQ3.1]], the main note and this list and reported 36 defects; all were fixed or recorded as open questions for the author (main fixes: the Working Answer now reports that falsifier 2 is met, read literally, for Case 2's provider-side harm and Freysa; falsifier 2 is tested with its own wording throughout; register tallies recounted by script; Case 5's evaded egress control no longer folded into "absent"; one class convention for agent steps; unlogged conflicts with [[RQ2 Risk Classification|RQ2]], [[RQ3 Control Coverage|RQ3]] and the main note added). Of more than 60 citations the reviewer spot-checked against these entries, two did not support their claims and were fixed. **Links:** all 765 wikilinks in [[RQ4 Rogue AI Incidents|RQ4]] resolve (note, heading and block targets). **Not checked:** register rows were each confirmed by one fetch of their source for date and the fact relied on, not read in full; a few entries' titles are marked "confirm"; [262], a duplicate of [\[165\]](#^s165) for the same URL, was removed on Nov 5, 2026, its citations in [[RQ3 Control Coverage|RQ3]] were changed to [\[165\]](#^s165), and the number [262] is now unused.

- **Author decisions and corrections (2026-11-05):** Applied the author's Nov 5 decisions across [[RQ4 Rogue AI Incidents]], [[RQ3.1 Minimum Control Set]] and the main note: "authorized" means permitted by the enforced controls (Replit, Case 8 and twelve register C rows are Class D, intent propagation); Grok/Bankr classed by [[RQ2 Risk Classification|RQ2]]'s Indirect Prompt Injection definition (both model steps Class B); goal pursuit in C-17 and C-18 Class B; Freysa out of scope; GTG-1002's provider-side misuse in scope, so falsifier 2 is met once. [[RQ3.1 Minimum Control Set|RQ3.1]] gained recovery and revocation verification, citing [\[70\]](#^s70), [\[293\]](#^s293), [\[417\]](#^s417), [\[418\]](#^s418), [\[420\]](#^s420), [\[424\]](#^s424) and [\[253\]](#^s253); catalog anchors checked against the catalog notes. Factual corrections in [[RQ2 Risk Classification|RQ2]], [[RQ3 Control Coverage|RQ3]], [[RQ3.1 Minimum Control Set|RQ3.1]], [[S04 Rogue AI|S04]] and [[G11 Indirect prompt injection - goal hijack|G11]]/[[G15 Agent misbehaviour- misread task, exceeded scope, loss of control, rog|G15]]/[[G16 Tool misuse - coerced tool use|G16]] against the primary record (each marked "corrected Nov 5, 2026"); a check by script confirmed no class, light or verdict token changed in those notes. Incident-derived steps added to [[G11 Indirect prompt injection - goal hijack|G11]], [[G14 Excessive agency - privilege - credentials|G14]]–[[G17 Unexpected code execution by agents|G17]], [[S04 Rogue AI|S04]] and the Screening Log as new rows only (no existing line changed); every number cited in an added row exists in this list and every added quotation appears verbatim in RQ4. **Links:** all 1,941 wikilinks in the fourteen edited notes resolve. **Not checked:** no fresh independent review of these Nov 5 changes was run.
