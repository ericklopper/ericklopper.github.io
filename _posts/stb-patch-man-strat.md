#   SCM, SCOM and SCCM PATCH AND Security Update STRATEGY

    Version 1.0

###         Contents

0.  Contents                                    2
1.	Control Sheet	                            3
        Authors	                                3
        Revisions	                            3
        Approvals	                            4
2.	Introduction	                            5
      1.    Overview and purpose	            5
      2.    Scope                               5
      3.    Audience	                        5
      4.    Role(s)? and responsibilities	        6
      5.    SQL Server versions	                6
3.	Patching strategy and rationale	            7
      1.    Strategy	                        7
      2.    Patching frequency and rationale	7
      3.    High level patch process	        8


1. Control Sheet

###         Authors

Please refer any queries regarding this document to the authors listed below:

         Name           | Role |Contact Details
------------------------|------|-------------------------------------------
Christopher Cullingworth|-ITSO-|Christopher.cullingworth@standardbank.co.za

Revisions | Date | Version | Changes | Author
----------|----------|----------|-----------|----------
 | 09-02-2016 | V1.0 | Initial Draft | Christopher Cullingworth

###         Approvals

Name:
Byron Ennion
Designation
Head: IT Security
Signature:

Date:


Name:
Kaveer Ramjathan
Designation
EUC Services: Head
Signature:

Date:


Name:
Caldon Thomson
Designation
Cyber Intelligence: Head
Signature:

Date:


Name:
Rashida Khan
Designation
IT Security Operations: Head
Signature:

Date:



2. Introduction
2.1 Overview and purpose
The primary goal of this strategy is to ensure the application of ongoing security fixes that resolve vulnerabilities leading to the exfiltration of information, execution of arbitrary code and ultimately the persistent compromise of any critical or key infrastructure services and devices on which they operate.
2.2 Scope
This strategy applies to Microsoft SCM, SCOM and SCCM servers owned or managed by the EUC infrastructure team/s as well as any additional teams that may be required to support the security patching process. The following patches form the basis of this strategy;
Patch Type
Patch Description
Release Schedule
CRITICAL
A vulnerability which, if exploited, could allow code execution without any user intervention. These scenarios include self-propagating malware
< 1 week after release
Important
A vulnerability whose exploitation could result in the compromise of confidentiality, integrity or availability of data.
< 4 weeks after release
Moderate
Impact of the vulnerability is mitigated by factors such as authentication prompts or non default configurations
< 4 weeks after release
Low
Impact of the vulnerability is almost completely mitigated by characteristics of the affected component.
< 4 weeks after release
	
2.3 Audience
All business units and personnel involved in the installation, maintenance, security and management of SCM, SCOM and SCCM services including the servers, on which they reside.








2.4 role and responsibilities
To conform to the Group adopted Vulnerability Management frameworks, policies and standards, the roles for the on going vulnerability remediation will be distributed as follows;
2.4.1 Vendor - Microsoft
Microsoft, being the vendor of the SCM, SCOM and SCCM products, develop and release updates. The update release frequency for these products may vary as they are highly dependant on disclosure. To ensure maximised availability, integrity and accessibility updates rated as Critical will be applied in test environments (UAT) within 7 days of release. Updates that do not mitigate or remediate any vulnerability or system exposure will only be installed when a Service Pack is released.
2.4.2 Software Deployment Team (SCCM)
The SCCM Team are responsible for;
Participating in the current standing Microsoft RAG session.
Download updates
Installing Updates 
Regularly Report on Device Compliance
Patch or Client Agent related Queries
2.4.3 EUC Team
The EUC team is responsible for: 
Participation in the current standing Microsoft RAG session where SCM, SCOM and SCCM server patches have been released
Allocating UAT hosts where testing can be done
Testing SCM, SCOM and SCCM environments for anomalies after updates have been applied
Reporting application anomalies after updates
Application based troubleshooting
Restarting of Services where required
2.4.4 Standard Bank Vulnerability Management Team
The Standard Bank Vulnerability Management Team is responsible for the following:
Hosting the Microsoft RAG session after Microsoft patch Tuesday releases
Management of deviations
Identifying vulnerabilities within the environment





2.4.5 IT Security 
IT Security are responsible for the following:
Ensuring compliance to this strategy
Attending the Microsoft RAG
Advisory service in terms of;
Governance
Regulatory Requirements
Statutory Requirements
Vulnerability Management
2.5 SCM, SCOM and SCCM Service versions
SCM, SCOM and SCCM follow the current approved methodology of n-1 for application versioning, meaning the environment should operate, at a minimum, one version prior to the latest release of the product.
Service Packs must be scheduled for installation within 30 days of release.
3. patching strategy and rationale

3.1 strategy
Ensure maximised system confidentiality, availability and integrity through regular and ongoing code correction. Furthermore maximised automation will lesson human resource consumtion and financial implication. 
3.2 patching frequency and rationale
The increasing number in Microsoft Windows releated cybercrime implies a need for ongoing control review and corrective configurational changes to be applied. The application of updates ensures vulnerability exposure is kept to the utmost minimum and introduces and increased level of security to the application.
It is important to note that the severity rating of vulnerabilities assigned by Microsoft is based on the inherent risk profile in the typical / average installation and does not take into account compensating controls that may be present within the environment which lowers the residual risk. These compensating controls are, but not limited to: security monitoring, logical access management, privileged user management, network security and antivirus.
Based on the chosen patch strategy and the controls for ensuring a regulated deployment frequency below will be followed: 
Patch Type
Severity Classification
Deployment Frequency
Security
Critical and High – Potential for significant impact in SBG and/or has known reported attacks.
Within 10 days after release.

Medium – Exploitable vulnerabilities. Easy to detect, easy to exploit / implement
Within 10 days after release.

Low and informational – Minimal impact to Standard Bank and/or difficult to exploit and potentially easy to detect.
Applied through installation of Service Packs or on request by application
Service Packs
Consists of packaged updates and cannot be measured accurately for severity. May also include driver and or feature packs.
Within 1 month after release.
Note: The timelines above are indicative of when and where the patch poses a risk to availability of the database and/or application, further testing will be conducted which may result in these timelines being breached.

3.3 high level patch process
This section provides a high-level overview of the process: 
1. Microsoft release patches on Microsoft Patch Tuesday, the second Tuesday of every month.
2. The RAG committee will convene within 7-working days to review the released patches.
3. Patches that have been approved for deployment by the RAG committee will be sent to the software deployment team.
4. The patches will be applied on the servers allocated for testing. 
5. SCM, SCOM and SCCM teams and Application Testers will test the applications and services for any negative affect.
6. In the event of a incident, root cause analysis is applied to impacted services, servers or applications
7. Successfully tested patches are applied to production environments
8. Failed patches are loaded for exclusion through deviation process. 
3.3 Exceptions
Any deviation to this strategy will be viewed as being in violation of the Vulnerability Management Standard and must conform to the formal exception process. Exceptions may be requested through the following url;
http://sharepoint.standardbank.co.za/sites/sd/Teamtrack/Webpages/TeamTrack%20Website.aspx



