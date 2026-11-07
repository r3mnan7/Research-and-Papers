---
tags: [control-catalog, ai-fud-whitepaper]
---
# CISA Zero Trust Maturity Model v2.0 Catalog

Built with AI assistance on November 4, 2026 from the primary source: CISA, *Zero Trust Maturity Model*, Version 2.0, April 2023 (TLP:CLEAR) [16], read from the CISA PDF. Extraction method: text with page coordinates taken from the PDF in the browser pane, column positions read from each page's own `Function | Traditional | Initial | Advanced | Optimal` header row, rows rebuilt from the function labels; footnotes and surrounding prose removed. Spot checks against the PDF: Authentication (p. 13), Networks Governance (p. 22), cross-cutting Governance (pp. 29–30). Five function names that the PDF breaks across a footnote marker were completed by hand (Device Threat Protection, Traffic Encryption, Application Threat Protections, Secure Application Development and Deployment Workflow, and one Visibility and Analytics Capability label).

**Scope note.** ZTMM is a maturity model, not a control catalog: its unit is a *function* (or cross-cutting capability) with four maturity stages. RQ3 treats the **Optimal** stage as the implemented state (see [[RQ3 Control Coverage]] Assumptions). Each function is one list item carrying a block anchor (`^ztmm-<pillar>-<function>`) so that a "ZTMM: Network Segmentation" citation in RQ3 or RQ3.1 can be checked at the stage it assumes. 40 rows: Identity 7, Devices 7, Networks 7, Applications and Workloads 8, Data 8, Cross-Cutting 3 (Tables 2–7, pp. 13–30).

**Reading the stages (CISA's definitions, p. 9, abridged).** Traditional: "manually configured lifecycles ... static security policies and solutions that address one pillar at a time ... siloed pillars of policy enforcement." Initial: "starting automation of attribute assignment and configuration of lifecycles, policy decisions and enforcement, and initial cross-pillar solutions." Advanced: "automated controls for lifecycle and assignment of configurations and policies with cross-pillar coordination; centralized visibility and identity control." Optimal: "fully automated, just-in-time lifecycles and assignments of attributes ... dynamic least privilege access (just-enough and within thresholds) ... cross-pillar interoperability with continuous monitoring."

**License.** U.S. Government work, TLP:CLEAR, distributed without restriction.

## Identity

Table 2, pp. 13–15.

- **Authentication** ^ztmm-identity-authentication
    - *Traditional:* Agency authenticates identity using either passwords or multi-factor authentication (MFA) with static access for entity identity.
    - *Initial:* Agency authenticates identity using MFA, which may include passwords as one factor and requires validation of multiple entity attributes (e.g., locale or activity).
    - *Advanced:* Agency begins to authenticate all identity using phishing-resistant MFA and attributes, including initial implementation of passwordless MFA via FIDO2 or PIV.
    - *Optimal:* Agency continuously validates identity with phishing-resistant MFA, not just when access is initially granted.
- **Identity Stores** ^ztmm-identity-identity-stores
    - *Traditional:* Agency only uses selfmanaged, on-premises (i.e., planned, deployed, and maintained by agency) identity stores.
    - *Initial:* Agency has a combination of self-managed identity stores and hosted identity store(s) (e.g., cloud or other agency) with minimal integration between the store(s) (e.g., Single Signon.).
    - *Advanced:* Agency begins to securely consolidate and integrate some self-managed and hosted identity stores.
    - *Optimal:* Agency securely integrates their identity stores across all partners and environments as appropriate.
- **Risk Assessments** ^ztmm-identity-risk-assessments
    - *Traditional:* Agency makes limited determinations for identity risk (i.e., likelihood that an identity is compromised).
    - *Initial:* Agency determines identity risk using manual methods and static rules to support visibility.
    - *Advanced:* Agency determines identity risk with some automated analysis and dynamic rules to inform access decisions and response activities.
    - *Optimal:* Agency determines identity risk in real time based on continuous analysis and dynamic rules to deliver ongoing protection.
- **Access Management (New Function)** ^ztmm-identity-access-management
    - *Traditional:* Agency authorizes permanent access with periodic review for both privileged and unprivileged accounts.
    - *Initial:* Agency authorizes access, including for privileged access requests, that expires with automated review.
    - *Advanced:* Agency authorizes needbased and session-based access, including for privileged access request, that is tailored to actions and resources.
    - *Optimal:* Agency uses automation to authorize just-in-time and just-enough access tailored to individual actions and individual resource needs.
- **Visibility and Analytics Capability** ^ztmm-identity-visibility-and-analytics-capability
    - *Traditional:* Agency collects user and entity activity logs, especially for privileged credentials, and performs some routine manual analysis.
    - *Initial:* Agency collects user and entity activity logs and performs routine manual analysis and some automated analysis, with limited correlation between log types.
    - *Advanced:* Agency performs automated analysis across some user and entity activity log types and augments collection to address gaps in visibility.
    - *Optimal:* Agency maintains comprehensive visibility and situational awareness across enterprise by performing automated analysis over user activity log types, including behavior-based analytics.
- **Automation and Orchestration Capability** ^ztmm-identity-automation-and-orchestration-capability
    - *Traditional:* Agency manually orchestrates (onboards, offboards, and disables) self-managed identities (users and entities), with little integration, and performs regular review.
    - *Initial:* Agency manually orchestrates privileged and external identities and automates orchestration of non-privileged users and of self-managed entities.
    - *Advanced:* Agency manually orchestrates privileged user identities and automates orchestration of all identities with integration across all environments.
    - *Optimal:* Agency automates orchestration of all identities with full integration across all environments based on behaviors, enrollments, and deployment needs.
- **Governance Capability** ^ztmm-identity-governance-capability
    - *Traditional:* Agency implements identity policies (authentication, credentials, access, lifecycle, etc.) with enforcement via static technical mechanisms and manual review.
    - *Initial:* Agency defines and begins implementing identity policies for enterprise-wide enforcement with minimal automation and manual updates.
    - *Advanced:* Agency implements identity policies for enterprise-wide enforcement with automation and updates policies periodically.
    - *Optimal:* Agency implements and fully automates enterprisewide identity policies for all users and entities across all systems with continuous enforcement and dynamic updates.

## Devices

Table 3, pp. 17–19.

- **Policy Enforcement & Compliance Monitoring (New Function)** ^ztmm-devices-policy-enforcement-compliance-monitoring
    - *Traditional:* Agency has limited, if any, visibility (i.e., ability to inspect device behavior) into device compliance with few methods of enforcing policies or managing software, configurations, or vulnerabilities.
    - *Initial:* Agency receives self - reported device characteristics (e.g., keys, tokens, users, etc., on the device) but has limited enforcement mechanisms. Agency has a preliminary, basic process in place to approve software use and push updates and configuration changes to devices.
    - *Advanced:* Agency has verified insights (i.e., an administrator can inspect and verify the data on device) on initial access to device and enforces compliance for most devices and virtual assets. Agency uses automated methods to manage devices and virtual assets, approve software, and identify vulnerabilities and install patches.
    - *Optimal:* Agency continuously verifies insights and enforces compliance throughout the lifetime of devices and virtual assets. Agency integrates device, software, configuration, and vulnerability management across all agency environments, including for virtual assets.
- **Asset & Supply Chain Risk Management (New Function)** ^ztmm-devices-asset-supply-chain-risk-management
    - *Traditional:* Agency does not track physical or virtual assets in an enterprise-wide or crossvendor manner and manages its own supply chain acquisition of devices and services in ad hoc fashion with a limited view of enterprise risks.
    - *Initial:* Agency tracks all physical and some virtual assets and manages supply chain risks by establishing policies and control baselines according to federal recommendations using a robust framework, (e.g., NIST SCRM.)
    - *Advanced:* Agency begins to develop a comprehensive enterprise view of physical and virtual assets via automated processes that can function across multiple vendors to verify acquisitions, track development cycles, and provide third-party assessments.
    - *Optimal:* Agency has a comprehensive, ator nearreal-time view of all assets across vendors and service providers, automates its supply chain risk management as applicable, builds operations that tolerate supply chain failures, and incorporates best practices.
- **Resource Access (Formerly Data Access)** ^ztmm-devices-resource-access
    - *Traditional:* Agency does not require visibility into devices or virtual assets used to access resources.
    - *Initial:* Agency requires some devices or virtual assets to report characteristics then use this information to approve resource access.
    - *Advanced:* Agency’s initial resource access considers verified device or virtual asset insights.
    - *Optimal:* Agency’s resource access considers real-time risk analytics within devices and virtual assets.
- **Device Threat Protection (New Function)** ^ztmm-devices-device-threat-protection
    - *Traditional:* Agency manually deploys threat protection capabilities to some devices.
    - *Initial:* Agency has some automated processes for deploying and updating threat protection capabilities to devices and to virtual assets with limited policy enforcement and compliance monitoring integration.
    - *Advanced:* Agency begins to consolidate threat protection capabilities to centralized solutions for devices and virtual assets and integrates most of these capabilities with policy enforcement and compliance monitoring.
    - *Optimal:* Agency has a centralized threat protection security solution(s) deployed with advanced capabilities for all devices and virtual assets and a unified approach for device threat protection, policy enforcement, and compliance monitoring.
- **Visibility and Analytics Capability** ^ztmm-devices-visibility-and-analytics-capability
    - *Traditional:* Agency uses a physically labeled inventory and limited software monitoring to review devices on a regular basis with some manual analysis.
    - *Initial:* Agency uses digital identifiers (e.g., interface addresses, digital tags) alongside a manual inventory and endpoint monitoring of devices when available. Some agency devices and virtual assets are under automated analysis (e.g., software-based scanning) for anomaly detection based on risk.
    - *Advanced:* Agency automates both inventory collection (including endpoint monitoring on all standard user devices, e.g., desktops and laptops, mobile phones, tablets, and their virtual assets) and anomaly detection to detect unauthorized devices.
    - *Optimal:* Agency automates status collection of all networkconnected devices and virtual assets while correlating with identities, conducting endpoint monitoring, and performing anomaly detection to inform resource access. Agency tracks patterns of provisioning and/or deprovisioning of virtual assets for anomalies.
- **Automation and Orchestration Capability** ^ztmm-devices-automation-and-orchestration-capability
    - *Traditional:* Agency manually provisions, configures, and/or registers devices within the enterprise.
    - *Initial:* Agency begins to use tools and scripts to automate the process of provisioning, configuration, registration, and/or deprovisioning for devices and virtual assets.
    - *Advanced:* Agency has implemented monitoring and enforcement mechanisms to identify and manually disconnect or isolate non-compliant (vulnerable, unverified certificate; unregistered mac address) devices and virtual assets.
    - *Optimal:* Agency has fully automated processes for provisioning, registering, monitoring, isolating, remediating, and deprovisioning devices and virtual assets.
- **Governance Capability** ^ztmm-devices-governance-capability
    - *Traditional:* Agency sets some policies for the lifecycle of their traditional and peripheral computing devices and relies on manual processes to maintain (e.g., update, patch, sanitize) these devices.
    - *Initial:* Agency sets and enforces policies for the procurement of new devices, the lifecycle of non-traditional computing devices and virtual assets, and for regularly conducting monitoring and scanning of devices.
    - *Advanced:* Agency sets enterprise-wide policies for the lifecycle of devices and virtual assets, including their enumeration and accountability, with some automated enforcement mechanisms.
    - *Optimal:* Agency automates policies for the lifecycle of all network-connected devices and virtual assets across the enterprise.

## Networks

Table 4, pp. 20–22.

- **Network Segmentation** ^ztmm-networks-network-segmentation
    - *Traditional:* Agency defines their network architecture using large perimeter/macrosegmentation with minimal restrictions on reachability within network segments. Agency may also rely on multi-service interconnections (e.g., bulk traffic VPN tunnels).
    - *Initial:* Agency begins to deploy network architecture with the isolation of critical workloads, constraining connectivity to least function principles, and a transition toward service-specific interconnections.
    - *Advanced:* Agency expands deployment of endpoint and application profile isolation mechanisms to more of their network architecture with ingress/egress microperimeters and servicespecific interconnections.
    - *Optimal:* Agency network architecture consists of fully distributed ingress/egress microperimeters and extensive micro-segmentation based around application profiles with dynamic just-in-time and just-enough connectivity for service-specific interconnections.
- **Network Traffic Management (New Function)** ^ztmm-networks-network-traffic-management
    - *Traditional:* Agency manually implements static network rules and configurations to manage traffic at service provisioning, with limited application performance monitoring or anomaly detection) and manual audits and reviews of profile changes for mission critical applications.
    - *Initial:* Agency establishes application profiles with distinct traffic management features and begins to map all applications to these application of static rules to all applications and performs periodic manual audits of application profile assessments.
    - *Advanced:* Agency implements dynamic network rules and configurations for resource optimization that are periodically adapted based and risk-responsive application profile assessments and monitoring.
    - *Optimal:* Agency implements dynamic network rules and configurations that continuously evolve to meet application profile needs and based on mission criticality, risk, etc.
- **Traffic Encryption (Formerly Encryption)** ^ztmm-networks-traffic-encryption
    - *Traditional:* Agency encrypts minimal traffic and relies on manual or ad hoc processes to manage and secure encryption keys.
    - *Initial:* Agency begins to encrypt all traffic to internal applications, to prefer encryption for traffic to external applications , to formalize key management policies, and to secure server/service encryption keys.
    - *Advanced:* Agency ensures encryption for all applicable internal and external traffic protocols, manages issuance and rotation of keys and certificates, and begins to incorporate best practices for cryptographic agility.
    - *Optimal:* Agency continues to encrypt traffic as appropriate, enforces least privilege principles for secure key management enterprisewide, and incorporates best practices for cryptographic agility as widely as possible.
- **Network Resilience (New Function)** ^ztmm-networks-network-resilience
    - *Traditional:* Agency configures network capabilities on a case-bycase basis to only match individual application availability demands with limited resilience mechanisms for workloads not deemed mission critical.
    - *Initial:* Agency begins to configure network capabilities to manage availability demands for additional applications and expand resilience mechanisms for workloads not deemed mission critical.
    - *Advanced:* Agency has configured network capabilities to dynamically manage the availability demands and resilience mechanisms for the majority of their applications.
    - *Optimal:* Agency integrates holistic delivery and awareness in adapting to changes in availability demands for all workloads and provides proportionate resilience.
- **Visibility and Analytics Capability** ^ztmm-networks-visibility-and-analytics-capability
    - *Traditional:* Agency incorporates limited boundary-focused network monitoring capabilities with
    - *Initial:* Agency employs network monitoring capabilities based on known indicators of
    - *Advanced:* Agency deploys anomalybased network detection capabilities to develop
    - *Optimal:* Agency maintains visibility into communication across all agency networks and
- **Automation and Orchestration Capability** ^ztmm-networks-automation-and-orchestration-capability
    - *Traditional:* Agency uses manual processes to manage the configuration and resource lifecycle for agency networks and environments with periodic integration of policy requirements and situational awareness.
    - *Initial:* Agency begins using automated methods to manage the configuration and resource lifecycle for some agency networks or environments and ensures that all resources have a defined lifetime based on policies and telemetry.
    - *Advanced:* Agency uses automated change management methods (e.g., CI/CD) to manage the configuration and resource lifecycle for all agency networks and environments, responding to and enforcing policies and protections against perceived risks.
    - *Optimal:* Agency networks and environments are defined using infrastructure-as-code managed by automated change management methods, including automated initiation and expiration to align with changing needs.
- **Governance Capability** ^ztmm-networks-governance-capability
    - *Traditional:* Agency implements static network policies (access, protocols, segmentation, alerts, and remediation) with an approach focused on perimeter protections.
    - *Initial:* Agency defines and begins to implement policies tailored to individual network segments and resources while also inheriting corporate-wide rules as appropriate.
    - *Advanced:* Agency incorporates automation in implementing tailored policies and facilitates the transition from perimeter-focused protections.
    - *Optimal:* Agency implements enterprise-wide network policies that enable tailored, local controls; dynamic updates; and secure external connections based on application and user workflows.

## Applications and Workloads

Table 5, pp. 23–25.

- **Application Access (Formerly Access Authorization)** ^ztmm-applications-application-access
    - *Traditional:* Agency authorizes access to applications primarily based on local authorization and static attributes.
    - *Initial:* Agency begins to implement authorizing access capabilities to applications that incorporate contextual information (e.g., identity, device compliance, and/or other attributes) per request with expiration.
    - *Advanced:* Agency automates application access decisions with expanded contextual information and enforced expiration conditions that adhere to least privilege principles.
    - *Optimal:* Agency continuously authorizes application access, incorporating realtime risk analytics and factors such as behavior or usage patterns.
- **Application Threat Protections (Formerly Threat Protections)** ^ztmm-applications-application-threat-protections
    - *Traditional:* Agency threat protections have minimal integration with application workflows, applying general purpose
    - *Initial:* Agency integrates threat protections into mission critical application workflows, applying
    - *Advanced:* Agency integrates threat protections into all application workflows, protecting against some
    - *Optimal:* Agency integrates advanced threat protections into all application workflows, offering real-time visibility
- **Accessible Applications (Formerly Accessibility)** ^ztmm-applications-accessible-applications
    - *Traditional:* Agency makes some mission critical applications available only over private networks and protected public network connections (e.g., VPN) with monitoring.
    - *Initial:* Agency makes some of their applicable mission critical applications available over open public networks to authorized users with need via brokered connections.
    - *Advanced:* Agency makes most of their applicable mission critical applications available over open public network connections to authorized users as needed.
    - *Optimal:* Agency makes all applicable applications available over open public networks to authorized users and devices, where appropriate, as needed.
- **Secure Application Development and Deployment Workflow (New Function)** ^ztmm-applications-secure-application-development-and-deployment-workflow
    - *Traditional:* Agency has ad hoc development, testing, and production environments with non-robust code deployment mechanisms.
    - *Initial:* Agency provides infrastructure for development, testing, and production environments (including automation) with formal code deployment mechanisms through CI/CD pipelines and requisite access controls in support of least privilege principles.
    - *Advanced:* Agency uses distinct and coordinated teams for development, security, and operations while removing developer access to production environment for code deployment.
    - *Optimal:* Agency leverages immutable workloads where feasible, only allowing changes to take effect through redeployment, and removes administrator access to deployment environments in favor of automated processes for code deployment.
- **Application Security Testing (Formerly Application Security)** ^ztmm-applications-application-security-testing
    - *Traditional:* Agency performs application security testing prior to deployment, primarily via manual testing methods.
    - *Initial:* Agency begins to use static and dynamic (i.e., application is executing) testing methods to perform security testing, including manual expert analysis, prior to application deployment.
    - *Advanced:* Agency integrates application security testing into the application development and deployment process, including the use of periodic dynamic testing methods.
    - *Optimal:* Agency integrates application security testing throughout the software development lifecycle across the enterprise with routine automated testing of deployed applications.
- **Visibility and Analytics Capability** ^ztmm-applications-visibility-and-analytics-capability
    - *Traditional:* Agency performs some performance and security monitoring of mission critical applications with limited aggregation and analytics.
    - *Initial:* Agency begins to automate application profile (e.g., state, health, and performance) and security monitoring for improved log collection, aggregation, and analytics.
    - *Advanced:* Agency automates profile and security monitoring for most applications with heuristics to identify application-specific and enterprise-wide trends and refines processes over time to address gaps in visibility.
    - *Optimal:* Agency performs continuous and dynamic monitoring across all applications to maintain enterprise-wide comprehensive visibility.
- **Automation and Orchestration Capability** ^ztmm-applications-automation-and-orchestration-capability
    - *Traditional:* Agency manually establishes static application hosting location and access at provisioning with limited maintenance and review.
    - *Initial:* Agency periodically modifies application configurations (including location and access) to meet relevant security and performance goals.
    - *Advanced:* Agency automates application configurations to respond to operational and environmental changes.
    - *Optimal:* Agency automates application configurations to continuously optimize for security and performance.
- **Governance Capability** ^ztmm-applications-governance-capability
    - *Traditional:* Agency relies primarily on manual enforcement policies for application access, development, deployment, software asset management, security testing and evaluation (ST&E) at technology insertion, patching, and tracking software dependencies.
    - *Initial:* Agency begins to automate policy enforcement for application development (including access to development infrastructure), deployment, software asset management, ST&E at technology insertion, patching, and tracking software dependencies based upon mission needs (for example, with Software Bill of Materials).
    - *Advanced:* Agency implements tiered, tailored policies enterprisewide for applications and all aspects of the application development and deployment lifecycles and leverages automation, where possible, to support enforcement.
    - *Optimal:* Agency fully automates policies governing applications development and deployment, including incorporating dynamic updates for applications through the CI/CD pipeline.

## Data

Table 6, pp. 26–28.

- **Data Inventory Management** ^ztmm-data-data-inventory-management
    - *Traditional:* Agency manually identifies and inventories some agency data (e.g., mission critical data).
    - *Initial:* Agency begins to automate data inventory processes for both on-premises and in cloud environments, covering most agency data, and begins to incorporate protections against data loss.
    - *Advanced:* Agency automates data inventory and tracking enterprise-wide, covering all applicable agency data, with data loss prevention strategies based upon static attributes and/or labels.
    - *Optimal:* Agency continuously inventories all applicable agency data and employs robust data loss prevention strategies that dynamically block suspected data exfiltration.
- **Data Categorization (New Function)** ^ztmm-data-data-categorization
    - *Traditional:* Agency employs limited and ad hoc data categorization capabilities.
    - *Initial:* Agency begins to implement a data categorization strategy with defined labels and manual enforcement mechanisms.
    - *Advanced:* Agency automates some data categorization and labeling processes in a consistent, tiered, targeted manner with simple, structured formats and regular review.
    - *Optimal:* Agency automates data categorization and labeling enterprise-wide with robust techniques; granular, structured formats; and mechanisms to address all data types.
- **Data Availability (New Function)** ^ztmm-data-data-availability
    - *Traditional:* Agency primarily makes data available from on-premises data stores with some off-site backups.
    - *Initial:* Agency makes some data available from redundant, highly available data stores (e.g., cloud) and maintains off-site backups for onpremises data.
    - *Advanced:* Agency primarily makes data available from redundant, highly available data stores and ensures access to historical data.
    - *Optimal:* Agency uses dynamic methods to optimize data availability, including historical data, according to user and entity need.
- **Data Access** ^ztmm-data-data-access
    - *Traditional:* Agency governs user and entity access (e.g., permissions to read, write, copy, grant others access, etc.) to data through static access controls.
    - *Initial:* Agency begins to deploy automated data access controls that incorporate elements of least privilege across the enterprise.
    - *Advanced:* Agency automates data access controls that consider various attributes such as identity, device risk, application, data category, etc., and are time limited where applicable.
    - *Optimal:* Agency automates dynamic just-in-time and just-enough data access controls enterprise-wide with continuous review of permissions.
- **Data Encryption** ^ztmm-data-data-encryption
    - *Traditional:* Agency encrypts minimal agency data at rest and in transit and relies on manual or ad hoc processes to manage and secure encryption keys.
    - *Initial:* Agency encrypts all data in transit and, where feasible, data at rest (e.g., mission critical data and data stored in external environments) and begins to formalize key management policies and secure encryption keys.
    - *Advanced:* Agency encrypts all data at rest and in transit across the enterprise to the maximum extent possible, begins to incorporate cryptographic agility, and protects encryption keys (i.e., secrets are not hard coded and are rotated on a regular basis).
    - *Optimal:* Agency encrypts data in use where appropriate, enforces least privilege principles for secure key management enterprise-wide, and applies encryption using up-to-date standards and cryptographic agility to the extent possible.
- **Visibility and Analytics Capability** ^ztmm-data-visibility-and-analytics-capability
    - *Traditional:* Agency has limited visibility into data including location, access, and usage, with analysis consisting primarily of manual processes.
    - *Initial:* Agency obtains visibility based on data inventory management, categorization, encryption, and access attempts, with some
    - *Advanced:* Agency maintains data visibility in a more comprehensive, enterprisewide manner with automated analysis and correlation and
    - *Optimal:* Agency has visibility across the full data lifecycle with robust analytics, including predictive analytics, that support comprehensive views of agency data and
- **Automation and Orchestration Capability** ^ztmm-data-automation-and-orchestration-capability
    - *Traditional:* Agency implements data lifecycle and security policies (e.g., access, usage, storage, encryption, configurations, protections, backups, categorization, sanitization) through manual, and potentially ad hoc, processes.
    - *Initial:* Agency uses some automated processes to implement data lifecycle and security policies.
    - *Advanced:* Agency implements data lifecycle and security policies primarily through automated methods for most agency data in a consistent, tiered, targeted manner across the enterprise.
    - *Optimal:* Agency automates, to the maximum extent possible, data lifecycles and security policies for all agency data across the enterprise.
- **Governance Capability** ^ztmm-data-governance-capability
    - *Traditional:* Agency relies on ad hoc data governance policies (e.g., for protection, categorization, access, inventorying, storage, recovery, removal, etc.) with manual implementation.
    - *Initial:* Agency defines high-level data governance policies and relies primarily on manual, segmented implementation.
    - *Advanced:* Agency begins integration of data lifecycle policy enforcement across the enterprise, enabling more unified definitions for data governance policies.
    - *Optimal:* Agency data lifecycle policies are unified to the maximum extent possible and dynamically enforced across the enterprise.

## Cross-Cutting Capabilities

Table 7, pp. 29–29.

- **Visibility and Analytics** ^ztmm-cross-cutting-visibility-and-analytics
    - *Traditional:* Agency manually collects limited logs across their enterprise with low fidelity and minimal analysis.
    - *Initial:* Agency begins to automate the collection and analysis of logs and events for mission critical functions and regularly assesses processes for gaps in visibility.
    - *Advanced:* Agency expands the automated collection of logs and events enterprise-wide (including virtual environments) for centralized analysis that correlates across multiple sources.
    - *Optimal:* Agency maintains comprehensive visibility enterprise-wide via centralized dynamic monitoring and advanced analysis of logs and events.
- **Automation and Orchestration** ^ztmm-cross-cutting-automation-and-orchestration
    - *Traditional:* Agency relies on static an d manual processes to orchestrate operations and response activities with limited automation.
    - *Initial:* Agency begins automating orchestration and response activities in support of critical mission functions.
    - *Advanced:* Agency automates orchestration and response activities enterprise-wide, leveraging contextual information from multiple sources to inform decisions.
    - *Optimal:* Agency orchestration and response activities dynamically respond to enterprise-wide changing requirements and environmental changes.
- **Governance** ^ztmm-cross-cutting-governance
    - *Traditional:* Agency implements policies in an ad hoc manner across the enterprise, with policies enforced via manual processes or static technical mechanisms.
    - *Initial:* Agency defines and begins implementing policies for enterprise-wide enforcement with minimal automation and manual updates.
    - *Advanced:* Agency implements tiered, tailored policies enterprisewide and leverages automation where possible to support enforcement. Access policy decisions incorporate contextual information from multiple sources.
    - *Optimal:* Agency implements and fully automates enterprise-wide policies that enable tailored local controls with continuous enforcement and dynamic updates.
