---
tags: [control-catalog, ai-fud-whitepaper]
---
# NIST SP 800-63-4 Normative Requirements Extraction

Built with AI assistance on November 4, 2026 from the primary source: the HTML edition of NIST SP 800-63-4, 800-63A-4, 800-63B-4, and 800-63C-4 (final, July 2025) at https://pages.nist.gov/800-63-4/ [18].

**This is an extraction, not a control catalog.** SP 800-63-4 is written as prose with normative keywords, not as numbered controls. Each row below is one paragraph or list item that contains at least one normative keyword (SHALL, SHALL NOT, SHOULD, SHOULD NOT, MAY, as the suite defines them in its Notations section), with the section number and heading it sits under (headings are prefixed with the volume, e.g. `63B §3.2.3.2`, so that links resolve to one place). Section numbers were computed from the HTML heading structure (the HTML numbers headings with CSS, not text) and spot-checked: 63A §3.8 Requirements for Confirmation Codes, 63B §3.1.1.2 Password Verifiers, 63B §3.1.3.2 Out-of-Band Verifiers. A statement that introduces a list ("one of the following SHALL take place:") is kept with its list items as separate rows. Non-normative text, tables, and figures are omitted; a requirement expressed only in a table is therefore not here. Where a lowercase keyword appears in the suite it is not normative, and those paragraphs are excluded unless they also carry an uppercase keyword. Row IDs (e.g., `63B-3.1.3.2-2`) are this extraction's own, for cross-reference from [[RQ3 Control Coverage]] and [[RQ3.1 Minimum Control Set]]; they are not NIST identifiers.

**Counts.** 
800-63-4: 72 statements (58 SHALL/SHALL NOT, 12 SHOULD/SHOULD NOT, 2 MAY). 800-63A-4: 255 statements (216 SHALL/SHALL NOT, 27 SHOULD/SHOULD NOT, 12 MAY). 800-63B-4: 249 statements (200 SHALL/SHALL NOT, 34 SHOULD/SHOULD NOT, 15 MAY). 800-63C-4: 297 statements (232 SHALL/SHALL NOT, 25 SHOULD/SHOULD NOT, 40 MAY). Total 873.

**License.** U.S. Government work, not subject to copyright in the United States.

## SP 800-63-4 Digital Identity Guidelines (base volume)

### 63 §1.4 Notations

- **63-1.4-1** SHALL NOT — The terms “SHALL” and “SHALL NOT” indicate requirements to be followed strictly in order to conform to the publication and from which no deviation is permitted. ^63-1-4-1
- **63-1.4-2** SHOULD NOT — The terms “SHOULD” and “SHOULD NOT” indicate that among several possibilities, one is recommended as particularly suitable without mentioning or excluding others, that a certain course of action is preferred but not necessarily required, or that (in the negative form) a certain possibility or course of action is discouraged but not prohibited. ^63-1-4-2
- **63-1.4-3** MAY — The terms “MAY” and “NEED NOT” indicate a course of action permissible within the limits of the publication. ^63-1-4-3

### 63 §3 Digital Identity Risk Management

- **63-3-1** SHALL — For relying parties, the intent of this process is to determine the assurance levels and any tailoring required to protect online services and the applications, transactions, and systems that comprise or are impacted by those services. This directly contributes to the selection, development, and procurement of CSP services. Federal RPs SHALL implement the DIRM process for all online services. ^63-3-1
- **63-3-2** SHALL — For credential service providers and identity providers, the intent of this process is to design service offerings that meet the requirements of the defined assurance levels, continuously guard against compromises to the identity system, and meet the needs of RPs. Whenever a service offering deviates from normative guidance, those deviations SHALL be clearly communicated to the RPs that utilize the service. ^63-3-2
- **63-3-3** SHOULD — This process augments the risk management processes required by [FISMA]. The results of the DIRM impact assessment for the online service may be different from the FISMA impact level for the underlying application or system. Identity process failures can result in different levels of impact for various user groups. For example, the overall assessed FISMA impact level for a payment system may result in a ‘FISMA Moderate’ impact category because sensitive financial data is being processed by the system. However, for individuals who are making guest payments where no persistent account is established, the authentication and proofing impact levels may be lower. Agency authorizing officials SHOULD require documentation that demonstrates adherence to the DIRM process as a part of the authority to operate (ATO) for the underlying information system that supports an online service. Agency authorizing officials SHOULD require documentation from CSPs that demonstrates adherence to the DIRM process as part of procurement or ATO processes for integration with CSPs. ^63-3-3
- **63-3-4** SHALL — Organizations SHOULD adapt and modify this overall approach to meet organizational processes, governance, and enterprise risk management practices. At a minimum, organizations SHALL execute and document each step and complete and document the normative mandates and outcomes of each step, regardless of any organization-specific processes or tools used in the overall DIRM process. Additionally, organizations SHOULD consult with a representative sample of the online service’s user population to inform the design and performance evaluation of the identity management system. ^63-3-4

### 63 §3.1 Define the Online Service

- **63-3.1-1** SHALL — RPs SHALL develop a description of the online service that includes, at minimum: ^63-3-1-1
- **63-3.1-2** SHALL — Accordingly, the scope of impact assessments SHALL include individuals who use the online application as well as the organization itself. Additionally, organizations SHALL identify other entities (e.g., mission partners, communities, and those identified in [SP800-30]) that need to be specifically included based on mission and business needs. At a minimum, organizations SHALL document all impacted entities (both internal and external to the organization) when conducting their impact assessments. ^63-3-1-2

### 63 §3.2 Conduct Initial Impact Assessment

- **63-3.2-1** SHALL — The purpose of the initial impact assessment is to identify the potential adverse impacts of failures in identity proofing, authentication, and federation that are specific to an online service, yielding an initial set of assurance levels. RPs SHOULD consider historical data and results from user focus groups when performing this step. The impact assessment SHALL include: ^63-3-2-1
- **63-3.2-2** SHALL — The level of impact for each user group identified in Sec. 3.1 SHALL be considered separately based on the transactions available to that user group. This gives organizations maximum flexibility in selecting and implementing assurance levels that are appropriate for each user group. While impacts to user groups, the organization, and other entities are primary considerations for impact assessments, organizations SHOULD also consider scale (e.g., number of persons impacted by transactions). ^63-3-2-2

### 63 §3.2.1 Identify Impact Categories and Potential Harms

- **63-3.2.1-1** SHALL — In this step, organizations identify the categories of impact that are applicable to the impacted entities for a given online service. At a minimum, organizations SHALL include the following impact categories in their impact assessments: ^63-3-2-1-1
- **63-3.2.1-2** SHALL — Organizations SHOULD include additional impact categories, as appropriate, based on their mission and business objectives. Each impact category SHALL be documented and consistently applied when implementing the DIRM process across different online services offered by the organization. ^63-3-2-1-2
- **63-3.2.1-3** SHALL — Harms refer to any adverse effects that would be experienced by an impacted entity. They provide a means to effectively understand the impact categories and how they may apply to specific entities impacted by the online service. For each impact category, organizations SHALL consider potential harms for each of the impacted entities identified in Sec. 3.1. ^63-3-2-1-3

### 63 §3.2.2 Identify Potential Impact Levels

- **63-3.2.2-1** SHALL — Each user group can have a distinct set of privileges and functionalities through the online service. Hence, it is necessary to consider the adverse consequences for each set of impacted entities in each of the impact categories, as a result of an intruder obtaining unauthorized access as a member of a particular user group. To provide a more objective basis for impact level assignments, organizations SHOULD develop thresholds and examples for the impact levels for each impact category. Where this is done, particularly with specifically defined quantifiable values, these thresholds SHALL be documented and used consistently in the DIRM assessments across an organization to allow for a common understanding of risks. ^63-3-2-2-1
- **63-3.2.2-2** MAY — This guideline provides three impact levels. However, organizations MAY define more granular impact levels and develop their own methodologies for their initial impact assessment activities. ^63-3-2-2-2

### 63 §3.2.3 Impact Analysis

- **63-3.2.3-1** SHALL — The impact analysis SHALL consider the level of impact for each impact category for each type of impacted entity if an intruder obtains unauthorized access as a member of each user group. Because different sets of transactions are available to each user group, it is important to consider each user group separately for this analysis. ^63-3-2-3-1
- **63-3.2.3-2** SHALL — The impact analysis SHALL be performed for each user group that has access to the online service. For each impact category, the impact level is estimated for each impacted entity as a result of a compromise of the online service caused by failures in the identity management functions. ^63-3-2-3-2
- **63-3.2.3-3** SHALL — The output of this impact analysis is a set of impact levels for each user group that SHALL be documented in a suitable format for further analysis in accordance with Sec. 3.4. ^63-3-2-3-3

### 63 §3.2.4 Determine the Combined Impact Level for Each User Group

- **63-3.2.4-1** SHALL — Organizations SHALL document the approach they use to combine their impact assessment into an overall impact level for each of their defined user groups and SHALL apply it consistently across all of its online services. At the conclusion of the combinatorial analysis, organizations SHALL document the impact for each user group. ^63-3-2-4-1

### 63 §3.3.1 Assurance Levels

- **63-3.3.1-1** SHALL — Depending on the functionality and deployed architecture of the online service, the support of one or more of the identity management functions (i.e., identity proofing, authentication, and federation) may be required. The strength of these functions is described in terms of assurance levels. The RP SHALL identify the types of assurance levels that apply to their online service from the following: ^63-3-3-1-1

### 63 §3.3.3 Initial Assurance Level Selection

- **63-3.3.3-1** SHALL — Organizations SHALL develop and document a process and governance model for selecting initial assurance levels and controls based on the potential impacts of failures in the digital identity system. The following subsections provide guidance on the major elements to consider in the process for selecting initial assurance levels. ^63-3-3-3-1

### 63 §3.3.3.1 Selecting Initial IAL

- **63-3.3.3.1-1** SHALL — The organization SHALL document whether identity proofing is required for their application and, if it is, SHALL select an initial IAL for each user group based on the effective impact level determination from Sec. 3.2.4. ^63-3-3-3-1-1

### 63 §3.3.3.2 Selecting Initial AAL

- **63-3.3.3.2-1** SHALL — The organization SHALL document whether authentication is needed for their online service and, if it is, SHALL select an initial AAL for each user group based on the effective impact level determination from Sec. 3.2.4. ^63-3-3-3-2-1

### 63 §3.3.3.3 Selecting Initial FAL

- **63-3.3.3.3-1** SHOULD — Identity federation brings many benefits, including a convenient customer experience that avoids redundant, costly, and often time-consuming identity processes. The benefits of federation through a general-purpose IdP model or a subscriber-controlled wallet model are covered in Sec. 5 of [SP800-63C]. However, not all online services will be able to make use of federation, whether for risk-based reasons or due to legal or regulatory requirements. Consistent with [M-19-17], federal agencies that operate online services SHOULD implement federation as an option for user access. ^63-3-3-3-3-1
- **63-3.3.3.3-2** SHALL — The organization SHALL document whether federation will be used for their online service and, if it is, SHALL select an initial FAL for each user group based on the effective impact level determination from Sec. 3.2.4. ^63-3-3-3-3-2
- **63-3.3.3.3-3** SHALL — For online services that are assessed to be high impact, organizations SHALL conduct a further assessment to evaluate the risk of a compromised IdP to determine whether FAL2 or FAL3 is more appropriate for their use case. Considerations SHOULD include the type of data being accessed, the location of the IdP (e.g., whether the IdP is internal or external to their enterprise boundary), and the availability of bound authenticators or holder-of-key capabilities. ^63-3-3-3-3-3

### 63 §3.3.4 Identify Baseline Controls

- **63-3.3.4-1** SHALL — Using the initial xALs selected in Sec. 3.3.3, the organization SHALL identify the applicable baseline controls for each user group as follows: ^63-3-3-4-1

### 63 §3.4 Tailor and Document Assurance Levels

- **63-3.4-1** SHALL — Within the tailoring step, organizations SHALL focus on impacts to mission delivery due to the implementation of identity management controls, including the possibility of legitimate users who are unable to access desired online services or experience sufficient friction or frustration with the identity system (and technology selection) that they abandon attempts to access the online service. ^63-3-4-1
- **63-3.4-2** SHALL — As a part of the tailoring process, organizations SHALL review the Digital Identity Acceptance Statements and practice statements1 from CSPs and IdPs that they use or intend to use. However, organizations SHALL also conduct their own analysis to ensure that the organization’s specific mission and the communities being served by the online service are given due consideration for tailoring purposes. As a result, the organization MAY require their chosen CSP to strengthen or provide optionality in the implementation of certain controls to address risks and unintended impacts to the organization’s mission and the communities served. ^63-3-4-2
- **63-3.4-3** SHOULD — To promote interoperability and consistency, organizations SHOULD implement their assessed or tailored xALs consistent with the normative guidance in this document. However, these guidelines provide flexibility to allow organizations to tailor the initial xALs and related controls to meet specific mission needs, address unique risk appetites, and provide secure and accessible online services. In doing so, CSPs MAY offer and organizations MAY utilize tailored sets of controls that differ from the normative statements in this guideline. ^63-3-4-3
- **63-3.4-4** SHALL — Organizations SHALL establish and document their xAL tailoring process. At a minimum, this process: ^63-3-4-4
- **63-3.4-5** SHALL — SHALL follow a documented governance approach to allow for decision-making ^63-3-4-5
- **63-3.4-6** SHALL — SHALL document all decisions in the tailoring process, including the assessed xALs, modified xALs, and supplemental and compensating controls in the Digital Identity Acceptance Statement (see Sec. 3.4.4) ^63-3-4-6
- **63-3.4-7** SHALL — SHALL justify and document all risk-based decisions or modifications to the initially assessed xALs in the Digital Identity Acceptance Statement (see Sec. 3.4.4) ^63-3-4-7
- **63-3.4-8** SHOULD — SHOULD establish a cross-functional capability to support subject-matter analysis of xAL selection impacts in the tailoring process (e.g., subject-matter experts who can speak about risks and considerations related to privacy, customer experience, fraud and impersonation impacts, and other germane areas) ^63-3-4-8

### 63 §3.4.1 Assess Privacy, Customer Experience, and Threat Resistance

- **63-3.4.1-1** SHALL — When selecting and tailoring assurance levels for specific online services, considerations extend beyond the initial impact assessment in Sec. 3.2. When progressing from the initial assurance level selection in Sec. 3.3.4 to the final xAL selection and implementation, organizations SHALL conduct detailed assessments of the controls defined for the initially selected xALs to identify potential impacts in the operational environment. ^63-3-4-1-1
- **63-3.4.1-2** SHALL — At a minimum, organizations SHALL assess the impacts and potential unintended consequences related to the following areas: ^63-3-4-1-2
- **63-3.4.1-3** SHOULD — Privacy – Identify unintended consequences to the privacy of individuals who will be subject to the controls at an assessed xAL and of individuals affected by organizational or third-party practices related to the establishment, management, or federation of a digital identity. A privacy assessment SHOULD leverage an existing Privacy Threshold Analysis (PTA) or Privacy Impact Assessment (PIA) as inputs during the privacy assessment process.2 However, as the goal of the privacy assessment is to identify privacy risks that arise from the initial assurance level selection, additional assessments and evaluations that are specific to the baseline controls for the assurance levels may be required for the underlying information system. ^63-3-4-1-3
- **63-3.4.1-4** SHALL — Customer Experience – Determine whether implementation of the initial assurance levels may create substantial or unacceptable barriers to individuals seeking to access services. Customer experience assessments SHALL consider impacts that result from the identity management controls to ensure that they do not cause undue burdens, frustrations, or frictions for individuals and that there are pathways to provide service to users of all capabilities, resources, technology access, and economic statuses. ^63-3-4-1-4
- **63-3.4.1-5** SHALL — Threat Resistance – Determine whether the defined assurance level and related controls will address specific threats to the online service based on the operational environment, its threat actors, and known tactics, techniques, and procedures (TTPs). Threat assessments SHALL consider specific known and potential threats, threat actors, and TTPs within the implementation environment for the identity management functions. For example, certain benefits programs may be more subject to familial threats or collusion. Based on their assessments, organizations MAY implement supplemental controls specific to the communities served by their online service. Conversely, organizations MAY tailor their assessed xAL down or modify their baseline controls if their threat assessment indicates that a reduced threat posture is appropriate based on their environment. ^63-3-4-1-5
- **63-3.4.1-6** SHOULD — Organizations SHOULD leverage consultation and feedback from the entities and communities served to ensure that the tailoring process addresses their known constraints. ^63-3-4-1-6
- **63-3.4.1-7** SHALL — Organizations SHOULD also conduct additional business-specific assessments as appropriate to fully represent mission- and domain-specific considerations that have not been captured here. All assessments applied during the tailoring phase SHALL be extended to any compensating or supplemental controls, as defined in Sec. 3.4.2 and Sec. 3.4.3. While identity system costs are not specifically included as an input for DIRM processes or as a metric for continuous evaluation, the costs and cost effectiveness of implementation and long-term operation are inherent considerations for responsible program and risk management. Based on their available funding and resources, organizations will likely need to make trade-offs that can be more effectively informed by the DIRM process and its outputs. Any cost-based decisions that result in modifications to assessed xALs or baseline controls SHALL be documented in the Digital Identity Acceptance Statement (see Sec. 3.4.4). ^63-3-4-1-7

### 63 §3.4.2 Identify Compensating Controls

- **63-3.4.2-1** SHALL — A compensating control is a management, operational, or technical control employed by an organization in lieu of a normative control (i.e., SHALL statements) in the defined xALs. To the greatest degree practicable, a compensating control is intended to address the same risks as the baseline control it is replacing. Organizations MAY choose to implement a compensating control if they are unable to implement a baseline control or when a risk assessment indicates that a compensating control sufficiently mitigates risk in alignment with organizational risk tolerance. This control MAY be a modification to the normative statements defined in these guidelines or MAY be applied elsewhere in an online service, digital transaction, or service life cycle. For example: ^63-3-4-2-1
- **63-3.4.2-2** SHALL — Where compensating controls are implemented, organizations SHALL document the compensating control, the rationale for the deviation, comparability of the chosen alternative, and any resulting residual risks. CSPs and IdPs that implement compensating controls SHALL communicate this information to all potential RPs prior to integration to allow the RP to assess and determine the acceptability of the compensating controls for their use cases. ^63-3-4-2-2

### 63 §3.4.3 Identify Supplemental Controls

- **63-3.4.3-1** SHOULD — Supplemental controls may be added to further strengthen the baseline controls specified for the organization’s selected assurance levels. Organizations SHOULD identify and implement supplemental controls to address specific threats in the operational environment that may not be addressed by the baseline controls. For example: ^63-3-4-3-1
- **63-3.4.3-2** SHALL — Any supplemental controls SHALL be assessed for impacts based on the same factors used to tailor the organization’s assurance level and SHALL be documented. ^63-3-4-3-2

### 63 §3.4.4 Digital Identity Acceptance Statement

- **63-3.4.4-1** SHALL — Organizations SHALL develop a Digital Identity Acceptance Statement (DIAS) to document the results of the DIRM process for (i) each online service managed by the organization, and (ii) each external online service used to support the mission of the organization, including software-as-a-service offerings (e.g., social media platforms, email services, online marketing services). RPs who intend to use a particular CSP/IdP SHALL review the latter’s DIAS and incorporate relevant information into the organization’s DIAS for each online service. ^63-3-4-4-1
- **63-3.4.4-2** SHALL — Organizations SHALL prepare a DIAS for their online service that includes, at a minimum: ^63-3-4-4-2
- **63-3.4.4-3** SHOULD — Federal agencies SHOULD include this information in the information system authorization package described in [NISTRMF]. ^63-3-4-4-3
- **63-3.4.4-4** SHALL — CSPs/IdPs SHALL implement the DIRM process and develop a DIAS for the services they offer if they deviate from the normative guidance in these guidelines, including when supplemental or compensating controls are added. To complete a DIRM of their offered assurance levels and controls, CSPs/IdPs MAY base their assessment on anticipated or representative digital identity services that they wish to support. In creating this risk assessment, they SHOULD seek input from real-world RPs on their user populations and anticipated context. The DIAS prepared by a CSP SHALL include, at a minimum: ^63-3-4-4-4
- **63-3.4.4-5** SHALL — The DIRM process for external online services used by the organization SHALL consider relevant inputs from the provider of the service and document the results in a DIAS. The DIAS prepared by the organization for external online services SHALL include, at a minimum: ^63-3-4-4-5

### 63 §3.5 Continuously Evaluate and Improve

- **63-3.5-1** SHALL — To address the shifting environment in which they operate and more rapidly address service capability gaps, organizations SHALL implement a continuous evaluation and improvement program that leverages input from end users who have interacted with the identity management system as well as performance metrics for the online service. This program SHALL be documented, including the metrics that are collected, the sources of data required to enable performance evaluation, and the processes in place for taking timely actions based on the continuous improvement process. This program and its effectiveness SHOULD be assessed on a regular basis to ensure that outcomes are being achieved and that programs are addressing issues in a timely manner. ^63-3-5-1
- **63-3.5-2** SHALL — Additionally, organizations SHALL monitor the evolving threat landscape to stay informed of the latest threats and fraud tactics. Organizations SHALL regularly assess the effectiveness of current security measures and fraud detection capabilities against the latest threats and fraud tactics. ^63-3-5-2

### 63 §3.5.1 Evaluation Inputs

- **63-3.5.1-1** SHALL — To fully understand the performance of their identity system, organizations will need to identify critical inputs to their continuous evaluation process. At a minimum, these inputs SHALL include: ^63-3-5-1-1
- **63-3.5.1-2** SHALL — RPs SHALL document their metrics, reporting requirements, and data inputs for any CSP, IdP, or other integrated identity service to ensure that expectations are appropriately communicated to partners and vendors. ^63-3-5-1-2

### 63 §3.5.2 Performance Metrics

- **63-3.5.2-1** SHOULD — The exact metrics available to organizations will vary based on the technologies, architectures, and deployment methods they use. Additionally, the availability and usefulness of certain metrics will vary over time. Therefore, these guidelines do not attempt to define a comprehensive set of metrics for all scenarios. Table 4 provides a set of recommended metrics that organizations SHOULD track as part of their continuous evaluation program. However, organizations are not constrained by this table and SHOULD implement metrics based on their specific systems, technology, and program needs. See [SP800-55V2] for more information on identifying additional performance metrics. In Table 4, all references to unique users include both legitimate users and imposters. ^63-3-5-2-1

### 63 §3.5.3 Measurement in Support of Customer Experience Outcomes

- **63-3.5.3-1** SHOULD — A primary goal of continuous improvement is to enhance customer experience, usability, and accessibility outcomes for different user populations. As a result, the metrics collected by organizations SHOULD be further evaluated to provide insights into the performance of their identity management systems for their supported communities. Where possible, these efforts SHOULD avoid the collection of additional personal information and instead use informed analyses of proxy data to identify potential performance issues. This can include comparing and filtering the metrics to understand deviations in performance across different user populations based on other available data, such as zip code, geographic region, age, or sex. ^63-3-5-3-1

### 63 §3.6 Redress

- **63-3.6-1** SHALL — RPs and CSPs SHALL enable individuals to convey grievances and seek redress through an issue handling process that is documented, accessible, trackable, and usable by all individuals and whose instructions are easy to find on a public-facing website. ^63-3-6-1
- **63-3.6-2** SHALL — RPs and CSPs SHALL institute a governance model for implementing this issue handling process, including documented roles and responsibilities. ^63-3-6-2
- **63-3.6-3** SHALL — The issue handling process SHALL be implemented as a dedicated function that includes procedures for: Impartially reviewing pertinent evidence, Requesting and collecting additional evidence that informs the issues, and Expeditiously resolving issues and determining corrective action. ^63-3-6-3
- **63-3.6-4** SHALL — RPs and CSPs SHALL make human support personnel available to intervene and override issue adjudication outputs generated by algorithmic support mechanisms. ^63-3-6-4
- **63-3.6-5** SHALL — RPs and CSPs SHALL educate support personnel on issue handling procedures for the digital identity management system, the avenues for redress, and the alternatives available to gain access to services. ^63-3-6-5
- **63-3.6-6** SHALL — RPs and CSPs SHALL implement a process for personnel and technologies that provides support functions to report and address major barriers that end users face and grievances they may have. ^63-3-6-6
- **63-3.6-7** SHALL — RPs and CSPs SHALL incorporate findings derived from the issue handling process into continuous evaluation and improvement activities. ^63-3-6-7
- **63-3.6-8** SHALL — Organizations are encouraged to consider these and other emerging redress practices. Prior to adopting any new redress practice, including supporting technology, organizations SHOULD test the practice with users to avoid the introduction of unintended consequences, particularly those that may counteract or contradict the goals associated with redress. In addition, organizations SHALL assess the integrity and performance of their redress mechanisms and implement controls to prevent, detect, and remediate attempted identity fraud involving those mechanisms. ^63-3-6-8

### 63 §3.7 Cybersecurity, Fraud, and Identity Program Integrity

- **63-3.7-1** SHALL — The close coordination of identity functions with teams that are responsible for cybersecurity, privacy, threat intelligence, fraud detection, and program integrity enables a more complete protection of business capabilities and constant improvement. For example, payment fraud data collected by program integrity teams could provide indicators of compromised subscriber accounts and potential weaknesses in identity proofing implementations. Similarly, threat intelligence teams may learn of new TTPs that could impact identity proofing, authentication, and federation processes. Organizations SHALL establish consistent mechanisms for the exchange of information between stakeholers that are responsible for critical internal security and fraud prevention. Organizations SHOULD do the same for external stakeholders and identity services that comprise their online services. ^63-3-7-1
- **63-3.7-2** SHALL — When organizations are supported by external identity providers (e.g., CSPs), the exchange of data related to security, fraud, and other RP functions may be complicated by regulations or policy. However, establishing the necessary mechanisms and guidelines to enable effective information sharing SHOULD be considered in contractual and legal mechanisms. All data collected, transmitted, or shared by the identity service provider SHALL be subject to a detailed privacy and legal assessment by either the entity generating the data (e.g., a CSP) or the related RP for whom the service is provided. ^63-3-7-2

### 63 §3.8 Artificial Intelligence and Machine Learning in Identity Systems

- **63-3.8-1** SHALL — All uses of AI/ML SHALL be documented and communicated to organizations that rely on these systems. The use of integrated technologies that leverage AI/ML by CSPs, IdPs, or verifiers SHALL be disclosed to all RPs that make access decisions based on information from these systems. ^63-3-8-1
- **63-3.8-2** SHALL — All organizations that use AI/ML SHALL provide information to any entities that use their technology on the methods and techniques used for training their models, a description of the data sets used in training, information on the frequency of model updates, and the results of all testing completed on their algorithms. ^63-3-8-2
- **63-3.8-3** SHOULD — All organizations that use AI/ML systems or rely on services that use these systems SHOULD implement the NIST AI Risk Management Framework ([NISTAIRMF]) to evaluate the risks that may be introduced by such systems. ^63-3-8-3
- **63-3.8-4** SHALL — All organizations that use AI/ML systems or rely on services that use these systems SHALL perform and document privacy risk assessments for personal information and data processed by such systems. ^63-3-8-4

## SP 800-63A-4 Identity Proofing and Enrollment

### 63A §1.3 Notations

- **63A-1.3-1** SHALL NOT — The terms “SHALL” and “SHALL NOT” indicate requirements to be followed strictly in order to conform to the publication and from which no deviation is permitted. ^63a-1-3-1
- **63A-1.3-2** SHOULD NOT — The terms “SHOULD” and “SHOULD NOT” indicate that among several possibilities, one is recommended as particularly suitable without mentioning or excluding others, that a certain course of action is preferred but not necessarily required, or that (in the negative form) a certain possibility or course of action is discouraged but not prohibited. ^63a-1-3-2
- **63A-1.3-3** MAY — The terms “MAY” and “NEED NOT” indicate a course of action permissible within the limits of the publication. ^63a-1-3-3

### 63A §2 Identity Proofing Overview

- **63A-2-1** SHOULD — These guidelines provide multiple methods by which resolution, validation, and verification can be accomplished, as well as multiple types of identity evidence that support the identity proofing process. CSPs and organizations SHOULD provide options when implementing their identity proofing services and processes to promote access for applicants with different means, capabilities, and technologies. These options SHOULD include accepting multiple types and combinations of identity evidence, supporting multiple data validation sources, enabling multiple methods for verifying identity, providing multiple identity proofing types, and offering exception handling for applicants (e.g., trusted referees, applicant references). ^63a-2-1
- **63A-2-2** SHALL — CSPs SHALL evaluate the risks associated with each identity proofing option offered (e.g., identity proofing types, validation sources, assistance mechanisms) and implement mitigating fraud controls, as appropriate. At a minimum, CSPs SHALL design each option such that the options provide comparable assurance in aggregate. ^63a-2-2

### 63A §2.1.2 Identity Proofing Roles

- **63A-2.1.2-1** SHALL — CSPs SHALL identify which of the above roles are applicable to their identity service and SHALL provide training and support resources consistent with the requirements and expectations provided in Sec. 3. ^63a-2-1-2-1

### 63A §2.1.3 Identity Proofing Types

- **63A-2.1.3-1** SHOULD — The requirements at each assurance level are structured to allow CSPs to implement different combinations of identity proofing types to meet the requirements of different assurance levels, as appropriate. CSPs SHOULD offer the combination of identity proofing types that best addresses the needs of the populations served by their identity service and the risk posture of the RPs that use their service. ^63a-2-1-3-1

### 63A §2.2 Core Attributes

- **63A-2.2-1** SHALL — The identity proofing process involves the presentation and validation of the minimum attributes necessary to accomplish identity proofing, including what is needed to complete resolution, validation, and verification. The CSP determines and documents the set of attributes that it considers to be core attributes, as specified in Sec. 3.1. CSPs SHALL include a government identifier1 and SHOULD include the following in their set of core attributes for identity proofing at any IAL: ^63a-2-2-1
- **63A-2.2-2** SHALL — Additional attributes MAY be added to these as required by the CSP and RP. The CSP and RP SHALL document all core attributes in trust agreements and practice statements. Following a privacy risk assessment, a CSP MAY request additional attributes that are not required to complete identity proofing, but that may support other RP business processes. See Sec. 3.3 for details on privacy requirements for requesting additional attributes. ^63a-2-2-2

### 63A §2.4.1.1 Fair Evidence Requirements

- **63A-2.4.1.1-1** SHALL — To be considered FAIR, identity evidence SHALL meet all of the following requirements: ^63a-2-4-1-1-1

### 63A §2.4.1.2 Strong Evidence Requirements

- **63A-2.4.1.2-1** SHALL — In order to be considered STRONG, identity evidence SHALL meet all of the following requirements: ^63a-2-4-1-2-1

### 63A §2.4.1.3 Superior Evidence Requirements

- **63A-2.4.1.3-1** SHALL — In order to be considered SUPERIOR, identity evidence SHALL meet all of the following requirements: ^63a-2-4-1-3-1

### 63A §2.4.2.1 Evidence Validation

- **63A-2.4.2.1-1** SHALL — The CSP SHALL validate the authenticity, accuracy, and validity of presented evidence by confirming that: ^63a-2-4-2-1-1

### 63A §2.4.2.3 Attribute Validation

- **63A-2.4.2.3-1** SHALL — The CSP SHALL validate all core attributes (Sec. 2.2), whether obtained from identity evidence or self-asserted by the applicant, with an authoritative or credible source (Sec. 2.4.2.4). ^63a-2-4-2-3-1

### 63A §2.4.2.4 Validation Sources

- **63A-2.4.2.4-1** SHALL — The CSP SHALL use authoritative or credible sources that meet the following criteria. ^63a-2-4-2-4-1

### 63A §2.5.1 Identity Verification Methods

- **63A-2.5.1-1** SHALL — The CSP SHALL verify the linkage between the claimed identity to the applicant engaged in the identity proofing process through one or more of the following methods. ^63a-2-5-1-1
- **63A-2.5.1-2** SHALL NOT — Knowledge-based verification (KBV) or knowledge-based authentication SHALL NOT be used for identity verification. ^63a-2-5-1-2

### 63A §3.1 Identity Service Documentation and Records

- **63A-3.1-1** SHALL — The CSP SHALL conduct its operations according to documented procedures or a practice statement that details all identity proofing processes as they are implemented to achieve the defined IAL. These documented procedures SHALL include, at a minimum: ^63a-3-1-1
- **63A-3.1-2** SHALL — CSPs SHALL make their documented procedures or practice statements available to RPs that use their identity service. CSPs SHOULD make a summarized version of their documented procedures or practice statements publicly available. ^63a-3-1-2
- **63A-3.1-3** MAY — SP 800-63C describes the use of trust agreements to define requirements between an identity provider (IdP), CSP, and RP in a federated relationship. CSP practice statements MAY be included directly in these agreements. ^63a-3-1-3

### 63A §3.2.1 CSP Fraud Management

- **63A-3.2.1-1** SHALL — CSPs SHALL establish and maintain a fraud management program that provides fraud identification, detection, investigation, reporting, and resolution capabilities. The specific capabilities and details of this program SHALL be documented within their CSP practice statement. ^63a-3-2-1-1
- **63A-3.2.1-2** SHALL — CSPs SHALL conduct a privacy risk assessment of all fraud checks and fraud mitigation technologies prior to implementation. ^63a-3-2-1-2
- **63A-3.2.1-3** SHALL — The CSP SHALL establish a self-reporting mechanism and investigation capability for subjects who believe they have been the victim of fraud or an attempt to compromise their involvement in the identity proofing processes. ^63a-3-2-1-3
- **63A-3.2.1-4** SHALL — CSPs SHALL analyze all remote proofing communication channels to look for high-risk indicators (e.g., blocklisted proxies and IP addresses). ^63a-3-2-1-4
- **63A-3.2.1-5** SHALL — The CSP SHALL take measures to prevent unsuccessful applicants from inferring the accuracy of any self-asserted information with that confirmed by authoritative or credible sources.1 ^63a-3-2-1-5
- **63A-3.2.1-6** SHALL — CSPs SHALL monitor the performance of their fraud checks and fraud mitigation technologies to ensure continued effectiveness in mitigating fraud risks. ^63a-3-2-1-6
- **63A-3.2.1-7** SHALL — CSPs SHALL establish a technical or process-based mechanism to communicate suspected and confirmed fraudulent events to RPs. ^63a-3-2-1-7
- **63A-3.2.1-8** SHALL — CSPs SHALL implement a death records check for all identity proofing processes by confirming with a credible, authoritative, or issuing source that the applicant is not deceased. Such checks can aid in preventing synthetic identity fraud, the use of stolen identity information, and exploitation by a close associate or relative. ^63a-3-2-1-8
- **63A-3.2.1-9** SHALL — Fraud indicator check: Evaluate records (e.g., reported, confirmed, or historical fraud events) to determine whether there is an elevated risk related to a specific applicant, applicant’s data, or device. Such checks can indicate identity theft or compromise. Where such information is collected, aggregated, or exchanged across commercial platforms and made available for use by RPs and other CSPs, users SHALL be made aware of any privacy implications based on a privacy risk assessment. This also applies to all websites that report user activity to federal RPs. ^63a-3-2-1-9
- **63A-3.2.1-10** SHOULD — CSPs SHOULD periodically employ independent testing (e.g., red teaming exercises) to validate the effectiveness of their fraud mitigation measures. ^63a-3-2-1-10
- **63A-3.2.1-11** SHOULD — CSPs SHOULD consider the recency of fraud-related data when factoring such data into fraud prevention capabilities and decisions. ^63a-3-2-1-11
- **63A-3.2.1-12** SHALL — For attended proofing processes, CSPs SHALL train proofing agents to detect indicators of fraud and SHALL provide proofing agents and trusted referees with tools to flag suspected fraudulent events for further treatment and investigation. ^63a-3-2-1-12
- **63A-3.2.1-13** SHALL — Collusion is possible whenever CSP representatives are directly involved in proofing processes or decisions. CSPs SHALL implement insider threat controls to detect and prevent collusion involving CSP representatives that are directly involved with or can intervene in proofing processes or decisions. ^63a-3-2-1-13
- **63A-3.2.1-14** SHOULD — CSPs SHOULD communicate fraud events in real time to RPs through methods such as shared signaling, as described in Sec. 4.8 of [SP800-63C]. ^63a-3-2-1-14
- **63A-3.2.1-15** MAY — CSPs MAY employ KBV as part of its fraud management program. ^63a-3-2-1-15
- **63A-3.2.1-16** SHALL — CSPs MAY implement fraud mitigation measures as compensating controls. When this is done, these SHALL be documented as deviations from the normative guidance of these guidelines and SHALL be conveyed to all RPs through a Digital Identity Acceptance Statement (DIAS) prior to integration. See Sec. 3.4.4 of [SP800-63] for more information about the DIAS. ^63a-3-2-1-16
- **63A-3.2.1-17** SHALL — CSPs that employ artificial intelligence (AI) or machine learning (ML) as part of their identity service SHALL adhere to the requirements provided in Sec. 3.8 of [SP800-63], as applicable. ^63a-3-2-1-17

### 63A §3.2.2 RP Fraud Management

- **63A-3.2.2-1** SHALL — RPs SHALL establish a point of contact with whom CSPs can interact and communicate fraud data. ^63a-3-2-2-1
- **63A-3.2.2-2** SHALL — RPs SHALL conduct a privacy risk assessment (see Sec. 3.3.1) of any CSP fraud checks and mitigation technologies to identify potential privacy risks or unintended harms. Federal agency RPs SHALL implement this consistent with the requirements contained in Sec. 3.7. ^63a-3-2-2-2
- **63A-3.2.2-3** SHOULD — RPs SHOULD include any requirements for fraud checks and fraud mitigation technologies in trust agreements with their CSPs. ^63a-3-2-2-3
- **63A-3.2.2-4** SHALL — RPs SHALL conduct periodic reviews of their CSP’s fraud management program, fraud checks, and fraud technologies to adjust thresholds, review investigations into fraud events, and evaluate the effectiveness and efficacy of fraud controls. ^63a-3-2-2-4
- **63A-3.2.2-5** SHALL — RPs SHALL review all fraud mitigation measures that have been deployed as compensating or supplemental controls by CSPs to align with their internal risk tolerance and acceptance. The RP SHALL record the CSP’s compensating controls in their own DIAS prior to integration. ^63a-3-2-2-5
- **63A-3.2.2-6** SHOULD — Pursuant to applicable laws and regulations, RPs SHOULD establish a mechanism to communicate the outcomes of fraud reports and investigations, including both positive and negative results, to CSPs and other partners in order to allow them to improve their own fraud identification, mitigation, and reporting capabilities. ^63a-3-2-2-6
- **63A-3.2.2-7** SHOULD — RPs SHOULD establish a fraud management program for digital identity management consistent with their mission, regulatory environment, systems, applications, data, and resources. ^63a-3-2-2-7
- **63A-3.2.2-8** MAY — Informed by risks identified in a privacy risk assessment, the RP MAY also request additional attributes beyond what a CSP provides as its core attributes to combat fraud or to support other business processes. ^63a-3-2-2-8

### 63A §3.2.3 Treatment of Fraud Check Failures

- **63A-3.2.3-1** SHALL — CSPs SHALL establish and document actions and practices related to each of their fraud checks and provide these actions and practices to RPs. ^63a-3-2-3-1
- **63A-3.2.3-2** SHALL — CSPs SHALL establish procedures for redress to allow applicants to resolve issues associated with fraud checks and mitigation technologies. See Sec. 3.6 of [SP800-63] for more information about redress. ^63a-3-2-3-2
- **63A-3.2.3-3** SHALL — The CSP SHOULD offer trusted referee services to applicants who fail fraud checks in unattended remote processes. If trusted referees are offered to applicants who fail fraud checks in unattended remote processes, the trusted referees SHALL be provided with a summary of the results of the fraud failures to inform their risk-based decision-making processes. ^63a-3-2-3-3

### 63A §3.3.1 Privacy Risk Assessment

- **63A-3.3.1-1** SHALL — The CSP SHALL conduct and document a privacy risk assessment for the processes used for identity proofing and enrollment.2 At a minimum, the privacy risk assessment SHALL assess the risks associated with: Processing personal information for the purposes of identity proofing, enrollment, or fraud management, including identity attributes, biometrics, images, video, scans, or copies of identity evidence Additional steps that the CSP takes to verify the identity of an applicant beyond the mandatory requirements specified herein Processing of personal information for purposes outside of the scope of identity proofing and enrollment, except to comply with law or legal processes The retention schedule for identity records and personal information Processing non-personal information that could be used to identify a person when aggregated or processed by an algorithm (e.g., AI or ML tools) Personal information that is processed by a third-party service on behalf of the CSP ^63a-3-3-1-1
- **63A-3.3.1-2** SHALL — Based on the results of its privacy risk assessment, the CSP SHALL document the measures it takes to maintain the disassociability, predictability, manageability, confidentiality, integrity, and availability of any personal information it collects or processes.3 In determining such measures, the CSP SHOULD apply relevant guidance and standards, such as the NIST Privacy Framework [NIST-Privacy] and NIST SP 800-53 [SP800-53]. ^63a-3-3-1-2
- **63A-3.3.1-3** SHALL — The CSP SHALL reassess privacy risks and update its privacy risk assessment any time it makes changes to its identity service that affect the processing of personal information. ^63a-3-3-1-3
- **63A-3.3.1-4** SHALL — The CSP SHALL review its privacy risk assessment periodically, as documented in its practice statement, to ensure that it accurately reflects the current risks associated with the collection and processing of personal information. ^63a-3-3-1-4
- **63A-3.3.1-5** SHALL — The CSP SHALL make a summary of its privacy risk assessment available to any RPs that use its services. The summary SHALL be in sufficient detail to enable such RPs to make reasonable determinations about privacy risks associated with the CSPs services and to complete their own privacy risk assessments. ^63a-3-3-1-5
- **63A-3.3.1-6** SHALL — The CSP SHALL perform a privacy risk assessment for the processing of any personal information maintained in subscriber accounts (see Sec. 5). ^63a-3-3-1-6

### 63A §3.3.2 Additional Privacy Protective Measures

- **63A-3.3.2-1** SHALL — The processing of personal information SHALL be limited to the minimum necessary to validate the existence of the claimed identity, associate the claimed identity with the applicant, mitigate fraud, and provide RPs with attributes that they may use to make authorization decisions. ^63a-3-3-2-1
- **63A-3.3.2-2** SHALL — The CSP SHALL provide privacy training to all personnel and any third-party service providers who have access to sensitive information associated with the CSP’s identity service. ^63a-3-3-2-2
- **63A-3.3.2-3** SHALL — The CSP MAY collect a Social Security number (SSN) as an attribute when necessary for identity resolution. Knowledge of an SSN is not sufficient to act as evidence of identity, nor is it considered an acceptable method of verifying possession of the Social Security card when used as evidence. If the SSN is collected on behalf of a federal, state, or local government agency, the CSP SHALL provide notice to the applicant for the collection in accordance with applicable laws. ^63a-3-3-2-3
- **63A-3.3.2-4** SHALL — At the time of collection, the CSP SHALL provide explicit notice to the applicant regarding the purpose for collecting any attributes and personal information. Such a notice SHALL include whether the personal information and attributes are voluntary or mandatory to complete the identity proofing process, the specific attributes and other sensitive data that the CSP intends to store in the applicant’s subsequent subscriber account, the consequences of not providing the attributes, and the details of any records retention requirement if one is in place, including an applicant’s right to request data deletion or engage in other forms of redress. ^63a-3-3-2-4
- **63A-3.3.2-5** SHOULD — CSPs SHOULD implement techniques that protect an applicant’s privacy based on the privacy considerations in Sec. 7. ^63a-3-3-2-5

### 63A §3.4 General Customer Experience Requirements

- **63A-3.4-1** SHALL — The CSP SHALL assess the elements of its identity proofing processes to identify processes or technologies that can result in customer experience challenges, particularly if those challenges prevent the CSP from consistently delivering identity proofing services to all users served by an RP. ^63a-3-4-1
- **63A-3.4-2** SHALL — CSPs SHALL provide RPs with a summary of their customer experience assessments that includes information about common challenges or issues faced by users. ^63a-3-4-2
- **63A-3.4-3** SHALL — Based on the results of its assessment, the CSP SHALL document any measures it takes to mitigate the possible access challenges. ^63a-3-4-3
- **63A-3.4-4** SHALL — The CSP SHALL reassess the customer experience risks periodically and any time the CSP makes changes to its identity service that affect the processes or technologies that impact customer experience. ^63a-3-4-4
- **63A-3.4-5** SHALL NOT — The CSP SHALL NOT make applicant participation in these risk assessments mandatory. ^63a-3-4-5

### 63A §3.5 General Security Requirements

- **63A-3.5-1** SHALL — Each online transaction within the identity proofing process, including transactions that involve third parties, SHALL occur over an authenticated protected channel. ^63a-3-5-1
- **63A-3.5-2** SHALL — The CSP SHALL implement automated attack protections for the identity proofing process, such as bot detection, mitigation, and management solutions; behavioral analytics4; web application firewall settings; and network traffic analysis. ^63a-3-5-2
- **63A-3.5-3** SHALL — All personal information that is collected as part of the identity proofing process SHALL be protected to maintain the confidentiality and integrity of the information, including the encryption of data at rest and the exchange of information using authenticated protected channels. ^63a-3-5-3
- **63A-3.5-4** SHALL — The CSP SHALL assess the information security and privacy risks associated with operating its identity service, according to the NIST Risk Management Framework [NIST-RMF] or equivalent risk management guidelines. At a minimum, the CSP SHALL apply appropriate controls consistent with the NIST SP 800-53 [SP800-53] moderate baseline, regardless of IAL. ^63a-3-5-4
- **63A-3.5-5** SHALL — The CSP SHALL assess risks associated with its use of third-party services and apply appropriate controls, as provided in the [SP800-161] Cybersecurity Supply Chain Risk Management Practices for Systems and Organizations. ^63a-3-5-5

### 63A §3.6 Redress Requirements

- **63A-3.6-1** SHALL — The CSP SHALL provide mechanisms for the redress of applicant complaints and problems that arise from the identity proofing process, including proofing failures, delays, difficulties, and the recovery of a compromised subscriber account (e.g., as a result of a scam or fraud). ^63a-3-6-1
- **63A-3.6-2** SHALL — These redress mechanisms SHALL be easy for applicants to find and use. ^63a-3-6-2
- **63A-3.6-3** SHALL — The CSP SHALL assess the mechanisms for their efficacy in achieving a resolution of complaints or problems. ^63a-3-6-3

### 63A §3.7 Additional Requirements for Federal Agencies

- **63A-3.7-1** SHALL — The agency SHALL consult with their Senior Agency Official for Privacy (SAOP) to determine whether the collection of personal information, including biometrics, to conduct identity proofing triggers Privacy Act requirements. ^63a-3-7-1
- **63A-3.7-2** SHALL — The agency SHALL consult with their SAOP to determine whether the collection of personal information, including biometrics, to conduct identity proofing triggers E-Government Act of 2002 [E-Gov] requirements. ^63a-3-7-2
- **63A-3.7-3** SHALL — The agency SHALL publish a System of Records Notice (SORN) to cover such collections, as applicable.5 ^63a-3-7-3
- **63A-3.7-4** SHALL — The agency SHALL publish a Privacy Impact Assessment (PIA) to cover such collections, as applicable. ^63a-3-7-4
- **63A-3.7-5** SHOULD — The agency SHOULD consult with public affairs and communications professionals within their organization to determine whether a communications or public awareness strategy should be developed to accompany the implementation of any new process or update to an existing process, including requirements associated with identity proofing. Such strategies should consider the use of materials that describe how to use the technology associated with the service, a Frequently Asked Questions (FAQs) page, prerequisites to participate in the identity proofing process (e.g., required evidence), or media (e.g., webinars, live or pre-recorded information sessions) to support adoption of the identity service and provide applicants with a mechanism to communicate questions, issues, and feedback. ^63a-3-7-5
- **63A-3.7-6** SHALL — If the agency uses a third-party CSP, the agency SHALL conduct its own PIA and use the CSP’s privacy risk assessment as input. ^63a-3-7-6

### 63A §3.8 Requirements for Confirmation Codes

- **63A-3.8-1** SHALL — Confirmation codes used for these purposes SHALL include at least 6 decimal digits (or equivalent) from an approved random bit generator (see Sec. 3.2.12 of [SP800-63B]). The confirmation code may be presented as numeric or printable ASCII representation for manual entry, a secure (e.g., https) link containing a representation of the confirmation code, or a machine-readable optical label (e.g., QR code) that contains the confirmation code. ^63a-3-8-1
- **63A-3.8-2** SHALL — Confirmation codes SHALL be valid for at most: ^63a-3-8-2
- **63A-3.8-3** SHALL — Upon its use, the CSP SHALL invalidate the confirmation code. ^63a-3-8-3

### 63A §3.9 Requirements for Continuation Codes

- **63A-3.9-1** SHOULD — As such, CSPs MAY use continuation codes when an applicant is unable to complete all of the steps necessary to be successfully identity-proofed and enrolled into the CSP’s identity service in a single session, particularly when switching between different identity proofing types. Continuation codes are intended to be maintained offline (e.g., printed or written down) and stored in a secure location by the applicant for use in reestablishing linkage to a previous, incomplete session. In order to facilitate the authentication of the applicant to a subsequent session with the CSP, the CSP SHOULD first bind an authenticator to a record or account that was established for the applicant prior to the cessation of the initial session. ^63a-3-9-1
- **63A-3.9-2** SHOULD — Continuation codes SHOULD be delivered in-session but MAY be delivered out-of-band to a physical mailing address, phone number, or email address. ^63a-3-9-2
- **63A-3.9-3** SHALL — Continuation codes SHALL include at least 64 bits from an approved random bit generator (see Sec. 3.2.12 of [SP800-63B]). ^63a-3-9-3
- **63A-3.9-4** MAY — The continuation code MAY be presented as numeric or printable ASCII representation for manual entry or as a machine-readable optical label (e.g., QR code). ^63a-3-9-4
- **63A-3.9-5** SHALL — The verification of continuation codes SHALL be subject to throttling requirements, as provided in Sec. 3.2.2 of [SP800-63B]. ^63a-3-9-5
- **63A-3.9-6** SHALL — Continuation codes SHALL be stored in hashed form using a Federal Information Processing Standards (FIPS)-approved or NIST-recommended one-way function. ^63a-3-9-6
- **63A-3.9-7** SHALL — Upon its use, the CSP SHALL invalidate the continuation code. ^63a-3-9-7

### 63A §3.10 Requirements for Notifications of Identity Proofing

- **63A-3.10-1** SHALL — SHALL be sent to a validated postal address or phone number at all IALs or MAY be sent to a validated email address at IAL1 ^63a-3-10-1
- **63A-3.10-2** SHALL — SHALL include details about the identity proofing event, including the name of the identity service and the date on which the identity proofing was completed ^63a-3-10-2
- **63A-3.10-3** SHALL — SHALL provide clear instructions, including contact information, on actions for the recipient to take if they repudiate their participation in the identity proofing event ^63a-3-10-3
- **63A-3.10-4** SHALL — SHALL provide information about how the organization or CSP protects the security and confidentiality of the information it collects ^63a-3-10-4
- **63A-3.10-5** SHALL — SHALL provide information about any responsibilities that the recipient has as a subscriber of the identity service ^63a-3-10-5
- **63A-3.10-6** SHOULD — SHOULD provide instructions on how to access their subscriber account or information about how the subscriber can update the information contained in that account ^63a-3-10-6
- **63A-3.10-7** SHALL — If a subscriber repudiates having been identity-proofed by the identity service, the CSP or RP SHALL respond in accordance with its established fraud management and redress policies. ^63a-3-10-7

### 63A §3.11 Requirements for the Use of Biometrics

- **63A-3.11-1** SHALL — CSPs SHALL provide clear, publicly available information about all uses of biometrics, including what biometric data is collected, how it is stored and protected, and how to remove biometric data consistent with applicable laws and regulations. ^63a-3-11-1
- **63A-3.11-2** SHALL — CSPs SHALL obtain explicit informed consent to collect and use biometrics from all applicants. ^63a-3-11-2
- **63A-3.11-3** SHALL — CSPs SHALL store a record of the subscriber’s consent for biometric use and associate it with the subscriber’s account. ^63a-3-11-3
- **63A-3.11-4** SHALL — CSPs SHALL have a documented and publicly available deletion process and default retention period for all biometric information. Retention periods SHALL be consistent with applicable regulations, policies, and statutes for the regions and sectors that the CSP serves. ^63a-3-11-4
- **63A-3.11-5** SHALL — CSPs SHOULD support the deletion of all of a subscriber’s biometric information upon the subscriber’s request, except where otherwise restricted by regulation, law, or policy. CSPs that do not support biometric deletion requests SHALL publicly document the regulatory, statutory, or risk-based justification for their policy. ^63a-3-11-5
- **63A-3.11-6** SHALL — CSPs SHALL have their biometric recognition and attack detection algorithms periodically tested by independent entities (e.g., accredited laboratories or research institutions) for their performance characteristics, including performance across demographic groups. In addition, the CSP SHOULD conduct internal testing on biometric algorithms based on the update schedule of the provider. ^63a-3-11-6
- **63A-3.11-7** SHALL — CSPs SHALL assess the performance and demographic impacts of employed biometric technologies in conditions that are substantially similar to the operational environment and user base of the system. The user base is defined by both the expected users and the devices they are expected to use. When such assessments include real-world users, participation by users SHALL be voluntary. ^63a-3-11-7
- **63A-3.11-8** SHALL — CSPs SHALL meet the following performance thresholds if one-to-one (1:1) comparison algorithms are used for verification against a claimed identity: False match rate: 1:10,000 or better False non-match rate: 1:100 or better ^63a-3-11-8
- **63A-3.11-9** SHALL — CSPs MAY use one-to-many (1:N) identification in support of resolution or deduplication, pursuant to a privacy risk assessment. In 1:N scenarios, CSPs SHALL meet a minimum performance threshold for false positive identification of 1:1,000 or better. ^63a-3-11-9
- **63A-3.11-10** SHALL — A 1:N search of an applicant’s collected biometric characteristics against a database is done to determine whether the applicant is already present in the database, possibly under a different name. The false positive identification rate (FPIR) refers to the proportion of 1:N searches in which a biometric system incorrectly identifies another person as a match, which is a false positive result. The performance metric of 1:1,000 means that a false positive outcome occurs for no more than 1 in every 1,000 searches. Tests that demonstrate this requirement SHALL employ a gallery no smaller than 90 % of the current or intended operational size (N). ^63a-3-11-10
- **63A-3.11-11** SHALL NOT — CSPs that make use of 1:N biometric identification for resolution, deduplication, or fraud detection purposes SHALL NOT decline a user’s enrollment without a manual review to confirm the automated search results and confirm that the results are not a false positive identification (e.g., twins submitting face photographs for different accounts with the same CSP). ^63a-3-11-11
- **63A-3.11-12** SHALL — Biometric verification technologies SHALL provide performance for applicants of different demographic types that is no more than 25 % worse than the performance for the overall population. For example, if the measured false non-match rate (FNMR) for the overall population is 0.006, the FNMR for a specific demographic group cannot exceed 0.0075. Similarly, if the false match rate (FMR) for the overall population is 0.0001, the FMR for each demographic group cannot exceed 0.000125. The biometric system SHALL be configured with a fixed threshold; it is not feasible to change the threshold for each demographic group. Demographic categories to be considered SHALL include sex, age, and skin tone when these factors affect biometric performance. ^63a-3-11-12
- **63A-3.11-13** SHALL — All biometric performance tests SHALL be conformant to ISO/IEC 19795-1:2021 and ISO/IEC 19795-10:2024, including demographics testing. ^63a-3-11-13
- **63A-3.11-14** SHALL — CSPs SHALL make the results of their biometric algorithm performance and biometric system operational test results publicly available. The CSP MAY provide these test results in summary form if the results indicate performance against the defined metrics in these guidelines and across the tested demographic groups. ^63a-3-11-14
- **63A-3.11-15** SHALL — CSP SHALL collect biometric characteristics in a way that provides reasonable assurance that the biometric characteristic is collected from the applicant and not another subject. ^63a-3-11-15
- **63A-3.11-16** SHALL — When collecting and comparing biometric characteristics remotely, the CSP SHALL implement presentation attack detection (PAD) capabilities that meet the impostor attack presentation accept rate (IAPAR) performance metric of <0.07 to confirm the genuine presence of a live human being and to mitigate spoofing and impersonation attempts. All biometric presentation attack detection tests SHALL be conformant to ISO/IEC 30107-3:2023. ^63a-3-11-16
- **63A-3.11-17** SHALL — When collecting biometric characteristics on-site, the CSP SHALL have the operator view the biometric source (e.g., fingers, face) for the presence of unexpected non-natural materials and perform such inspections as part of the proofing process. ^63a-3-11-17

### 63A §3.12 Requirements for Visual Facial Image Comparison

- **63A-3.12-1** SHALL — Proofing agents and trusted referees SHALL be trained to conduct visual facial image comparison. This training SHALL include techniques and methods for identifying facial characteristics, unique traits, and other indicators of matches or non-matches between an applicant and their presented evidence. ^63a-3-12-1
- **63A-3.12-2** SHALL — Proofing agents and trusted referees SHALL be assessed on their ability to conduct visual facial image comparisons. Additionally, proofing agents and trusted referees SHALL be reassessed on an annual basis and remedially trained, if needed. Training SHALL be designed to reflect potential real-world attack scenarios, such as comparing applicants to images of relatives, twins, and individuals with a similar appearance. ^63a-3-12-2
- **63A-3.12-3** SHALL — CSPs SHALL provide proofing agents and trusted referees that conduct visual facial comparisons during remote attended transactions with resources that support accurate comparisons, such as high-quality image feeds, high-definition monitors, and image analysis software. ^63a-3-12-3
- **63A-3.12-4** SHALL — CSPs SHALL document their training and assessment procedures for visual image comparisons and make them available to RPs upon request. ^63a-3-12-4
- **63A-3.12-5** SHALL — These requirements SHALL apply for visual facial image comparisons done as manual reviews for failures of automated biometric comparisons (e.g., failure of 1:N checks conducted for resolution or deduplication). ^63a-3-12-5

### 63A §3.13 Requirements for the Validation of Physical Evidence

- **63A-3.13-1** SHALL — Automated evidence validation technology SHALL meet the following performance measures: Document false acceptance rate (DFAR) of 0.1 or less6 Document false rejection rate (DFRR) of 0.1 or less7 ^63a-3-13-1
- **63A-3.13-2** SHALL — If a Machine Readable Zone (MRZ) or barcode is present on the evidence, the optical capture and inspection SHALL compare the MRZ data to the printed data on the evidence for consistency. ^63a-3-13-2
- **63A-3.13-3** SHALL — CSPs SHALL implement live capture of documents during the validation process and SHALL implement passive or active document presence checks (also called document liveness). Live capture techniques confirm that the document is physically present and that the image captured during the identity proofing session is not a manipulated digital copy. For additional requirements to prevent the injection of modified media (i.e., digitally generated video or images of evidence), see Sec. 3.14. ^63a-3-13-3
- **63A-3.13-4** SHALL — CSPs SHALL assess the performance of employed optical capture and inspection technologies in conditions that are substantially similar to the operational environment and the types of evidence presented by the user base of the system. These tests SHALL account for all available identity evidence types that the CSPs allow to be validated using optical capture and inspection technology. If subscribers’ documents, personal information, or images are used as part of the testing, it SHALL be on a voluntary basis and with subscriber notification and consent. ^63a-3-13-4
- **63A-3.13-5** SHOULD — CSPs SHOULD have their evidence validation technology periodically tested by independent entities (e.g., accredited laboratories or research institutions) for their performance characteristics. ^63a-3-13-5
- **63A-3.13-6** SHALL — CSPs SHALL make the results of their testing publicly available. ^63a-3-13-6
- **63A-3.13-7** SHALL — Proofing agents and trusted referees SHALL be trained and provided with the resources to visually inspect all forms of evidence supported by the CSP. This training SHALL include: Authentic layouts and topography of evidence types Physical security features (e.g., raised letters, holographic features, microprinting) Techniques for assessing features (e.g., tools to be used, where tactile inspection is needed, manipulation required to view specific features) Common indications of tampering (e.g., damage to the lamination, image modification) ^63a-3-13-7
- **63A-3.13-8** SHALL — Proofing agents and trusted referees SHALL be assessed regarding their ability to visually inspect evidence based on their training. Additionally, proofing agents and trusted referees SHALL be reassessed on an annual basis or whenever significant new threats to the evidence validation process are identified and remedially trained as needed. ^63a-3-13-8
- **63A-3.13-9** SHALL — Proofing agents and trusted referees SHALL be provided with specialized tools and equipment to support the visual inspection of evidence (e.g., magnifiers, ultraviolet lights, barcode readers) as appropriate for the identity evidence type. ^63a-3-13-9
- **63A-3.13-10** SHALL — Proofing agents and trusted referees who conduct visual inspections via remote means SHALL be provided with devices and internet connections that support sufficiently high-quality imagery to be able to effectively inspect presented evidence. In these instances, the visual validation SHOULD be supported by automated document validation technologies that provide additional confidence in the authenticity of the evidence (e.g., submitting and validating evidence in advance of an attended remote session). ^63a-3-13-10
- **63A-3.13-11** SHALL — CSPs SHALL document their training and assessment procedures for visual inspections of evidence and make them available to RPs upon request. ^63a-3-13-11

### 63A §3.14 Digital Injection Prevention and Forged Media Detection

- **63A-3.14-1** SHALL — CSPs SHALL implement technical controls to increase confidence that digital media is being produced by a genuine sensor during the proofing process (e.g., detect the presence of a virtual camera, device emulator, or a jailbroken device). ^63a-3-14-1
- **63A-3.14-2** SHALL — CSPs SHALL analyze all digital media submitted during the identity proofing process for artifacts and indicators of potential modification, manipulation, tampering, or forgery. Automated image analysis algorithms SHALL be tested against available attack artifacts (i.e., forged and manipulated images and videos) and genuine media to provide a baseline of performance and to determine the expected rate of false positives and false negatives generated by the system. The kinds of available attack artifacts that were tested and the corresponding false negative rates SHALL be documented and made available to RPs upon request. Algorithmic analysis of media and automated decisioning SHOULD be augmented by manual reviews to address detection errors. ^63a-3-14-2
- **63A-3.14-3** SHALL — CSPs SHALL only use authenticated protected channels for the exchange of data during remote identity proofing processes. ^63a-3-14-3
- **63A-3.14-4** SHOULD — CSPs SHOULD introduce a passive means of detecting forged or manipulated media for all capture scenarios. ^63a-3-14-4
- **63A-3.14-5** SHOULD — CSPs SHOULD authenticate capture sensors or implement device attestation to increase the confidence in a device being used to transmit digital media as part of a remote identity proofing process. ^63a-3-14-5
- **63A-3.14-6** SHOULD — CSPs SHOULD analyze digital media for signatures of generative AI algorithms and deepfake tools that are known to be used to create forged digital media. ^63a-3-14-6
- **63A-3.14-7** SHALL — CSPs SHALL train proofing agents and trusted referees to look for indications of manipulated media (e.g., high latency, synchronization issues, inconsistent skin tone and resolution). ^63a-3-14-7
- **63A-3.14-8** SHALL — CSPs SHALL introduce random “human-in-the-loop” cues into their capture processes to increase the possibility of forged or manipulated media being detected (e.g., by requesting user movements or requesting that the user move objects between the capture sensor and their face). ^63a-3-14-8

### 63A §3.15 Exception and Error Handling

- **63A-3.15-1** SHALL — In order to increase the accessibility of their identity proofing services and address customer experience challenges, CSPs SHALL document their operational processes for dealing with errors and handling exceptions. These documented processes SHOULD include providing trusted referees to support applicants who are otherwise unable to meet the requirements of IALs 1 and 2. Additionally, CSPs SHOULD support the use of applicant references who can vouch for an applicant’s attributes, conditions, or identity. ^63a-3-15-1

### 63A §3.15.1 Requirements for Trusted Referees

- **63A-3.15.1-1** SHALL — The CSP SHALL notify the public of the availability of trusted referee services and how such services are obtained. ^63a-3-15-1-1
- **63A-3.15.1-2** SHALL — The CSP SHALL establish written policies and procedures for the use of trusted referees as part of its practice statement, as specified in Sec. 3.1. ^63a-3-15-1-2
- **63A-3.15.1-3** SHALL — The CSP SHALL train and certify its trusted referees to make risk-based decisions that allow applicants to be successfully identity-proofed based on their unique circumstances. At a minimum, such training SHALL include: Document identification and validation, such as common templates, security features, layouts, and topography (see Sec. 3.13) Indicators of fraudulent documents, such as damage, tampering, modification, fabrication, or forgery (see Sec. 3.13) Facial image comparisons to verify applicants against presented documents (see Sec. 3.12) Indicators of social engineering exhibited by an applicant, such as distress, confusion, or coercion An annual review of the trusted referee’s abilities to visually inspect evidence and make visual facial image comparisons (see Sec. 3.12) ^63a-3-15-1-3
- **63A-3.15.1-4** SHALL — The CSP SHALL establish a record of any identity proofing session that involves a trusted referee, including the reasons why a trusted referee was used (e.g., automated process failure, applicant request, established exception policy), the identity of the trusted referee, what evidence was presented, which processes were completed (e.g., validation or verification), and the trusted referee’s decision and, if negative, their rationale. ^63a-3-15-1-4
- **63A-3.15.1-5** SHALL — The CSP MAY offer trusted referee services for either on-site attended or remote attended sessions. These sessions SHALL be consistent with the requirements of these proofing types based on the IAL of the proofing event. ^63a-3-15-1-5

### 63A §3.15.2 Uses of Trusted Referees

- **63A-3.15.2-1** SHALL — CSPs SHALL document which types of exceptions and failures are eligible for the use of a trusted referee. ^63a-3-15-2-1
- **63A-3.15.2-2** SHOULD — CSPs SHOULD offer trusted referee services for failures of automated verification processes (e.g., biometric comparisons). ^63a-3-15-2-2
- **63A-3.15.2-3** SHALL — CSPs SHALL provide a policy for additional evidence types that may be used to corroborate core attributes or changes in core attributes. ^63a-3-15-2-3
- **63A-3.15.2-4** SHALL — Trusted referees SHALL review additional evidence types for authenticity to the greatest degree allowed by the evidence. ^63a-3-15-2-4
- **63A-3.15.2-5** MAY — If no authoritative or credible records are available to support validation, the trusted referee MAY compare the attributes on additional pieces of evidence with the strongest piece of evidence available to corroborate the consistency of core attributes. ^63a-3-15-2-5
- **63A-3.15.2-6** SHALL — If there is a partial mismatch of core attributes to authoritative records, the trusted referee SHALL review evidence that supports the legitimacy of the asserted attribute value (e.g., recent move or change of name). ^63a-3-15-2-6

### 63A §3.15.3 Requirements for Applicant References

- **63A-3.15.3-1** SHALL — The CSP SHALL notify the public of the allowability of applicant references and any requirements for the relationship between the reference and an applicant. ^63a-3-15-3-1
- **63A-3.15.3-2** SHALL — The CSP SHALL establish written policies and procedures for the use of applicant references as part of its practice statement, as specified in Sec. 3.1. ^63a-3-15-3-2
- **63A-3.15.3-3** SHALL — The CSP SHALL identity-proof an applicant reference to the same or higher IAL intended for the applicant. The CSP SHALL include the information collected, recorded, and retained for identity proofing the applicant references in its privacy risk assessment, as required in section Sec. 3.3.1. ^63a-3-15-3-3
- **63A-3.15.3-4** SHALL — The CSP SHALL record the use of an applicant reference in the subscriber account and maintain a record of the applicant reference and their relationship to the applicant. ^63a-3-15-3-4
- **63A-3.15.3-5** SHALL — The RP SHALL conduct a risk assessment to determine the applicability, business requirements, and potential risks associated with excluding or including applicant references for proofing events. ^63a-3-15-3-5

### 63A §3.15.4 Uses of Applicant References

- **63A-3.15.4-1** SHALL — Applicant references can take several different actions to support an applicant in the identity proofing process, depending on the circumstances and context of the CSP and RP services. CSPs SHOULD offer the use of applicant references if the risks to the online service of doing so allow for it. If CSPs allow the use of applicant references, the CSPs and the RPs that use their services SHALL document all acceptable uses for applicant references in their contracts or trust agreements. ^63a-3-15-4-1
- **63A-3.15.4-2** MAY — The applicant reference MAY vouch for one or more claimed core attributes relative to the applicant as part of the evidence and attribute validation process. ^63a-3-15-4-2
- **63A-3.15.4-3** MAY — The applicant reference MAY vouch for the identity of the applicant in the absence of sufficient identity evidence. ^63a-3-15-4-3
- **63A-3.15.4-4** MAY — The applicant reference MAY vouch for a specific condition or status of an applicant relative to the identity proofing process (e.g., homelessness, disaster scenarios). ^63a-3-15-4-4
- **63A-3.15.4-5** SHALL — In all instances, the CSP SHALL establish a record of the role that the applicant reference played in the process and document these actions sufficient to support any applicable legal and regulatory requirements. This MAY include: ^63a-3-15-4-5
- **63A-3.15.4-6** SHALL — CSPs SHALL make available to the applicant reference clear and understandable information relative to the legal and liability impacts that may result from their participation as an applicant reference. ^63a-3-15-4-6

### 63A §3.15.5 Establishing Applicant Reference Relationships

- **63A-3.15.5-1** SHALL — In many cases, there will be business, legal, or fraud prevention reasons to confirm the relationship between the applicant and an applicant reference. If such steps are deemed necessary by a risk assessment, the following requirements SHALL apply: ^63a-3-15-5-1
- **63A-3.15.5-2** SHALL — The CSP and RP SHALL establish requirements for applicant reference relationship confirmation processes and document them in any contracts or trust agreements. ^63a-3-15-5-2
- **63A-3.15.5-3** SHALL — The CSP SHALL make a list of acceptable evidence of relationship available to the applicant reference prior to initiating the relationship confirmation process. ^63a-3-15-5-3
- **63A-3.15.5-4** SHALL — The CSP SHALL request evidence of the applicant’s relationship (e.g., notarized power of attorney, a professional certification). ^63a-3-15-5-4
- **63A-3.15.5-5** SHALL — Upon successfully identity proofing an applicant, the CSP SHALL record the evidence used to confirm the applicant reference’s relationship to the applicant in the subscriber account. ^63a-3-15-5-5

### 63A §3.15.6 Requirements for Interacting With Minors

- **63A-3.15.6-1** SHALL — The CSP SHALL establish a written policy and procedures as part of its practice statement for identity proofing minors who may not be able to meet the evidence requirements for a given IAL. ^63a-3-15-6-1
- **63A-3.15.6-2** SHALL — When interacting with persons under the age of 13, the CSP SHALL ensure compliance with the Children’s Online Privacy Protection Act of 1998 [COPPA] or other laws and regulations that deal with the protection of minors, as applicable. ^63a-3-15-6-2
- **63A-3.15.6-3** SHALL — CSPs SHALL support the use of applicant references when interacting with individuals under the age of 18. ^63a-3-15-6-3

### 63A §3.16 Elevating Subscriber IALs

- **63A-3.16-1** SHOULD — CSPs SHOULD allow subscribers to elevate IALs related to their subscriber accounts to support higher assurance transactions with RPs. For CSPs that support these functions, the following requirements apply: ^63a-3-16-1
- **63A-3.16-2** SHALL — CSPs SHALL document their approved approaches for elevating assurance levels in their practice statements. ^63a-3-16-2
- **63A-3.16-3** SHALL — CSPs SHALL require subscribers to authenticate at the highest authentication assurance level (AAL) available on their account prior to initiating the upgrade process. ^63a-3-16-3
- **63A-3.16-4** SHALL — CSPs SHALL collect, validate, and verify additional evidence, as mandated to achieve the higher IAL. ^63a-3-16-4
- **63A-3.16-5** SHOULD — CSPs SHOULD avoid collecting, validating, and verifying previously processed evidence, though they MAY do so based on an extended period of account inactivity, indicators of fraud, or if evidence has become invalidated since the original proofing event. ^63a-3-16-5

### 63A §4.1.1 Proofing Types

- **63A-4.1.1-1** MAY — IAL1 identity proofing MAY be delivered through any proofing type, as described in Sec. 2.1.3. ^63a-4-1-1-1
- **63A-4.1.1-2** SHALL — CSPs MAY combine proofing types and their stated requirements to create hybrid processes. For example, a CSP might leverage remote unattended identity proofing validation processes in advance of a remote attended session where the verification will take place. If such steps are combined, CSPs SHALL document their hybrid process and state how the applicable requirements for each of the employed proofing types are met. ^63a-4-1-1-2

### 63A §4.1.2 Evidence Collection

- **63A-4.1.2-1** SHALL — For identity proofing at IAL1, the CSP SHALL collect: ^63a-4-1-2-1

### 63A §4.1.3 Attribute Collection

- **63A-4.1.3-1** SHALL — The CSP SHALL collect all core attributes, including at least one government identifier. Validated evidence is the preferred source of identity attributes. If the presented identity evidence does not provide all of the attributes that the CSP considers to be core attributes, it MAY collect attributes that are self-asserted by the applicant. ^63a-4-1-3-1

### 63A §4.1.4 Evidence Validation

- **63A-4.1.4-1** SHALL — Each piece of evidence presented SHALL be validated using one of the following methods: ^63a-4-1-4-1

### 63A §4.1.5 Attribute Validation

- **63A-4.1.5-1** SHALL — The CSP SHALL validate all core attributes and the government identifier against an authoritative or credible source to determine accuracy. ^63a-4-1-5-1
- **63A-4.1.5-2** SHOULD — CSPs SHOULD evaluate attributes obtained from different sources (e.g., presented evidence, self-asserted, authoritative or credible sources) for consistency. ^63a-4-1-5-2
- **63A-4.1.5-3** SHOULD — CSPs SHOULD validate any reference numbers on the presented identity evidence, if available. ^63a-4-1-5-3

### 63A §4.1.6 Verification Requirements

- **63A-4.1.6-1** SHALL — The CSP SHALL verify the applicant’s ownership of one piece of evidence using one of the following methods: ^63a-4-1-6-1
- **63A-4.1.6-2** SHALL — Visually comparing the applicant’s facial image to a facial portrait on evidence or in records associated with the evidence during an on-site attended session (i.e., in-person with a proofing agent), a remote attended session (i.e., live video with a proofing agent), or an asynchronous process (i.e., visual comparison made by a proofing agent at a different time). If the comparison is performed asynchronously at a later time, the CSP SHALL implement PAD and passive or active document presence checks to increase confidence that both the live applicant and physical documents are present during the submission or capture event. ^63a-4-1-6-2

### 63A §4.1.8 Remote Attended Requirements

- **63A-4.1.8-1** SHALL — During the video session, the applicant SHALL remain in view of the proofing agent during each step of the proofing process. ^63a-4-1-8-1
- **63A-4.1.8-2** SHALL — The video quality SHALL be sufficient to support the necessary steps in the validation and verification processes, such as inspecting evidence and comparing the applicant to the evidence. ^63a-4-1-8-2
- **63A-4.1.8-3** SHALL — The proofing agent SHALL be trained to identify signs of manipulation, coercion, or social engineering occurring during the session. ^63a-4-1-8-3
- **63A-4.1.8-4** SHALL — The CSP SHALL notify the applicant of the recording prior to initiating a recorded session. ^63a-4-1-8-4
- **63A-4.1.8-5** SHALL — The CSP SHALL gain consent from the applicant prior to initiating a recorded session. ^63a-4-1-8-5
- **63A-4.1.8-6** SHALL — The CSP SHALL publish their retention schedule and deletion processes for all video records. ^63a-4-1-8-6
- **63A-4.1.8-7** SHALL — The CSP SHALL implement injection protection and modified media controls, as defined in Sec. 3.14. ^63a-4-1-8-7
- **63A-4.1.8-8** SHALL — The CSP SHALL provide proofing agents with a method or mechanism to flag events for potential fraud. ^63a-4-1-8-8

### 63A §4.1.9 On-Site Attended Requirements

- **63A-4.1.9-1** SHALL — The CSP SHALL provide a physical setting in which on-site identity proofing sessions are conducted. ^63a-4-1-9-1
- **63A-4.1.9-2** SHALL — All devices SHALL be protected by appropriate baseline security features comparable to FISMA moderate controls, including malware protection, administrator-specific access controls, and software update processes. ^63a-4-1-9-2
- **63A-4.1.9-3** SHALL — CSP proofing agents SHALL be trained to identify signs of manipulation, coercion, or social engineering occurring during the on-site session. ^63a-4-1-9-3
- **63A-4.1.9-4** SHALL — The CSP SHALL provide proofing agents with a method or mechanism to covertly flag events for potential fraud. ^63a-4-1-9-4

### 63A §4.1.10 On-Site Unattended Requirements

- **63A-4.1.10-1** SHALL — All devices SHALL be safeguarded from tampering through observation by CSP representatives and/or physical and digital tamper prevention features. ^63a-4-1-10-1
- **63A-4.1.10-2** SHALL — All devices SHALL be inspected periodically by trained technicians to deter tampering, modification, or damage. ^63a-4-1-10-2

### 63A §4.1.11 Notification of Proofing

- **63A-4.1.11-1** SHALL — Upon the successful completion of identity proofing at IAL1, the CSP SHALL send a notification of proofing to a validated address for the applicant, as specified in Sec. 3.10. ^63a-4-1-11-1

### 63A §4.1.12 Initial Authenticator Binding

- **63A-4.1.12-1** SHOULD — Once a unique subscriber account is established for the applicant (now subscriber) in the CSP’s identity system, one or more authenticators can be associated (i.e., bound) to the subscriber’s account. To minimize the need for account recovery, CSPs SHOULD encourage subscribers to bind at least two separate means of authentication. See Sec. 5 for more information about subscriber accounts and Sec. 4.1.2.1 of [SP800-63B] for more information on binding authenticators. ^63a-4-1-12-1
- **63A-4.1.12-2** SHALL — The CSP SHALL provide the ability for the applicant to bind an authenticator using one of the following methods: Remote enrollment of a subscriber-provided authenticator consistent with the requirements for the authenticator type, as defined in Sec. 4.1.3 of [SP800-63B] Distribution of a physical authenticator to a validated address Distribution or on-site enrollment of an authenticator ^63a-4-1-12-2
- **63A-4.1.12-3** SHALL — If authenticators are bound outside of a single protected session with the user, the CSP SHALL confirm the presence of the intended subscriber through one of the following methods: Return of a continuation code Comparison against a biometric collected at the time of proofing ^63a-4-1-12-3

### 63A §4.2.1 Proofing Types

- **63A-4.2.1-1** MAY — IAL2 identity proofing MAY be delivered through any identity proofing type, as described in Sec. 2.1.3. ^63a-4-2-1-1
- **63A-4.2.1-2** SHALL — CSPs MAY combine identity proofing types and their stated requirements to create hybrid processes. For example, a CSP might leverage remote unattended identity proofing validation processes in advance of a remote attended session where the verification will take place. If such steps are combined, CSPs SHALL document their hybrid process and state how the applicable requirements for each of the employed proofing types are met. ^63a-4-2-1-2

### 63A §4.2.2 Evidence Collection

- **63A-4.2.2-1** SHALL — For identity proofing at IAL2, the CSP SHALL collect: ^63a-4-2-2-1

### 63A §4.2.4 Evidence Validation

- **63A-4.2.4-1** SHALL — Each piece of FAIR or STRONG evidence that is presented SHALL be validated using one of the following techniques: Confirming the authenticity of the digital evidence by interrogating the digital security features (e.g., signatures on assertions or data) Confirming the authenticity of the physical evidence using automated scanning technology that can detect physical security features Confirming the integrity of any physical security features through a visual inspection by a proofing agent using a real-time or asynchronous process (e.g., offline manual review) Confirming the integrity of any physical security features through physical and tactile inspection by a proofing agent at an on-site location ^63a-4-2-4-1
- **63A-4.2.4-2** SHALL — Each piece of SUPERIOR evidence SHALL be validated through the cryptographic verification of the evidence contents and the issuing source, including digital signature verification and the validation of any trust chain back to a trust anchor. Any piece of SUPERIOR evidence that cannot be validated using this method MAY be considered STRONG evidence if it can be validated by using one of the techniques provided above. ^63a-4-2-4-2

### 63A §4.2.5 Attribute Validation

- **63A-4.2.5-1** SHALL — The CSP SHALL validate all core attributes by either: Comparing the government identifier and other core attributes against an authoritative or credible source to determine accuracy Validating the accuracy of digitally signed attributes that are contained on SUPERIOR evidence through the public key of the issuing source ^63a-4-2-5-1

### 63A §4.2.6 Verification Requirements

- **63A-4.2.6-1** SHOULD — Verification pathways SHOULD be implemented consistent with relevant policy and be responsive to the use cases, populations, and threat environment of the online service being protected. CSPs SHOULD deploy more than one pathway to IAL2 verification and MAY combine pathways in order to achieve desired outcomes. ^63a-4-2-6-1
- **63A-4.2.6-2** SHALL — CSPs that offer multiple verification pathways SHALL record in the subscriber record which pathways were followed to achieve IAL2 and SHALL make that information available to RPs in the assertion, API, or as part of their trust agreement. When the Non-Biometric Pathway is used, the CSP SHALL additionally record whether a mailed confirmation code or a visual comparison of the applicant against evidence was used for verification. ^63a-4-2-6-2

### 63A §4.2.6.1 IAL2 Verification — Non-Biometric Pathway

- **63A-4.2.6.1-1** SHALL — The IAL2 Non-Biometric Pathway provides verification methods that do not use an automated comparison of biometric samples provided by the applicant. This pathway can still involve the collection and verification of biometric data (e.g., visual comparison to a facial image contained on identity evidence performed by a proofing agent), but such comparisons are done through manual rather than automated means. Additional verification methods that do not require the use of automated biometric comparison are also included in the Digital Evidence Pathway requirements specified in Sec. 4.2.6.2. If provided as an option at IAL2, CSPs SHALL communicate their use of the Non-Biometric Pathway to all RPs that use their identity service. ^63a-4-2-6-1-1
- **63A-4.2.6.1-2** SHALL — For remote attended, remote unattended, and on-site unattended identity proofing, the CSP SHALL verify the applicant’s ownership of all pieces of presented identity evidence. For on-site attended identity proofing, the CSP SHALL verify the applicant’s ownership of the strongest piece of presented identity evidence. ^63a-4-2-6-1-2
- **63A-4.2.6.1-3** SHALL — Visually comparing the applicant’s facial image to a facial portrait on the presented evidence or in records associated with the evidence during an on-site attended session (i.e., in-person with a proofing agent), a remote attended session (i.e., live video with a proofing agent), or an asynchronous process (i.e., visual comparison made by a proofing agent at a different time). If the comparison is performed asynchronously at a later time, the CSP SHALL implement PAD and passive or active document presence checks to increase confidence that both the live applicant and physical documents are present during the captured identity proofing event. ^63a-4-2-6-1-3

### 63A §4.2.8 Remote Attended Requirements

- **63A-4.2.8-1** SHALL — The video quality SHALL be sufficient to support the necessary steps in the validation and verification processes, such as inspecting evidence and comparing the user to the evidence. ^63a-4-2-8-1
- **63A-4.2.8-2** SHALL — The proofing agent SHALL be trained to identify signs of manipulation, coercion, or social engineering occurring during the recorded session. ^63a-4-2-8-2

### 63A §4.2.9 On-Site Attended Requirements

- **63A-4.2.9-1** SHALL — The CSP SHALL provide proofing agents with a method or mechanism to safely flag events for potential fraud. ^63a-4-2-9-1

### 63A §4.2.11 Notification of Proofing

- **63A-4.2.11-1** SHALL — Upon the successful completion of identity proofing at IAL2, the CSP SHALL send a notification of proofing to a validated address for the applicant, as specified in Sec. 3.10. CSPs SHOULD send the notification of proofing to the applicant’s postal address. ^63a-4-2-11-1

### 63A §4.3.1 Proofing Types

- **63A-4.3.1-1** SHALL — IAL3 identity proofing SHALL only be delivered as on-site attended. The proofing agent MAY be co-located with the applicant or attend the identity proofing session via a CSP-controlled kiosk or device. ^63a-4-3-1-1

### 63A §4.3.2 Evidence Collection

- **63A-4.3.2-1** SHALL — For identity proofing at IAL3, the CSP SHALL collect: ^63a-4-3-2-1

### 63A §4.3.3 Attribute Requirements

- **63A-4.3.3-1** SHALL — The CSP SHALL collect all core attributes, including at least one government identifier. Validated evidence is the preferred source of identity attributes. If the presented identity evidence does not provide all of the attributes that a CSP considers to be core attributes, the CSP MAY collect attributes that are self-asserted by the applicant. ^63a-4-3-3-1
- **63A-4.3.3-2** SHALL — The CSP SHALL collect and retain a biometric sample from the applicant during the identity proofing process to support account recovery and non-repudiation and to establish a high level of confidence that the same participant is present in the proofing and issuance processes, if done separately. CSPs MAY choose to periodically re-enroll user biometrics based on the modalities they use and the likelihood that subscriber accounts will persist long enough to warrant such a refresh. ^63a-4-3-3-2

### 63A §4.3.5 Attribute Validation

- **63A-4.3.5-1** SHALL — The CSP SHALL validate all core attributes by either: Comparing the government identifier and other core attributes against an authoritative or credible source to determine accuracy or Validating the accuracy of digitally signed attributes that are contained on SUPERIOR evidence through the public key of the issuing source ^63a-4-3-5-1

### 63A §4.3.6 Verification Requirements

- **63A-4.3.6-1** SHALL — The CSP SHALL verify the applicant’s ownership of the strongest piece of evidence (STRONG or SUPERIOR) by one of the following methods: Confirming the applicant’s ability to successfully authenticate to a physical device or application (e.g., a mobile driver’s license) and comparing a digitally protected and transmitted facial portrait to the applicant Comparing the applicant’s facial image to the facial portrait on the presented evidence via an automated comparison Visually comparing the applicant’s facial image to the facial portrait on the presented evidence during an on-site attended session or a remote attended session Performing an automated comparison of a stored biometric on the identity evidence or in the authoritative records associated with the evidence to a sample provided by the applicant ^63a-4-3-6-1

### 63A §4.3.7 On-Site Attended Requirements — Colocated Agent

- **63A-4.3.7-1** SHALL — The CSP SHALL provide a secure, physical setting in which on-site identity proofing sessions are conducted. ^63a-4-3-7-1
- **63A-4.3.7-2** SHALL — The CSP SHALL provide sensors and capture devices for the collection of biometrics from the applicant. ^63a-4-3-7-2
- **63A-4.3.7-3** SHALL — The CSP SHALL have the proofing agent view the source of the collected biometric for the presence of any non-natural materials (e.g., putty, glue). ^63a-4-3-7-3
- **63A-4.3.7-4** SHALL — The CSP SHALL have the proofing agent collect the biometric samples in such a way that ensures the sample was collected from the applicant and no other source. ^63a-4-3-7-4
- **63A-4.3.7-5** SHALL — The CSP SHALL ensure that all information systems and technology leveraged by proofing agents and trusted referees are protected consistent with at least FISMA moderate or comparable levels of controls, including physical controls for the proofing facility. ^63a-4-3-7-5
- **63A-4.3.7-6** SHALL — The CSP SHALL provide proofing agents with a method or mechanism to discretely flag events or actions as potential fraud. ^63a-4-3-7-6

### 63A §4.3.8 On-Site Attended Requirements — Kiosk-Based

- **63A-4.3.8-1** MAY — The CSP MAY offer a remote means of interacting with a proofing agent whereby the agent and the applicant are not co-located (i.e., in the same room). For example, applicants might interact with a CSP-controlled kiosk with the proofing agent participating remotely in the session over video. In such cases, the following requirements apply in addition to those provided for the on-site attended identity proofing in Sec. 4.3.7. In previous versions of this document, this approach was referred to as Supervised Remote Identity Proofing (SRIP). ^63a-4-3-8-1
- **63A-4.3.8-2** SHALL — The CSP SHALL monitor the entire identity proofing session through a high-resolution video transmission with the applicant. ^63a-4-3-8-2
- **63A-4.3.8-3** SHALL — The CSP SHALL have a live proofing agent participate remotely with the applicant for the evidence collection, evidence validation, and verification steps of the identity proofing process. Data entry of attributes for resolution and enrollment MAY be done without the presence of a live proofing agent. ^63a-4-3-8-3
- **63A-4.3.8-4** SHALL — The CSP SHALL require all actions taken by the applicant during the evidence collection, evidence validation, and verification steps to be clearly visible to the remote proofing agent. ^63a-4-3-8-4
- **63A-4.3.8-5** SHALL — The CSP SHALL require that all digital validation and verification of evidence (e.g., via chip or wireless technologies) be performed by integrated scanners and sensors (e.g., embedded fingerprint reader). ^63a-4-3-8-5
- **63A-4.3.8-6** SHALL — All devices used to support interaction between the proofing agent and the applicant SHALL be protected by appropriate baseline security features that are comparable to at least FISMA moderate controls, including malware protection, administrator-specific access controls, and software update processes. ^63a-4-3-8-6
- **63A-4.3.8-7** SHALL — All devices used to support interaction between the proofing agent and the applicant SHALL be inspected periodically by trained technicians to deter tampering, modification, or damage. ^63a-4-3-8-7

### 63A §4.3.9 Notification of Proofing

- **63A-4.3.9-1** SHALL — Upon the successful completion of identity proofing at IAL3, the CSP SHALL send a notification of proofing to a validated address for the applicant, as specified in Sec. 3.10. CSPs SHOULD send the notification of proofing to the applicant’s postal address. ^63a-4-3-9-1

### 63A §4.3.10 Initial Authenticator Binding

- **63A-4.3.10-1** SHALL — The CSP SHALL distribute or enroll the subscriber’s initial authenticator during an on-site attended interaction with a proofing agent. ^63a-4-3-10-1
- **63A-4.3.10-2** SHALL — If the CSP distributes or enrolls the initial authenticator outside of a single authenticated protected session with the subscriber, the CSP SHALL compare a biometric sample collected from the subscriber to the one collected at the time of proofing prior to registration of the authenticator and MAY request that the subscriber bring the identity evidence used during the proofing process to further strengthen the process of binding the authenticator to the subscriber. ^63a-4-3-10-2

### 63A §5.1 Subscriber Accounts

- **63A-5.1-1** SHALL — The CSP SHALL establish and maintain a unique subscriber account for each active subscriber in its identity system from the time of enrollment to the time of account closure. The CSP establishes a subscriber account to record each subscriber as a unique identity within its identity service and to maintain a record of all authenticators associated with that account. ^63a-5-1-1
- **63A-5.1-2** SHALL — The CSP SHALL assign a unique identifier to each subscriber account. The identifier SHOULD be randomly generated by the CSP’s system and of sufficient length and entropy to ensure uniqueness within its user population and to support federation with RPs, where applicable. The identifier MAY be used as a subject identifier in the generation of assertions, consistent with [SP800-63C]. ^63a-5-1-2
- **63A-5.1-3** SHALL — At a minimum, the CSP SHALL include the following information in each subscriber account: ^63a-5-1-3

### 63A §5.2 Subscriber Account Access

- **63A-5.2-1** SHALL — The CSP SHALL provide the capability for subscribers to authenticate and access information in their subscriber account. ^63a-5-2-1
- **63A-5.2-2** SHALL — For subscriber accounts that contain personal information, this capability SHALL be accomplished through AAL2 or AAL3 authentication processes using authenticators that are registered to the subscriber account. ^63a-5-2-2

### 63A §5.3 Subscriber Account Maintenance and Updates

- **63A-5.3-1** SHALL — The CSP SHALL provide the capability for a subscriber to request that information be updated in their subscriber account. The CSP MAY provide a mechanism for subscribers to directly update non-core attributes. ^63a-5-3-1
- **63A-5.3-2** SHALL — With the exception of physical addresses, the CSP SHALL validate any changes to core attribute information maintained in the subscriber account. The CSP SHOULD validate a change to the subscriber’s physical address if it is considered a core attribute by the CSP. ^63a-5-3-2
- **63A-5.3-3** SHALL — The CSP SHALL notify the subscriber of any updates made to information in the subscriber account. ^63a-5-3-3
- **63A-5.3-4** SHALL — The CSP SHALL provide the capability for the subscriber to report any unauthorized access or potential compromise to information in their subscriber account. ^63a-5-3-4

### 63A §5.4 Subscriber Account Suspension or Termination

- **63A-5.4-1** SHALL — The CSP SHALL promptly suspend or terminate the subscriber account when one of the following occurs: ^63a-5-4-1
- **63A-5.4-2** SHALL — The CSP SHALL notify the subscriber if their account has been suspended or terminated. Such notices SHALL include information about why the account was suspended or terminated, reactivation or renewal options, and any options for redress if the subscriber thinks the account was suspended or terminated in error. ^63a-5-4-2
- **63A-5.4-3** SHALL — The CSP SHALL delete all personal information from the subscriber account records following account termination in accordance with the record retention and disposal requirements, as documented in its practices statement (see Sec. 3.1). ^63a-5-4-3

### 63A §5.5 Data Breach Notification

- **63A-5.5-1** SHALL — In the event of a data breach of CSP records, the CSP SHALL provide notification to subscribers whose personal information may have been exposed to unauthorized access. Such notification SHALL include information about the breach and actions for subscribers to take to recover or maintain access to their accounts and to protect against any unauthorized disclosure of their personal information. The CSP SHALL send such notifications as expeditiously as possible to the subscribers’ validated address. ^63a-5-5-1

### 63A §5.6 Multiple Subscriber Account Scenarios

- **63A-5.6-1** SHOULD — Some CSPs need to support a single user’s ability to interact with the CSP while fulfilling different roles or personas. For example, a subscriber may interact as themselves and also as a representative of a business across different services supported by the CSP. Another scenario is a CSP that serves both commercial and federal RPs and must maintain a separation between its services. To limit fraud and avoid redundant costs and processes, CSPs SHOULD provide users with a means to manage multiple user personas without having to create multiple subscriber accounts. If this is not possible, and multiple subscriber accounts are supported for a single subscriber, the CSP SHOULD implement its subscriber accounts in a manner that avoids unnecessary re-proofing of the same subscriber (e.g., linking accounts via a common identifier or through biometric or attribute resolution). ^63a-5-6-1
- **63A-5.6-2** SHALL — The CSP SHALL develop and document their process for reviewing and assessing subscribers with multiple accounts to identify possible fraud. ^63a-5-6-2
- **63A-5.6-3** SHALL — The CSP SHALL maintain a mapping of all accounts associated with a unique government identifier or common core attributes. ^63a-5-6-3
- **63A-5.6-4** SHALL — The CSP SHALL provide individuals with visibility into the full list of subscriber accounts associated with their identity. ^63a-5-6-4
- **63A-5.6-5** SHOULD — The CSP SHOULD allow subscribers to block the creation of additional accounts using their personal information. ^63a-5-6-5

## SP 800-63B-4 Authentication and Authenticator Management

### 63B §1.1 Notations

- **63B-1.1-1** SHALL NOT — The terms “SHALL” and “SHALL NOT” indicate requirements to be followed strictly in order to conform to the publication and from which no deviation is permitted. ^63b-1-1-1
- **63B-1.1-2** SHOULD NOT — The terms “SHOULD” and “SHOULD NOT” indicate that among several possibilities, one is recommended as particularly suitable without mentioning or excluding others, that a certain course of action is preferred but not necessarily required, or that (in the negative form) a certain possibility or course of action is discouraged but not prohibited. ^63b-1-1-2
- **63B-1.1-3** MAY — The terms “MAY” and “NEED NOT” indicate a course of action permissible within the limits of the publication. ^63b-1-1-3

### 63B §2 Authentication Assurance Levels

- **63B-2-1** SHALL — To satisfy the requirements of a given AAL and be recognized as a subscriber, a claimant SHALL authenticate to an RP (or IdP, as described in [SP800-63C]) with a process whose strength is equal to or greater than the requirements at that level. The authentication process results in an identifier that uniquely identifies the subscriber each time they authenticate to that RP. The identifier MAY be pseudonymous. Other attributes that identify the subscriber as a unique subject MAY also be provided. Detailed normative requirements for authenticators and verifiers at each AAL are provided in Sec. 3. See [SP800-63] Sec. 3 for details on how to choose the most appropriate AAL. ^63b-2-1
- **63B-2-2** SHALL — Personal information collected during and after identity proofing (see [SP800-63A]) MAY be made available to the subscriber by the digital identity service through the subscriber account. The release or online availability of any personal information by federal agencies requires multi-factor authentication in accordance with [EO13681]. Therefore, federal agencies SHALL select a minimum of AAL2 when personal information is made available online. ^63b-2-2
- **63B-2-3** SHALL — At all AALs, indicators of potential fraud, including applicable indicators described in Sec. 5.3, MAY be used to lower the risk of misauthentication. For example, authentication from an unexpected geolocation or IP address block (e.g., a cloud service) might prompt the use of additional risk-based controls. CSPs or verifiers SHALL assess their use of indicators of potential fraud for efficacy and to identify and mitigate potential negative impacts on their user populations. CSPs or verifiers SHALL include fraud indicators in the authentication privacy risk assessment. The use of potential fraud indicators prior to or during the authentication process does not impact or change the AAL of a transaction or substitute for an authentication factor. ^63b-2-3

### 63B §2.1 Authentication Assurance Level 1

- **63B-2.1-1** SHOULD — AAL1 provides basic confidence that the claimant controls an authenticator that is bound to the subscriber account. AAL1 requires either single-factor or multi-factor authentication using a wide range of available authentication technologies. Verifiers SHOULD make multi-factor authentication options available at AAL1 and encourage their use. Successful authentication requires that the claimant prove possession and control of the authenticator through a secure authentication protocol. ^63b-2-1-1

### 63B §2.1.1 Permitted Authenticator Types

- **63B-2.1.1-1** SHALL — AAL1 authentication SHALL use any of the following authentication types, which are further defined in Sec. 3: ^63b-2-1-1-1

### 63B §2.1.2 Authenticator and Verifier Requirements

- **63B-2.1.2-1** SHALL — Authenticators used at AAL1 SHALL use approved cryptography. In other words, they must use approved algorithms, but the implementation need not be validated under [FIPS140]. ^63b-2-1-2-1
- **63B-2.1.2-2** SHALL — Communication between the claimant and verifier SHALL occur via one or more authenticated protected channels. ^63b-2-1-2-2
- **63B-2.1.2-3** SHALL — Cryptography used by verifiers operated by or on behalf of federal agencies at AAL1 SHALL be validated to meet the requirements of [FIPS140] Level 1. ^63b-2-1-2-3

### 63B §2.1.3 Reauthentication

- **63B-2.1.3-1** SHALL — Periodic reauthentication of subscriber sessions SHALL be performed, as described in Sec. 5.2. A definite reauthentication overall timeout SHALL be established, which SHOULD be no more than 30 days at AAL1. An inactivity timeout MAY be applied but is not required at AAL1. ^63b-2-1-3-1

### 63B §2.2.1 Permitted Authenticator Types

- **63B-2.2.1-1** SHALL — At AAL2, authentication SHALL use either a multi-factor authenticator or a combination of two separate authentication factors. A multi-factor authenticator requires two factors to execute a single authentication event, such as a cryptographically secure device with an integrated biometric sensor that is required to activate the device. Authenticator requirements are specified in Sec. 3. ^63b-2-2-1-1
- **63B-2.2.1-2** MAY — When a multi-factor authenticator is used, any of the following MAY be used: ^63b-2-2-1-2
- **63B-2.2.1-3** SHALL — When a combination of two single-factor authenticators is used, the combination SHALL include one physical authenticator (i.e., “something you have”) from the following list in conjunction with either a password (Sec. 3.1.1) or a biometric comparison: ^63b-2-2-1-3

### 63B §2.2.2 Authenticator and Verifier Requirements

- **63B-2.2.2-1** SHALL — Authenticators used at AAL2 SHALL use approved cryptography. Cryptographic authenticators procured by federal agencies SHALL be validated to meet the requirements of [FIPS140] Level 1. At least one authenticator used at AAL2 SHALL be replay-resistant, as described in Sec. 3.2.7. Authentication at AAL2 SHOULD demonstrate authentication intent from at least one authenticator, as discussed in Sec. 3.2.8. ^63b-2-2-2-1
- **63B-2.2.2-2** SHALL — Cryptography used by verifiers operated by or on behalf of federal agencies at AAL2 SHALL be validated to meet the requirements of [FIPS140] Level 1 unless otherwise specified. ^63b-2-2-2-2
- **63B-2.2.2-3** SHALL — Verifiers SHALL offer at least one phishing-resistant authentication option at AAL2, as described in Sec. 3.2.5. Federal agencies SHALL require their staff, contractors, and partners to use phishing-resistant authentication to access federal information systems. In all cases, verifiers SHOULD encourage the use of phishing-resistant authentication at AAL2 whenever practical since phishing is a significant threat vector [IC3]. ^63b-2-2-2-3

### 63B §2.2.3 Reauthentication

- **63B-2.2.3-1** SHALL — Periodic reauthentication of subscriber sessions SHALL be performed, as described in Sec. 5.2. A definite reauthentication overall timeout SHALL be established, which SHOULD be no more than 24 hours at AAL2. The inactivity timeout SHOULD be no more than 1 hour. When the inactivity timeout has occurred but the overall timeout has not yet occurred, the verifier MAY allow the subscriber to reauthenticate using only a successful password or biometric comparison in conjunction with the session secret, as described in Sec. 5.1. ^63b-2-2-3-1

### 63B §2.3.1 Permitted Authenticator Types

- **63B-2.3.1-1** SHALL — AAL3 authentication SHALL require one of the following authenticator combinations: ^63b-2-3-1-1

### 63B §2.3.2 Authenticator and Verifier Requirements

- **63B-2.3.2-1** SHALL NOT — Single-factor and multi-factor authenticators used at AAL3 SHALL be validated to meet the requirements of [FIPS140] Level 1 or higher overall. As described in Sec. 3.2.12, cryptographic authenticators used at AAL3 are required to provide a hardware-protected, isolated environment to prevent authentication keys from being leaked or extracted. Since syncable authenticators (described in Appendix B) require the private key to be exportable, syncable authenticators SHALL NOT be used at AAL3. ^63b-2-3-2-1
- **63B-2.3.2-2** SHALL — Cryptography used by verifiers at AAL3 SHALL be validated at [FIPS140] Level 1 or higher. ^63b-2-3-2-2
- **63B-2.3.2-3** SHOULD — Hardware-based authenticators and verifiers at AAL3 SHOULD resist relevant side-channel (e.g., timing and power-consumption analysis) attacks. ^63b-2-3-2-3

### 63B §2.3.3 Reauthentication

- **63B-2.3.3-1** SHALL — Periodic reauthentication of subscriber sessions SHALL be performed, as described in Sec. 5.2. At AAL3, the overall timeout for reauthentication SHALL be no more than 12 hours. The inactivity timeout SHOULD be no more than 15 minutes. Unlike AAL2, AAL3 reauthentication requirements are the same as for initial authentication at AAL3. ^63b-2-3-3-1

### 63B §2.4.1 Security Controls

- **63B-2.4.1-1** SHALL — The verifier SHALL employ appropriately tailored security controls from the moderate baseline security controls defined in [SP800-53] or an equivalent federal (e.g., [FEDRAMP]) or industry standard that the organization has chosen for the information systems, applications, and online services that these guidelines are used to protect. ^63b-2-4-1-1

### 63B §2.4.2 Records Retention Policy

- **63B-2.4.2-1** SHALL — The verifier SHALL comply with its respective records retention policies in accordance with applicable laws, regulations, and policies, including any National Archives and Records Administration (NARA) records retention schedules that may apply. If the verifier opts to retain records in the absence of mandatory requirements, the verifier or the CSP or IdP of which it is a part SHALL conduct a risk management process [NISTRMF], including assessments of privacy and security risks, to determine how long records should be retained and SHALL inform the subscriber of that retention policy. ^63b-2-4-2-1

### 63B §2.4.3 Privacy Requirements

- **63B-2.4.3-1** SHALL — The verifier SHALL employ appropriately tailored privacy controls defined in [SP800-53] or an equivalent industry standard. ^63b-2-4-3-1
- **63B-2.4.3-2** SHALL NOT — If CSPs or IdPs process attributes for purposes other than identity services (i.e., identity proofing, authentication, or attribute assertions), related fraud mitigation, or compliance with laws or legal processes, they SHALL implement measures to maintain predictability and manageability commensurate with the privacy risks that arise from the additional processing. Examples of such measures include providing clear notice, obtaining subscriber consent, and enabling the selective use or disclosure of attributes. When CSPs or IdPs use consent measures, they SHALL NOT make consent for the additional processing a condition of the identity service. ^63b-2-4-3-2
- **63B-2.4.3-3** SHALL — The agency SHALL consult with their Senior Agency Official for Privacy (SAOP) and conduct an analysis to determine whether the collection of personal information to issue or maintain authenticators triggers the requirements of the Privacy Act of 1974 [PrivacyAct] (see Sec. 7.4). ^63b-2-4-3-3
- **63B-2.4.3-4** SHALL — The agency SHALL publish a System of Records Notice (SORN) to cover such collections, as applicable. ^63b-2-4-3-4
- **63B-2.4.3-5** SHALL — The agency SHALL consult with its SAOP and conduct an analysis to determine whether the collection of personal information to issue or maintain authenticators triggers the requirements of the E-Government Act of 2002 [E-Gov]. ^63b-2-4-3-5
- **63B-2.4.3-6** SHALL — The agency SHALL publish a Privacy Impact Assessment (PIA) to cover such collection, as applicable. ^63b-2-4-3-6

### 63B §2.4.4 Redress Requirements

- **63B-2.4.4-1** SHALL — The verifier and associated CSP or IdP SHALL provide mechanisms for the redress of subscriber complaints and problems that arise from subscriber authentication processes, as described in Sec. 5.6 of [SP800-63]. These mechanisms SHALL be easy for subscribers to find and use. The CSP or IdP SHALL assess the mechanisms for efficacy in resolving complaints or problems. ^63b-2-4-4-1

### 63B §3 Authenticator and Verifier Requirements

- **63B-3-1** SHOULD NOT — In many circumstances, subscribers need to share devices that are used in authentication processes, such as a family phone that receives OTPs. In public-facing applications, CSPs SHOULD NOT prevent a device from being registered as an authenticator by multiple subscribers. However, they MAY establish restrictions to prevent large-scale fraud or misuse (e.g., limiting the total number of subscriber accounts a single device can be registered with). ^63b-3-1

### 63B §3.1.1.1 Password Authenticators

- **63B-3.1.1.1-1** SHALL — Passwords SHALL either be chosen by the subscriber or assigned randomly by the CSP. ^63b-3-1-1-1-1
- **63B-3.1.1.1-2** SHALL NOT — If the CSP disallows a chosen password because it is on a blocklist of commonly used, expected, or compromised values (see Sec. 3.1.1.2), the subscriber SHALL be required to choose a different password. Other composition requirements for passwords SHALL NOT be imposed. A rationale for this is presented in Appendix A, Strength of Passwords. ^63b-3-1-1-1-2

### 63B §3.1.1.2 Password Verifiers

- **63B-3.1.1.2-1** SHALL — Verifiers and CSPs SHALL require passwords that are used as a single-factor authentication mechanism to be a minimum of 15 characters in length. Verifiers and CSPs MAY allow passwords that are only used as part of multi-factor authentication processes to be shorter but SHALL require them to be a minimum of eight characters in length. ^63b-3-1-1-2-1
- **63B-3.1.1.2-2** SHOULD — Verifiers and CSPs SHOULD permit a maximum password length of at least 64 characters. ^63b-3-1-1-2-2
- **63B-3.1.1.2-3** SHOULD — Verifiers and CSPs SHOULD accept all printing ASCII [RFC20] characters and the space character in passwords. ^63b-3-1-1-2-3
- **63B-3.1.1.2-4** SHALL — Verifiers and CSPs SHOULD accept Unicode [ISO/ISC 10646] characters in passwords. Each Unicode code point SHALL be counted as a single character when evaluating password length. ^63b-3-1-1-2-4
- **63B-3.1.1.2-5** SHALL NOT — Verifiers and CSPs SHALL NOT impose other composition rules (e.g., requiring mixtures of different character types) for passwords. ^63b-3-1-1-2-5
- **63B-3.1.1.2-6** SHALL NOT — Verifiers and CSPs SHALL NOT require subscribers to change passwords periodically. However, verifiers SHALL force a change if there is evidence that the authenticator has been compromised. ^63b-3-1-1-2-6
- **63B-3.1.1.2-7** SHALL NOT — Verifiers and CSPs SHALL NOT permit the subscriber to store a hint (e.g., a reminder of how the password was created) that is accessible to an unauthenticated claimant. ^63b-3-1-1-2-7
- **63B-3.1.1.2-8** SHALL NOT — Verifiers and CSPs SHALL NOT prompt subscribers to use knowledge-based authentication (KBA) (e.g., “What was the name of your first pet?”) or security questions when choosing passwords. ^63b-3-1-1-2-8
- **63B-3.1.1.2-9** SHALL — Verifiers SHALL request the password to be provided in full (not a subset of it) and SHALL verify the entire submitted password (e.g., not truncate it). ^63b-3-1-1-2-9
- **63B-3.1.1.2-10** SHOULD — If Unicode characters are accepted in passwords, the verifier SHOULD apply the normalization process for stabilized strings using the Normalization Form Canonical Composition (NFC) normalization defined in Sec. 12.1 of Unicode Normalization Forms [UAX15]. This process is applied before hashing the byte string that represents the password. Subscribers choosing passwords that contain Unicode characters SHOULD be advised that some endpoints may represent some characters differently, which would affect their ability to authenticate successfully. ^63b-3-1-1-2-10
- **63B-3.1.1.2-11** SHALL — When processing a request to establish or change a password, verifiers SHALL compare the prospective secret against a blocklist that contains known commonly used, expected, or compromised passwords. The entire password SHALL be subject to comparison, not substrings or words that might be contained therein. For example, the list may include: ^63b-3-1-1-2-11
- **63B-3.1.1.2-12** SHALL — If the chosen password is found on the blocklist, the CSP SHALL require the subscriber to select a different secret and SHALL provide the reason for rejection. Since the blocklist is used to defend against brute-force attacks and unsuccessful attempts are rate-limited, the blocklist SHOULD be of sufficient size to prevent subscribers from choosing passwords that attackers are likely to guess before reaching the attempt limit. ^63b-3-1-1-2-12
- **63B-3.1.1.2-13** SHALL — Verifiers SHALL offer guidance to the subscriber to help the subscriber choose a strong password. This is particularly important following the rejection of a password on the blocklist as it discourages trivial modifications of listed weak passwords [Blocklists]. ^63b-3-1-1-2-13
- **63B-3.1.1.2-14** SHALL — Verifiers SHALL implement a rate-limiting mechanism that effectively limits the number of failed authentication attempts that can be made on the subscriber account, as described in Sec. 3.2.2. ^63b-3-1-1-2-14
- **63B-3.1.1.2-15** SHALL — Verifiers SHALL allow the use of password managers and autofill functionality. Verifiers SHOULD permit claimants to use the “paste” function when entering a password to facilitate password manager use when password autofill APIs are unavailable. Password managers have been shown to increase the likelihood that subscribers will choose stronger passwords, particularly if the password managers include password generators [Managers]. ^63b-3-1-1-2-15
- **63B-3.1.1.2-16** SHOULD — To help the claimant successfully enter a password, the verifier SHOULD offer an option to display the password — rather than a series of dots or asterisks — while it is entered and until it is submitted to the verifier. This allows the claimant to confirm their entry if they are in a location where their screen is unlikely to be observed. The verifier MAY also permit the claimant’s device to display individual entered characters for a short time after each character is typed to verify the correct entry. This is common on mobile devices. ^63b-3-1-1-2-16
- **63B-3.1.1.2-17** MAY — Verifiers MAY make limited allowances for mistyping (e.g., removing leading and trailing whitespace characters before verification, allowing the verification of passwords with differing cases for the leading character) if the password remains at least the required minimum length after such processing and the complexity of the resulting password is not significantly reduced. ^63b-3-1-1-2-17
- **63B-3.1.1.2-18** SHALL — Verifiers and CSPs SHALL use approved encryption and an authenticated protected channel when requesting passwords. ^63b-3-1-1-2-18
- **63B-3.1.1.2-19** SHALL — Verifiers SHALL store passwords in a form that is resistant to offline attacks. Passwords SHALL be salted and hashed using a suitable password hashing scheme. Password hashing schemes take a password, a salt, and a cost factor as inputs and generate a password hash. Their purpose is to make each password guess more expensive for an attacker who has obtained a hashed password file, thereby making the cost of a guessing attack high or prohibitive. The chosen cost factor SHOULD be as high as practical without negatively impacting verifier performance. It SHOULD be increased over time to account for increases in computing performance. An approved password hashing scheme published in the latest revision of [SP800-132] or updated NIST guidelines on password hashing schemes SHOULD be used. The chosen output length of the password verifier, excluding the salt and versioning information, SHOULD be the same as the length of the underlying password hashing scheme output. ^63b-3-1-1-2-19
- **63B-3.1.1.2-20** SHALL — The salt SHALL be at least 32 bits in length and chosen to minimize salt value collisions among stored hashes (i.e., to prevent multiple subscriber accounts from having the same hashed password). Both the salt value and the resulting hash SHALL be stored for each password. A reference to the password hashing scheme used, including the cost factor, SHOULD be stored for each password to allow migration to new algorithms and work factors. ^63b-3-1-1-2-20
- **63B-3.1.1.2-21** SHALL — In addition, verifiers SHOULD perform an additional iteration of a keyed hashing or encryption operation using a secret key known only to the verifier. If used, this key value SHALL be generated by an approved random bit generator, as described in Sec. 3.2.12. The secret key value SHALL be stored separately from the hashed passwords. It SHOULD be stored and used within a hardware-protected area, such as a hardware security module or trusted execution environment (TEE), such as a trusted platform module (TPM). With this additional iteration, brute-force attacks on the hashed passwords are impractical as long as the secret key value remains secret. ^63b-3-1-1-2-21

### 63B §3.1.2.1 Look-Up Secret Authenticators

- **63B-3.1.2.1-1** SHALL — CSPs that create look-up secret authenticators SHALL use an approved random bit generator, as described in Sec. 3.2.12, to generate the list of secrets and SHALL deliver the authenticator list securely to the subscriber (e.g., in an in-person session, via an online session, through the postal mail to a contact address). If delivered via an online session, the session SHALL be authenticated by the subscriber at AAL2 or higher and SHALL deliver the secrets through an authenticated protected channel and in accordance with the post-enrollment binding requirements in Sec. 4.1.2. Look-up secrets SHALL be at least six decimal digits (or equivalent) in length. Additional requirements described in Sec. 3.1.2.2 may also apply, depending on their length. ^63b-3-1-2-1-1

### 63B §3.1.2.2 Look-Up Secret Verifiers

- **63B-3.1.2.2-1** SHALL — Verifiers of look-up secrets SHALL prompt the claimant for a secret from their authenticator. A secret from a look-up secret authenticator SHALL be used successfully only once. If the look-up secret is derived from a grid card, each grid cell SHOULD be used only once, which limits the number of authentications that can be accomplished using look-up secrets. A very long list of secrets is potentially required. ^63b-3-1-2-2-1
- **63B-3.1.2.2-2** SHALL — Verifiers SHALL store look-up secrets in a form that is resistant to offline attacks. All look-up secrets SHALL be stored in a hashed form using an approved hashing function. ^63b-3-1-2-2-2
- **63B-3.1.2.2-3** SHALL — Look-up secrets SHALL be at least six decimal digits (or equivalent) in length, as specified in Sec. 3.1.2.1. Look-up secrets that are shorter than specified lengths have additional verification requirements as follows: ^63b-3-1-2-2-3
- **63B-3.1.2.2-4** SHALL — Look-up secrets that are shorter than the minimum security strength specified in the latest revision of [SP800-131A] (i.e., 112 bits as of the date of this publication) SHALL be stored in a salted and hashed form using a suitable password hashing scheme, as described in Sec. 3.1.1.2. The salt value SHALL be at least 32 bits in length and arbitrarily chosen to minimize salt value collisions among stored hashes. Both the salt value and the resulting hash SHALL be stored for each look-up secret. ^63b-3-1-2-2-4
- **63B-3.1.2.2-5** SHALL — The verifier SHALL implement a rate-limiting mechanism that effectively limits the number of failed authentication attempts that can be made on the subscriber account, as described in Sec. 3.2.2. ^63b-3-1-2-2-5
- **63B-3.1.2.2-6** SHALL — The verifier SHALL use approved encryption and an authenticated protected channel when requesting look-up secrets. ^63b-3-1-2-2-6

### 63B §3.1.3.1 Out-of-Band Authenticators

- **63B-3.1.3.1-1** SHALL — The out-of-band authenticator SHALL establish a separate channel with the verifier to retrieve the out-of-band secret or authentication request. This channel is considered to be out-of-band with respect to the primary communication channel (even if it terminates on the same device), provided that the device does not leak information from one channel to the other without the claimant’s participation. ^63b-3-1-3-1-1
- **63B-3.1.3.1-2** SHALL — The out-of-band device SHOULD be uniquely addressable by the verifier. Communication over the secondary channel SHALL use approved encryption unless sent via the public switched telephone network (PSTN). For additional authenticator requirements that are specific to using the PSTN for out-of-band authentication, see Sec. 3.1.3.3. ^63b-3-1-3-1-2
- **63B-3.1.3.1-3** SHALL NOT — Email SHALL NOT be used for out-of-band authentication because it may be vulnerable to: ^63b-3-1-3-1-3
- **63B-3.1.3.1-4** SHALL — The out-of-band authenticator SHALL uniquely authenticate itself in one of the following ways when communicating with the verifier: ^63b-3-1-3-1-4
- **63B-3.1.3.1-5** SHALL — Using approved cryptography, establish a mutually authenticated protected channel (e.g., client-authenticated transport layer security (TLS) [RFC8446]) with the verifier. Communication between the out-of-band authenticator and the verifier MAY use a trusted intermediary service to which each authenticates. The key used to establish the channel SHALL be provisioned in a mutually authenticated session during authenticator binding, as described in Sec. 4.1. ^63b-3-1-3-1-5
- **63B-3.1.3.1-6** SHALL — Authenticate to a public mobile telephone network using a SIM card or equivalent secret that uniquely identifies the subscriber. This method SHALL only be used if a secret is sent from the verifier to the out-of-band device via the PSTN (i.e., SMS or voice) or an encrypted instant messaging service. ^63b-3-1-3-1-6
- **63B-3.1.3.1-7** SHOULD NOT — For single-factor out-of-band authenticators, if a secret is sent by the verifier to the out-of-band device, the device SHOULD NOT display the authentication secret while it is locked by the owner. Rather, the device SHOULD require the presentation and verification of a PIN, passcode, or biometric characteristic to view the secret. However, authenticators SHOULD indicate the receipt of an authentication secret on a locked device. ^63b-3-1-3-1-7
- **63B-3.1.3.1-8** SHALL — If the out-of-band authenticator requests approval over the secondary communication channel rather than by presenting a secret that the claimant transfers to the primary communication channel, it SHALL accept a transfer of the secret from the primary channel and send it to the verifier over the secondary channel to associate the approval with the authentication transaction. The claimant MAY perform the transfer manually or with the assistance of a representation, such as a barcode or quick response (QR) code. ^63b-3-1-3-1-8

### 63B §3.1.3.2 Out-of-Band Verifiers

- **63B-3.1.3.2-1** SHALL NOT — The verifier waits for an authenticated protected channel to be established with the out-of-band authenticator and verifies its identifying key. The verifier SHALL NOT store the identifying key itself but SHALL use a verification method (e.g., an approved hash function or proof of possession of the identifying key) to uniquely identify the authenticator. Once authenticated, the verifier transmits the authentication secret to the authenticator. The connection with the out-of-band authenticator MAY be either manually initiated or prompted by a mechanism, such as a push notification. ^63b-3-1-3-2-1
- **63B-3.1.3.2-2** SHALL — Depending on the type of out-of-band authenticator, one of the following SHALL take place: ^63b-3-1-3-2-2
- **63B-3.1.3.2-3** SHALL — Transfer of the secret from the secondary to the primary channel. As shown in Fig. 1, the verifier MAY signal the device that contains the subscriber’s authenticator to indicate a readiness to authenticate. It SHALL then transmit a random secret to the out-of-band authenticator and wait for the secret to be returned via the primary communication channel. ^63b-3-1-3-2-3
- **63B-3.1.3.2-4** SHALL — Transfer of the secret from the primary to the secondary channel. As shown in Fig. 2, the verifier SHALL transmit a random authentication secret to the claimant via the primary channel. It SHALL then wait for the secret to be returned via the secondary channel from the claimant’s out-of-band authenticator. The verifier MAY additionally display an address, such as a phone number or VoIP address, for the claimant to use in addressing its response to the verifier. ^63b-3-1-3-2-4
- **63B-3.1.3.2-5** SHALL — In all cases, the authentication SHALL be considered invalid unless completed within 10 minutes. Verifiers SHALL accept a given authentication secret as valid only once during the validity period to provide replay resistance, as described in Sec. 3.2.7. ^63b-3-1-3-2-5
- **63B-3.1.3.2-6** SHALL NOT — The verifier SHALL generate random authentication secrets that are at least six decimal digits (or equivalent) in length using an approved random bit generator as described in Sec. 3.2.12. If the authentication secret is less than 64 bits long, the verifier SHALL implement a rate-limiting mechanism that effectively limits the total number of consecutive failed authentication attempts that can be made on the subscriber account as described in Sec. 3.2.2. Generating a new authentication secret SHALL NOT reset the failed authentication count. ^63b-3-1-3-2-6
- **63B-3.1.3.2-7** SHOULD — Out-of-band verifiers that send a push notification to a subscriber device SHOULD implement a reasonable limit on the rate or total number of push notifications that will be sent since the last successful authentication. ^63b-3-1-3-2-7

### 63B §3.1.3.3 Authentication Using the Public Switched Telephone Network

- **63B-3.1.3.3-1** SHALL — Use of the PSTN for out-of-band verification is restricted as described in this section and SHALL satisfy the requirements of Sec. 3.2.9. Setting or changing the pre-registered telephone number is considered to be the binding of a new authenticator and SHALL only occur as described in Sec. 4.1.2. ^63b-3-1-3-3-1
- **63B-3.1.3.3-2** SHALL — Some subscribers may be unable to use PSTN to deliver out-of-band authentication secrets in areas with limited telephone coverage, particularly without mobile phone service. Accordingly, verifiers SHALL ensure that alternative authenticator types are available to all subscribers and SHOULD remind subscribers of this limitation of PSTN out-of-band authenticators before binding one or more devices controlled by the subscriber. ^63b-3-1-3-3-2
- **63B-3.1.3.3-3** SHOULD — Verifiers SHOULD consider risk indicators (e.g., device swap, SIM change, number porting, other abnormal behavior) before using the PSTN to deliver an out-of-band authentication secret. ^63b-3-1-3-3-3

### 63B §3.1.3.4 Multi-Factor Out-of-Band Authenticators

- **63B-3.1.3.4-1** SHALL — Multi-factor out-of-band authenticators operate similarly to single-factor out-of-band authenticators (see Sec. 3.1.3.1). However, they require the presentation and verification of an activation factor (i.e., a password or a biometric characteristic) before allowing the claimant to complete the authentication transaction (i.e., before accessing or entering the authentication secret as appropriate for the authentication flow being used). Each use of the authenticator SHALL require the presentation of the activation factor. ^63b-3-1-3-4-1
- **63B-3.1.3.4-2** SHALL — Authenticator activation secrets SHALL meet the requirements of Sec. 3.2.10. A biometric activation factor SHALL meet the requirements of Sec. 3.2.3, including limits on the number of consecutive authentication failures. The password or biometric sample used for activation and any biometric data derived from the biometric sample (e.g., a fingerprint image and feature locations produced by a fingerprint feature extractor) SHALL be erased immediately after an authentication operation. ^63b-3-1-3-4-2

### 63B §3.1.4.1 Single-Factor OTP Authenticators

- **63B-3.1.4.1-1** SHALL — The secret key and its algorithm SHALL provide at least the minimum security strength specified in the latest revision of [SP800-131A] (i.e., 112 bits as of the date of this publication). The nonce SHALL be of sufficient length to ensure that it is unique for each operation of the authenticator over its lifetime. If a subscriber needs to change the device on which a software-based OTP authenticator resides, they SHOULD bind the authenticator application on the new device to their subscriber account, as described in Sec. 4.1.2, and invalidate the authenticator application that will no longer be used. Alternatively, the subscriber MAY export the secret key and store it in a sync fabric that meets the requirements in Appendix B.2 and then retrieve the key with their new device. ^63b-3-1-4-1-1
- **63B-3.1.4.1-2** MAY — The authenticator output is obtained using an approved block cipher or hash function to securely combine the key and nonce. In coordination with the verifier, the authenticator MAY truncate its output to as few as six decimal digits (or an equivalent representation). ^63b-3-1-4-1-2
- **63B-3.1.4.1-3** SHALL — If the nonce used to generate the authenticator output is based on a real-time clock, the nonce SHALL be changed at least once every two minutes. ^63b-3-1-4-1-3

### 63B §3.1.4.2 Single-Factor OTP Verifiers

- **63B-3.1.4.2-1** SHALL — Single-factor OTP verifiers effectively duplicate the process of generating the OTP used by the authenticator. As such, the symmetric keys used by authenticators are also present in the verifier and SHALL be strongly protected against unauthorized disclosure by access controls that limit access to the keys to only those software components that require access. ^63b-3-1-4-2-1
- **63B-3.1.4.2-2** SHALL — When binding a single-factor OTP authenticator to a subscriber account, the verifier or associated CSP SHALL use approved cryptography for key establishment to generate and exchange keys or to obtain the secrets required to duplicate the authenticator output. ^63b-3-1-4-2-2
- **63B-3.1.4.2-3** SHALL — The verifier SHALL use approved encryption and an authenticated protected channel when collecting the OTP. Verifiers SHALL accept a given OTP only once while it is valid to provide replay resistance, as described in Sec. 3.2.7. If a claimant’s authentication is denied due to the duplicate use of an OTP, verifiers MAY warn the claimant if an attacker has been able to authenticate in advance. Verifiers MAY also warn a subscriber in an existing session of the attempted duplicate use of an OTP. ^63b-3-1-4-2-3
- **63B-3.1.4.2-4** SHALL — Time-based OTPs [TOTP] SHALL have a defined lifetime that is determined by the expected clock drift in either direction of the authenticator over its lifetime plus an allowance for network delay and claimant entry of the OTP. ^63b-3-1-4-2-4
- **63B-3.1.4.2-5** SHALL — The verifier SHOULD implement or, if the authenticator output is less than 64 bits in length, SHALL implement a rate-limiting mechanism that effectively limits the number of failed authentication attempts that can be made on the subscriber account, as described in Sec. 3.2.2. ^63b-3-1-4-2-5

### 63B §3.1.5.1 Multi-Factor OTP Authenticators

- **63B-3.1.5.1-1** SHALL — Multi-factor OTP authenticators operate similarly to single-factor OTP authenticators (see Sec. 3.1.4.1), except they require the presentation and verification of an activation factor (i.e., a password or a biometric characteristic) to obtain the OTP from the authenticator. Each use of the authenticator SHALL require the input of the activation factor. ^63b-3-1-5-1-1
- **63B-3.1.5.1-2** SHALL — The secret key and its algorithm SHALL provide at least the minimum security strength specified in the latest revision of [SP800-131A] (i.e., 112 bits as of the date of this publication). The nonce SHALL be of sufficient length to ensure that it is unique for each operation of the authenticator over its lifetime. If a subscriber needs to change the device on which a software-based OTP authenticator resides, they SHOULD bind the authenticator application on the new device to their subscriber account, as described in Sec. 4.1.2, and invalidate the authenticator application that will no longer be used. Alternatively, the subscriber MAY export the secret key and store it in a sync fabric that meets the requirements in Appendix B.2 and retrieve the key with their new device. ^63b-3-1-5-1-2
- **63B-3.1.5.1-3** MAY — The authenticator output is obtained using an approved cryptography block cipher or hash function to securely combine the key and nonce. In coordination with the verifier, the authenticator MAY truncate its output to as few as six decimal digits or equivalent. ^63b-3-1-5-1-3
- **63B-3.1.5.1-4** SHALL — Authenticator activation secrets SHALL meet the requirements of Sec. 3.2.10. A biometric activation factor SHALL meet the requirements of Sec. 3.2.3, including limits on the number of consecutive authentication failures. The unencrypted key and activation secret or biometric sample and any biometric data derived from the biometric sample (e.g., a fingerprint image and feature locations produced by a fingerprint feature extractor) SHALL be erased immediately after an OTP has been generated. ^63b-3-1-5-1-4

### 63B §3.1.5.2 Multi-Factor OTP Verifiers

- **63B-3.1.5.2-1** SHALL — Multi-factor OTP verifiers effectively duplicate the process of generating the OTP used by the authenticator without requiring a second authentication factor. As such, the symmetric keys used by authenticators SHALL be strongly protected against unauthorized disclosure by access controls that limit access to the keys to only those software components that require access. ^63b-3-1-5-2-1
- **63B-3.1.5.2-2** SHALL — When binding a multi-factor OTP authenticator to a subscriber account, the verifier or associated CSP SHALL use approved cryptography for key establishment to generate and exchange keys or to obtain the secrets required to duplicate the authenticator output. ^63b-3-1-5-2-2
- **63B-3.1.5.2-3** SHALL — The verifier SHALL implement a rate-limiting mechanism that effectively limits the number of consecutive failed authentication attempts that can be made on the subscriber account, as required by Sec. 3.2.10. ^63b-3-1-5-2-3

### 63B §3.1.6 Single-Factor Cryptographic Authentication

- **63B-3.1.6-1** SHALL — Single-factor cryptographic authentication is accomplished by proving the possession and control of a cryptographic key via an authentication protocol. Depending on the strength of authentication required, the authentication key may be stored in a manner that is accessible to the endpoint associated with the authenticator or in a separate, directly connected processor or device. The authenticator output is highly dependent on the specific cryptographic protocol used but is generally some type of signed message. A single-factor cryptographic authenticator is “something you have.” Single-factor cryptographic authenticators used at AAL3 SHALL use public-key cryptography to protect the authentication secrets from compromise of the verifier. ^63b-3-1-6-1

### 63B §3.1.6.1 Single-Factor Cryptographic Authenticators

- **63B-3.1.6.1-1** SHALL — Single-factor cryptographic authenticators encapsulate one or more authentication keys. Authentication keys are described as either exportable (see Sec. 3.2.13) or non-exportable. Exportable authentication keys (usable at AAL2 or below) SHOULD be stored in appropriate storage that is available to the authenticator (e.g., keychain storage). If they are accessible to the endpoint being authenticated, exportable authentication keys SHALL be strongly protected against unauthorized disclosure with access controls that limit access to the key to only those software components that require access. Non-exportable authentication keys (usable at AAL3 or below) SHALL be stored in an isolated execution environment that is protected by hardware or in a separate processor with a controlled interface to the central processing unit of the user endpoint. ^63b-3-1-6-1-1
- **63B-3.1.6.1-2** SHALL — External (i.e., non-embedded) cryptographic authenticators SHALL meet the requirements for connected authenticators in Sec. 3.2.11. ^63b-3-1-6-1-2

### 63B §3.1.6.2 Single-Factor Cryptographic Verifiers

- **63B-3.1.6.2-1** SHALL — The verifier has a public cryptographic key that corresponds to each authenticator. While both types of keys SHALL be protected against modification, symmetric keys SHALL additionally be protected against unauthorized disclosure by access controls that limit access to the key to only those software components that require access. ^63b-3-1-6-2-1
- **63B-3.1.6.2-2** SHALL — The authentication key and its algorithm SHALL provide at least the minimum security strength specified in the latest revision of [SP800-131A] (i.e., 112 bits as of the date of this publication). The challenge nonce SHALL be at least 64 bits in length and SHALL either be unique over the authenticator’s lifetime or statistically unique (i.e., generated using an approved random bit generator, as described in Sec. 3.2.12). The verification operation SHALL use approved cryptography. ^63b-3-1-6-2-2

### 63B §3.1.7 Multi-Factor Cryptographic Authentication

- **63B-3.1.7-1** SHALL — Multi-factor cryptographic authentication uses an authentication protocol to prove possession and control of an authentication key that requires activation through a second authentication factor. Depending on the strength of authentication needed, the authentication key may be stored in a manner that is accessible to the endpoint being authenticated or in a separate, directly connected processor or device. The authenticator output is highly dependent on the specific cryptographic protocol used but is generally some type of signed message. A multi-factor cryptographic authenticator is “something you have” and is activated by an activation factor that represents either “something you know” or “something you are.” Multi-factor cryptographic authenticators used at AAL3 SHALL use public-key cryptography to protect the authentication secrets from compromise of the verifier. ^63b-3-1-7-1

### 63B §3.1.7.1 Multi-Factor Cryptographic Authenticators

- **63B-3.1.7.1-1** SHALL — Multi-factor cryptographic authenticators encapsulate one or more authentication keys that SHALL only be accessible through the presentation and verification of an activation factor (i.e., a password or a biometric characteristic). Non-exportable authentication keys, suitable for use at AAL3, SHALL be stored in an isolated execution environment that is protected by hardware or in a separate processor with a controlled interface to the central processing unit of the user endpoint. Exportable authentication keys (usable at AAL2 or below) SHOULD be stored in appropriate storage that is available to the authenticator (e.g., keychain storage). If accessible to the endpoint being authenticated, authentication keys SHALL be strongly protected against unauthorized disclosure by using access controls that limit access to the authentication keys to only those software components that require access. ^63b-3-1-7-1-1
- **63B-3.1.7.1-2** SHALL — External (non-embedded) cryptographic authenticators SHALL meet the requirements for connected authenticators in Sec. 3.2.11. Each authentication event SHALL require input and verification of the local activation factor. Authenticator activation secrets SHALL meet the requirements of Sec. 3.2.10. A biometric activation factor SHALL meet the requirements of Sec. 3.2.3, including limits on the number of consecutive authentication failures. The activation secret or biometric sample and any biometric data derived from the biometric sample (e.g., a fingerprint image and feature locations produced by a fingerprint feature extractor) SHALL be erased after an authentication transaction. ^63b-3-1-7-1-2

### 63B §3.1.7.2 Multi-Factor Cryptographic Verifiers

- **63B-3.1.7.2-1** SHALL — The requirements for a multi-factor cryptographic verifier are identical to those for a single-factor cryptographic verifier, as described in Sec. 3.1.6.2. Some multi-factor authenticators include flags to indicate whether an activation factor was used. If such a flag is present and indicates that an activation factor was not used, the authentication SHALL be treated as single-factor. Otherwise, verification of the output from a multi-factor cryptographic authenticator indicates that the activation factor was used. ^63b-3-1-7-2-1

### 63B §3.1.7.3 Usage With Subscriber-Controlled Wallets

- **63B-3.1.7.3-1** SHALL — Access to the private key SHALL require an activation factor. Authenticator activation secrets SHALL meet the requirements of Sec. 3.2.10. Biometric activation factors SHALL meet the requirements of Sec. 3.2.3, including limits on the number of consecutive authentication failures. The password or biometric sample used for activation and any biometric data derived from the biometric sample SHALL be erased immediately after an authentication transaction. ^63b-3-1-7-3-1
- **63B-3.1.7.3-2** SHALL NOT — Authentication processes using subscriber-controlled wallets SHALL be used with a federation process as detailed in Sec. 5 of [SP800-63C]. Signed audience-restricted assertions that are generated by subscriber-controlled wallets are considered phishing-resistant because they prevent an assertion presented to an impostor RP from being used by the legitimate one. Assertions that lack a valid signature from the wallet or an audience restriction SHALL NOT be considered phishing-resistant. Assertions SHALL also include sufficient information to determine the nature of the activation method used to activate the wallet. ^63b-3-1-7-3-2

### 63B §3.2.1 Physical Authenticators

- **63B-3.2.1-1** SHALL — CSPs SHALL provide subscriber instructions for appropriately protecting the authenticator against theft or loss. The CSP SHALL provide a mechanism to invalidate1 the authenticator immediately upon notification from a subscriber that the authenticator’s loss, theft, or compromise is suspected. ^63b-3-2-1-1

### 63B §3.2.2 Rate Limiting (Throttling)

- **63B-3.2.2-1** SHALL — When required by the authenticator type descriptions in Sec. 3.1, the verifier SHALL implement controls to protect against online guessing attacks. Unless otherwise specified in the description of a given authenticator, the verifier SHALL limit consecutive failed authentication attempts using a specific authenticator on a single subscriber account to no more than 100 by disabling that authenticator. If more than one authenticator is involved with an excessive number of authentication attempts (e.g., single-factor cryptographic authenticator and centrally verified password), both authenticators SHALL be disabled. Authenticators that have been disabled SHALL be required to rebind to the subscriber account, as described in Sec. 4.1, to be usable in the future. ^63b-3-2-2-1
- **63B-3.2.2-2** MAY — The limit of 100 attempts is an upper bound, and agencies MAY impose lower limits. The limit of 100 was chosen to balance the likelihood of a correct guess (e.g., 100 attempts against a six-digit decimal OTP authenticator output) versus the potential need for account recovery when the limit is exceeded. ^63b-3-2-2-2
- **63B-3.2.2-3** MAY — Additional techniques MAY be used to reduce the likelihood that an attacker will lock the legitimate claimant out due to rate limiting. These include: ^63b-3-2-2-3
- **63B-3.2.2-4** SHOULD — When the subscriber successfully authenticates, the verifier SHOULD disregard any previous failed attempts for the authenticators used in the successful authentication. ^63b-3-2-2-4
- **63B-3.2.2-5** SHALL — Following successful authentication at a given AAL, the verifier SHOULD reset the retry count of the authenticators that were used. If this is provided, the maximum AAL of the authenticator being reset SHALL not exceed the AAL of the session from which it is being reset. If the subscriber cannot authenticate at the required AAL, the account recovery procedures in Sec. 4.2 SHALL be used. ^63b-3-2-2-5

### 63B §3.2.3 Use of Biometrics

- **63B-3.2.3-1** SHALL — Biometrics SHALL only be used as part of multi-factor authentication with a physical authenticator (i.e., “something you have”). The biometric characteristic SHALL be presented and compared for each authentication operation. An alternative non-biometric authentication option SHALL always be provided to the subscriber. Biometric data SHALL be treated and secured as sensitive personal information. ^63b-3-2-3-1

### 63B §3.2.3.1 Biometric Accuracy

- **63B-3.2.3.1-1** SHALL — The biometric system SHALL operate with an FMR [ISO/IEC2382-37] of one in 10000 or better for all demographic groups. Demographic categories to be considered SHALL include sex and skin tone when these factors affect biometric performance. This FMR SHALL be achieved under the conditions of a conformant attack (i.e., zero-effort impostor attempt), as defined in [ISO/IEC30107-1]. The biometric system SHOULD demonstrate a false non-match rate (FNMR) of less than 5 %. Biometric performance SHALL be tested in accordance with [ISO/IEC19795-1]. The biometric system SHALL be configured with a fixed threshold; it is not feasible to change the threshold for each demographic. ^63b-3-2-3-1-1

### 63B §3.2.3.2 Presentation Attack Detection

- **63B-3.2.3.2-1** SHALL NOT — The biometric system SHOULD implement PAD for iris and fingerprint modalities and SHALL implement PAD for facial recognition. Biometric comparison based on voice SHALL NOT be used. Testing the biometric system for deployment SHOULD demonstrate an impostor attack presentation accept rate (IAPAR) of less than 0.07. Presentation attack resistance SHOULD be tested in accordance with Clause 13 of [ISO/IEC30107-3] following security evaluation methodologies in [ISO/IEC19792] or [ISO/IEC19989-1] and [ISO/IEC19989-3]. The PAD decision MAY be made either locally on the claimant’s device or by a central verifier. ^63b-3-2-3-2-1

### 63B §3.2.3.3 Injection Attack Detection

- **63B-3.2.3.3-1** SHALL — The biometric system SHALL allow no more than five consecutive failed authentication attempts or 10 consecutive failed attempts if PAD is implemented and meets the above requirements. Once that limit has been reached, the biometric authenticator SHALL impose a delay of at least 30 seconds before each subsequent attempt with an overall limit of no more than 50 consecutive failed authentication attempts or 100 if PAD is implemented due to the mitigation of presentation attacks. Once the overall limit is reached, the biometric system SHALL disable biometric authentication and offer another factor (e.g., a different biometric modality or an activation secret if it is not a required factor) if such an alternative method is already available. These limits are upper bounds, and agencies MAY make risk-based decisions to impose lower limits. ^63b-3-2-3-3-1
- **63B-3.2.3.3-2** SHOULD — The verifier SHOULD determine the performance and integrity of the sensor and its associated endpoint. This increases the likelihood of detecting injection attacks due to compromised endpoints, sensor emulators, and similar threats. Acceptable methods for making this determination include: ^63b-3-2-3-3-2
- **63B-3.2.3.3-3** SHOULD — Biometric comparison can be performed locally on a device being used by the claimant or at a central verifier. Since the potential for attacks on a larger scale is greater at central verifiers, comparison SHOULD be performed locally. ^63b-3-2-3-3-3
- **63B-3.2.3.3-4** SHALL — The presentation of a biometric factor for authenticator activation SHALL be a separate operation from unlocking the host device (e.g., smartphone). However, the same activation factor used to unlock the host device MAY be used in the authentication operation. Agencies MAY lower this requirement for authenticators that are managed by or on behalf of the CSP (e.g., via mobile device management) and constrained to have short agency-determined inactivity timeouts and biometric systems that meet the above requirements. ^63b-3-2-3-3-4
- **63B-3.2.3.3-5** SHALL — The sensor or endpoint SHALL be authenticated before capturing the biometric sample from the claimant. The verifier MAY limit the use of the centrally stored biometric template to particular sensors or sensor classes (e.g., sensor manufacturers or models). ^63b-3-2-3-3-5
- **63B-3.2.3.3-6** SHALL — Appropriate controls (e.g., encryption and access controls) for sensitive personal information SHALL be implemented. ^63b-3-2-3-3-6
- **63B-3.2.3.3-7** SHALL — An authenticated protected channel between the sensor (or an endpoint containing a sensor that resists sensor replacement) and the verifier SHALL be established. All transmission of biometric information SHALL be conducted over that authenticated protected channel. ^63b-3-2-3-3-7

### 63B §3.2.3.4 Use of Biometric Samples

- **63B-3.2.3.4-1** SHALL — Biometric samples collected in the authentication process MAY be used locally within the authenticator or verifier performing the biometric comparison to update the templates for the purpose of compensating for changes in subscriber characteristics or — with explicit subscriber consent — other research purposes. The biometric samples and any other biometric data derived from them SHALL be erased immediately after any adaptation or research data has been derived. A limit on the allowable time for adaptation SHALL be established and enforced by the authenticator or the CSP. ^63b-3-2-3-4-1

### 63B §3.2.4 Attestation

- **63B-3.2.4-1** MAY — The CSP needs to have a reliable basis for evaluating the characteristics of the authenticator, such as the inclusion of a signed attestation. An attestation is information conveyed to the CSP, generally when an authenticator is bound, regarding that connected authenticator or the endpoint involved in an authentication operation. Information conveyed by attestation MAY include but is not limited to: ^63b-3-2-4-1
- **63B-3.2.4-2** SHALL — Attestations SHALL be signed using a digital signature that provides at least the minimum security strength specified in the latest revision of [SP800-131A] (i.e., 112 bits as of the date of this publication). ^63b-3-2-4-2
- **63B-3.2.4-3** SHOULD — Verifiers in federal enterprise systems2 SHOULD use attestation features to verify the capabilities and sources of authenticators. In other applications, attestation information MAY be used as part of a verifier’s risk-based authentication decisions. ^63b-3-2-4-3

### 63B §3.2.5 Phishing Resistance

- **63B-3.2.5-1** SHALL — Approved cryptographic algorithms SHALL be used to establish phishing resistance where required. Keys used for this purpose SHALL provide at least the minimum security strength specified in the latest revision of [SP800-131A] (i.e., 112 bits as of the date of this publication). ^63b-3-2-5-1
- **63B-3.2.5-2** SHALL NOT — Phishing resistance requires single- or multi-factor cryptographic authentication. Authenticators that involve the manual entry of an authenticator output (e.g., out-of-band and OTP authenticators) SHALL NOT be considered phishing-resistant because the manual entry does not bind the authenticator output to the specific session being authenticated. For example, an impostor verifier could relay an authenticator output to the verifier and successfully authenticate. ^63b-3-2-5-2

### 63B §3.2.5.1 Channel Binding

- **63B-3.2.5.1-1** SHALL — An authentication protocol with channel binding SHALL establish an authenticated protected channel with the verifier. The protocol SHALL then strongly and irreversibly bind a channel identifier negotiated in establishing the authenticated protected channel to the authenticator output (e.g., by signing the two values together using a private key controlled by the claimant for which the public key is known to the verifier). The verifier SHALL validate the signature or other information used to prove phishing resistance. This prevents an impostor verifier — even one that has obtained a certificate that represents the actual verifier — from successfully relaying that authentication on a different authenticated protected channel. ^63b-3-2-5-1-1

### 63B §3.2.5.2 Verifier Name Binding

- **63B-3.2.5.2-1** SHALL — An authentication protocol with verifier name binding SHALL establish an authenticated protected channel with the verifier. The protocol SHALL then generate an authenticator output that is cryptographically bound to a verifier identifier that is authenticated as part of the protocol. In the case of DNS identifiers, the verifier identifier SHALL be either the authenticated hostname of the verifier or a parent domain that is at least one level below the public suffix [PSL] associated with that hostname. The binding MAY be established by choosing an associated authenticator secret, deriving an authenticator secret using the verifier identifier, cryptographically signing the authenticator output with the verifier identifier, or using similar cryptographically secure means. ^63b-3-2-5-2-1

### 63B §3.2.6 Verifier-CSP or IdP Communications

- **63B-3.2.6-1** SHALL — If the verifier and CSP or IdP are separate entities (as shown by the dotted line in Fig. 3 of [SP800-63]), communications between the verifier and CSP or IdP SHALL occur through a mutually authenticated protected channel (e.g., a client-authenticated TLS connection) using approved cryptography. ^63b-3-2-6-1

### 63B §3.2.8 Authentication Intent

- **63B-3.2.8-1** SHALL — An authentication process demonstrates intent if it requires the claimant to respond explicitly to each authentication or reauthentication request. The goal of authentication intent is to make it more difficult for authenticators (e.g., multi-factor cryptographic authenticators) to be used without the claimant’s knowledge, such as by malware on the endpoint. The authenticator itself SHALL establish authentication intent. Multi-factor authenticators MAY establish intent by reentry of the activation factor for the authenticator. ^63b-3-2-8-1
- **63B-3.2.8-2** MAY — Authentication intent MAY be established in several ways. Authentication processes that require the claimant’s intervention can be used to prove intent (e.g., a claimant entering an authenticator output from an OTP authenticator). Cryptographic authenticators that require claimant action for each authentication or reauthentication operation can also be used to establish intent (e.g., by pushing a button or reinsertion). ^63b-3-2-8-2
- **63B-3.2.8-3** SHALL — The presentation of biometric characteristics does not always establish authentication intent. For example, using a front-facing camera on a mobile phone to capture a face biometric does not necessarily constitute intent, as it can be reasonably expected to capture a face image while the device is used for other non-authentication purposes. In these scenarios, an explicit mechanism (e.g., tapping a software or physical button) SHALL be provided to establish authentication intent. ^63b-3-2-8-3

### 63B §3.2.9 Restricted Authenticators

- **63B-3.2.9-1** SHALL NOT — The acceptance of a restricted authenticator requires the implementing organization to assess, understand, and accept the risks associated with that authenticator and acknowledge that risks will likely increase over time. It is the RP’s responsibility to determine the level of acceptable risk for their systems and associated data, define any methods for mitigating excessive risks, and communicate those determinations to the verifier. If the RP determines that the risk to any party is unacceptable, the restricted authenticator SHALL NOT be used, and an alternative authenticator type SHALL be used. ^63b-3-2-9-1
- **63B-3.2.9-2** SHALL — Furthermore, the risk of an authentication error is typically borne by multiple parties, including the implementing organization, organizations that rely on the authentication decision, and the subscriber. Because the subscriber may be exposed to additional risks when an organization accepts a restricted authenticator and the subscriber may have a limited understanding of and ability to control those risks, the CSP SHALL do all of the following: ^63b-3-2-9-2

### 63B §3.2.10 Activation Secrets

- **63B-3.2.10-1** SHALL — A password used locally as an activation factor for a multi-factor authenticator is referred to as an activation secret. An activation secret is used to obtain access to a stored authentication key. In all cases, the activation secret SHALL remain within the authenticator and its associated user endpoint. ^63b-3-2-10-1
- **63B-3.2.10-2** SHALL — Authenticators that use activation secrets SHALL require the secrets to be at least four characters in length and SHOULD require the secrets to be at least six characters in length. Activation secrets MAY be entirely numeric (i.e., a PIN). Otherwise, all printing ASCII [RFC20] characters, the space character, and Unicode [ISO/ISC 10646] characters SHOULD be permitted in activation secrets. The authenticator or its management tools SHOULD implement a blocklist to discourage subscribers from selecting commonly used activation secrets (e.g., 123456). ^63b-3-2-10-2
- **63B-3.2.10-3** SHALL — The authenticator or verifier SHALL implement a retry-limiting mechanism that limits the number of consecutive failed activation attempts using the authenticator to no more than 10. If an incorrect activation secret entry causes the authenticator to provide an invalid output to the central verifier, the verifier MAY implement this retry-limiting mechanism. Otherwise, retry limiting SHALL be implemented in the authenticator. Once the limit of attempts is reached, the authenticator SHALL be disabled, and a different authenticator SHALL be required for authentication. ^63b-3-2-10-3
- **63B-3.2.10-4** SHALL — For authenticators that are usable at AAL3, verification of activation secrets SHALL be performed in a hardware-protected environment (e.g., a secure element, TPM, or TEE). At AAL2, if a hardware-protected environment is not used, the authenticator SHALL use the activation secret to derive a key used to decrypt the authentication key. ^63b-3-2-10-4
- **63B-3.2.10-5** SHALL — Submitting the activation factor SHALL be a separate operation from unlocking the host device (e.g., smartphone). However, the same activation factor used to unlock the host device MAY be used in the authentication operation. Agencies MAY relax this requirement for authenticators that are managed by or on behalf of the CSP (e.g., via mobile device management), are constrained to have short agency-determined inactivity timeouts, and use device activation factors that meet the corresponding requirements in this section. ^63b-3-2-10-5

### 63B §3.2.11 Connected Authenticators

- **63B-3.2.11-1** SHALL — Cryptographic authenticators require a trustworthy connection between the authenticator and the endpoint being authenticated that provides resistance to eavesdropping, injection, and relay attacks. This connection SHALL be made using a wired connection (e.g., USB or direct connection with a smartcard), a wireless technology, or a hybrid of those technologies, including network connections. ^63b-3-2-11-1
- **63B-3.2.11-2** SHALL — Approved cryptography SHALL be used for all cases in which cryptographic operations are required. All communication of authentication data between authenticators and endpoints SHALL occur directly between those devices or through an authenticated protected channel between the authenticator and endpoint. ^63b-3-2-11-2

### 63B §3.2.11.1 Wired Connections

- **63B-3.2.11.1-1** SHOULD — Wired connections, including those with embedded authenticators, MAY be assumed to be trustworthy because their attack surface is minimal. Claimants SHOULD be advised to use trusted hardware (e.g., cables, adapters) to ensure that they have not been compromised. ^63b-3-2-11-1-1

### 63B §3.2.11.2 Wireless Connections

- **63B-3.2.11.2-1** SHALL — The potential for such attacks on wireless connections depends on the technology’s effective range. To minimize the attack surface for threats to the authenticator-endpoint connection, the authentication process SHALL require physical proximity between the authenticator and endpoint by establishing a wireless connection with a range of no more than 240 meters.3 ^63b-3-2-11-2-1
- **63B-3.2.11.2-2** SHALL — Wireless connections SHALL establish a key for encrypted communication between the authenticator and endpoint in one of the following ways: ^63b-3-2-11-2-2
- **63B-3.2.11.2-3** SHALL — Through an association process that is similar to a pairing process but does not require a persistent relationship between devices to establish a key for encrypted communication between the authenticator and endpoint. The association process SHALL employ a pairing code4 or other shared secret between the devices. Either the authenticator or endpoint SHALL have a pairing code that MAY be printed on the device. The pairing code SHALL be at least six decimal digits (or equivalent) in length. It SHALL be conveyed between the devices by manual entry or using a QR code or similar representation that is optically communicated. ^63b-3-2-11-2-3
- **63B-3.2.11.2-4** SHALL — When using a wireless technology with an effective range of less than 1 meter (e.g., NFC), any activation secret transmitted from the endpoint to the authenticator SHALL be encrypted using a key that is established between the devices. An authenticated connection SHOULD be used. A pairing code SHALL be used if the authenticator is configured to require authenticated pairing. ^63b-3-2-11-2-4
- **63B-3.2.11.2-5** SHOULD — Encrypting only the activation secret and not the entire authentication transaction may expose sensitive information (e.g., the identity of the RP), although this would require the attacker to be very close to the subscriber. Special care should be taken with authenticators that contain personal information but do not require authenticated pairing. Encryption SHOULD be used to protect that information against eavesdropping attacks. ^63b-3-2-11-2-5
- **63B-3.2.11.2-6** SHALL — Network connections and wireless technologies with an effective range of 1 meter or more (e.g., Bluetooth Low Energy [BLE]) SHALL use an authenticated protected channel between the authenticator and endpoint. The entire authentication transaction SHALL be encrypted. ^63b-3-2-11-2-6
- **63B-3.2.11.2-7** SHALL — The key established by the association process may be either temporary (i.e., valid for a limited number of transactions or time-limited) or persistent. A mechanism for endpoints to remove persistent keys SHALL be provided. ^63b-3-2-11-2-7

### 63B §3.2.11.3 Hybrid Connections

- **63B-3.2.11.3-1** SHALL — Hybrid connections (e.g., hybrid transports specified by the CTAP2.2 protocol [FIDO2]) SHALL be established between authenticators and endpoints in one of the following ways: ^63b-3-2-11-3-1
- **63B-3.2.11.3-2** SHALL — By communicating initial keying information and the identity of the tunnel service to be used via a displayed QR code or similar visual representation coupled with the receipt by the endpoint of wireless data containing the additional information required to establish the tunnel connection. The wireless data SHALL be conveyed over a technology with a maximum effective range of no more than 240 meters. ^63b-3-2-11-3-2
- **63B-3.2.11.3-3** SHALL — A mechanism for endpoints to remove cached associations with authenticators SHALL be provided. ^63b-3-2-11-3-3

### 63B §3.2.12 Random Values

- **63B-3.2.12-1** SHALL — Random values are extensively used in authentication processes in a variety of roles (e.g., nonces, authentication secrets). Unless otherwise specified, random values that reference this section SHALL be generated by an approved random bit generator [RBG]5 that provides at least the minimum security strength specified in the latest revision of [SP800-131A] (i.e., 112 bits as of the date of this publication). ^63b-3-2-12-1

### 63B §3.2.13 Exportability

- **63B-3.2.13-1** SHALL NOT — To be considered non-exportable, an authenticator SHALL either be a separate piece of hardware or an embedded processor or execution environment (e.g., secure element, TEE, TPM). These hardware authenticators and embedded processors are separate from a host processor, such as the CPU on a laptop or mobile device. A non-exportable authenticator SHALL be designed to prohibit the export of the authentication secret to the host processor and SHALL NOT be capable of being reprogrammed by the host processor to allow the secret to be extracted. The authenticator is subject to applicable [FIPS140] requirements. Organizations SHOULD employ authenticators that have undergone independent security testing, such as authenticators validated to [FIPS140] security level 2 overall with level 3 physical security6 or evaluated against relevant Common Criteria Protection Profiles. ^63b-3-2-13-1

### 63B §4.1 Authenticator Binding

- **63B-4.1-1** SHALL — Authenticators SHALL be bound to subscriber accounts by either: ^63b-4-1-1
- **63B-4.1-2** SHALL — Throughout the lifetime of a digital identity, CSPs SHALL maintain a record of all authenticators that are bound to each subscriber account. The CSP SHALL determine the characteristics of the authenticator being bound (e.g., single-factor versus multi-factor, phishing-resistant or not) so that verifiers can assess compliance with the requirements at each AAL. This determination MAY be based on strong evidence (e.g., authenticator attestation), direct information from having issued the authenticator, or typical characteristics of authenticator implementations (e.g., whether a user verification bit is set by [WebAuthn]). ^63b-4-1-2
- **63B-4.1-3** SHALL — The CSP SHALL also maintain other state information that is required to meet the authenticator verification requirements. For example, the throttling of authentication attempts described in Sec. 3.2.2 requires the CSP or verifier to maintain state information on recent failed authentication attempts, except for activation factors verified at the authenticator. ^63b-4-1-3
- **63B-4.1-4** SHALL — The record created by the CSP SHALL contain the date and time of significant authenticator life cycle events (e.g., binding to the subscriber account, renewal, update, expiration). The record SHOULD include information about the source of the binding (e.g., IP address, device identifier) of any device associated with the event. ^63b-4-1-4
- **63B-4.1-5** MAY — As part of the binding process, the CSP MAY require additional information about the new authenticator or its associated endpoint to determine whether it is suitable for the requested AAL. ^63b-4-1-5

### 63B §4.1.2.1 Binding an Additional Authenticator

- **63B-4.1.2.1-1** SHOULD — To minimize the need for account recovery, CSPs and verifiers SHOULD encourage subscribers to maintain at least two separate means of authentication. For example, a subscriber who usually uses an OTP authenticator as a physical authenticator MAY also be issued look-up secret authenticators or register a device for out-of-band authentication to be used if the physical authenticator is lost, stolen, or damaged. See Sec. 4.2 for more information on replacing passwords. ^63b-4-1-2-1-1
- **63B-4.1.2.1-2** SHALL — Accordingly, CSPs SHALL permit the binding of multiple authenticators to a subscriber account. When any new authenticator is bound to a subscriber account, the CSP SHALL ensure that the process requires authentication at either the maximum AAL currently available in the subscriber account or the maximum AAL at which the new authenticator will be used, whichever is lower. For example, binding an authenticator that is suitable for use at AAL2 requires authentication at AAL2 unless the subscriber account currently has only AAL1 authentication capabilities. When an authenticator is added, the CSP SHALL notify the subscriber via a mechanism independent of the transaction binding the new authenticator, as described in Sec. 4.6. ^63b-4-1-2-1-2

### 63B §4.1.2.2 Binding Across Endpoints

- **63B-4.1.2.2-1** SHALL — The binding process SHALL proceed in one of the following ways: ^63b-4-1-2-2-1
- **63B-4.1.2.2-2** SHALL — In addition to the requirements in Sec. 4.1.2.1 and Sec. 4.2, the following requirements SHALL apply when binding an external authenticator: ^63b-4-1-2-2-2
- **63B-4.1.2.2-3** SHALL — An authenticated protected channel SHALL be established by the endpoint associated with the new authenticator and the CSP. ^63b-4-1-2-2-3
- **63B-4.1.2.2-4** MAY — The subscriber MAY be prompted to enter an identifier by which the CSP knows them on the endpoint associated with the new authenticator. ^63b-4-1-2-2-4
- **63B-4.1.2.2-5** SHALL — The CSP SHALL generate a binding code using an approved random bit generator, as described in Sec. 3.2.12 and send it to either the new authenticator endpoint or the authenticated endpoint approving the binding. The binding code SHALL be at least 40 bits in length if it is used with an identifier that was entered in the previous step. Otherwise, a binding code of at least 112 bits in length SHALL be required. ^63b-4-1-2-2-5
- **63B-4.1.2.2-6** SHALL NOT — The subscriber SHALL transfer the binding code to the other endpoint. This transfer SHALL either be manual or via a local out-of-band method (e.g., QR code). The binding code SHALL NOT be communicated over any insecure channel (e.g., email). ^63b-4-1-2-2-6
- **63B-4.1.2.2-7** SHALL — The binding code SHALL be usable only once and SHALL be valid for a maximum of 10 minutes. ^63b-4-1-2-2-7
- **63B-4.1.2.2-8** SHOULD — Following the binding of the new authenticator (or issuance of a certificate, in the case of PKI-based authenticators), the CSP SHOULD encourage the subscriber to authenticate with the new authenticator to confirm that the process has been completed successfully. ^63b-4-1-2-2-8
- **63B-4.1.2.2-9** SHALL — The CSP SHALL provide clear instructions on what the subscriber should do in the event of an authenticator binding mishap (e.g., making a button available to be pressed or a contact address to be used to allow a misbound authenticator to be quickly invalidated), as appropriate. This MAY be provided in the authenticated session in addition to the binding notification described in Sec. 4.6. ^63b-4-1-2-2-9

### 63B §4.1.3 Binding to a Subscriber-Provided Authenticator

- **63B-4.1.3-1** SHALL — CSPs SHOULD, where practical, accommodate subscriber-provided authenticators to relieve the burden on the subscriber of managing many authenticators. The binding of these authenticators SHALL be done as described in Sec. 4.1.2. ^63b-4-1-3-1
- **63B-4.1.3-2** SHALL — As part of this process, CSPs will need to establish the capabilities and characteristics of the subscriber-provided authenticator that they wish to accept to determine its suitability for the use case and the intended AAL. The level of assurance that the CSP requires in the fidelity of these authenticator attributes MAY vary depending on the use case and threat environment. Some authenticators, such as those based on the WebAuthn standard [WebAuthn], provide metadata about the authenticator during the binding or authentication process that can be used by the CSP to inform its decisions. This metadata, for example, could indicate whether an authenticator uses an activation factor to function as a multi-factor authenticator. Similarly, some subscriber-controlled wallets will also offer metadata about its functions, including information about the mechanisms used to unlock the wallet. CSPs SHOULD consider this metadata when choosing how to support a subscriber-provided authenticator. In many cases, such information will not be available, and CSPs SHOULD evaluate the characteristics of commercially available authenticators that are likely to be used by their subscribers and make determinations about what authenticators they will accept. The types of authenticators accepted by the CSP SHALL be documented in the CSP practice statement. ^63b-4-1-3-2
- **63B-4.1.3-3** SHOULD NOT — In some high assurance use cases, CSPs may desire additional confidence in the attributes of the authenticators registered by their subscribers. Some authenticators support attestation features that can be used to determine the capabilities and manufacturers of specific authenticators. However, such attestation features are not widely available in authenticators that are likely to be used by public users. The lack of support for attestations SHOULD NOT block the use of authenticators for broad public-facing applications. ^63b-4-1-3-3

### 63B §4.1.4 Renewal

- **63B-4.1.4-1** SHOULD — The subscriber SHOULD bind a new or updated authenticator before an existing authenticator’s expiration. The process for this SHOULD conform closely to the binding process for an additional authenticator, as described in Sec. 4.1.2. The CSP MAY periodically take other actions (e.g., confirming contact addresses) as a part of the renewal process or separately. Following the successful use of the replacement authenticator, the CSP SHOULD invalidate the expiring authenticator. ^63b-4-1-4-1

### 63B §4.2.1 Account Recovery Methods

- **63B-4.2.1-1** SHALL — CSPs SHALL support one or more of these and MAY support an application-specific method (e.g., interaction with a CSP agent) to recover a subscriber account. The use of alternative methods SHALL be based on a risk analysis and documented by the CSP. ^63b-4-2-1-1

### 63B §4.2.1.1 Saved Recovery Codes

- **63B-4.2.1.1-1** SHALL — At enrollment, a CSP that supports this recovery option SHOULD issue a recovery code to the subscriber. The recovery code SHALL include at least 64 bits from an approved random bit generator. The saved recovery code may be presented as numeric or a printable ASCII representation (e.g., Base64) for manual entry or as a machine-readable optical label (e.g., QR code) that contains the recovery code. At any point following enrollment, the subscriber MAY request a replacement recovery code. The issuance of a replacement recovery code SHALL result in an account recovery notification, as described in Sec. 4.6. ^63b-4-2-1-1-1
- **63B-4.2.1.1-2** SHALL — Saved recovery codes are intended to be maintained offline (e.g., printed or written down) and stored securely by the subscriber for future use. The verification of saved recovery codes SHALL be subject to the throttling requirements in Sec. 3.2.2. Saved recovery codes SHALL be stored in the subscriber account in hashed form using an approved one-way function, as described in Sec. 3.1.1.2. Following the use of a saved recovery code, the CSP SHALL invalidate that recovery code and SHALL issue a new saved recovery code to the subscriber. ^63b-4-2-1-1-2

### 63B §4.2.1.2 Issued Recovery Codes

- **63B-4.2.1.2-1** SHALL — CSPs that support this option allow the subscriber to maintain one or more recovery addresses (e.g., postal, email, text message, voice). When recovery is required, a recovery code will be sent to a claimant-chosen address. The issued recovery code SHALL include at least six decimal digits (or equivalent) from an approved random bit generator, as described in Sec. 3.2.12. The issued recovery code may be presented as a numeric or a printable ASCII representation (e.g., Base64) for manual entry, a secure (e.g., https) link with a representation of the recovery code, or a machine-readable optical label (e.g., QR code) that contains the recovery code. ^63b-4-2-1-2-1
- **63B-4.2.1.2-2** SHALL — Issued recovery codes SHALL be valid for at most: ^63b-4-2-1-2-2
- **63B-4.2.1.2-3** SHALL — The verification of issued recovery codes SHALL be subject to the throttling requirements in Sec. 3.2.2. ^63b-4-2-1-2-3
- **63B-4.2.1.2-4** SHALL — When establishing recovery addresses other than those validated or verified as part of the identity proofing process, the address SHALL be verified. To verify an address, the CSP SHALL send a confirmation code with the same characteristics as a recovery code to the newly established recovery address. A recovery address SHALL be established only after the subscriber provides the correct confirmation code to the CSP. CSPs SHALL allow the subscriber to establish at least two recovery addresses. ^63b-4-2-1-2-4

### 63B §4.2.1.3 Recovery Contacts

- **63B-4.2.1.3-1** SHALL — CSPs that support the use of recovery contacts SHALL allow the subscriber to specify one or more addresses of trusted associates to receive issued recovery codes. The requirements for recovery contacts are very similar to those for issued recovery codes with the following exceptions: ^63b-4-2-1-3-1
- **63B-4.2.1.3-2** MAY — The validity time for recovery codes sent to recovery contacts MAY be extended by 24 hours (e.g., valid for no more than 24 hours and 10 minutes if sent via text messaging) to provide additional time for the recovery contact to communicate the recovery code to the subscriber. ^63b-4-2-1-3-2
- **63B-4.2.1.3-3** MAY — Confirmation of the recovery code address MAY also be extended by 24 hours to allow the recovery contact to send the confirmation code to the subscriber for entry. ^63b-4-2-1-3-3
- **63B-4.2.1.3-4** SHALL — If the CSP supports the use of recovery contacts, the CSP SHALL provide methods for subscribers to view and manage recovery contacts. CSPs SHOULD send a reminder annually to subscribers to review their list of recovery contacts. ^63b-4-2-1-3-4

### 63B §4.2.1.4 Repeated Identity Proofing

- **63B-4.2.1.4-1** SHALL — When the subscriber account has been identity-proofed at a minimum of identity assurance level 1 (IAL1), CSPs SHOULD support account recovery by repeating a portion of the identity proofing process. The CSP SHALL repeat the necessary steps of identity proofing consistent with the level of initial identity proofing and SHALL confirm that the claimant’s identity is consistent with the previously established account. If the CSP has retained a biometric sample from the user or a copy of the evidence used during the initial proofing that is of sufficient quality and resolution, the CSP MAY repeat only the verification portion of the identity proofing process, as described in [SP800-63A]. ^63b-4-2-1-4-1

### 63B §4.2.2.1 Recovery Without Identity Proofing

- **63B-4.2.2.1-1** SHALL — When subscribers have not been identity-proofed, a reproofing option is not available to support account recovery. The recovery of such subscriber accounts SHALL require the successful use of a saved recovery code, issued recovery code, or recovery contact. ^63b-4-2-2-1-1

### 63B §4.2.2.2 Recovery at AAL2

- **63B-4.2.2.2-1** SHALL — To recover an account that can authenticate at a maximum of AAL2, the CSP SHALL require the subscriber to complete one of the following: ^63b-4-2-2-2-1

### 63B §4.2.2.3 Recovery at AAL3

- **63B-4.2.2.3-1** SHALL — If an account that can authenticate at AAL3 has been identity-proofed at IAL3, the CSP SHALL successfully perform a successful biometric comparison against the biometric characteristic collected during an initial on-site attended identity proofing session, as described in [SP800-63A]. The CSP MAY also require the presentation of the evidence used in the initial identity proofing process. ^63b-4-2-2-3-1

### 63B §4.2.3 Account Recovery Notification

- **63B-4.2.3-1** SHALL — In all cases, account recovery SHALL cause a notification to be sent to the subscriber or their designee, as described in Sec. 4.6. ^63b-4-2-3-1

### 63B §4.3 Loss, Theft, Damage, and Compromise

- **63B-4.3-1** SHALL — The CSP SHALL suspend, invalidate, or destroy compromised authenticators from the subscriber’s account promptly following compromise detection. Organizations SHOULD establish time limits for this process. ^63b-4-3-1
- **63B-4.3-2** SHALL — To facilitate the secure reporting of an authenticator’s loss, theft, damage, or compromise, the CSP SHOULD provide the subscriber with a method of authenticating using a backup or alternate authenticator. This backup authenticator SHALL be a password or a physical authenticator. Either could be used, but only one authentication factor is required to make this report. Alternatively, the subscriber MAY establish an authenticated protected channel for the CSP to verify the information collected during identity proofing. The CSP MAY choose to verify a contact address (i.e., the email address, telephone number, or postal address) and suspend or invalidate authenticators that are reported to have been compromised. ^63b-4-3-2
- **63B-4.3-3** SHOULD — CSPs MAY support the temporary suspension of authenticators that are suspected of possible compromise. If suspension is supported, it SHOULD be reversed after the subscriber successfully authenticates to the CSP using a valid (i.e., not suspended) authenticator and requests reactivation of the suspended authenticator. The CSP MAY set a time limit after which a suspended authenticator can no longer be reactivated. ^63b-4-3-3

### 63B §4.4 Expiration

- **63B-4.4-1** SHALL NOT — CSPs MAY bind authenticators that expire to subscriber accounts. When an authenticator expires, it SHALL NOT be usable for authentication. When an authentication is attempted using an expired authenticator, the CSP SHOULD indicate to the subscriber that the authentication failure is due to expiration rather than some other cause. ^63b-4-4-1
- **63B-4.4-2** SHOULD — The CSP SHOULD retrieve any authenticator that contains personal information or provide for its erasure or destruction promptly following expiration. ^63b-4-4-2
- **63B-4.4-3** SHALL — The replacement of expired authenticators SHALL conform to the binding process for an additional authenticator, as described in Sec. 4.1.2. ^63b-4-4-3

### 63B §4.5 Invalidation

- **63B-4.5-1** SHALL — CSPs SHALL promptly invalidate authenticators when a subscriber account ceases to exist (e.g., subscriber’s death, the discovery of a fraudulent subscriber), when requested by the subscriber, when the authenticator is compromised, or when the CSP determines that the subscriber no longer meets its eligibility requirements. The CSP SHALL make a risk-based determination of the authenticity of invalidation requests from the subscriber. The consequences of not invalidating a compromised authenticator are usually more significant than the denial-of-service potential of invalidating one in error. ^63b-4-5-1
- **63B-4.5-2** SHOULD — The CSP SHOULD retrieve any authenticator that contains personal information or provide for its erasure or destruction promptly following invalidation. The CSP SHOULD notify the subscriber when an authenticator is invalidated, as described in Sec. 4.6. ^63b-4-5-2

### 63B §4.6 Account Notifications

- **63B-4.6-1** SHALL — Events that require notification SHALL cause a notification to be sent to the notification addresses stored in the subscriber account. Notification addresses may be any means by which the subscriber can be reliably contacted, such as: ^63b-4-6-1
- **63B-4.6-2** SHALL — CSPs SHALL support at least two notification addresses per subscriber account. For subscriber accounts that have undergone identity proofing, at least one address SHALL have been validated during the identity proofing process. The CSP SHOULD allow subscribers with authentication at AAL2 or higher (or at AAL1 if that is the highest AAL available for the subscriber account) to update their notification addresses. The CSP SHOULD encourage the subscriber to maintain multiple notification addresses to improve the likelihood of contacting them if a contact address changes. ^63b-4-6-2
- **63B-4.6-3** SHALL — Notifications SHALL be sent to all notification addresses except postal addresses. However, notifications SHALL be sent to postal addresses if no other form of notification address is stored in the subscriber account or if the notification is for account recovery at AAL3. Account recovery notifications SHALL also be sent to a postal address if the only other notification address in the subscriber account is the address to which an issued recovery code was sent. ^63b-4-6-3
- **63B-4.6-4** SHALL — The notification SHALL provide clear instructions, including contact information, in case the recipient repudiates the event associated with the notification. ^63b-4-6-4

### 63B §5 Session Management

- **63B-5-1** MAY — To facilitate this behavior, a session MAY be started in response to an authentication event and continue until it is terminated. The session MAY be terminated for any number of reasons, including an inactivity timeout or an explicit logout event. The session MAY be extended through a reauthentication event (see Sec. 5.2) in which the subscriber repeats some of the initial authentication process or performs a full authentication, thereby reestablishing the authenticated session. ^63b-5-1

### 63B §5.1 Session Bindings

- **63B-5.1-1** SHALL — A session occurs between the software (i.e., the session subject) that a subscriber is running (e.g., browser, application, operating system) and the RP or CSP that the subscriber is accessing (i.e., the session host). A session secret SHALL be shared between the subscriber’s software and the accessed service. This secret binds the two ends of the session and allows the subscriber to continue using the service over time. The secret SHALL be directly presented by the subscriber’s software, or possession of the secret SHALL be proven using a cryptographic mechanism. ^63b-5-1-1
- **63B-5.1-2** SHALL — The continuity of authenticated sessions SHALL be based on the possession of a session secret that is issued by the session host at the time of authentication and optionally refreshed during the session. The nature of a session depends on the application, such as: ^63b-5-1-2
- **63B-5.1-3** SHALL NOT — Session secrets that are used as bearer tokens for session management SHOULD NOT be persistent (i.e., retained across a restart of the associated application or a reboot of the host device) because they are tied to specific sessions that a restart or reboot would end. Cookies and similar “remember my browser” features SHALL NOT be used instead of authentication except as provided for reauthentication at AAL2 in Sec. 2.2.3 when the inactivity limit has been exceeded but the time limit has not. ^63b-5-1-3
- **63B-5.1-4** SHALL — Some technologies (e.g., the emerging device bound session credentials specification [DBSC]) mitigate the risk of theft of session secrets by using cryptographic protocols that prove the possession of a session secret rather than using them as bearer tokens. These technologies might additionally store and use these session secrets in protected keystores to reduce the risk of exfiltration by malware. Session secrets used with such proof of possession techniques MAY persist. However, RPs and CSPs SHALL ensure that the session lifetime limits described in Sec. 2.2.3 are enforced even when a knowledge of the session secret is demonstrated. ^63b-5-1-4
- **63B-5.1-5** SHALL NOT — The secret used for session binding SHALL be generated by the session host in direct response to an authentication event. A session SHOULD inherit the AAL properties of the authentication event that triggered its creation. A session MAY be considered at a lower AAL than the authentication event but SHALL NOT be considered at a higher AAL than the authentication event. ^63b-5-1-5
- **63B-5.1-6** SHALL — The secrets used for session binding SHALL meet all of the following requirements: ^63b-5-1-6
- **63B-5.1-7** SHOULD NOT — In addition, the secrets used for session binding SHOULD be erased on the subscriber endpoint when they log out or when the secret is deemed to have expired. They SHOULD NOT be placed in insecure locations (e.g., HTML5 Local Storage) due to the potential exposure of local storage to cross-site scripting (XSS) attacks. ^63b-5-1-7
- **63B-5.1-8** SHALL NOT — Following authentication, authenticated sessions SHALL NOT fall back to an insecure transport (e.g., from https to http). ^63b-5-1-8
- **63B-5.1-9** SHALL — POST/PUT content SHALL contain a session identifier that the RP SHALL verify to protect against cross-site request forgery (CSRF). ^63b-5-1-9
- **63B-5.1-10** SHOULD — Sessions SHOULD provide a readily accessible mechanism for subscribers to terminate (i.e., log off) their session when their interaction is complete. Session logoff gives the subscriber additional confidence and control over the security of their session, particularly if the endpoint might be accessible to others. ^63b-5-1-10

### 63B §5.1.1 Browser Cookies

- **63B-5.1.1-1** SHALL — SHALL be tagged to be accessible only on secure (i.e., HTTPS) sessions. ^63b-5-1-1-1
- **63B-5.1.1-2** SHALL — SHALL be accessible to the minimum practical hostnames and paths. ^63b-5-1-1-2
- **63B-5.1.1-3** SHOULD — SHOULD be tagged as inaccessible via JavaScript (i.e., HttpOnly). ^63b-5-1-1-3
- **63B-5.1.1-4** SHALL NOT — SHOULD be tagged to expire at or soon after the session’s validity period. This requirement is intended to limit the accumulation of cookies but SHALL NOT be relied upon to enforce session timeouts. ^63b-5-1-1-4
- **63B-5.1.1-5** SHOULD — SHOULD have the “__Host-“ prefix and set “Path=/”. ^63b-5-1-1-5
- **63B-5.1.1-6** SHOULD — SHOULD set “SameSite=Lax” or “SameSite=Strict”. ^63b-5-1-1-6
- **63B-5.1.1-7** SHALL NOT — SHOULD contain only an opaque string (e.g., a session identifier) and SHALL NOT contain cleartext personal information. ^63b-5-1-1-7

### 63B §5.1.2 Access Tokens

- **63B-5.1.2-1** SHALL NOT — An access token (e.g., OAuth [RFC6749]) is used to allow an application to access a set of services on a subscriber’s behalf following an authentication event. The RP SHALL NOT interpret the presence of an access token as an indicator of the subscriber’s presence in the absence of other signals. The access token and any associated refresh tokens could be valid long after the authentication session has ended and the subscriber has left the application. ^63b-5-1-2-1

### 63B §5.2 Reauthentication

- **63B-5.2-1** SHALL — The periodic reauthentication of sessions SHALL be performed to confirm the subscriber’s continued presence at an authenticated session (e.g., that the subscriber has not walked away without logging out). ^63b-5-2-1
- **63B-5.2-2** SHALL — Session management uses two types of timeouts. An overall timeout limits the duration of an authenticated session to a specific period following authentication or a previous reauthentication. An inactivity timeout terminates a session without activity from the subscriber for a specific period. For both types of timeouts, the RP MAY alert the subscriber that the session is about to be terminated and allow the subscriber to make the session active or reauthenticate as appropriate before the session expires. When either timeout expires, the session SHALL be terminated. Session activity SHALL reset the inactivity timeout, and successful reauthentication during a session SHALL reset both timeouts. ^63b-5-2-2
- **63B-5.2-3** SHALL — The overall and inactivity timeout expiration limits depend on several factors, including the AAL of the session, the environment in which the session is conducted (e.g., whether the subscriber is in a restricted area), the type of endpoint being used (e.g., mobile application, web-based), whether the endpoint is a managed device,1 and the nature of the application itself. The limits MAY also be extended when higher security session maintenance technologies (e.g., device-bound mechanisms) are used. Agencies SHALL establish and document the inactivity and overall time limits being enforced in a system security plan, such as that described in [SP800-39]. Detailed requirements for each AAL are given in Sec. 2.1.3, Sec. 2.2.3, and Sec. 2.3.3. ^63b-5-2-3
- **63B-5.2-4** SHALL — Consequently, when an RP session expires and the RP requires reauthentication, it is possible that the session at the IdP has not expired and that a new assertion could be generated from this session at the IdP without explicitly reauthenticating the subscriber. The IdP can communicate the time and details of the authentication event to the RP, but the RP SHALL be authoritative as to whether the reauthentication requirements have been met. Section 4.7 of [SP800-63C] provides additional details and requirements for session management within a federation context. ^63b-5-2-4

### 63B §5.3 Session Monitoring

- **63B-5.3-1** SHOULD — Session monitoring (sometimes called continuous authentication) is the ongoing evaluation of session characteristics to detect possible fraud during a session. Session monitoring MAY be performed by the RP in coordination with the CSP or IdP and associated verifier as a risk reduction measure. When potential fraud is detected during a session, the RP SHOULD act in conjunction with the CSP, IdP, or verifier to reauthenticate, terminate the session, or notify appropriate support personnel. Session characteristics that MAY be evaluated include: ^63b-5-3-1
- **63B-5.3-2** SHALL — Most of these characteristics have privacy implications. Collection, the storage of expected subscriber characteristics, and the processing of session characteristics SHALL be included in the privacy risk assessment described in Sec. 7. ^63b-5-3-2
- **63B-5.3-3** MAY — Session monitoring MAY be facilitated by the use of shared signaling between the RP and CSP or IdP, as described in [SP800-63C]. ^63b-5-3-3

### 63B §B.2 Cloning Authentication Keys

- **63B-B.2-1** SHALL — All keys SHALL be generated using approved cryptography. ^63b-b-2-1
- **63B-B.2-2** SHALL — Authentication keys that are cloned or exported from a device to a sync fabric SHALL only be stored in an encrypted form using a key with the minimum security strength specified in the latest revision of [SP800-131A] (i.e., 112 bits as of the date of this publication). These keys SHOULD be encrypted using a method that employs a user-controlled secret. ^63b-b-2-2
- **63B-B.2-3** SHALL — All authentication transactions SHALL perform private-key operations on the local device using cryptographic keys that are generated on-device or recovered from the sync fabric. ^63b-b-2-3
- **63B-B.2-4** SHALL — Authentication keys stored in the sync fabric SHALL be protected by access control mechanisms such that only the authenticated user can access their authentication keys in the sync fabric. ^63b-b-2-4
- **63B-B.2-5** SHALL — User access to authentication keys in the sync fabric SHALL be protected by AAL2-equivalent MFA to preserve the integrity of the authentication protocols using the synced keys. ^63b-b-2-5
- **63B-B.2-6** SHALL — These general requirements and any other agency-specific requirements for using syncable authenticators SHALL be documented and communicated, including on public-facing websites and digital service policies, where applicable. ^63b-b-2-6
- **63B-B.2-7** SHALL NOT — Authenticators that enable the use of syncable authentication keys SHOULD provide a user interface (UI) that allows subscribers to view the services for which they have created a syncable authentication key, whether that key has been synced, and where that key has been synced. The UI SHALL NOT expose the authentication key itself. ^63b-b-2-7
- **63B-B.2-8** SHALL — Federal enterprise authentication keys SHALL be stored in sync fabrics that have achieved Federal Information Security Modernization Act (FISMA) [FISMA] moderate protections or equivalent. ^63b-b-2-8
- **63B-B.2-9** SHALL — Devices (e.g., mobile phones, laptops, tablets) that generate, store, and sync authenticators containing federal enterprise authentication keys SHALL be protected by mobile device management software or other device configuration controls that prevent the syncing or sharing of keys to unauthorized devices or sync fabrics. ^63b-b-2-9
- **63B-B.2-10** SHALL — Access to the sync fabric SHALL be controlled by agency-managed accounts (e.g., a central identity and access management solution, platform-based managed account) to maintain federal enterprise control over the authentication key’s life cycle. ^63b-b-2-10
- **63B-B.2-11** SHOULD — Authenticators that generate authentication keys SHOULD support attestation features that can be used to verify the capabilities and sources of the authenticator (e.g., enterprise attestation). ^63b-b-2-11

### 63B §B.3 Implementation Requirements

- **63B-B.3-1** SHOULD — In addition to the flags specified above, agencies may wish to gain additional information on the origins and capabilities of the syncable authenticators that they choose to implement and accept. Within the context of WebAuthn, some authenticators support attestation features that can be used to determine the capabilities and manufacturers of specific authenticators. For federal enterprise use cases, agencies SHOULD implement attestation capabilities based on the functionality offered by their platform providers. This would take the form of a manufacturer attestation in which the RP requests identifying information about the authenticator. ^63b-b-3-1
- **63B-B.3-2** SHOULD NOT — The unavailability of attestations SHOULD NOT block the use of syncable authenticators for broad public-facing applications. Due to the limited availability of attestations in consumer products, requiring their use is likely to divert users to less secure authentication options that are vulnerable to phishing (e.g., PSTN-based out-of-band authentication). While authentication transaction metadata (e.g., the User Verified flag indicating the use of a local activation factor) is available in WebAuthn responses, attestation can provide stronger assurance of the characteristics of the authenticator used in a transaction. RPs SHOULD use attestation to determine the level of confidence they have in a syncable authenticator when attestations are available. ^63b-b-3-2
- **63B-B.3-3** SHALL — When the RP receives flag and attestation data, the authenticator may provide information that is incomplete or inconsistent with access to a resource. Agencies SHALL evaluate the use cases for syncable authenticators and determine the appropriate access policy decisions that they intend to make based on the returned information. ^63b-b-3-3

### 63B §B.5 Example

- **63B-B.5-1** SHOULD — If the subscriber provides their own authenticator, the verifier may have limited visibility into the features and capabilities of the sync fabric and the devices to which the user may sync their authentication keys. In this scenario, the verifier SHOULD leverage additional risk indicators or trust signals that may be available from the transaction, device, or sync fabric to increase confidence in the authentication event. ^63b-b-5-1

## SP 800-63C-4 Federation and Assertions

### 63C §1.1 Notations

- **63C-1.1-1** SHALL NOT — The terms “SHALL” and “SHALL NOT” indicate requirements to be followed strictly in order to conform to the publication and from which no deviation is permitted. ^63c-1-1-1
- **63C-1.1-2** SHOULD NOT — The terms “SHOULD” and “SHOULD NOT” indicate that among several possibilities, one is recommended as particularly suitable without mentioning or excluding others, that a certain course of action is preferred but not necessarily required, or that (in the negative form) a certain possibility or course of action is discouraged but not prohibited. ^63c-1-1-2
- **63C-1.1-3** MAY — The terms “MAY” and “NEED NOT” indicate a course of action permissible within the limits of the publication. ^63c-1-1-3

### 63C §2 Federation Assurance Level (FAL)

- **63C-2-1** SHALL — This section defines federation assurance levels (FALs) and the requirements for securing federation transactions at each FAL. In order to fulfill the requirements for a given FAL, the federation transaction SHALL meet or exceed all requirements listed for that FAL. ^63c-2-1

### 63C §2.1 Common FAL Requirements

- **63C-2.1-1** SHALL — At all FALs, all federation transactions SHALL comply with the requirements in Sec. 3 to deliver an assertion to the RP and create an authenticated session at the RP. Examples of assertions used in federation protocols include the ID Token in OpenID Connect [OIDC] and the Security Assertion Markup Language [SAML] Assertion format. ^63c-2-1-1
- **63C-2.1-2** SHALL — At all FALs, the RP SHALL validate the assertion from the IdP, since the RP needs to trust the IdP to provide valid assertions representing the subscriber’s authentication event. ^63c-2-1-2
- **63C-2.1-3** SHALL — All parties in the federation SHALL employ security controls, as discussed in Sec. 3.11. ^63c-2-1-3

### 63C §2.2 Federation Assurance Level 1 (FAL1)

- **63C-2.2-1** SHOULD — At FAL1, the federation protocol SHOULD apply assertion injection protection, as discussed in Sec. 3.11.1. The federation transaction SHOULD be initiated by the RP. ^63c-2-2-1
- **63C-2.2-2** SHALL — At FAL1, the IdP SHALL sign the assertion using approved cryptography. The RP SHALL validate the signature using the verification key associated with the expected IdP. The signature protects the integrity of the assertion contents and allows for the IdP to be verified as the source of the assertion. ^63c-2-2-2
- **63C-2.2-3** SHALL — At FAL1, the assertion SHALL be audience-restricted to a specific RP or set of RPs, and the RP SHALL validate that it is one of the targeted RPs for the given assertion. Each RP in the audience SHALL enforce replay protection mechanisms in the assertion to ensure that the same assertion is not accepted by a given RP multiple times. An assertion with multiple audiences could be accepted by multiple RPs but only once by each RP. ^63c-2-2-3
- **63C-2.2-4** SHOULD NOT — At FAL1, federated identifiers SHOULD NOT contain plaintext personal information, such as usernames, email addresses, employee numbers, etc. ^63c-2-2-4
- **63C-2.2-5** MAY — At FAL1, the trust agreement MAY be established by the subscriber during the federation transaction, as discussed in Sec. 4.3.2. Alternatively, the trust agreement MAY be established prior to the federation transaction (i.e., a “pre-established” trust agreement), as discussed in Sec. 4.3.1. ^63c-2-2-5

### 63C §2.3 Federation Assurance Level 2 (FAL2)

- **63C-2.3-1** SHALL — At FAL2, the assertion SHALL be strongly protected from assertion injection attacks, as discussed in Sec. 3.11.1. The federation transaction SHALL be initiated by the RP. ^63c-2-3-1
- **63C-2.3-2** SHALL — At FAL2, the assertion SHALL be audience restricted to a single RP. The RP SHALL enforce replay protection mechanisms in the assertion. ^63c-2-3-2
- **63C-2.3-3** SHALL NOT — At FAL2, federated identifiers SHALL NOT contain plaintext personal information, such as usernames, email addresses, employee numbers, etc. ^63c-2-3-3
- **63C-2.3-4** SHALL — At FAL2, a trust agreement SHALL be established prior to the federation transaction taking place (i.e., a “pre-established” trust agreement), as discussed in Sec. 4.3.1. ^63c-2-3-4
- **63C-2.3-5** SHALL — IdPs operated by or on behalf of federal agencies that present assertions at FAL2 or higher SHALL protect signing keys that are used in the generation of assertions with mechanisms validated at [FIPS140] Level 1 or higher. ^63c-2-3-5

### 63C §2.4 Federation Assurance Level 3 (FAL3)

- **63C-2.4-1** SHALL — At FAL3, the RP SHALL verify that the subscriber is in control of an authenticator in addition to the assertion. This authenticator is either identified in a holder-of-key assertion (see Sec. 3.15) or is a bound authenticator (see Sec. 3.16). ^63c-2-4-1
- **63C-2.4-2** SHALL — At FAL3, a trust agreement SHALL be established prior to the federation transaction taking place (i.e., a “pre-established” trust agreement), as discussed in Sec. 4.3.1. ^63c-2-4-2
- **63C-2.4-3** SHALL — At FAL3, the identifiers for the CSP, IdP, and RP SHALL be established manually. Each identifier SHALL be uniquely associated with the verification keys for the party represented. Verification keys SHALL be transmitted through a trusted mechanism, which could be manual or automated, as indicated in the trust agreement. For example, a public-key certificate that represents the RP is uploaded to the IdP during a manual registration process. The RP is manually configured with a URL that it can use to download the IdP’s public key. Alternatively, the IdP and RP could each upload their respective public keys to a federation authority and then download each other’s keys from that same location. For a subscriber-controlled wallet, the RP could be manually configured with the URL that represents the CSP’s public key. The RP fetches this public key and uses it to validate the signature of the attribute bundle presented by the subscriber-controlled wallet. See Sec. 3.6 for more information on the establishment, management, rotation, and revocation of keys and their association with identifiers. ^63c-2-4-3

### 63C §2.5 Requesting and Processing xALs

- **63C-2.5-1** SHALL — IdPs SHALL support a mechanism for RPs to specify a set of minimum acceptable xALs as part of the trust agreement and SHOULD support the RP specifying a more strict minimum set at runtime as part of the federation transaction. When an RP requests a particular xAL, the IdP SHOULD fulfill that request, if possible, or SHOULD fail the request if it cannot fulfil the RP’s requested xALs. The IdP SHALL always indicate the resulting xAL in the assertion, even if the request has not been met. For example, if the subscriber has an active session that was authenticated at AAL1, but the RP has requested AAL2, the IdP needs to prompt the subscriber for AAL2 authentication to increase the security of the session at the IdP during the subscriber’s interaction at the IdP, if possible. The IdP sends the resulting AAL as part of the returned assertion, whether it is AAL1 (i.e., the step-up authentication request was not met) or AAL2 (i.e., the step-up authentication request was met successfully). ^63c-2-5-1
- **63C-2.5-2** SHALL — The IdP SHALL inform the RP of the following information for each federation transaction: ^63c-2-5-2
- **63C-2.5-3** SHALL — The RP obtains this xAL information from a combination of the terms of the trust agreement (see Sec. 3.5) and information included in the assertion (see Sec. 4.9 and Sec. 5.8). If the xAL is unchanging for all messages between the IdP and RP (e.g., enterprise scenarios in which all subscribers are identity-proofed at the same IAL and use the same authenticator type), the xAL information SHALL be included in the terms of the trust agreement between the IdP and RP. If the xAL could be within a range of possible values specified by the trust agreement, then sufficient information SHALL be included as part of the assertion contents to allow the RP to determine the xALs. ^63c-2-5-3
- **63C-2.5-4** MAY — The IdP MAY indicate that no claim is made to the IAL or AAL for a given federation transaction. In such cases, no default value is assigned to the resulting xAL by the RP. That is, a federation transaction without an IAL declaration in either the trust agreement or the assertion is functionally considered to have “no IAL” and the RP cannot assume the account meets “IAL1,” which is the lowest numbered IAL described in this suite. ^63c-2-5-4
- **63C-2.5-5** SHALL — The RP SHALL determine the minimum IAL, AAL, and FAL that it is willing to accept for access to any offered functionality and assess all IdP assertions to ensure that these xALs have been met before granting access to protected resources. If IdP responses do not meet the requested parameters, the RP SHALL have a mechanism for addressing these requests (e.g., declining the request or routing the user to an exception handling process). The RP MAY vary its functionality based on the IAL, AAL, and FAL of a specific federated authentication. For example, an RP can allow federation transactions authenticated at AAL2 for common functionality (e.g., viewing the status of a dam system) but require AAL3 to be used for higher risk functionality (e.g., changing the flow rates of a dam system). Similarly, an RP could restrict high-risk functionality (e.g., accessing sensitive information) to only certain subscriber accounts that have been identity-proofed at IAL2 while allowing basic functionality for all subscriber accounts, regardless of IAL. ^63c-2-5-5
- **63C-2.5-6** SHALL — In a federation process, the RP does not have direct access to the details of the subscriber account that have been provided to the IdP by the CSP, which details determine the IAL for the subscriber account. Additionally, since the RP does not participate in the authentication event or activation event at the IdP, the RP cannot determine the AAL. The RP sees many aspects of the federation transaction that determine the FAL, but the IdP also has its own responsibilities related to FAL, including signaling the IdP’s intended FAL of the federation transaction to the RP. Consequently, the IdP SHALL provide the RP with sufficient information to determine the IAL, AAL, and the IdP’s intended FAL for each federation transaction. This MAY be done in the assertions, through previous arrangement in the trust agreement, or a combination of both. ^63c-2-5-6
- **63C-2.5-7** SHALL — The RP SHALL ensure that it meets its obligations in the federation transaction for the FAL declared in the transaction. For example, the RP needs to ensure that the presentation method meets the assertion injection protection requirements at FAL2 and above and that the appropriate holder-of-key proof or bound authenticator is presented at FAL3. ^63c-2-5-7

### 63C §3.3.3 Proxied Federation

- **63C-3.3.3-1** SHALL — In some architectures, the IdP and RP do not communicate directly with each other. A federation proxy acts as an intermediary between the IdP and RP for all communication in the federation protocol. The proxy functions as an RP on the upstream side and an IdP on the downstream side, as shown in Fig. 1. When communicating through a proxy, the upstream IdP and downstream RP communicate with the proxy using a standard federation protocol, and the subscriber takes part in two separate federation transactions. As a consequence, all normative requirements that apply to IdPs and RPs SHALL apply to proxies in their respective roles on each side. Additionally, a proxy can act as an upstream IdP to a downstream proxy in a chaining scenario. ^63c-3-3-3-1
- **63C-3.3.3-2** SHALL — The federated identifier (see Sec. 3.4) of an assertion from a proxy SHALL indicate the proxy as the issuer of the assertion. ^63c-3-3-3-2
- **63C-3.3.3-3** SHALL — The FAL of the connection between the proxy and the downstream RP is considered to be the lowest FAL along the entire path, and the proxy SHALL accurately represent this to the downstream RP. For example, if the connection between the upstream IdP and the proxy is FAL1 and the connection between the proxy and the downstream RP otherwise meets the requirements of FAL2, the connection between the proxy and the downstream RP is still considered FAL1. Likewise, if the connection between the upstream IdP and the proxy is FAL2 and the connection between the proxy and the downstream RP is only FAL1, the overall connection through the proxy is considered FAL1. ^63c-3-3-3-3

### 63C §3.4 Federated Identifiers

- **63C-3.4-1** SHALL — When federated identifiers are used, the federated identifier SHALL be unique to that subscriber. Federated identifiers SHALL be associated with a single subscriber at the RP. ^63c-3-4-1

### 63C §3.4.1.1 General Requirements

- **63C-3.4.1.1-1** SHALL — When using pairwise pseudonymous identifiers within the assertions generated by the IdP for the RP, the IdP SHALL generate a different federated identifier for each RP (see Sec. 3.4.1.2) or set of RPs (see Sec. 3.4.1.3). ^63c-3-4-1-1-1
- **63C-3.4.1.1-2** SHALL — Some identity attributes such as names, physical addresses, phone numbers, email addresses, and others can be used to identify a subscriber outside of a federation transaction. When PPIs are used alongside these kinds of identifying attributes, it may still be possible for multiple colluding RPs to re-identify a subscriber by correlation across systems. For example, if two independent RPs each see the same subscriber identified with a different PPI, the RPs could still determine that the subscriber is the same person by comparing the name, email address, physical address, or other identifying attributes carried alongside the PPI in the respective assertions. If PPIs are used alongside identifying attributes, RPs SHALL establish privacy policies, processes, and procedures to prevent the correlation of subscriber data consistent with applicable legal and regulatory requirements. ^63c-3-4-1-1-2
- **63C-3.4.1.1-3** SHALL — In a proxied federation model (see Sec. 3.3.3), the upstream IdP may not be able to generate a PPI for the downstream RP, since the proxy could blind the IdP from knowing which RP is being accessed by the subscriber. In such situations, the PPI is generally established between the IdP and the federation proxy. Acting as an IdP, the proxy can provide a PPI to the downstream RP. Depending on the protocol, the federation proxy may need to map the PPI back to the associated identifiers from upstream IdPs in order to allow the identity protocol to function. In such cases, the proxy will be able to track and determine which PPIs represent the same subscriber at different RPs. The mapping of a PPI to other identifiers is considered subscriber information and SHALL be treated in accordance with the requirements in Sec. 3.10.1. ^63c-3-4-1-1-3

### 63C §3.4.1.2 Pairwise Pseudonymous Identifier Generation

- **63C-3.4.1.2-1** SHALL — The PPI SHALL contain no identifying information about the subscriber (e.g., username, email address, employee number). The PPI SHALL be difficult to guess by a party with access to information about the subscriber and SHALL provide sufficient entropy as to be unguessable by an attacker. PPIs can be generated randomly and assigned to subscribers by the IdP or derived from other subscriber information if the derivation is done in an irreversible, unguessable manner (e.g., using a keyed hash function with a secret key, as discussed in [SP800-131A]). ^63c-3-4-1-2-1
- **63C-3.4.1.2-2** SHALL — Unless the PPI is designated as shared by the trust agreement, the PPI SHALL be disclosed to only a single RP. ^63c-3-4-1-2-2

### 63C §3.4.1.3 Shared Pairwise Pseudonymous Identifiers

- **63C-3.4.1.3-1** SHALL — The same shared PPI SHALL be used for a specific set of RPs if all of the following criteria are met: ^63c-3-4-1-3-1
- **63C-3.4.1.3-2** SHALL — The RPs SHALL conduct a privacy risk assessment to consider the privacy risks associated with requesting a shared PPI. See Sec. 7.2 for further privacy considerations. ^63c-3-4-1-3-2
- **63C-3.4.1.3-3** SHALL — The IdP SHALL ensure that only intended RPs are included in the set. Otherwise, a rogue RP could learn the shared PPI for a set of RPs by fraudulently posing as part of that set. ^63c-3-4-1-3-3

### 63C §3.5 Trust Agreements

- **63C-3.5-1** SHALL — Trust agreements are a construct that represent the set of trust relationships established to support parties in a federation transaction. A trust agreement SHALL address one or more of the following relationships: ^63c-3-5-1
- **63C-3.5-2** SHALL — All federation transactions SHALL be governed by the terms of one or more trust agreements between the applicable parties. Different relationships MAY be established at different times and by different processes. For example, a CSP and IdP entering into a trust agreement is generally separate from an RP and IdP entering into a trust agreement, but the overall set of terms for a federation transaction under these parties is drawn from both sets of relationships. ^63c-3-5-2
- **63C-3.5-3** SHALL — Trust agreements establish the terms for federation transactions between the parties they affect, including the allowed xALs and the intended purposes of identity attributes exchanged in the federation transaction. The trust agreement SHALL establish customer experience requirements for the federation transaction, as discussed in Sec. 8. The trust agreement SHALL include details of the proofing process used at the CSP for subscribers covered by the trust agreement, including any compensating controls and exception handling processes. ^63c-3-5-3
- **63C-3.5-4** SHALL — All trust agreements SHALL define a specific population of subscriber accounts to which the agreement is applicable. The exact means of defining this population are out of scope for this document. In many cases, the population is defined as the full set of subscriber accounts that the CSP manages and makes available through an IdP. In other cases, the population is a demarcated subset of accounts that are available through an IdP. It is also possible for an RP to have a distinct trust agreement established with an IdP for a single subscriber account, such as in a subscriber-driven trust agreement. ^63c-3-5-4
- **63C-3.5-5** SHALL — During the course of a single federation transaction, it is important for the policies and expectations of all parties to be unambiguous. Therefore, there SHOULD only be one set of trust agreements in effect for a given transaction. This will usually be determined by the unique combination of CSP, IdP, and RP that are participating in the transaction. However, these agreements could vary in other ways, such as different populations of subscribers being governed by different trust agreements. If more than one trust agreement is applicable to a federation transaction, the combined set of terms of all applicable trust agreements SHALL constitute the effective trust agreement of that transaction. ^63c-3-5-5
- **63C-3.5-6** SHALL — Trust agreements SHALL establish terms regarding expected and acceptable IALs, AALs, and FALs in connection with the federated relationship. ^63c-3-5-6
- **63C-3.5-7** SHALL — Trust agreements SHALL define necessary mechanisms and materials to coordinate redress and issues between the different participants in the federation, as discussed in Sec. 3.5.3. ^63c-3-5-7
- **63C-3.5-8** SHALL — Trust agreements SHALL declare the data retention policies expected of all parties. ^63c-3-5-8
- **63C-3.5-9** SHALL — Even though subscribers are not generally directly involved in the trust agreement’s terms, subscribers are affected by the terms of the trust agreement and the resulting federation transactions. As such, the relevant terms of the trust agreement SHALL be made available to subscribers in clear and understandable language. The terms of the trust agreement SHALL be reviewed by all parties (e.g., the CSP, IdP, RP, or a federation authority) that are responsible for informing the subscriber of the terms of the trust agreement before the disclosure to the subscriber occurs in order to avoid revealing sensitive security information. ^63c-3-5-9

### 63C §3.5.2 Multilateral Trust Agreements

- **63C-3.5.2-1** SHALL — The trust agreement SHALL enumerate the required practices for vetting all parties and SHALL indicate the party or parties that are responsible for performing the vetting process. ^63c-3-5-2-1
- **63C-3.5.2-2** SHALL — At a minimum, the vetting of CSPs, IdPs, and RPs SHALL establish that: ^63c-3-5-2-2
- **63C-3.5.2-3** MAY — The federation authority MAY provide a programmatic means for parties under the trust agreement to verify the membership of other parties in the trust agreement. For example, a federation authority could provide a discovery API that provides the vetted capabilities of an IdP for providing identities to RPs within the system. Alternatively, the federation authority could provide a signed attestation for RPs to present to IdPs during a registration step. ^63c-3-5-2-3
- **63C-3.5.2-4** SHALL — Federation authorities SHALL periodically reevaluate members for compliance with terms disclosed in the trust agreement. ^63c-3-5-2-4
- **63C-3.5.2-5** MAY — A multilateral trust agreement MAY establish trust based on other trust agreements that are managed by other entities by creating an interfederation agreement. For example, IdP1 has been vetted under a multilateral agreement with federation authority A1, and RP2 has been vetted under a multilateral agreement with federation authority A2. In order to facilitate connection between IdP1 and RP2, a new federation authority A3 can provide a multilateral agreement that accepts IdPs from A1 and RPs from A2. If IdP1 and RP2 accept the authority of A3, the federation connection can continue under the auspices of this interfederation agreement. ^63c-3-5-2-5

### 63C §3.5.3 Redress Requirements

- **63C-3.5.3-1** SHALL — As the recipient of a subscriber’s identity attributes, the RP is the subscriber’s primary view into the federated system. In some instances, the subscriber may be unaware that an IdP is involved with their use of the RP. Therefore, it falls to the RP to provide the subscriber with a clear and accessible method of contacting the RP to request redress. For matters that involve the RP subscriber account (including any attributes stored in the account), RP functionality, bound authenticators, RP allowlists, and other items under the RP’s control, the RP SHALL provide a clear and accessible means of redress to the subscriber. For matters that involve the IdP or CSP, the RP SHALL provide the subscriber with a means of initiating the redress process with the IdP or CSP, as appropriate. ^63c-3-5-3-1
- **63C-3.5.3-2** SHALL — For matters that involve the use of the subscriber account in federation transactions, including attribute values and derived attribute values made available over federation transactions, IdP functionality, holder-of-key authenticators, IdP allowlists, and other items in the IdP’s control, the IdP SHALL provide a clear and accessible means of redress to the subscriber. For matters that also involve a particular RP, the IdP SHALL provide the subscriber with a means of initiating the redress process with the RP. For matters that involve a subscriber account that has been made available to the IdP, the IdP SHALL provide the subscriber with a means of initiating the redress process with the CSP. ^63c-3-5-3-2
- **63C-3.5.3-3** SHALL — For matters that involve the subscriber account, including identity attributes and authenticators in the subscriber account, the CSP SHALL provide the subscriber with a clear and accessible means of redress. ^63c-3-5-3-3

### 63C §3.6 Identifiers and Cryptographic Key Management for CSPs, IdPs, and RPs

- **63C-3.6-1** SHALL — The discovery and registration processes SHALL be established in a secure fashion, as defined by the trust agreement that governs the federation transaction. In many cases, the identifier is associated with a trusted source of cryptographic key material and not the key material itself. For example, a URL hosted by an IdP can serve the public signing keys for that IdP. Even if the RP is manually configured with this association, the RP can fetch the actual cryptographic key material at runtime. Protocols that require the transfer of cryptographic key information SHALL use an authenticated protected channel to exchange the cryptographic key information needed to operate the federated relationship, including any shared secrets or public keys. Any symmetric keys used in this relationship SHALL be unique to a pair of federation participants. ^63c-3-6-1
- **63C-3.6-2** MAY — CSPs, IdPs (including subscriber-controlled wallets), and RPs MAY have multiple identifiers and cryptographic keys to serve different purposes within a trust agreement or different trust agreements. For example, an IdP could use one set of assertion signing keys for all FAL1 and FAL2 transactions and use a separately managed set of signing keys for FAL3 transactions that are stored in a higher security container. ^63c-3-6-2
- **63C-3.6-3** SHALL NOT — When domain names, URIs, or other structured identifiers are used to identify parties, wildcards SHALL NOT be used. For example, if an RP is deployed at “www.example.com”, “service.example.com”, and “gateway.example.com”, then each of these identifiers would have to be registered for the RP. A wildcard of “*.example.com” cannot be used, as it would unintentionally allow access to “user.example.com” and “unknown.example.com” under the same RP identifier. ^63c-3-6-3

### 63C §3.6.1 Cryptographic Key Rotation

- **63C-3.6.1-1** SHALL — Over time, it can be desirable or necessary to update the cryptographic key associated with a CSP, IdP, or RP. The allowable update process for any identifiers and cryptographic keys SHALL be defined by the trust agreement and SHALL be executed using an authenticated protected channel, as in the initial cryptographic key establishment. ^63c-3-6-1-1

### 63C §3.6.2 Cryptographic Key Storage

- **63C-3.6.2-1** SHALL — CSPs, IdPs (including subscriber-controlled wallets), and RPs SHALL store all signing keys, decryption keys, and symmetric keys in a secure fashion. Cryptographic key storage is subject to applicable [FIPS140] requirements, including applicable tamper resistance requirements. ^63c-3-6-2-1
- **63C-3.6.2-2** SHALL NOT — Some circumstances require the cryptographic keys to be stored in a non-exportable manner, such as reaching FAL3 with a subscriber-controlled wallet on a subscriber’s device (see Sec. 5.4.1). To be considered non-exportable, key storage SHALL either be a separate piece of hardware or an embedded processor or execution environment, such as a secure element, trusted execution environment (TEE), or trusted platform module (TPM). These hardware modules or embedded processors are separate from a host processor, such as the CPU on a laptop or mobile device. Non-exportable key storage SHALL be designed to prohibit the export of the secret keys to the host processor and SHALL NOT be capable of being reprogrammed by the host processor to allow the secret keys to be extracted. ^63c-3-6-2-2

### 63C §3.6.3 Software Attestations

- **63C-3.6.3-1** SHALL — When attestations are required by the trust agreement or requested as part of the federation protocol, received attestations SHALL be validated by the receiver. ^63c-3-6-3-1

### 63C §3.7 Authentication and Attribute Disclosure

- **63C-3.7-1** SHALL — A subscriber’s identity attributes SHALL only be transmitted between the IdP and the RP for federation transactions or support functions, such as identification of compromised subscriber accounts (see Sec. 3.10.1), even when parties are allowlisted for federation purposes. ^63c-3-7-1
- **63C-3.7-2** SHALL NOT — A subscriber’s identity attributes SHALL NOT be used by the RP for purposes other than those stipulated in the trust agreement unless the subscriber specifically consents to such purposes. A subscriber’s attributes SHALL be stored and managed in accordance with Sec. 3.11.3. ^63c-3-7-2
- **63C-3.7-3** SHALL — The subscriber SHALL be informed of the transmission of attributes to an RP. If the authorized party is the organization, the organization SHALL make the list of approved RPs and the associated sets of attributes sent to those RPs available to the subscriber. If the authorized party is the subscriber, the subscriber SHALL be prompted prior to the release of attributes using a runtime decision at the IdP, as described in Sec. 4.6.1.3. ^63c-3-7-3

### 63C §3.8 RP Subscriber Accounts

- **63C-3.8-1** MAY — An RP subscriber account is provisioned when the RP has associated a set of attributes about the subscriber with a data record that represents the subscriber account at the RP. The provisioning can happen prior to authentication or as a result of the federated authentication process, depending on the deployment patterns (see Sec. 4.6.3). The RP subscriber account MAY be associated with one or more federated identifiers at the time of provisioning or MAY be later linked to federated identifiers through account resolution, as discussed in Sec. 3.8.2. ^63c-3-8-1
- **63C-3.8-2** SHALL — An RP subscriber account is terminated when the RP removes all access to the account at the RP. Termination SHALL include the removal of all federated identifiers, bound authenticators, attributes, and identity information associated with the account, in accordance with Sec. 3.11.3. An RP MAY terminate an RP subscriber account independently from the IdP, regardless of the current validity of the subscriber account from which it is derived. ^63c-3-8-2
- **63C-3.8-3** MAY — An RP MAY offer a means of recovery of an RP subscriber account with no current means of access. ^63c-3-8-3
- **63C-3.8-4** SHALL — The RP SHALL document the practices and policies that it enacts when an RP subscriber account reaches a state of having zero associated federated identifiers; no means of access, including alternative authenticators (see Sec. 3.8.3); and no means of recovery, including account linking (see Sec. 3.8.1) and account resolution (see Sec. 3.8.2). In such cases, the RP subscriber account SHOULD be disabled or terminated. ^63c-3-8-4
- **63C-3.8-5** SHALL — The RP SHALL provide a notice to the subscriber when: ^63c-3-8-5
- **63C-3.8-6** SHALL — The RP SHOULD provide a notice to the subscriber when the RP subscriber account is disabled or terminated. The RP SHALL consider the reason for termination when determining whether to send a notice to the subscriber, as discussed in Sec. 5.4 of [SP800-63A]. ^63c-3-8-6

### 63C §3.8.1 Account Linking

- **63C-3.8.1-1** SHALL — A single RP subscriber account MAY be associated with more than one federated identifier. This practice is sometimes known as account linking. If the RP allows a subscriber to link multiple subscriber accounts in this way, the RP SHALL require an authenticated session with the subscriber account for all linking functions. This authenticated session SHOULD require authentication using one existing federated identifier before linking the new federated identifier to the RP subscriber account. ^63c-3-8-1-1
- **63C-3.8.1-2** SHALL — When a federated identifier is removed from an RP subscriber account, the RP SHALL disallow access to the RP subscriber account from the removed federated identifier. ^63c-3-8-1-2
- **63C-3.8.1-3** MAY — The RP MAY associate different access rights with the same account, depending on which federated account is used to access the RP. The means by which an RP determines authorization and access is out of scope for these guidelines. ^63c-3-8-1-3

### 63C §3.8.2 Account Resolution

- **63C-3.8.2-1** SHALL — An RP that performs account resolution SHALL ensure that the attributes requested from the IdP are sufficient to uniquely resolve the subscriber within the RP’s system before linking the federated identifier with the RP subscriber account and granting access. The intended use of each attribute by the RP is detailed in the trust agreement, including whether the attribute is used for account resolution in this manner. ^63c-3-8-2-1
- **63C-3.8.2-2** SHALL — An RP that performs account resolution SHALL design the process such that it does not associate an RP subscriber account’s information with a federated identifier that does not belong to the subscriber. ^63c-3-8-2-2
- **63C-3.8.2-3** SHALL — A similar account resolution process is also used when the RP verifies an authenticator used in a holder-of-key assertion for the first time. In this case, the RP SHALL ensure that the attributes carried with the authenticator uniquely resolve to the RP subscriber account before accepting the authenticator. ^63c-3-8-2-3

### 63C §3.8.3 Alternative Authentication Processes

- **63C-3.8.3-1** SHALL — The RP MAY allow a subscriber to access their RP subscriber account using direct authentication processes by allowing the subscriber to add and remove authenticators in the RP subscriber account. The RP SHALL follow the requirements in [SP800-63B] to manage all alternative authenticators. ^63c-3-8-3-1
- **63C-3.8.3-2** SHOULD — If the RP allows this kind of access, the RP SHOULD disclose the following in the trust agreement to allow IdPs to make decisions regarding information shared with the RP: ^63c-3-8-3-2
- **63C-3.8.3-3** SHALL — While it is possible for bound authenticators (see Sec. 3.16) to be used as an alternative authenticator for direct access to the RP, these uses are distinct from each other and an RP SHALL determine whether a given authenticator can be used in one or both scenarios. ^63c-3-8-3-3

### 63C §3.9 Authenticated Sessions at the RP

- **63C-3.9-1** SHALL — The ultimate goal of a federation transaction is to create an authenticated session between the subscriber and the RP that is backed by a verified assertion from the IdP. This authenticated session can be used for allowing the subscriber access to functions at the RP (i.e., logging in), identifying the subscriber to the RP, or processing attributes about the subscriber carried in the federation transaction. An authenticated session SHALL be created by the RP only when the following conditions are true: ^63c-3-9-1
- **63C-3.9-2** SHALL — If the assertion is a holder-of-key assertion at FAL3, the authenticator indicated in the assertion SHALL be verified before the RP subscriber account is associated with an authenticated session, as discussed in Sec. 3.15. If the assertion also requires authentication with a bound authenticator at FAL3, a bound authenticator SHALL be verified before the RP subscriber account is associated with an authenticated session, as discussed in Sec. 3.16. ^63c-3-9-2
- **63C-3.9-3** MAY — The authenticated session MAY be ended by the RP at any time. ^63c-3-9-3

### 63C §3.10 Privacy Requirements

- **63C-3.10-1** SHOULD — If the same subscriber account is asserted to multiple RPs, and those RPs communicate with each other, the colluding RPs could track a subscriber’s activity across multiple applications and security domains. The IdP SHOULD employ technical measures (e.g., the use of pairwise pseudonymous identifiers described in Sec. 3.4.1, privacy-enhancing cryptographic protocols) to provide disassociability and discourage subscriber activity tracking and profiling between RPs. When determining such measures, the IdP SHOULD apply relevant guidelines and standards, such as the NIST Privacy Framework [NIST-Privacy]. ^63c-3-10-1
- **63C-3.10-2** SHALL — The agency SHALL consult with their Senior Agency Official for Privacy (SAOP) to conduct an analysis that determines whether the requirements of the Privacy Act are triggered by the agency that is acting as an IdP, by the agency that is acting as an RP, or both (see Sec. 7.4). ^63c-3-10-2
- **63C-3.10-3** SHALL — The agency SHALL publish or identify coverage by a System of Records Notice (SORN), as applicable. ^63c-3-10-3
- **63C-3.10-4** SHALL — The agency SHALL consult with their SAOP to conduct an analysis that determines whether the requirements of the E-Government Act are triggered by the agency that is acting as an IdP, the agency that is acting as an RP, or both. ^63c-3-10-4
- **63C-3.10-5** SHALL — The agency SHALL publish or identify coverage by a Privacy Impact Assessment (PIA), as applicable. ^63c-3-10-5
- **63C-3.10-6** SHALL — The agency SHALL conduct a privacy risk assessment regarding the sharing of subscriber identity information between the IdP and RP. ^63c-3-10-6
- **63C-3.10-7** SHALL — If the RP subscriber account life cycle process gives the RP access to attributes through a provisioning API (see Sec. 4.6.3), additional privacy measures SHALL be implemented to account for the difference in the RP subscriber account life cycle (e.g., separation of non-active subscriber accounts, proactive removal of disabled and terminated accounts). The IdP SHALL minimize the attributes that are made available to the RP through the provisioning API. The IdP SHALL limit the population of subscriber accounts that are available via the provisioning API to the population of subscribers authorized to use the RP by the trust agreement. To prevent RP retention of identity attributes for accounts that have been terminated at the IdP, the IdP SHALL use the provisioning API to de-provision RP subscriber accounts for terminated subscriber accounts except where restricted by RP data retention requirements, policies, or regulation. This measure helps enforce data minimization principles (see the example in Sec. 9.5). When an RP subscriber account is linked to multiple federated identifiers (see Sec. 3.8.1), the de-provisioning process could result in the RP subscriber account still existing at the RP but linked to a different federated identifier. ^63c-3-10-7
- **63C-3.10-8** SHALL — The IdP and RP SHALL exchange only the minimum data necessary to achieve the function of the system. ^63c-3-10-8
- **63C-3.10-9** SHOULD — To increase subscriber control over the release of their identity attributes, trust agreements SHOULD use a runtime decision to control attribute release, as discussed in Sec. 4.6.1.3. ^63c-3-10-9
- **63C-3.10-10** SHOULD — When the federation transaction uses an ephemeral provisioning mechanism (see Sec. 4.6.3), the IdP SHOULD use an ephemeral federated identifier for each authorization request to the RP to prevent the RP from storing or correlating information between sessions. ^63c-3-10-10

### 63C §3.10.1 Transmitting Subscriber Information

- **63C-3.10.1-1** SHALL — The IdP SHALL limit the transmission of subscriber information to only that which is necessary for the system to function and is stipulated and disclosed by the trust agreement. These functions include the following: ^63c-3-10-1-1
- **63C-3.10.1-2** SHALL NOT — If an IdP discloses information on subscriber activities at an RP to any party or processes the subscriber’s attributes for any purpose other than these cases, the IdP SHALL implement measures to maintain predictability and manageability commensurate with the privacy risks that arise from the additional processing. Measures MAY include providing clear notice, obtaining subscriber consent, or enabling the selective use or disclosure of attributes. When an IdP gathers the subscriber’s consent to use information outside the identity transaction, the IdP SHALL NOT make consent for the additional processing a condition of the identity service. For example, an IdP cannot require a subscriber to consent to receiving a newsletter in order to allow the subscriber to log into an RP. ^63c-3-10-1-2
- **63C-3.10.1-3** SHALL — An RP SHALL limit the transmission of subscriber activities to the associated IdP to the following cases and only if stipulated and disclosed by the trust agreement: ^63c-3-10-1-3
- **63C-3.10.1-4** SHALL — If an RP uses the subscriber’s identity information for any purpose other than those stipulated in the trust agreement, the RP SHALL inform the subscriber and obtain their consent for such additional uses. ^63c-3-10-1-4

### 63C §3.10.2 Sharing Information Between CSPs

- **63C-3.10.2-1** SHALL — All information transmissions between CSPs and/or IdPs SHALL be subject to the limitations for IdPs enumerated in Sec. 3.10.1. Any such information sharing between CSPs and/or IdPs SHALL be included in their privacy risk assessments. ^63c-3-10-2-1
- **63C-3.10.2-2** SHALL — The terms of the trust agreement that connects CSPs SHALL define the policies that apply for the transfer of information shared between CSPs. In a trust agreement managed by a federation authority, the federation authority defines these terms. ^63c-3-10-2-2

### 63C §3.11 Security Controls

- **63C-3.11-1** SHALL — IdPs and CSPs SHALL employ appropriately tailored security controls from at least the moderate baseline security controls defined in [SP800-53] or an equivalent federal (e.g., [FEDRAMP]) or industry standard that the organization has determined for the information systems, applications, and online services that these guidelines are used to protect. RPs SHALL employ appropriately tailored security controls from at least the low baseline security controls defined in [SP800-53] or an equivalent federal (e.g., [FEDRAMP]) or industry standard that the organization has determined for the information systems, applications, and online services that these guidelines are used to protect. RPs that request or process personal information SHALL employ appropriately tailored security controls from at least the moderate baseline security controls defined in [SP800-53] or an equivalent federal (e.g., [FEDRAMP]) or industry standard. CSPs, IdPs, and RPs SHALL ensure that the minimum assurance-related controls for the appropriate systems or equivalent are satisfied or exceeded. ^63c-3-11-1

### 63C §3.11.2 Protecting Subscriber Information

- **63C-3.11.2-1** SHALL — Communications between the IdP and the RP SHALL be protected in transit using an authenticated protected channel. Communications between the subscriber and either the IdP or the RP (usually through a user agent) SHALL be made using an authenticated protected channel. ^63c-3-11-2-1
- **63C-3.11.2-2** MAY — The IdP may have access to information that may be useful to the RP in enforcing security policies, such as device identity, location, system health checks, and configuration management. The IdP MAY disclose this information to the RP within the bounds of the trust agreement and subject to the subscriber’s notice and consent, as described in Sec. 7.2. ^63c-3-11-2-2
- **63C-3.11.2-3** SHALL — Identity attributes MAY be included outside of the assertion itself by authorizing access to an identity API, as discussed in Sec. 3.12.3. Splitting identity information in this manner can help protect subscriber privacy and can allow for the limited disclosure of personal information in addition to the essential information in the authentication assertion itself. The use of identity APIs SHALL be enumerated in the terms of the trust agreement. ^63c-3-11-2-3
- **63C-3.11.2-4** SHOULD — When derived attribute values are available and fulfill the RP’s needs, the RP SHOULD request derived attribute values rather than full attribute values, as described in Sec. 7.3. The IdP SHOULD support derived attribute values to the extent that the underlying federation protocol allows. ^63c-3-11-2-4

### 63C §3.11.3 Storing Subscriber Information

- **63C-3.11.3-1** SHALL — Whether the account is active or not, the IdP and RP SHALL store personal information in a subscriber account or RP subscriber account using tailored security controls defined in [SP800-53] or an equivalent federal (e.g., [FEDRAMP]) or industry standard. ^63c-3-11-3-1
- **63C-3.11.3-2** SHOULD — When an RP subscriber account can no longer be accessed by a subscriber (e.g., when there are no federated identifiers associated with the account and no alternate means of authentication), the RP SHOULD terminate the RP subscriber account. In particular, if an RP supports account linking (see Sec. 3.8.1) or alternative authenticators (see Sec. 3.8.3), the RP MAY choose to not terminate the RP subscriber account and instead disable the account and retain necessary information in it. ^63c-3-11-3-2
- **63C-3.11.3-3** SHALL — The IdP and RP SHOULD support the deletion of personal information in the subscriber account and RP subscriber account upon account termination, except when otherwise restricted by regulations, laws, or policies or when the risk of an application deems it essential to retain the subscriber’s information. IdPs and RPs that do not support deletion SHALL provide a statutory or risk-based justification and document it in the trust agreement. For example, the RP could record the federated identifier in access and audit logs that are retained even after the account has been terminated. However, all identity attributes and personal information are removed from the RP’s own storage as the RP no longer needs them for its functions. ^63c-3-11-3-3
- **63C-3.11.3-4** SHALL — When the RP subscriber account is terminated, the RP SHALL remove all subscriber attributes from storage, except when otherwise restricted by regulations, laws, or policies or when the risk of an application deems it essential. ^63c-3-11-3-4

### 63C §3.12 Identity Attributes

- **63C-3.12-1** SHALL — Trust agreements SHALL point to the CSP’s practice statements that describe the processes and sources used for attribute validation. ^63c-3-12-1

### 63C §3.12.1 Attribute Bundles

- **63C-3.12.1-1** SHALL — The presentation of an attribute bundle SHALL be protected by the IdP in the same manner as non-bundled attributes. That is, attribute bundles that are presented in an assertion are covered by the signature of the assertion, and attribute bundles that are made available by an identity API are protected by the limited access controls to that API. ^63c-3-12-1-1
- **63C-3.12.1-2** SHALL — The RP SHALL validate the signature specific to the attribute bundle as well as any container signatures, such as the signature of the assertion as a whole. ^63c-3-12-1-2
- **63C-3.12.1-3** SHALL — An attribute bundle MAY optionally include a verification key for the IdP to which the bundle has been issued. In such cases, the RP SHALL confirm that the assertion is presented by the identity claimed in the attribute bundle by verifying the signature over the assertion using the IdP’s verification key in the signed attribute bundle. ^63c-3-12-1-3

### 63C §3.12.2 Derived Attribute Values

- **63C-3.12.2-1** SHALL NOT — Derived attribute values increase the privacy of a system since they allow a more focused release of information to the RP. While some federation systems allow the RP to dynamically query for an arbitrary derived attribute value at request time, many common use cases can be accommodated by the IdP pre-calculating common derived attribute values and offering them as alternatives to the full attribute value. To preserve privacy, derived attribute values SHALL NOT disclose the underlying attribute value to a requester. Selective disclosure technology, as found in some attribute bundles, can be used to carry both full attribute values and derived attribute values in the same response, disclosing only that which is necessary for the application. ^63c-3-12-2-1

### 63C §3.12.3 Identity APIs

- **63C-3.12.3-1** SHOULD — Attributes about the subscriber, including profile information, MAY be provided to the RP through a protected API known as the identity API. The RP is granted limited access to the identity API during the federation transaction in concert with the assertion. For example, in OpenID Connect, the UserInfo Endpoint provides a standardized identity API for fetching attributes about the subscriber. This API is protected by an OAuth 2.0 Access Token, which is issued to the RP along with OpenID Connect’s assertion, the ID Token. Identity APIs SHOULD require sender-constrained access to ensure that identity information is only made available to authorized RPs. ^63c-3-12-3-1
- **63C-3.12.3-2** SHALL NOT — All possible use of identity APIs, including which provisioning models are available through the API, SHALL be recorded and disclosed as part of the trust agreement. Access to the identity API SHALL be time-limited by the trust agreement. Access to the identity API SHOULD be limited to the duration of the federation transaction plus the time necessary to synchronize attributes, as discussed in Sec. 4.6.4. Since the time limitation is separate from the validity time window of the assertion and the lifetime of the authenticated session at the RP, access to an identity API by the RP without an associated valid assertion SHALL NOT be sufficient for the establishment of an authenticated session at the RP. ^63c-3-12-3-2
- **63C-3.12.3-3** SHALL — A given identity API deployment is expected to be capable of providing attributes for all subscribers for whom the IdP can create assertions. However, when access to the identity API is granted within the context of a federation transaction, the attributes provided by an identity API SHALL be associated with only the single subscriber identified in the associated assertion. If the identity API is hosted by the IdP, the returned attributes SHALL include the subject identifier for the subscriber. This allows the RP to positively correlate the assertion’s subject to the returned attributes. When access to an identity API is provided as part of pre-provisioning RP subscriber accounts (see Sec. 4.6.3), the RP is usually granted blanket access to the identity API outside of the context of the federation transaction, and these requirements do not apply. For pre-provisioning use cases, the privacy considerations SHALL be evaluated and recorded as part of the trust agreement. If the identity API is hosted externally from the IdP, the requirements in Sec. 3.12.3.1 apply. ^63c-3-12-3-3

### 63C §3.12.3.1 External Identity APIs

- **63C-3.12.3.1-1** MAY — As the attributes returned by the external identity API are assumed to be independent of those returned directly from the IdP, the contents of the external Identity API MAY use different identifiers, formats, or schemas from those used by the IdP. In particular, an external identity API is not expected to use the same federated identifier as an IdP-hosted identity API. For example, an IdP could provide access to a subscriber’s medical license information. Instead of the IdP asserting the license status directly, the IdP provides the RP access to a record at a medical licensure agency that represents the subscriber. The federation protocol can enable this by allowing the IdP to provide a link to an API with the record that represents the subscriber as well as a credential that allows limited access to this API. The RP can then make a strong association between the subscriber and the medical license record, even though the license record will likely use a different identifier and would not otherwise be correlatable by the RP. The IdP remains responsible for providing this link to the RP. ^63c-3-12-3-1-1
- **63C-3.12.3.1-2** SHALL — Any use of external identity APIs for providing attributes SHALL be enumerated by the trust agreement as part of listing attribute sources. ^63c-3-12-3-1-2

### 63C §3.13 Assertion Protection

- **63C-3.13-1** SHALL — Assertions SHALL include a set of protections to prevent attackers from manufacturing valid assertions or reusing captured assertions at different RPs. The required protections depend on the details of the use case being considered, and specific protections are listed in the following subsections. ^63c-3-13-1

### 63C §3.13.1 Assertion Identifier

- **63C-3.13.1-1** SHALL — Assertions SHALL be sufficiently unique to permit unique identification by the target RP. Assertions MAY accomplish this by using an embedded nonce, issuance timestamp, assertion identifier, or a combination of these or other techniques. ^63c-3-13-1-1

### 63C §3.13.2 Signed Assertion

- **63C-3.13.2-1** SHALL — Assertions SHALL be cryptographically signed by the issuer (IdP). The RP SHALL validate the digital signature or MAC of each such assertion based on the issuer’s verification key. This signature SHALL cover the entire assertion, including its identifier, issuer, audience, subject, and time validity window. ^63c-3-13-2-1
- **63C-3.13.2-2** SHALL — The assertion signature SHALL either be a digital signature using asymmetric keys or a MAC using a symmetric key that is shared between the RP and issuer with approved cryptography. ^63c-3-13-2-2

### 63C §3.13.3 Encrypted Assertion

- **63C-3.13.3-1** MAY — A trust agreement MAY require the encryption of assertion contents in other situations. ^63c-3-13-3-1
- **63C-3.13.3-2** SHALL — When encrypting assertions, the IdP SHALL encrypt the contents of the assertion using the RP’s encryption key with approved cryptography. For example, a SAML assertion can be encrypted using XML-Encryption, while an OpenID Connect ID Token can be encrypted using JSON Web Encryption (JWE). ^63c-3-13-3-2

### 63C §3.13.4 Audience Restriction

- **63C-3.13.4-1** SHALL — Assertions SHALL use audience restriction techniques to allow an RP to recognize whether it is the intended target of an issued assertion. All RPs SHALL check that the audience of an assertion contains an identifier for their RP to prevent the assertion injection and replay of an assertion generated for one RP at another RP. ^63c-3-13-4-1
- **63C-3.13.4-2** SHOULD — In order to limit the places that an assertion could successfully be replayed by an attacker, IdPs SHOULD issue assertions that are designated for only a single audience. Restriction to a single audience is required at FAL2 and above. ^63c-3-13-4-2

### 63C §3.15 Holder-of-Key Assertions

- **63C-3.15-1** SHALL — A holder-of-key assertion (Fig. 3) SHALL include a unique identifier for an authenticator that can be verified independently by the RP, such as the public key of a certificate controlled by the subscriber. The RP SHALL verify that the subscriber possesses the authenticator identified by the assertion. Holder-of-key assertions are most often used when the authenticator technology is tied to a public-key infrastructure (PKI) trusted by both the IdP and RP. ^63c-3-15-1
- **63C-3.15-2** SHALL — The authenticator identified in a holder-of-key assertion MAY be distinct from the primary authenticator that the subscriber uses to authenticate to the IdP. The authenticator identified in a holder-of-key assertion SHALL be phishing-resistant, as defined by Sec. 3.2.5 of [SP800-63B]. When the RP encounters an authenticator in a holder-of-key assertion for the first time, the RP SHALL ensure that the authenticator can be uniquely resolved to the RP subscriber account, as discussed in Sec. 3.8.2. ^63c-3-15-2
- **63C-3.15-3** SHALL NOT — A holder-of-key assertion SHALL NOT include an unencrypted private key or symmetric key to be used as an authenticator. ^63c-3-15-3

### 63C §3.16 Bound Authenticators

- **63C-3.16-1** SHALL — A bound authenticator (Fig. 4) is an authenticator that is bound to the RP subscriber account and managed by the RP. The IdP SHALL include an indicator in the assertion when the assertion is to be used with a bound authenticator at FAL3. The unique identifier for the authenticator (such as its public key) SHALL be stored in the RP subscriber account. The RP needs to have a reliable basis for evaluating the characteristics of the bound authenticator, such as the inclusion of a signed attestation, as discussed in Sec. 3.2.4 of [SP800-63B]. Bound authenticators are most often used when the authenticator technology is not tied to a PKI trusted by both the IdP and RP, for example when no such PKI exists. ^63c-3-16-1
- **63C-3.16-2** SHALL — A bound authenticator SHALL be unique per subscriber at the RP such that two subscribers cannot present the same authenticator for their separate RP subscriber accounts. All bound authenticators SHALL use phishing-resistant authentication mechanisms, as defined by Sec. 3.2.5 of [SP800-63B]. Consequently, subscriber-chosen values such as a password cannot be used as bound authenticators. Bound authenticators SHALL be accepted for authentication in the context of processing an FAL3 assertion for a federated transaction. While it is possible for the same authenticator to also be used for direct authentication to the RP (see Sec. 3.8.3), such use is not considered a bound authenticator, and the RP SHALL document these as distinct use cases. ^63c-3-16-2
- **63C-3.16-3** MAY — The IdP MAY specify types or characteristics for allowable bound authenticators in the trust agreement. ^63c-3-16-3
- **63C-3.16-4** SHALL — Before an RP can successfully accept an FAL3 assertion, the RP subscriber account SHALL include a reference to a bound authenticator that is to be verified during the FAL3 transaction. These authenticators can be provided by either the RP (as in Sec. 13.15.1) or the subscriber (as in Sec. 13.15.2), and different requirements apply to the initial binding of the authenticator to the RP subscriber account in each case. ^63c-3-16-4
- **63C-3.16-5** SHALL — The RP SHALL send a notification to the subscriber via an out-of-band mechanism (e.g., an email to an address previously associated with the subscriber) and SHOULD notify the IdP using a shared signaling system (see Sec. 4.8) if any of the following events occur: ^63c-3-16-5

### 63C §3.16.1 RP-Provided Bound Authenticator Issuance

- **63C-3.16.1-1** SHALL — For RP-provided authenticators, the system administrator of the RP SHALL issue the authenticator directly to the subscriber for use with an FAL3 federation transaction. The system administrator of the RP SHALL use an independent means to determine whether the identified subject of the RP subscriber account is the party to which the authenticator is issued. The system administrator of the RP SHALL follow the initial authenticator binding requirements in Sec. 4 of [SP800-63A] or the post-enrollment binding requirements in Sec. 4.1.2 of [SP800-63B], as appropriate. The system administrator of the RP SHALL store a unique identifier for the bound authenticator in the RP subscriber account, such as the public key of the authenticator. ^63c-3-16-1-1

### 63C §3.16.2 Subscriber-Provided Bound Authenticator Binding Ceremony

- **63C-3.16.2-1** MAY — The RP MAY provide a process for associating subscriber-provided authenticators to the RP subscriber account on a trust-on-first-use basis. This process is known as a binding ceremony and has additional requirements beyond a typical FAL3 federation process. The binding cermony is similar to the subscriber-provided authenticator binding process discussed in Sec. 4.1.3 of [SP800-63B]. ^63c-3-16-2-1
- **63C-3.16.2-2** SHALL NOT — If no bound authenticators are associated with the RP subscriber account, the RP SHALL perform a binding ceremony to establish the connection between the authenticator, the subscriber, and the RP subscriber account, as shown in Fig. 5. The RP SHALL first establish an authenticated session using federation with an assertion that meets all the other requirements of FAL3, including an indication that the assertion is intended for use at FAL3 with a bound authenticator (e.g., the assertion contains an authentication class reference or a Vectors of Trust [RFC8485] value indicating this). The subscriber SHALL immediately be prompted to present and authenticate with the proposed authenticator. Upon successful presentation of the authenticator, the RP SHALL store a unique identifier for the authenticator (such as its public key) and associate this with the RP subscriber account that is associated with the federated identifier. If the subscriber fails to successfully authenticate to the RP using an appropriate authenticator, the binding ceremony fails. The binding ceremony session SHALL have a timeout of five minutes or less and SHALL NOT be used as an authenticated session for any other purpose, as described in Sec. 3.9. Upon successful completion of the binding ceremony, the RP SHALL immediately request a new assertion from the IdP at FAL3. Upon receiving the new assertion, the RP SHALL prompt the subscriber for the newly bound authenticator and SHALL validate the authenticator output. ^63c-3-16-2-2
- **63C-3.16.2-3** SHALL — An RP MAY allow a subscriber to bind multiple subscriber-provided authenticators at FAL3. If this is the case, and the RP subscriber account has one or more existing bound authenticators, the binding ceremony makes use of one of the subscriber’s existing bound authenticators to reach FAL3. During the initial authentication step of the binding ceremony, the RP SHALL request authentication with an existing bound authenticator to reach FAL3. Once this authentication is complete and the binding ceremony session is established, the RP SHALL request authentication with the new authenticator and associate it with the RP subscriber account as a bound authenticator. The RP completes the binding ceremony by requesting a new assertion at FAL3. ^63c-3-16-2-3
- **63C-3.16.2-4** SHALL NOT — In addition to an RP determining that a bound authenticator is no longer viable, a subscriber could choose to stop using a bound authenticator for a variety of reasons, such as the authenticator being lost, compromised, or no longer usable due to technology and platform changes. In such cases, an RP MAY allow a subscriber to remove a subscriber-provided bound authenticator from their RP subscriber account, thereby removing the ability to use that authenticator for FAL3 sessions. When a bound authenticator is removed, the RP SHALL terminate all current FAL3 sessions for the subscriber and SHALL require reauthentication of the subscriber from the IdP at FAL3. The RP SHALL NOT prompt the subscriber to authenticate with the authenticator being removed, since the subscriber will often not have access to the authenticator in question during the unbinding process, particularly if the authenticator is lost or compromised. If all bound authenticators are removed, the subscriber will no longer be able to reach FAL3 until a new bound authenticator is added to the RP subscriber account. This situation poses similar risks to account recovery at the RP. ^63c-3-16-2-4

### 63C §3.17 RP Processing of Holder-of-Key Assertions and Bound Authenticators

- **63C-3.17-1** SHALL — The subscriber SHALL prove possession of the bound authenticator to the RP in addition to presenting the assertion itself. ^63c-3-17-1
- **63C-3.17-2** SHALL — For a holder-of-key assertion, a reference to a given authenticator that is found within an assertion SHALL be trusted at the same level as all other information within the assertion, as stipulated in the trust agreement. ^63c-3-17-2
- **63C-3.17-3** SHALL — The RP SHALL process and validate the assertion in addition to the bound authenticator. ^63c-3-17-3
- **63C-3.17-4** SHALL NOT — Failure to authenticate with the bound authenticator SHALL result in an error at the RP and SHALL NOT create an authenticated session at the RP. ^63c-3-17-4

### 63C §4.1 IdP Account Provisioning

- **63C-4.1-1** SHALL — In order to make subscriber accounts available through an IdP, the subscriber accounts need to be provisioned at the IdP. The means by which the subscriber account is provisioned to the IdP SHALL be disclosed in the trust agreement. ^63c-4-1-1
- **63C-4.1-2** SHALL — The CSP can provide attributes from the subscriber account to the IdP as attribute values, derived attribute values, or attribute bundles. The CSP SHALL sign attribute bundles issued to the IdP. ^63c-4-1-2

### 63C §4.3 Trust Agreements

- **63C-4.3-1** SHALL — Trust agreements for general-purpose IdPs SHALL be established either: ^63c-4-3-1

### 63C §4.3.1 Pre-Established Trust Agreements

- **63C-4.3.1-1** SHALL — When the trust agreement is established by the federated parties prior to the federation transaction, the trust agreement SHALL establish the following terms: ^63c-4-3-1-1
- **63C-4.3.1-2** SHALL — The terms of the trust agreement SHALL be available to the operators of the RP and the IdP upon its establishment. The terms of the trust agreement SHALL be made available to subscribers upon request to the IdP or RP. ^63c-4-3-1-2
- **63C-4.3.1-3** SHALL — The IdP and RP SHALL each assess their respective redress mechanisms for efficacy in resolving complaints or problems and disclose the results of this assessment as part of the trust agreement. See Sec. 3.5.3 for additional requirements and considerations for redress mechanisms. ^63c-4-3-1-3
- **63C-4.3.1-4** SHALL — If FAL3 is allowed within the trust agreement, the trust agreement SHALL stipulate the following terms regarding holder-of-key assertions (see Sec. 3.15) and bound authenticators (see Sec. 3.16): ^63c-4-3-1-4
- **63C-4.3.1-5** SHALL — If shared signaling is used by the IdP or RP (see Sec. 4.8), the terms of the trust agreement SHALL establish: ^63c-4-3-1-5
- **63C-4.3.1-6** MAY — Runtime decisions at the IdP (see Sec. 4.6.1.3), MAY be used to further limit which subscriber attributes are sent between parties in the federated transaction (e.g., a runtime decision could opt to not disclose an email address, even though this attribute was included in the terms of the trust agreement). ^63c-4-3-1-6
- **63C-4.3.1-7** SHALL — The trust agreement SHALL be reviewed periodically to ensure that it is still fit for purpose and to avoid unnecessary data exchange and the over-collection of subscriber data. ^63c-4-3-1-7

### 63C §4.3.2 Subscriber-Driven Trust Agreement Establishment

- **63C-4.3.2-1** SHALL — When the trust agreement is established as the result of a subscriber’s decision (e.g., a subscriber starting a federation transaction between an RP and their IdP without an established agreement), the trust agreement is anchored by the subscriber. In a subscriber-driven trust agreement, the trust agreement takes the form of a set of terms of use as opposed to a formal contract between parties. Consequently, the following terms SHALL be disclosed to the subscriber upon request: ^63c-4-3-2-1
- **63C-4.3.2-2** SHALL — The IdP SHALL assess its redress mechanisms for efficacy in resolving complaints or problems and disclose the results of this assessment to the subscriber. See Sec. 3.5.3 for additional requirements and considerations for redress mechanisms. ^63c-4-3-2-2
- **63C-4.3.2-3** SHALL — The following terms of the trust agreement SHALL be disclosed to the subscriber during the runtime decision: ^63c-4-3-2-3

### 63C §4.4 Discovery and Registration

- **63C-4.4-1** SHALL — The RP SHALL associate the assertion validation keys and other relevant configuration information with the IdP’s identifier, as stipulated by the trust agreement. If the validation keys and configuration information are retrieved over a network connection, request and retrieval SHALL be made over an authenticated protected channel from a location that is associated with the IdP’s identifier by the trust agreement. In many federation protocols, this is accomplished by the RP fetching the public keys and configuration data from a URL that is specified in the trust agreement as being controlled by the IdP or offered on the IdP’s behalf. It is also possible for the RP to be configured directly with this information in a manual fashion, whereby the RP’s system administrator enters the IdP information directly into the RP software’s configuration. ^63c-4-4-1
- **63C-4.4-2** SHALL — Additionally, the RP SHALL register its information with either the IdP or an authority that the IdP trusts, as stipulated by the trust agreement. In many federation protocols, the RP is assigned an identifier during this stage, which the RP will use in subsequent communication with the IdP. ^63c-4-4-2
- **63C-4.4-3** MAY — Parties that seek to federate MAY use a trusted third party to facilitate the discovery and registration processes if that trusted third party is identified in the trust agreement. For example, a consortium could use a hosted service that collects the configuration records of IdPs and RPs directly from participants. Instead of going to the IdP directly for its discovery record, an RP would instead go to this service and retrieve the key material for its target IdP. The IdP would, in turn, go to this service to find the identifiers and configuration information for RPs that are needed to connect. This service is often managed by the same party that fulfills the federation authority role in multilateral trust agreements, as discussed in Sec. 3.5.2. ^63c-4-4-3

### 63C §4.4.1 Manual Registration

- **63C-4.4.1-1** SHALL — This process MAY be facilitated by some level of automated tooling, whereby the manual configuration points the systems in question to a trusted source of information that can be updated over time. If such automation is used, the trust agreement SHALL enumerate the allowable terms of the cryptographic key distribution and assignment, including allowable cache lifetimes. ^63c-4-4-1-1

### 63C §4.4.2 Dynamic Registration

- **63C-4.4.2-1** SHALL — At FAL1 and FAL2, the cryptographic keys and identifiers of the RP can be exchanged in a dynamic process, whereby the RP software presents its configuration to the IdP either directly or through a trusted third party and receives the identifier to use with that IdP. This process is specific to the federation protocol in use but requires machine-readable configuration data to be made available over the network. All transmission of configuration information SHALL be made over a secure protected channel to endpoints that are associated with the IdP’s identifier by the trust agreement. ^63c-4-4-2-1
- **63C-4.4.2-2** SHOULD — IdPs SHOULD consider the risks of information leakage to multiple RP instances and take appropriate countermeasures, such as issuing PPIs for subscribers who access dynamically registered RPs, as discussed in Sec. 3.4.1. ^63c-4-4-2-2
- **63C-4.4.2-3** SHOULD — Dynamic registration SHOULD be augmented by attestations about the RP software and device, as discussed in Sec. 3.6.3. ^63c-4-4-2-3

### 63C §4.5 Subscriber Authentication at the IdP

- **63C-4.5-1** SHALL — The IdP SHALL require the subscriber to have an authenticated session before any of the following events: ^63c-4-5-1

### 63C §4.6 Authentication and Attribute Disclosure

- **63C-4.6-1** SHALL — The authorized party stipulated by the trust agreement SHALL decide whether a federation transaction proceeds and, therefore, whether an assertion is issued and attributes are released to the RP. This decision can be calculated in a variety of ways, including: ^63c-4-6-1
- **63C-4.6-2** SHALL — The IdP SHALL provide effective mechanisms for the redress of subscriber complaints or problems (e.g., subscriber identifies an inaccurate attribute value). See Sec. 3.5.3 for additional requirements and considerations for redress mechanisms. ^63c-4-6-2

### 63C §4.6.1.1 IdP Allowlists of RPs

- **63C-4.6.1.1-1** SHALL — In a pre-established trust agreement, IdPs MAY establish allowlists of RPs that are authorized to receive authentication and attributes from the IdP without a runtime decision from the subscriber. When placing an RP on its allowlist, the IdP SHALL confirm that the RP abides by the terms of the trust agreement. The IdP SHALL determine which identity attributes are passed to the allowlisted RP upon authentication. IdPs SHALL make allowlists available to subscribers, as described in Sec. 7.2. ^63c-4-6-1-1-1
- **63C-4.6.1.1-2** SHALL NOT — IdP allowlists SHALL uniquely identify RPs through fully qualified domain names, cryptographic keys, or other identifiers that are applicable to the federation protocol in use. Any entities that share an identifier SHALL be considered equivalent for the purposes of the allowlist. Allowlists SHOULD be as specific as possible to avoid unintentional impersonation of an RP. An allowlist entry for an RP SHALL NOT use a wildcard domain identifier. ^63c-4-6-1-1-2
- **63C-4.6.1.1-3** SHALL — IdP allowlist entries for an RP SHALL indicate which attributes are included as part of an allowlisted decision. If additional attributes are requested by the RP, the request SHALL be: ^63c-4-6-1-1-3
- **63C-4.6.1.1-4** MAY — IdP allowlist entries MAY be applied based on aspects of the federation transaction, such as the xALs required for the transaction. For example, an IdP could use an allowlist entry to bypass a consent screen for an FAL1 transaction but require confirmation of consent from the subscriber during an FAL3 transaction. ^63c-4-6-1-1-4

### 63C §4.6.1.2 IdP Blocklists of RPs

- **63C-4.6.1.2-1** SHALL NOT — IdPs MAY establish blocklists of RPs that are not authorized to receive authentication assertions or attributes from the IdP, even if requested to do so by the subscriber. If an RP is on an IdP’s blocklist, the IdP SHALL NOT produce an assertion that targets the RP in question under any circumstances. ^63c-4-6-1-2-1
- **63C-4.6.1.2-2** SHALL — IdP blocklists SHALL uniquely identify RPs through the means of fully qualified domain names, cryptographic keys, or other identifiers that are applicable to the federation protocol in use. Any entities that share an identifier SHALL be considered equivalent for the purposes of the blocklist. For example, a wildcard domain identifier of “*.example.com” would match the domains “www.example.com”, “service.example.com”, and “unknown.example.com” equally. All three of these sites would be blocked by the same blocklist entry. ^63c-4-6-1-2-2

### 63C §4.6.1.3 IdP Runtime Decisions

- **63C-4.6.1.3-1** SHALL — Every RP that is in a trust agreement with an IdP but not on an allowlist with that IdP SHALL be governed by a default policy in which runtime authorization decisions will be made by an authorized party that is identified by the trust agreement. Since the runtime decision occurs during the federation transaction, the authorized party is generally a person and, in most circumstances, is the subscriber. However, it is possible for another party such as a system administrator to be prompted on behalf of the subscriber. In a subscriber-driven trust agreement, a runtime decision with the subscriber is the only allowable means to authorize the release of subscriber attributes. ^63c-4-6-1-3-1
- **63C-4.6.1.3-2** SHALL — When processing a runtime decision, the IdP interactively prompts the authorized party during the federation transaction. The authorized party provides consent to release an authentication assertion and specific attributes to the RP. The IdP SHALL provide the authorized party with explicit notice and prompt them for positive confirmation before any attributes about the subscriber are transmitted to the RP. At a minimum, the notice SHOULD be provided by the party in the position to provide the most effective notice and obtain confirmation, consistent with Sec. 7.2. The IdP SHALL disclose which attributes will be released to the RP if the transaction is approved. If the federation protocol in use allows for optional or selective attribute disclosure at runtime, the authorized party SHALL be given the option to decide whether to transmit specific attributes to the RP without terminating the federation transaction entirely. ^63c-4-6-1-3-2
- **63C-4.6.1.3-3** SHALL — If the authorized party is the subscriber, the IdP SHALL provide mechanisms for the subscriber to view the attribute values and derived attribute values to be sent to the RP. To mitigate the risk of unauthorized exposure of sensitive information (e.g., shoulder surfing), the IdP SHALL, by default, mask sensitive information displayed to the subscriber. For more details on masking, see Sec. 8 on usability considerations. ^63c-4-6-1-3-3
- **63C-4.6.1.3-4** SHALL — An IdP MAY employ mechanisms to remember the authorized party’s decision and re-transmit the same set of attributes to the same RP. This mechanism is associated with the subscriber account as managed by the IdP. If such a mechanism is provided, the IdP SHALL disclose to the authorized party that the storage mechanism is in use and SHALL allow the authorized party to revoke such remembered access at a future time. ^63c-4-6-1-3-4

### 63C §4.6.2.1 RP Allowlists of IdPs

- **63C-4.6.2.1-1** SHALL — RPs MAY establish allowlists of IdPs from which the RP will accept authentication and attributes without a runtime decision from the subscriber to use the IdP. In practice, many RPs interface with only a single IdP, and this IdP is allowlisted as the only possible entry for that RP. When placing an IdP in its allowlist, the RP SHALL confirm that the IdP abides by the terms of the trust agreement. This confirmation can be facilitated by a federation authority or undertaken directly by the RP. ^63c-4-6-2-1-1
- **63C-4.6.2.1-2** SHALL NOT — RP allowlists SHALL uniquely identify IdPs through fully qualified domain names, cryptographic keys, or other identifiers that are applicable to the federation protocol in use. Allowlists SHOULD be as specific as possible to avoid unintentional impersonation of an IdP. An allowlist entry for an IdP SHALL NOT use a wildcard domain identifier. ^63c-4-6-2-1-2
- **63C-4.6.2.1-3** MAY — RP allowlist entries MAY be applied based on aspects of the federation transaction, such as the xALs required for the transaction. For example, an RP could use a runtime decision for FAL1 transactions but require an allowlisted IdP for FAL3 transactions. ^63c-4-6-2-1-3

### 63C §4.6.2.2 RP Blocklists of IdPs

- **63C-4.6.2.2-1** MAY — RPs MAY establish blocklists of IdPs from which the RP will not accept authentication or attributes, even when requested by the subscriber. A blocklisted IdP can otherwise be in a valid trust agreement with the RP, such as when both are under the same federation authority. ^63c-4-6-2-2-1
- **63C-4.6.2.2-2** SHALL — RP blocklists SHALL uniquely identify IdPs through fully qualified domain names, cryptographic keys, or other identifiers that are applicable to the federation protocol in use. Any entities that share an identifier SHALL be considered equivalent for the purposes of the blocklist. For example, a wildcard domain identifier of “*.example.com” would match the domains “www.example.com”, “service.example.com”, and “unknown.example.com” equally. All three of these sites would be blocked by the same blocklist entry. ^63c-4-6-2-2-2

### 63C §4.6.2.3 RP Runtime Decisions

- **63C-4.6.2.3-1** SHALL — Every IdP that is in a trust agreement with an RP but not on an allowlist with that RP SHALL be governed by a default policy in which runtime authorization decisions will be made by the authorized party indicated in the trust agreement. In this mode, the authorized party is prompted by the RP to select or enter which IdP to contact for authentication on behalf of the subscriber. This process can be facilitated by a discovery mechanism that allows the subscriber to enter a human-facing identifier, such as an email address that is then used to programmatically select the IdP for the entered address. Since the runtime decision occurs during the federation transaction, the authorized party is generally a person and, in most circumstances, the subscriber. ^63c-4-6-2-3-1
- **63C-4.6.2.3-2** SHALL — The RP MAY employ mechanisms to remember the authorized party’s decision to use a given IdP. Since this mechanism is employed prior to authentication at the RP, the manner in which the RP provides this mechanism (e.g., a browser cookie outside of the authenticated session) is separate from the RP subscriber account, as described in Sec. 3.8. If such a mechanism is provided, the RP SHALL disclose to the authorized party that the storage mechanism is in use and SHALL allow the authorized party to revoke such remembered access at a future time. ^63c-4-6-2-3-2

### 63C §4.6.3 Provisioning Models for RP Subscriber Accounts

- **63C-4.6.3-1** SHALL — The life cycle of the provisioning process for an RP subscriber account varies based on factors including the trust agreement discussed in Sec. 3.5 and the deployment pattern of the IdP and RP. However, in all cases, the RP subscriber account SHALL be provisioned at the RP prior to the establishment of an authenticated session at the RP in one of the following ways: ^63c-4-6-3-1
- **63C-4.6.3-2** SHALL — In this model, the RP also receives attributes about subscribers who have not yet interacted with the RP and who may never do so. This is in contrast to other models in which the RP only receives information about the subset of subscribers that use the RP, and then only after the subscriber uses the RP for the first time. The privacy considerations of the RP having access to this information prior to a federation transaction SHALL be accounted for in the trust agreement. ^63c-4-6-3-2
- **63C-4.6.3-3** SHALL — All organizations SHALL document their provisioning models as part of their trust agreement. ^63c-4-6-3-3

### 63C §4.6.4 Attribute Synchronization

- **63C-4.6.4-1** MAY — From the RP’s perspective, the IdP is the trusted source for any attributes that the IdP asserts as being associated with the subscriber account at the IdP. However, the RP MAY collect and optionally verify other attributes to associate with the RP subscriber account, as discussed in Sec. 4.6.6. ^63c-4-6-4-1
- **63C-4.6.4-2** SHOULD — While it is possible for the IdP to proactively push updated attributes to the RP with every assertion, this practice exposes personal information on every transaction. To limit the amount of personal information sent at each transaction, the IdP SHOULD signal downstream RPs when the attributes of a subscriber account available to the RP have been updated. RPs MAY respond to this signal by requesting the new attributes from the IdP and updating the RP subscriber account. This synchronization can be accomplished by using shared signaling (see Sec. 4.8), through a provisioning API (see Sec. 4.6.5), or by signaling the RP (e.g., by providing a timestamp of when the subscriber account attributes were last updated) to request updated attributes through an identity API (see Sec. 3.12.3). ^63c-4-6-4-2
- **63C-4.6.4-3** SHOULD — If the RP is granted access to an identity API, the IdP SHOULD allow the RP to access the identity API for sufficient time to perform synchronization operations after the federation transaction has concluded. While an identity API is most often used during the first login, especially with a just-in-time provisioning process, on subsequent logins it is possible that attributes could have changed since the RP last fetched them. Therefore, the RP ought to be given access to the identity API beyond the initial login process to allow the RP to update its cache of attributes in the RP subscriber account. For example, if the assertion is valid for five minutes, access to the identity API could be valid for 30 minutes to allow the RP to fetch and update attributes out of band if the RP has determined that the RP subscriber account is out of date. ^63c-4-6-4-3
- **63C-4.6.4-4** SHALL — The IdP SHOULD signal downstream RPs when a subscriber account is terminated or when the subscriber account’s access to an RP is revoked. This can be accomplished through shared signaling (see Sec. 4.8), through a provisioning API (see Sec. 4.6.5), or through an out-of-band mechanism. Upon receiving such a signal, the RP SHALL process the RP subscriber account, as stipulated in the trust agreement and in accordance with Sec. 3.11.3. If the reason for termination is suspicious or fraudulent activity, the IdP SHALL notify the RP of the termination and include the reason in its signal to the RP to allow the RP to review the associated RP subscriber account’s activity for suspicious activity, if specified in the trust agreement with that RP. ^63c-4-6-4-4

### 63C §4.6.5 Provisioning APIs

- **63C-4.6.5-1** SHALL — The attributes in the provisioning API that are available to a given RP SHALL be limited to only those necessary for the RP to perform its functions, including any audit and security purposes, as discussed in Sec. 3.10.1. As part of establishing the trust agreement, the IdP SHALL document when an RP is given access to a provisioning API, including at least the following: ^63c-4-6-5-1
- **63C-4.6.5-2** SHALL — Access to the provisioning API SHALL occur over a mutually authenticated protected channel. The exact means of authentication varies depending on the specifics of the API and whether it is a push model (i.e., the IdP initiates the connection to the RP) or a pull model (i.e., the RP initiates the connection to the IdP). ^63c-4-6-5-2
- **63C-4.6.5-3** SHALL NOT — A provisioning API SHALL NOT be made available under a subscriber-driven trust agreement. The IdP SHALL NOT make a provisioning API available to any RP outside of an established trust agreement. The IdP SHALL provide access to a provisioning API only as part of a federated identity relationship with an RP to facilitate federation transactions with that RP and related functions, such as signaling revocation of the subscriber account. The IdP SHALL revoke an RP’s access to the provisioning API once access is no longer required by the RP for its functioning purposes or when the trust agreement is terminated. ^63c-4-6-5-3
- **63C-4.6.5-4** SHALL — Any provisioning API provided to the RP SHALL be under the control and jurisdiction of the IdP. External attribute providers MAY be used as information sources by the IdP to provide attributes through this provisioning API, but the IdP is responsible for the content and accuracy of the information provided by the referenced attribute providers. ^63c-4-6-5-4
- **63C-4.6.5-5** SHALL — When a provisioning API is in use, the IdP SHALL signal to the RP when the state of a subscriber account has been changed, such as when the account has been terminated or disabled. When receiving such a signal, the RP SHALL remove the binding of the federated identifier from the account. The RP MAY terminate the RP subscriber account if it can no longer be accessed by the subscriber. The RP SHALL treat all personal information sourced from the provisioning API in accordance with Sec. 3.11.3. ^63c-4-6-5-5

### 63C §4.6.6 Collection of Additional Attributes by the RP

- **63C-4.6.6-1** MAY — The RP MAY collect and maintain additional attributes from the subscriber beyond those provided by the IdP. For example, the RP could collect a preferred display name directly from the subscriber that is not provided by the IdP. The RP could also have a separate agreement with an attribute provider that gives the RP access to an identity API that is not associated with the IdP. For example, the RP could receive a state license number from the IdP but use a separate attribute verification API to check whether a particular license number is currently valid. The assertion from the IdP binds the license to the subscriber, but the attribute verification API provides additional information beyond what the IdP can share or be authoritative for. ^63c-4-6-6-1
- **63C-4.6.6-2** SHALL — These attributes are governed separately from the trust agreement since they are collected by the RP outside of a federation transaction. However, all attributes in the RP subscriber account — regardless of source — SHALL be stored in accordance with Sec. 3.11.3. ^63c-4-6-6-2
- **63C-4.6.6-3** SHALL — The RP SHALL disclose to the subscriber the purpose for collecting any additional attributes. These attributes SHALL be used solely for the stated purposes of the RP’s functionality. The transmission of additionally collected attributes SHALL be handled in accordance with Sec. 3.10.1. ^63c-4-6-6-3
- **63C-4.6.6-4** SHALL — The RP SHALL provide a secure and effective means of redress for the subscriber to update and remove these additionally collected attributes from the RP subscriber account. See Sec. 3.5.3 for additional requirements and considerations for redress mechanisms. ^63c-4-6-6-4
- **63C-4.6.6-5** SHALL — An RP SHALL disclose any additional attributes collected and their use as part of its System of Records Notice (SORN). ^63c-4-6-6-5

### 63C §4.6.7 Time-Based Removal of RP Subscriber Accounts

- **63C-4.6.7-1** MAY — If an RP is using a just-in-time provisioning mechanism, the RP only learns of the existence of a subscriber account when that account is first used at the RP. If the IdP does not inform the RP of terminated subscriber accounts using shared signaling (see Sec. 4.8), an RP could accumulate RP subscriber accounts that are no longer accessible from the IdP. This poses a risk to the RP for holding personal information in the RP subscriber accounts and providing potentially exploitable accounts for an attacker to target. In such circumstances, the RP MAY employ a time-based mechanism to identify RP subscriber accounts for termination that have not been accessed after a period of time that is tailored to the usage patterns of the application. For example, an RP that is usually accessed on a weekly basis could set a timeout of 120 days since last access at the RP to mark the RP subscriber account for termination. An RP that expects longer gaps between access (e.g., a service used annually) should have a much longer time frame for time-based termination, such as five years. ^63c-4-6-7-1
- **63C-4.6.7-2** SHALL — When processing an inactive account, the RP SHALL provide sufficient notice to the subscriber about the pending termination of the account and provide the subscriber with an option to re-activate the account prior to its scheduled termination. Upon termination, the RP SHALL remove all personal information associated with the RP subscriber account in accordance with Sec. 3.11.3. ^63c-4-6-7-2

### 63C §4.7 Reauthentication and Session Requirements in Federated Environments

- **63C-4.7-1** MAY — The IdP terminating the subscriber’s session at the IdP will not necessarily terminate any sessions that subscriber might have at downstream RPs. The RP and IdP MAY communicate end-session events to each other if supported by the federation protocol or through shared signaling (see Sec. 4.8). ^63c-4-7-1
- **63C-4.7-2** SHALL — At the time of a federated transaction request, the subscriber could have a pre-existing authenticated session at the IdP that MAY be used to generate an assertion to the RP. The IdP SHALL communicate to the RP any information that the IdP has regarding the recency of the subscriber’s latest authentication event at the IdP, and the RP MAY use this information to make authorization and access decisions. Depending on the capabilities of the federation protocol in use, the IdP SHOULD allow the RP to request that the subscriber provide a fresh authentication at the IdP, such as requesting a maximum time since the subscriber’s last authentication event. For example, suppose that the subscriber authenticates at the IdP for one transaction. The subscriber then starts a federation transaction at the RP 30 minutes later. Depending on xAL requirements, the subscriber’s existing session at the IdP can be used to avoid prompting the subscriber for their authenticators. The resulting assertion to the RP will indicate that the last time the subscriber authenticated to the RP was 30 minutes in the past. The RP can then use this information to determine whether this is reasonable for the RP’s needs. If the authentication time is not sufficient for the RP, the RP can request the IdP to prompt the subscriber for a fresh authentication event. ^63c-4-7-2
- **63C-4.7-3** SHALL NOT — If an RP is granted access to an identity API at the same that time the RP receives an assertion, the lifetime of the access to the identity API is independent of the lifetime of the assertion. As a consequence, the RP’s ability to successfully fetch additional attributes through an identity API SHALL NOT be used to establish or extend a session at the RP. Likewise, the inability to access an identity API SHOULD NOT be used to end the session at the RP. ^63c-4-7-3
- **63C-4.7-4** MAY — The RP MAY terminate its authenticated session with the subscriber or restrict access to the RP’s functions if the assertion, authentication event, or attributes do not meet the RP’s requirements. For example, if an RP is configured to allow access to certain high-risk functionality only if the federation transaction was at FAL3, but the incoming assertion only meets the requirements for FAL2, the RP could decide to deny access to the high-risk functionality while allowing access to a lower risk functionality, or the RP could choose to terminate the session entirely. ^63c-4-7-4

### 63C §4.8 Shared Signaling

- **63C-4.8-1** SHALL NOT — In some environments, it is useful for the IdP and RP to send information to each other outside of the federation transaction. These signals can communicate important changes in state between parties that would not otherwise be known, such as suspected fraud or an account status change. Shared signaling SHALL be limited to the allowable functions of the identity process, as discussed in Sec. 3.10.1. All uses of shared signaling SHALL be documented in the trust agreement and made available to the authorized party stipulated by the trust agreement. This documentation SHALL include the events under which a signal is sent, the type of information included in such a signal (including any personal information), any additional parameters sent with the signal, and the expected processing of a received signal. The use of shared signaling SHALL be subject to privacy review under the trust agreement. Shared signals SHALL NOT include personal information except what is necessary to identify the subscriber account in question (e.g., an account identifier or attributes that can be correlated by the receiving party). ^63c-4-8-1
- **63C-4.8-2** SHALL — Signaling from the IdP to the RP SHALL require a pre-established trust agreement. Signaling from the RP to the IdP MAY be used in both pre-established and subscriber-driven trust agreements. ^63c-4-8-2
- **63C-4.8-3** SHOULD — The IdP SHOULD send a signal to the RP regarding the following changes to the subscriber account: ^63c-4-8-3
- **63C-4.8-4** SHOULD — If the RP receives a signal that an RP subscriber account is suspected of compromise, the RP SHOULD review actions taken by that account at the RP for suspicious activity. ^63c-4-8-4
- **63C-4.8-5** SHOULD — The RP SHOULD send a signal to the IdP regarding the following changes to the RP subscriber account: ^63c-4-8-5
- **63C-4.8-6** SHALL — If the IdP receives a signal that a subscriber account is suspected of compromise, the IdP SHALL review actions taken by that account at the IdP for suspicious activity. If suspicious activity is confirmed at the IdP, the IdP SHALL signal any additional RPs that the subscriber account was used for during the suspected time frame. ^63c-4-8-6
- **63C-4.8-7** SHALL — Additional signals from both the IdP and RP SHALL be subject to a security review, included in the privacy risk assessment, and addressed in the trust agreement. ^63c-4-8-7
- **63C-4.8-8** SHALL — If the RP allows for account linking to multiple IdPs, the RP SHALL document their practices regarding signals for linked accounts. The RP SHALL ensure that the shared signals do not reveal the identity of a subscriber’s linked IdPs. ^63c-4-8-8

### 63C §4.9 Assertion Contents

- **63C-4.9-1** SHALL — Assertions SHALL represent a discrete authentication event of the subscriber at the IdP and SHALL be processed as a discrete authentication event at the RP. ^63c-4-9-1
- **63C-4.9-2** SHALL — All assertions SHALL include the following attributes: ^63c-4-9-2
- **63C-4.9-3** SHALL NOT — Validity time window: A period of time outside of which the assertion SHALL NOT be accepted as valid by the RP for the purposes of authenticating the subscriber and starting an authenticated session at the RP. This is usually communicated by means of an expiration timestamp for the assertion in addition to the issuance timestamp. ^63c-4-9-3
- **63C-4.9-4** SHALL — If the RP subscriber account does not use an ephemeral provisioning process, the subscriber SHALL be identified in the assertion using a federated identifier (see Sec. 3.4) or through an account resolution process (see Sec. 3.8.2). ^63c-4-9-4
- **63C-4.9-5** SHALL — If the subscriber is identified using a federated identifier, the assertion SHALL include: ^63c-4-9-5
- **63C-4.9-6** SHALL — The following aspects of the federation transaction SHALL be provided through information contained in the assertion contents or the applicable trust agreement: ^63c-4-9-6
- **63C-4.9-7** SHOULD — The assertion SHOULD contain additional information about the authentication method used at the IdP, if available (e.g., whether the authenticator used is phishing-resistant). Some technologies that can carry information include Vectors of Trust [RFC8485] or authentication class references in [OIDC] and [SAML]. ^63c-4-9-7
- **63C-4.9-8** SHALL — At FAL2 and above, the assertion SHALL include: ^63c-4-9-8
- **63C-4.9-9** SHALL — At FAL3, the assertion SHALL include one of the following: ^63c-4-9-9
- **63C-4.9-10** SHALL NOT — Assertions SHALL NOT contain subscriber authentication secrets (e.g., passwords). ^63c-4-9-10
- **63C-4.9-11** MAY — Assertions MAY also include additional items, including: ^63c-4-9-11
- **63C-4.9-12** SHALL — The RP SHALL validate the assertion by checking that all of the following are true: ^63c-4-9-12
- **63C-4.9-13** SHALL NOT — An RP that uses the federated identifier to identify the subscriber SHALL NOT treat subject identifiers as inherently globally unique across IdPs. Instead, the value of the assertion’s subject identifier is processed in a namespace under the assertion issuer’s control, as discussed in Sec. 3.4. This allows an RP to talk to multiple IdPs without incorrectly conflating subjects from different IdPs. ^63c-4-9-13
- **63C-4.9-14** MAY — Any release of identity attributes to the RP is subject to the terms of the trust agreement. Section 3.10 contains privacy requirements for presenting attributes in assertions. The RP MAY be given limited access to an identity API (see Sec. 3.12.3), either in the same response as the assertion is received or through some other mechanism. The RP can use this API to fetch additional identity attributes for the subscriber that are not included in the assertion itself. These attributes are also subject to the terms of the trust agreement. ^63c-4-9-14
- **63C-4.9-15** SHALL NOT — The assertion’s validity time window is the time between its issuance and its expiration. This window needs to be large enough to allow the RP to process the assertion and create a local application session for the subscriber but should not be longer than necessary for such establishment, including reasonable clock drift between the IdP and RP. Long-lived assertions have a greater risk of being stolen or replayed; a short assertion validity time window mitigates this risk. Assertion validity time windows SHALL NOT be used to limit the session at the RP. See Sec. 4.7 for more information. ^63c-4-9-15

### 63C §4.10 Assertion Requests

- **63C-4.10-1** SHALL — When the federation transaction is initiated by the RP, the RP’s request for an assertion SHALL contain: ^63c-4-10-1
- **63C-4.10-2** SHOULD — The RP’s request SHOULD additionally contain: ^63c-4-10-2

### 63C §4.11 Assertion Presentation

- **63C-4.11-1** MAY — There are trade-offs with each model, but both require the proper validation of the assertion. Assertions MAY also be proxied to facilitate federation between IdPs and RPs using different presentation methods, as discussed in detail in Sec. 3.3.3. ^63c-4-11-1

### 63C §4.11.1 Back-Channel Presentation

- **63C-4.11.1-1** SHALL — In the back-channel presentation model shown in Fig. 11, the subscriber is given an assertion reference to present to the RP, generally through the front channel. The assertion reference itself contains no information about the subscriber and SHALL be resistant to tampering and fabrication by an attacker. The RP presents the assertion reference to the IdP to fetch the assertion. Methods for achieving this vary based on the federation protocol in use. In the authorization code flow and some forms of the hybrid flow of [OIDC], the assertion (i.e., the ID Token) is presented in the back channel in exchange for the assertion reference (i.e., the authorization code). In the artifact binding profile of [SAML-Bindings], the SAML assertion is presented in the back channel. ^63c-4-11-1-1
- **63C-4.11.1-2** SHALL — SHALL be limited to use by a single RP ^63c-4-11-1-2
- **63C-4.11.1-3** SHALL — SHALL be single-use ^63c-4-11-1-3
- **63C-4.11.1-4** SHALL — SHALL be time-limited and SHOULD have a validity time window of no more than five minutes ^63c-4-11-1-4
- **63C-4.11.1-5** SHALL — SHALL be presented along with authentication of the RP to the IdP ^63c-4-11-1-5
- **63C-4.11.1-6** SHALL NOT — SHALL NOT be predictable or guessable by an attacker ^63c-4-11-1-6
- **63C-4.11.1-7** SHALL — Conveyance of the assertion reference from the IdP to the subscriber and from the subscriber to the RP SHALL be made over an authenticated protected channel. Conveyance of the assertion reference from the RP to the IdP and vice versa SHALL be made over an authenticated protected channel. ^63c-4-11-1-7
- **63C-4.11.1-8** SHALL — The RP SHALL protect itself against the injection of manufactured or captured assertion references by using cross-site scripting (XSS) and cross-site request forgery (CSRF) protection, rejecting assertion references outside of the correct stage of a federation transaction, or other accepted techniques discussed in Sec. 3.11.1. When assertion references are presented to the IdP, the IdP SHALL verify that the RP presenting the assertion reference is the same RP that made the assertion request that resulted in the assertion reference. Examples for this are discussed in Sec. 9.12, including authorization code flow of [OIDC] with additional security profiles, such as [FAPI] and [iGov]. ^63c-4-11-1-8

### 63C §4.11.2 Front-Channel Presentation

- **63C-4.11.2-1** SHALL — The RP SHALL use the assertion identifier to ensure that a given assertion is presented at most once during the assertion’s validity time window. ^63c-4-11-2-1
- **63C-4.11.2-2** SHALL — The RP SHALL protect itself against the injection of manufactured or captured assertions by using XSS and CSRF protection, rejecting assertions outside of the correct stage of a federation transaction, or other accepted techniques discussed in Sec. 3.11.1. ^63c-4-11-2-2
- **63C-4.11.2-3** SHALL — Conveyance of the assertion from the IdP to the subscriber and from the subscriber to the RP SHALL be made over an authenticated protected channel. ^63c-4-11-2-3
- **63C-4.11.2-4** SHALL — With general-purpose IdPs, it is common for front-channel communications to be accomplished using HTTP redirects, where the contents of the assertion are made available as part of an HTTP request URL. Due to the nature of the HTTP ecosystem, these request URLs are sometimes available in unexpected places, such as access logs, web proxies, and browser histories. These artifacts tend to live on long past the federation transaction and are available in other contexts, which increases the attack surface for reading the assertion. As a consequence, an IdP that uses HTTP redirects for the front-channel presentation of assertions SHALL encrypt all personal information in the assertion, as discussed in Sec. 3.13.3. Other front-channel presentation mechanisms that do not share these characteristics (e.g., HTTP form-post binding, application-specific URLs) SHOULD encrypt all personal information in the assertion. ^63c-4-11-2-4

### 63C §5.1 Issuing Attribute Bundles to the Subscriber-Controlled Wallet

- **63C-5.1-1** SHALL — When the CSP issues attribute bundles to the subscriber-controlled wallet, the process SHALL include the following steps: ^63c-5-1-1
- **63C-5.1-2** MAY — The subscriber-controlled wallet MAY generate and use a different signing key and verification key for each issuance request with the CSP. ^63c-5-1-2
- **63C-5.1-3** SHALL — The CSP SHALL create a unique attribute bundle for each requesting wallet and SHOULD create a unique attribute bundle for each request from an individual wallet. ^63c-5-1-3
- **63C-5.1-4** SHALL — Many subscriber-controlled wallets can carry attribute bundles from multiple CSPs simultaneously. The simultaneous presentation of attribute bundles from multiple CSPs in a single assertion is possible with some technologies. When this occurs, the assertion of multiple attribute bundles SHALL conform to the assertion requirements in this guideline. ^63c-5-1-4

### 63C §5.1.1 Invalidating Attribute Bundles for the Subscriber-Controlled Wallet

- **63C-5.1.1-1** SHALL — The CSP SHALL provide a means of invalidating attribute bundles that are issued to a subscriber-controlled wallet. This process is used when: ^63c-5-1-1-1
- **63C-5.1.1-2** SHALL — To accomplish this, the CSP SHOULD issue attribute bundles with a limited time validity window. The CSP SHOULD provide a means to independently verify the status of attribute bundles (i.e., whether a specific bundle has been revoked by the CSP). If such a service is offered, the service SHALL be deployed in a privacy-preserving way such that the CSP is not alerted to the use of a specific attribute bundle at a specific RP. ^63c-5-1-1-2

### 63C §5.3 Trust Agreements

- **63C-5.3-1** SHALL — The release of subscriber attributes SHALL be managed using a runtime decision managed by the wallet, as described in Sec. 4.6.1.3. ^63c-5-3-1
- **63C-5.3-2** SHALL — The authorized party SHALL be the subscriber. ^63c-5-3-2
- **63C-5.3-3** SHALL — The following terms SHALL be disclosed to the subscriber during the runtime decision: The set of subscriber attributes, derived attributes, and attribute bundles that the RP will request (a subset of the attributes made available) The purpose of each attribute requested by the RP ^63c-5-3-3
- **63C-5.3-4** MAY — The xALs required by the RP MAY also be disclosed to the subscriber at runtime. ^63c-5-3-4

### 63C §5.3.1 CSPs and RPs

- **63C-5.3.1-1** SHALL — Trust between the CSP and RP in subscriber-controlled wallet scenarios will not typically be bidirectional. In the general case, the RP trusts the CSP as the source of attribute bundles that are presented by subscriber-controlled wallets during a federation transaction, while the CSP is not expected to have direct knowledge of the RP. This trust relationship between the RP and CSP MAY be facilitated by a federation authority (see Sec. 3.5.2) that defines overarching trust agreements between members of an ecosystem representing RPs, CSPs, and subscriber-controlled wallets. Such trust agreements SHALL contain: ^63c-5-3-1-1
- **63C-5.3.1-2** SHALL — Trust MAY also be established unilaterally by RP evaluation of publicly available information about CSPs and their processes for issuing attribute bundles. To facilitate this, CSPs SHALL publish the following information to a trusted location for RPs to evaluate: ^63c-5-3-1-2
- **63C-5.3.1-3** MAY — This information MAY be made available by a trusted third party, such as a federation authority that assesses and evaluates CSP attribute bundle issuance and makes CSP features available through a discovery service. ^63c-5-3-1-3
- **63C-5.3.1-4** MAY — Trust between RPs and CSPs MAY be accomplished in either a pre-established (see Sec. 4.3.1) or subscriber-driven fashion (see Sec. 4.3.2). For example, an RP could be statically configured to accept attribute bundles from only a specific set of CSPs for its purposes, or the RP could alternatively accept attribute bundles from any CSP by prompting the subscriber for consent at runtime. This trust relationship could also be made more explicit by the RP being provided a means of verifying CSP-approved subscriber-controlled wallet identifiers beyond the verification of the attribute bundle, such as a discovery service provided through a federation authority. ^63c-5-3-1-4

### 63C §5.3.2 CSPs and Subscriber-Controlled Wallets

- **63C-5.3.2-1** SHALL — The trust relationship between the CSP and the subscriber-controlled wallets will always be direct in nature. As such, there SHALL be a trust agreement between the CSP and the subscriber-controlled wallets into which they issue attribute bundles. At a minimum, this trust agreement SHALL include the following: ^63c-5-3-2-1

### 63C §5.3.3 RPs and Subscriber-Controlled Wallets

- **63C-5.3.3-1** SHALL — Information about the features and capabilities of a subscriber-controlled wallet can help inform the degree to which RPs trust a given transaction. This information can demonstrate confidence that the subscriber presenting an attribute bundle is the individual represented by that attribute bundle. For example, information about how the wallet locally authenticates the subscriber, protects verification keys, and enforces trust agreement requirements indicated by the CSP or RP all support improved RP federation and access decisions. As such, subscriber-controlled wallets SHALL disclose to RPs: ^63c-5-3-3-1
- **63C-5.3.3-2** MAY — This information MAY be provided at runtime or through discovery mechanisms for wallet metadata. For more on this topic, see Sec. 5.8. ^63c-5-3-3-2

### 63C §5.3.4 FAL3 for Subscriber-Controlled Wallets

- **63C-5.3.4-1** MAY — Since assertions from a subscriber-controlled wallet always contain a reference to one of the wallet’s verification keys inside the signed attribute bundle from the CSP, subscriber-controlled wallets that run on a subscriber-controlled device are capable of issuing holder-of-key assertions if all of the requirements for holder-of-key assertions are met (see Sec. 3.15). These assertions MAY be used to reach FAL3 if all requirements for FAL3 are met (see Sec. 2.4). ^63c-5-3-4-1
- **63C-5.3.4-2** SHALL — The verification keys of a subscriber-controlled wallet on a hosted service do not meet the requirements for holder-of-key assertions on their own since the subscriber is not in control of the key material as they would be on a subscriber-controlled device. To reach FAL3, federation transactions with a subscriber-controlled wallet on a hosted service SHALL use either a holder-of-key assertion (see Sec. 3.15) or a bound authenticator (see Sec. 3.16). All requirements for FAL3 in Sec. 2.4 SHALL be met. For example, a holder-of-key assertion from a subscriber-controlled wallet on a hosted service could include the verification key of an authenticator separate from the wallet verification key. The subscriber would present this additional authenticator to the RP along with the wallet’s assertion. ^63c-5-3-4-2

### 63C §5.4 Wallet Activation

- **63C-5.4-1** SHALL — The subscriber-controlled wallet SHALL require the presentation of an activation factor from the subscriber for the following actions that result in the creation of a signed artifact from the wallet’s signing keys: ^63c-5-4-1
- **63C-5.4-2** SHOULD — The subscriber-controlled wallet SHOULD require the presentation of an activation factor before any other operations that result in the creation of a signed artifact from the wallet’s signing keys. For example, using the wallet as an authenticator at AAL2 or above requires the presentation of an activation factor as per Sec. 3.2.10 of [SP800-63B]. ^63c-5-4-2
- **63C-5.4-3** MAY — The wallet MAY request the reissuance of previously issued attribute bundles from the same CSP without requiring subscriber involvement. ^63c-5-4-3
- **63C-5.4-4** SHALL — For subscriber-controlled wallets that run on a device that the subscriber controls, the submission of the activation factor SHALL be a separate operation from the unlocking of the host device (e.g., smartphone), although the same activation factor used to unlock the host device MAY be used in the activation operation. Organizations MAY relax this requirement for subscriber-controlled wallets managed by or on behalf of the CSP (e.g., via mobile device management) and that are constrained to have short, organization-determined inactivity timeouts and device activation factors that meet the above requirements. Additional discussion of activation factors for authenticators is found in Sec. 3.2.10 of [SP800-63B]. ^63c-5-4-4
- **63C-5.4-5** MAY — For subscriber-controlled wallets that are hosted on a remote service, activation of the wallet is performed using an authenticator that is registered to the wallet service. This authenticator MAY be separate from those bound to the subscriber account at the CSP. ^63c-5-4-5

### 63C §5.4.1 Key Storage

- **63C-5.4.1-1** SHALL NOT — Keys used for signing assertions SHALL NOT be synced or shared across devices, and wallet implementations SHOULD use non-exportable key storage, as discussed in Sec. 3.6.2. ^63c-5-4-1-1
- **63C-5.4.1-2** SHALL — If the wallet’s signing key is used as a holder-of-key authenticator for FAL3, the key SHALL be stored in non-exportable key storage, as discussed in Sec. 3.6.2. ^63c-5-4-1-2

### 63C §5.5 Discovery and Registration

- **63C-5.5-1** SHALL — To perform a federation transaction with a subscriber-controlled wallet, the RP SHALL first determine the attribute bundle verification key of the CSP through a secure process as stated by the trust agreement. In some systems, this is accomplished by retrieving the CSP’s attribute bundle verification keys from a URL that is known to be controlled by the CSP. In other systems, the RP is configured manually with the verification keys of the CSP before being deployed. In systems governed by multi-lateral trust agreements, this process can be facilitated by a third-party discovery and registration service, such as one provided by a federation authority. ^63c-5-5-1
- **63C-5.5-2** MAY — Parties that seek to federate MAY use a trusted third party to facilitate the discovery and registration processes if that trusted third party is identified in the trust agreement. For example, consider an ecosystem has a centralized service for managing discovery and registration. When an RP joins the ecosystem, it registers itself with the trusted service, downloads the CSP’s verification keys, and receives an identifier to use with wallets. When the CSP issues attribute bundles to the subscriber-controlled wallet, the subscriber-controlled wallet is informed where it can find the list of valid RP identifiers within the ecosystem. When the RP connects to the wallet, the wallet can verify the RP’s identifier without the RP having to register itself directly with the wallet. Likewise, the RP can trust the wallet’s verification keys by verifying the CSP’s signature over the wallet’s verification keys or identifier. ^63c-5-5-2

### 63C §5.6 Authentication and Attribute Disclosure

- **63C-5.6-1** SHALL — The decision of whether a federation transaction proceeds and, therefore, an assertion is issued and attributes are released to the RP SHALL be determined by the subscriber acting in the role of the authorized party. The decision MAY be augmented by the use of allowlists and blocklists to allow the wallet to help the subscriber make a decision based on configured policies and trust agreements. The subscriber-controlled wallet MAY remember the subscriber’s decision to allow for future actions at the same RP without separate authorization from the subscriber. The use of a stored authorization decision does not supersede the requirement for wallet activation, as discussed in Sec. 5.4. ^63c-5-6-1
- **63C-5.6-2** SHALL — The subscriber-controlled wallet MAY provide a mechanism to remember a disclosure decision by the authorized party (i.e., the subscriber) to apply to future requests from the same RP. If such a mechanism is provided, the subscriber-controlled wallet SHALL disclose to the authorized party that the storage mechanism is in use and SHALL allow the authorized party to revoke such remembered access at a future time. ^63c-5-6-2
- **63C-5.6-3** SHOULD — The subscriber-controlled wallet SHOULD provide a means to selectively disclose a subset of the attributes in the attribute bundle from the CSP. ^63c-5-6-3
- **63C-5.6-4** SHALL — The CSP SHALL provide secure and effective means of redress of subscriber complaints or problems (e.g., subscriber identifies an inaccurate attribute value, the need to invalidate attribute bundles that were previously issued to a subscriber-controlled wallet). See Sec. 3.5.3 for additional requirements and considerations for redress mechanisms. ^63c-5-6-4

### 63C §5.7 Assertion Requests

- **63C-5.7-1** SHALL — When federation transactions are initiated by the RP, the RP’s request for an assertion SHALL contain: ^63c-5-7-1

### 63C §5.8 Assertion Contents

- **63C-5.8-1** SHALL — Assertions from a subscriber-controlled wallet SHALL contain: ^63c-5-8-1
- **63C-5.8-2** MAY — Assertions MAY contain: ^63c-5-8-2
- **63C-5.8-3** SHALL — If a subscriber-controlled wallet is hosted as a remote service, the AAL of the subscriber’s current session at the hosted wallet service SHALL be provided through information contained in the assertion contents or the applicable trust agreement. In this case, the assertion SHOULD contain additional information about the authentication method used at the IdP, if available (e.g., whether the authenticator used is phishing-resistant). Some technologies that can carry this information include Vectors of Trust [RFC8485] or authentication class references in [OIDC] and [SAML]. ^63c-5-8-3
- **63C-5.8-4** MAY — The public key, key identifier, or other identifier for a holder-of-key assertion. This MAY be the same key that the subscriber-controlled wallet uses to sign the assertion. ^63c-5-8-4
- **63C-5.8-5** SHALL — The signed attribute bundle from the CSP SHALL contain: ^63c-5-8-5
- **63C-5.8-6** SHALL — If the RP subscriber account does not use an ephemeral provisioning process (see Sec. 4.6.5) or an account resolution process (see Sec. 3.8.2), the subscriber SHALL be identified in the assertion using a federated identifier (see Sec. 3.4). The issuer identifier SHALL be of the CSP that issued the signed attribute bundle, and the subject identifier SHALL be contained in the signed attribute bundle and processed in the namespace of the CSP that issued the attribute bundle. ^63c-5-8-6
- **63C-5.8-7** SHALL NOT — The signed attribute bundle from the CSP SHOULD contain a validity time window, which is defined as a period of time outside of which the attribute bundle SHALL NOT be accepted as valid by the RP for the purposes of authenticating the subscriber and starting an authenticated session at the RP. This is usually communicated by means of an expiration timestamp for the attribute bundle in addition to the issuance timestamp. ^63c-5-8-7
- **63C-5.8-8** MAY — The signed attribute bundle from the CSP MAY contain additional information about the subscriber account, such as the set of controls used to determine the IAL. ^63c-5-8-8
- **63C-5.8-9** SHALL — Additional identity attributes and derived attribute values MAY be included in the attribute bundle. These attributes SHALL be made available to the RP using a selective disclosure method if such a method is made available by the underlying attribute bundle. In selective disclosure, a subset of attributes is revealed rather than the entire set. This may be driven by a minimum set required to complete a transaction as defined by the RP or through selection by the subscriber at runtime. ^63c-5-8-9
- **63C-5.8-10** SHALL — Identity attributes that are in the assertion but outside of a signed attribute bundle SHALL be considered self-asserted. The RP MAY validate these additional attributes using its own validation process. ^63c-5-8-10

### 63C §5.9 Assertion Presentation

- **63C-5.9-1** SHALL — Assertions SHALL be presented to the RP through an authenticated protected channel. ^63c-5-9-1
- **63C-5.9-2** SHALL — The presentation SHALL include the cryptographic nonce from the RP’s request, if present (this is required at FAL2 and above). The RP SHALL verify the nonce in accordance with the federation protocol. ^63c-5-9-2
- **63C-5.9-3** SHOULD — If the presentation mechanism passes the assertion through a component other than the wallet or RP, personal information in the assertion SHOULD be encrypted by the wallet using the RP’s encryption key, as discussed in Sec. 3.13.3. ^63c-5-9-3
- **63C-5.9-4** SHOULD — To enhance privacy, the presentation mechanism SHOULD provide features to enable unlinkability of the subscriber and their information at different RPs. ^63c-5-9-4

### 63C §5.10 Assertion Validation

- **63C-5.10-1** SHALL — The RP SHALL validate the signature on all signed attribute bundles in the assertion using the verification key from the CSP that issued the signed attribute bundle. The RP SHALL validate the signature of the assertion using the verification key of the subscriber-controlled wallet contained in the signed attribute bundle. ^63c-5-10-1
- **63C-5.10-2** SHALL — The RP SHALL validate the assertion by checking that all the following are true: ^63c-5-10-2
- **63C-5.10-3** SHOULD — Additionally, if a mechanism for invalidating attribute bundles is provided by the CSP, the RP SHOULD use this mechanism to determine whether the attribute bundle has been invalidated by the CSP since its issuance, as discussed in Sec. 5.1.1. This validation mechanism is particularly suited for attribute bundles with long or indeterminate lifetimes, since proactive invalidation by the CSP could occur long before expiration of the attribute bundle. ^63c-5-10-3

### 63C §5.11 RP Subscriber Accounts

- **63C-5.11-1** SHALL — For many RPs that use wallet-based attribute bundles, the RP will use an account resolution process to link the information in the attribute bundle to a set of functionality at the RP, as discussed in Sec. 3.8.2. If the RP subscriber account is not ephemeral and a federated identifier is present, the RP SHOULD associate the federated identifier presented by the subscriber-controlled wallet with the RP subscriber account and use the federated identifier for future federated transactions with the same subscriber. If a federated identifier is not present (e.g., in the case of mDL), the RP will need to request the necessary attributes to resolve the subscriber to the RP subscriber account for each federated transaction. This attribute set SHALL be the minumum necessary to achieve accurate resolution. Linking to multiple federated identifiers SHALL be managed as discussed in Sec. 3.8.1. ^63c-5-11-1
- **63C-5.11-2** SHALL — The RP SHALL disclose its practices for managing subscriber information as part of the trust agreement. The RP SHALL provide effective means of redress to the subscriber for correcting information in the RP subscriber account. See Sec. 3.5.3 for additional requirements and considerations for redress mechanisms. ^63c-5-11-2
