# Cloud Security Framework

5 functions as stated in the NIST CSF with adaptation to focus on 16 infrastructure-related domains. 

Items are defined according to their priority levels: Foundation (60 criteria), Secure (39 criteria), Hardened (14 criteria) resulting in an overall 113 security requirements.

Items are mapped to existing security labels as well as the Public Cloud Requirements (PCR). The following were not mapped as their definitions are too specific.

R.42 R.22
PCR.36

In the shared responsibility model, GTS can delegate these controls execution while keeping an overall audit capability and regular reporting from delegates. Attribution still need to be defined.

Unmapped: G-014, VNS-002 (unclear), HYS-001, HOS-002, AS-004, IAM-004, 

Consider reading the mapping to older versions and referential only if you have performed an assessment to previous document, otherwise it can be ignored.

## (ID) Identify

### ID. Assets management & Documentation

- **Assets inventory**

	- Assets must be identified, classified and consistently managed with their business value. Inventory referential is regularly updated (and ideally dynamically updated) and covers Software and Hardware assets.

		- 1

- **Architecture Documentation**

	- System architecture is documented and details security claims and measures.

		- 1

- **Data flow documentation**

	- Network architecture diagrams shall identify data flows between system components and with external network (eg. Internet). 

		- 1

### ID. Risk Assessment & Management

- **Security baseline defined

	- Baseline security requirements shall be established for all IT components (infra, app) and be aligned with regulatory obligations. Deviations from standard baseline configurations must be authorized and documented. Organization and governance shall be adapted to enforce the identified baseline

		- 1

- **Risk assessment and monitoring

	- Aligned with the enterprise-wide framework, formal risk assessments shall be performed at planned intervals or in conjunction with any changes to app/information system. Management should be involved in high risks review.

		- 1

- **Risk mitigation/acceptance

	- Risks shall be mitigated to an acceptable level. Otherwise, Acceptance conditions shall be approved by stakeholder and *documented*. Process is established for risk tolerance, the associated decision making flow, and communication.

		- 1

- **Data-focus risk assessment

	- When sensitive data are handled, Data-Focus risk assessment shall be conducted (where it is stored and transmitted, enforcement of retention period, disposal, Confidentiality, Integrity, Availability, Traceability)

		- 2

- **Risk assessment continuous improvement**

	- Risk assessment results shall include updates to security policies, procedures, standards, and controls to ensure that they remain relevant and effective.

		- 3

### ID. Supply Chain Risk Management

- **Communication on external implication**

	- If external entities are involved on managing the information system, information shall be shared within the organization.

		- 1

- **Security responsibility model**

	- Responsibility model (ie. shared responsibility) is defined with partners and providers regarding information security requirements. If internal entities are acting as service provider, this item shall be covered as well.

		- 1

- **Provider compliance**

	- Third-party service providers shall demonstrate compliance with information security and confidentiality, access control, service definitions, and delivery level agreements and formalized in third-party contracts. Resulting reports shall undergo audit and review at least annually.

		- 1

- **Provider security information**

	- The providers shall make security incident information available to all affected customers and periodically supply it through appropriate methods (e.g., newsletter, portals).

		- 2

- **Provider Internal assessment**

	- The provider shall perform annual internal assessments of conformance to, and effectiveness of, its policies, procedures, and technical means regarding information security and share the results. Providers shall apply a risk assessment, management and governance processes and share the results.

		- 2

### ID.GV. Governance, Audit Assurance & Compliance

- **Regulation compliance**

	- Information System shall be mapped to regulation requirements (eg. GDPR) using an organization level control framework and perform an annual review.

		- 1

- **Regulation-related roles and requirements**

	- Policies and procedures in place with cyber security responsibilities identified and legal, regulatory or operational requirements identified.

		- 1

- **Logs and information retention**

	- Information Retention policy is identified and implemented using proper mechanisms and aligned with business or regulation requirements.

		- 1

- **Data localization control**

	- Data localization laws and constraints have been identified and proper controls in place

		- 1

- **Reversibility Plan**

	- A reversibility plan must defined when migrating workloads or data to cloud infrastructure

		- 1

- **Audit and admin account/tools**

	- Audit capabilities (tools, accounts, etc.) are available within the organization for qualified personnel.

		- 2

- **Proper usage of audit tools**

	- Access to, and use of, audit tools that interact with the organization's information systems shall be appropriately segregated and access restricted to prevent inappropriate disclosure or tampering with log data.

		- 2

- **Audit management and planning**

	- Audits are planned at regular intervals or aligned with relevant change to information system, and handled by independent entities.

		- 2

- **Management cyber security responsibilities**

	- Managers are responsible for maintaining awareness of, and complying with, security policies, procedures, and standards that are relevant to their area of responsibility.

		- 2

- **Pen-test/Code audit**

	- A pen-test/audit is performed at relevant intervals. The level and coverage (black box, white box, code review) are adapted to data classification and environment considerations. This operation shall be conducted by external teams to ensure objectivity.

		- 2

## (PR) Protect

### PR. Operations, Change Control & Maintenance

- **Change control**

	- Change control and configuration management policies and procedures are established, implemented and includes quality testing and gates. This should cover common best practices such as versioning, audit log and release management work flow.

		- 1

- **Unauthorized software restricted**

	- Policies, procedures and tools shall be established to restrict the installation of unauthorized software on organization-owned resources. Outliers assets shall be detected. 

		- 1

- **Peer review for code and sensitive operations**

	- Peer review for production code change and any production-related sensitive actions is enforced (4 eyes principle). When possible and applicable, this should be the default behavior.

		- 1

- **Maintenance/operation secure workflow**

	- Maintenance and repair of assets are performed and logged using approved and validated tools and process.

		- 1

- **Incident response & management process**

	- Policies shall be established, and supporting business processes and technical measures implemented, to filter security-related events and ensure timely and thorough incident response.|(eg. operational playbook, DRP, etc.) Response and recovery plan is defined and tested.

		- 1

- **Partners change control managed**

	- External partners adhere to the same policies and procedures for change control as the organization. Otherwise, internal teams shall have the process and tools to handle changes on external dependencies.

		- 2

- **Exploitation documentation available**

	- System exploitation documentation is available and regularly updated to ensure business continuity, skillset transfer and a standardized new joiner on-boarding.

		- 2

- **Recovery process defined and tested**

	- Data/configuration backups are regularly conducted. System/data recovery process identified and tested.

		- 2

### PR. Data Security & Information protection

- **Data classification**

	- Data classification is performed and includes sensitivity, criticality and ownership.

		- 1

- **Avoid Client data in non-prod env**

	- Client Production data shall not be replicated or used in non production environments. Any exception should be justified, approved and traced.

		- 1

- **Data Center security**

	- Data Center security policy is identified and enforced. If this managed by external providers, this shall be covered by provider compliance checks.

		- 1

- **Keys and secrets management**

	- Keys shall be handled using approved and secure platforms. Keys management and key usage shall be separated duties.  Limiting the number of secret management solutions is advised

		- 1

- **Encryption in transit**

	- Using approved cipher suites and algorithms, and as per applicable regulatory compliance, data shall be encrypted in transit (over system interfaces, networks). 

		- 1

- **PKI implementation**

  Note: might be an issue for public cloud

	- PKI management process and technical means are in place and implementation according to industry best practices. CA private keys (Root, Intermediates) shall be considered as critical information and protected accordingly. 

		- 1

- **Personal Data protection**

	- Assuming data breach, limit the personal data collected and ensure tokenization/anonymization for sensitive data

		- 1

- **Workstation/workspace security**

	- Workstation and workspaces (mobile, virtual) interacting with the information system shall be properly secured according to organization policy. Processes and policies should be regularly reviewed.

		- 1

- **Keys policy enforced**

	- Keys/secrets policy is defined and implemented including keys expiration, rotation and revocation.

		- 2

- **Encryption at rest**

	- Using approved cipher suites and algorithms, and as per applicable regulatory compliance, data shall be encrypted at rest (in storage).

		- 2

- **Secure data deletion**

	- Data lifecycle established and technical measures are in place to ensure secure disposal (ie. data shall not be recoverable by any forensic means).

		- 2

- **Data leakage prevention**

	- Data leakage prevention process and technical means are in defined and implemented. 

		- 1

- **Encryption in memory**

	- Using approved cipher suites and algorithms, and as per applicable regulatory compliance, data shall be encrypted in use (memory).

		- 3

- **Default encryption**

	- Encryption shall be in the default configuration for data in transit and at rest.

		- 2

- **Data integrity controls**

	- Integrity checking mechanisms are defined and implemented (data, software, firmware, etc.) 

		- 3

### PR. Awarness & Training

- **Security awareness program**

	- A security awareness training program shall be established for all contractors, third-party users, and employees of the organization and mandated when appropriate. All individuals with access to organizational data shall receive appropriate awareness training and regular updates in organizational procedures, processes, and policies relating to their professional function relative to the organization.

		- 1

- **Security training per duty**

	- Personnel are provided cybersecurity awareness training to perform their cybersecurity-related duties (dev, deploy, audit/monitor) and responsibilities consistent with related policies, procedures, and agreements.

		- 2

### PR. Identity Management & Access Control

- **Restrictive by default principle**

	- Default behavior of information system components should apply a *restricted by default* approach (eg. buckets are private by default, security groups blocking, etc.)

		- 1

- **IAM restrictive principles enforcement**

	- Separation of duties (roles) and least privileges shall be the leading principles for identity management and be enforced. RBAC based approach should be implemented. This shall apply for all components with the proper tools (provider services, API, applications, etc.)

		- 1

- **Restrictions on diagnostics and configurations tools**

	- Restricted access to diagnostic and configuration ports/interfaces shall be enforced and controlled (ie. authorized to specific individuals and applications with appropriate logs).

		- 1

- **Access traceability**

	- Audit trail for access shall be defined and implemented, indicating *who* accessed *what* and *when* it occurred.

		- 1

- **Controlling 3rd party access**

	- Third party access to resources shall be handled in compliance with organization policy while limiting access to the minimum required and enforcing monitoring and traceability.

		- 1

- **Trustability of identity systems**

	- Resources and systems used for authentication and provisioning have been reviewed for trustability and are only accessible for qualified operators and based on least privileges.

		- 1

- **Restricting tools overriding IAM controls**

	- Utility programs capable of potentially overriding IAM controls shall be restricted and properly controlled.

		- 1

- **Provisioning/credential lifecycle & tools**

	- Policies, procedures and technical measures are in defined and implemented to handle credentials lifecycle and provisioning management. (policy enforcement)

		- 2

- **Management involvement in provisioning**

	- Provisioning user access to data and organization assets shall involve organization management (review/approval) and shall include traceability.

		- 2

- **Managerial controls for the need-to-know**

  Note: consider including managerial controls performed by CoE

	- The Need to Know principle shall be applied on top of least privileges by enforcing managerial controls. Audit trails can be used for this purpose.

		- 2

- **Entitlement periodic revalidation (account policy)**

	- At planned intervals, users accesses shall be revalidated for entitlement appropriateness. This shall covers account de-provisioning as well (revocation or modification).

		- 2

- **IAM central reference**

	- Centralized IAM solution should be defined and implemented and interacts with organization tools for identity and provisioning management. This should facilitate actions and changes (CRUD) propagation.

		- 2

- **MFA on admin/control interfaces**

	- Human access to admin/control interfaces and consoles shall go through Multi-Factor Authentication. Administrative actions shall be properly traced. 

		- 2

- **Cyber security in HR process**

	- Cybersecurity is included in human resources practices (e.g., de-provisioning, personnel screening)

		- 2

- **Remote access policy**

	- Remote access to information system is properly managed according to the overall policy, with adapted restrictions on sensitive assets.

		- 3

### PR. Business Continuity

- **High Availability capabilities**

	- Resilience capabilities designed, documented, implemented and aligned with business requirements.

		- 1

- **Roles and responsibilities defined and shared**

	- Roles, responsibilities and communication channels identified and shared to ensure business continuity and proper response.

		- 1

- **Business continuity plan tested**

	- Efficiency of business continuity plan tested including security incident management.

		- 1

- **Impact analysis documented**

	- Impact Analysis has been performed and documented identifying critical components and services and indicating dependencies.

		- 2

### PR. Segregation

- **Isolation between environments**

	- Production and non-production environments shall be separated to prevent unauthorized access or changes to information assets. 

		- 1

- **Network flow constrained**

	- Ingress and Egress flows and interfaces are constrained and filtered (security groups, firewalls, VPC/vNets, etc). This should cover as well the interaction between organization IT and external ones. This should cover physical network security

		- 1

- **Secure access to admin interfaces**

	- Access to administrative consoles (eg. hypervisor management) shall be restricted, traced and based upon the principle of least privileges. It shall be supported through technical controls (e.g., Bastion, MFA, audit trails, IP address filtering, firewalls, and TLS).

		- 2

- **Network flow monitored**

	- Ingress and Egress flows and interfaces are monitored. This should cover as well the interaction between organization IT and external ones.

		- 2

- **Isolation between tenants**

	- Multi-tenant organizationally-owned or managed infrastructure shall provide capabilities for business critical assets (sensitive data) isolation, in compliance with regulation obligations. 

		- 3

### PR. System, Application & Interfaces (ie. API) security

- **Secure development/deployment with auditability**

	- SDLC practices are in place and include security considerations and reviews. Infrastructure deployment should use IaC for reproducibility, change management and audit capabilities. App design, dev, deploy & testing are done according to industry standards (eg. OWASP ASVS) & applicable legal, statutory or regulatory compliance. This should include organization validated practices for deployment (WAF, API GW, etc.)

		- 1

- **Static analysis**

	- SAST & linters are defined and implemented to assess source code for vulnerabilities. It shall block unsafe code outside development stage. Ideally, hooks should be implemented to prevent unsafe code before commit.

		- 1

- **Restrictions on source code**

	- Access to the organization's own developed applications source code shall be appropriately restricted, even for open source components (read/write/merge/push controls).

		- 1

- **Prevent committing secrets**

	- Tools and process are in place to prevent pushing secrets. As it may occur, processes should be in place to manage this incident.

		- 1

- **OS hardening**

	- Each operating system shall be hardened to provide only necessary ports, protocols, and services to meet business needs. Supporting technical controls such as: antivirus, vulnerability scan, file integrity monitoring, and logging shall be as part of their baseline. Baseline should be enforced using build standard or template. Components composing compute services (OS, Containers, Orchestrators, etc.) shall be compliant with CIS benchmark guidelines.

		- 1

- **Standard and open api when exposed**

	- Open standards shall be used when publishing APIs to ensure interoperability between components and to facilitate applications migrations. Proper documentation shall be exposed as well.

		- 1

- **Standard protocols for interactions**

	- Communications shall be made through secure (e.g., non-clear text and authenticated) and standard network protocols for the import and export of data and to manage the service. Documentation shall be made available to consumers (tenants) detailing the relevant interoperability and portability standards if applicable.

		- 1

- **Components/services hardening**

	- For packaged information system components (eg. Open source stacks, CSP services, etc.), a proper hardening should be applied according to the providers guidelines and industry best practices.

		- 1

- **Hardening continuous check**

	- Each information system component shall be configured according to hardening guidelines and its compliance continuously monitored. CIS benchmarks are the selected baselines for compute services (OS, Containers, Orchestrators, etc.) as well as for the underlying CSP.

		- 1

- **Secure Exposure to untrusted networks**

	- Exposing assets or applications to untrusted networks (eg. Internet) shall be made through secure and approved patterns (eg. cIAP)

		- 1

- **Dynamic analysis**

	- DAST is enforced for compatible app and blocks non-compliant deployment at the pre-prod stage.

		- 2

- **Secure dependencies management**

	- Applications/systems dependencies are properly managed using trusted and sanitized sources. Whitelisting is advised to manage dependencies.

		- 2

- **Integrity control**

	- Each assets handling sensitive data shall provide capabilities to ensure data integrity and its control over time.

		- 2

- **Data portability**

	- All structured and unstructured data shall be available to the customers and provided to them upon request in an industry-standard format (ie. portability). This is related to the reversibility plan

		- 2

- **Secure migration**

	- Secure and encrypted channels shall be used when migrating servers, applications, or data and, where possible, shall use a network segregated from production-level networks for such migrations.

		- 3

- **Hardened intra-system connections**

	- Hardened connections between system internal components shall be used when handling sensitive data. Mutual authentication and proper encryption shall be enforced (eg. mTLS)

		- 3

## (DE) Detect

### DE. Logs & Events detection

- **Logs policy and centralization**

	- Logging strategy shall be defined and implemented on assets. It shall indicate *who*, *when* and *what*. Logs format shall be defined and enforced to facilitate centralization and exploitation. Controls should be made to ensure logs availability and conformity.

		- 1

- **VMs/Containers *images* integrity and security controlled**

	- Integrity of virtual machine images guaranteed at all times. Any changes made to virtual machine images must be logged and an alert raised regardless of their state (e.g., dormant, off, or running). Images registry shall enforce control for write (push) operations, integrity control as well as vulnerability monitoring.

		- 1

- **Logs protection**

	- Logs protection mechanisms are defined and implemented and retention duration defined according to regulation (integrity, access control for view, privileged access for deletion).

		- 2

- **Reliable time reference for logs/events**

	- A reliable and mutually agreed upon external time source shall be used to synchronize the system clocks of all relevant information processing systems to facilitate tracing and reconstitution of activity timelines.

		- 2

- **Availability monitoring and capacity management/planning**

	- The availability, quality, and adequate capacity and resources shall be planned, prepared, and measured to deliver the required SLA in compliance with security guidelines.

		- 3

### DE. Threat detection & Continuous monitoring

- **Network events monitoring**

	- Appropriate tools shall be implemented for a timely detection of network events and allow a timely-response to network-based attacks (scans, DOS, etc.). This should cover organization internal flows as well as the interaction with external systems (eg. Internet).

		- 1

- **Vulnerabilities scanner and reporting**

	- Security vulnerability assessment tools shall be available and accommodate the virtualization technologies used (VM, containers). Risk rating tools and process should be defined and implemented with proper reporting.

		- 1

- **Cyber threat intelligence**

	- Cyber threat intelligence regarding underlying components is received from information sharing forums and sources (including cloud provider specific services when applicable) and properly processed.  

		- 1

- **Obsolescence management**

	- Obsolescence management of IT resources, to prevent vulnerabilities resulting from lack of support, including both commercial and open source components (eg. ensure active community).

		- 1

- **Malware detection & defense**

	- Anti Malware tools (Antivirus, anti-APT, Virtual patching, etc) are deployed across endpoints as well as servers, and regular review is performed.

		- 2

- **Security reports**

	- Global review of security reports is regular performed at relevant intervals.

		- 2

- **Detection process/tools regular review**

	- Detection process and tools are regularly reviewed and tested for their efficiency. 

		- 3

## (RS) Respond

### RS. Response Management

- **Compliance-related points of contact**

	- Points of contact for applicable regulation authorities shall be maintained and regularly updated (e.g., change in impacted-scope and/or a change in any compliance obligation) to ensure direct compliance liaisons have been established and to be prepared for a forensic investigation requiring rapid engagement.

		- 1

- **Workforce security reporting responsibility**

	- Workforce personnel and external business relationships shall be informed of their responsibilities and, if required, shall consent and/or contractually agree to report all information security events in a timely manner. 

		- 1

- **Communication on response**

	- Information is consistently shared with stakeholders within the identified response plan.

		- 1

- **Forensics tools and procedures**

	- Proper forensic procedures and tools, including chain of custody, are available to investigate a security incident, and for the presentation of evidence to support potential legal action.

		- 2

- **Security incident monitoring's monitoring**

	- Mechanisms shall be put in place to monitor and quantify the types, volumes, and costs of information security incidents. This should facilitate the evaluation of incidents response efficiency.

		- 3

- **Feedback on response plan**

	- Response plans incorporate lessons learned and response strategy are updated.

		- 3

### RS. Incident Analysis & Mitigation

- **Incidents mitigation**

	- Action are performed (mitigation, containment, acceptance) to prevent expansion of an event, mitigate its effects, and resolve the incident. The action plan shall be traced.

		- 2

- **Communication on security incidents**

	- Internal communication is performed on identified vulnerability and associated mitigation plan. If external entities are impacted by the security incident (eg. customer data), communication shall be made in compliance with organization process.

		- 1

- **Logs monitoring & analysis**

	- Process and technical measures shall be established to dynamically detect security incident (eg. log parsing by SIEM) with the associated scenarios and possible impacts. Alert threshold and escalation shall be identified and implemented according to business impact.

		- 2

- **Response processes execution**

	- Response processes and procedures are executed and maintained, to ensure response to detected cybersecurity incidents in a formal manner.

		- 3

- **Response Feedback included**

	- Organizational response activities are improved by incorporating lessons learned from current and previous detection and response activities.

		- 3

## (RC) Recover

### RC. Recovery Management

- **Recovery execution**

	- Recovery procedures are executed and maintained to ensure restoration of systems or assets affected by cybersecurity incidents.

		- 2

- **Internal/external coordination for recovery**

	- Restoration activities are coordinated with internal and external parties (e.g.  coordinating centers, Internet Service Providers, owners of attacking systems, victims, other CSIRTs, and vendors).

		- 2

- **Feedback on recovery**

	- Recovery planning and processes are improved by incorporating lessons learned into future activities.

		- 3

