# AI-Assisted Threat Intelligence Investigation  
## Infostealer Credential Exposure & Third-Party Supply Chain Risk

<p align="center">
  <img width="900" height="400" alt="ChatGPT Image Mar 4, 2026, 04_11_57 PM" src="https://github.com/user-attachments/assets/c1fc83a8-a3c1-4326-87c0-c1edfd26cf9b" />
</p>

Capstone Project – Applied AI for Cybersecurity Incident Response  

Author: James Moore  
Role: Security Analyst / Threat Intelligence Researcher  

---

# Capstone Presentation

🎥 **Watch the Full Capstone Presentation**

[<img width="1000" height="500" alt="Untitled design" src="https://github.com/user-attachments/assets/3da0fbb2-bcf0-4785-bdb2-af332a9422d4" />
](https://youtu.be/0cANdViZH8E)

---

# Table of Contents

- Executive Summary
- Investigation Methodology
- Key Findings
- Threat Actor Profile
- Infostealer Malware Ecosystem
- Threat Scenario Overview
- Attack Chain (MITRE ATT&CK Kill Chain)
- Incident Timeline
- Compromised Host Profile
- Evidence: Infostealer Log
- Corporate Credential Exposure
- Enterprise Infrastructure Identified
- Installed Software Analysis
- Initial Access Vector
- MITRE ATT&CK Mapping
- Threat Actor Opportunity
- Business Impact
- OSINT Investigation
- AI-Assisted Investigation
- Prompt Engineering Methodology
- AI Prompt Bank
- Detection Opportunities
- Defensive Recommendations
- Risk Assessment
- Lessons Learned
- Technologies Used

---


# Executive Summary

This investigation analyzes a **credential compromise scenario involving LG Electronics (LGE) infrastructure and potential third-party supply chain exposure affecting Jaguar Land Rover (JLR)**.

The case study examines evidence from **infostealer malware logs**, which show that credentials belonging to a corporate engineering environment were harvested from a compromised endpoint.

The malware collected:

• Stored browser credentials  
• Enterprise authentication tokens  
• Development environment access credentials  

The harvested data was subsequently available in an **infostealer log marketplace**, where threat actors frequently obtain credentials for enterprise intrusion.

The investigation demonstrates how **OSINT research, threat intelligence analysis, and AI-assisted prompt engineering** can be used to investigate potential enterprise credential exposure and produce a structured threat intelligence report.

---

# Investigation Methodology

This investigation followed a structured **AI-assisted SOC investigation workflow** combining traditional threat intelligence analysis with generative AI-assisted reasoning.

The workflow illustrates the analytical process used to identify the potential supply chain exposure risk.

<img width="300" height="550" alt="ChatGPT Image Mar 4, 2026, 02_09_32 PM" src="https://github.com/user-attachments/assets/55e6529e-bcc2-4f1b-addb-f4d7cab5752a" />

### Investigation Workflow Stages

1. Threat scenario definition  
2. Initial OSINT research  
3. Prompt engineering for AI analysis  
4. Infostealer log analysis  
5. Enterprise infrastructure mapping  
6. MITRE ATT&CK technique mapping  
7. Detection gap identification  
8. Threat hunting hypothesis development  
9. Mitigation playbook creation  
10. Executive risk communication  

This methodology reflects modern **SOC investigation processes used by enterprise security teams**, where AI accelerates analysis while human investigators maintain validation and oversight.

---

# Key Findings

The investigation identified evidence that:

• A **Windows 10 engineering workstation was infected by Generic Stealer malware**

• The compromised system contained **credentials associated with enterprise engineering platforms**

• The device was likely used for **remote enterprise access and development collaboration**

• Harvested credentials included **enterprise systems used by LG Electronics engineering teams**

• Exposure of these credentials presents **potential supply chain risk to partner organizations**

---

# Threat Landscape

Infostealer malware has become one of the fastest-growing sources of enterprise credential exposure.

Security researchers estimate that **millions of corporate credentials are exposed each year through infostealer log marketplaces**, enabling threat actors to gain unauthorized access to enterprise systems without exploiting software vulnerabilities.

These marketplaces operate as part of a broader cybercrime ecosystem where attackers purchase stolen credentials to perform:

• corporate network intrusion  
• account takeover attacks  
• intellectual property theft  
• ransomware deployment  
• supply chain compromise  

In many cases, attackers rely on **valid credentials rather than exploits**, allowing malicious activity to blend in with legitimate authentication behavior.

This investigation demonstrates how credential exposure from a single compromised endpoint can introduce **risk across multiple organizations connected through trusted development relationships.**

---

# Threat Actor Profile

The credential exposure scenario aligns with activity typically associated with **credential harvesting operations and initial access brokers**.

These threat actors specialize in harvesting credentials from infected endpoints and selling the data on underground markets.

### Threat Actor Characteristics

| Attribute | Description |
|---|---|
| Actor Type | Cybercriminal / Credential Access Broker |
| Primary Objective | Monetization of stolen credentials |
| Access Model | Sale of infostealer logs |
| Targeting | Corporate endpoints and development environments |

### Distribution Methods

Infostealer malware is commonly delivered through:

• phishing attachments  
• malicious downloads  
• cracked software installers  
• trojanized vendor documents  
• compromised software updates  

Once deployed, infostealer malware automatically extracts authentication data from the infected endpoint.

This model is commonly associated with **Initial Access Brokerage (IAB)** within the cybercrime ecosystem.

---

# Infostealer Malware Ecosystem

Infostealer malware has become one of the **most common credential theft mechanisms used by cybercriminal operations**.

Rather than exploiting vulnerabilities directly, attackers harvest credentials from infected systems and sell them to other threat actors.

### Infostealer Ecosystem Model

1. Malware operators distribute infostealer payloads
2. Victim systems become infected
3. Credentials and authentication tokens are harvested
4. Data is uploaded to attacker infrastructure
5. Logs are aggregated and sold on underground marketplaces
6. Buyers use stolen credentials for enterprise intrusion

### Common Infostealer Malware Families

Examples include:

• RedLine Stealer  
• Raccoon Stealer  
• Vidar Stealer  
• Azorult  
• Generic Stealer variants  

These malware families extract:

• browser stored passwords  
• authentication cookies  
• enterprise login credentials  
• development environment tokens  

Infostealers frequently serve as the **initial stage of larger enterprise attacks**, including ransomware and supply chain compromise.

---

# Threat Scenario Overview

This case models a common modern breach scenario involving **infostealer malware and credential harvesting**.

### Attack Flow

1. Employee downloads malicious file disguised as legitimate content  
2. Infostealer malware executes silently  
3. Browser credentials and session tokens are extracted  
4. Malware uploads data to attacker infrastructure  
5. Credentials are posted in underground infostealer log markets  
6. Threat actors purchase the logs  
7. Attackers authenticate directly into enterprise systems using valid credentials  

Because the attacker logs in using legitimate credentials, this technique bypasses many traditional detection controls.

---

---

# Supply Chain Attack Path

The credential exposure scenario introduces potential **supply chain risk through trusted engineering relationships**.

In this case, credentials harvested from a compromised LG Electronics engineering workstation could provide access to enterprise systems used in collaboration with Jaguar Land Rover.

<p align="center">
<img width="1000" height="500" alt="ChatGPT Image Mar 4, 2026, 04_20_55 PM" src="https://github.com/user-attachments/assets/aca5938e-1822-466b-9579-6f535328ba2d" />
</p>

### Attack Path

1. LG Electronics engineer workstation becomes infected with infostealer malware  
2. Credentials and authentication tokens are harvested  
3. Infostealer logs are uploaded to attacker infrastructure  
4. Logs are sold in underground credential marketplaces  
5. Threat actor purchases the credential dataset  
6. Attacker authenticates into enterprise systems using valid credentials  
7. Access may extend into partner development environments

Because authentication uses **valid credentials**, the activity may appear legitimate within enterprise authentication logs.

This technique has been observed in multiple real-world breaches involving **trusted third-party relationships and software development environments.**

---

# Attack Chain (MITRE ATT&CK Kill Chain)

The observed activity aligns with adversary behavior patterns defined in the **MITRE ATT&CK framework**.

<img width="650" height="400" alt="ChatGPT Image Mar 4, 2026, 03_16_58 PM" src="https://github.com/user-attachments/assets/88cc3744-ca61-4b0d-a6ab-ac9188e4b257" />

| Phase | Technique | Description |
|---|---|---|
| Initial Access | T1566 | Phishing or malicious download |
| Execution | T1204 | User executes malicious file |
| Credential Access | T1056 | Infostealer harvests credentials |
| Credential Dumping | T1555 | Browser password extraction |
| Persistence | T1078 | Valid credentials reused |
| Supply Chain Risk | T1199 | Trusted relationship exploitation |

---

# Incident Timeline

| Date | Event |
|-----|------|
| July 8, 2021 | Host system infected with infostealer malware |
| Aug 8, 2021 | Initial detection recorded in infostealer log |
| Sept 2022 | Infostealer data still available in log marketplace |
| Investigation Period | OSINT and threat intelligence analysis performed |

---

# Compromised Host Profile

| Attribute | Value |
|---|---|
| Hostname | DESKTOP-BBJ8T6T |
| Operating System | Windows 10 Pro x64 |
| Malware Family | Generic Stealer |
| Antivirus | Not Detected |
| Initial Detection | Aug 8, 2021 |

---

# Evidence: Infostealer Log

<img width="1600" height="500" alt="Untitled design" src="https://github.com/user-attachments/assets/5b7cfdff-5050-4966-a6e8-429dc750d6c2" />

Sanitized report and removed internal infrastructure details and screenshots

## Evidence Source

During this investigation, a security observation was identified that contained sensitive information related to enterprise development infrastructure.

Due to responsible disclosure practices, specific infrastructure details and screenshots have been removed from this public report.

The incident demonstrates how operational tooling such as issue tracking systems can inadvertently become a source of credential exposure.

This case reinforces the importance of:

• Secrets management policies  
• Data classification controls  
• Internal monitoring of collaboration tools  
• Automated scanning for sensitive information in tickets and repositories


This log indicates the compromised device contained **corporate authentication credentials and enterprise system access tokens**.

---

# Corporate Credential Exposure

Example credential discovered in the infostealer dataset:

```
URL:
https://jira.sd...........x

Credential Type:
Corporate Jira Account

Password Strength:
Weak
```

This suggests the compromised endpoint had access to **enterprise development infrastructure**.

---

# Enterprise Infrastructure Identified

### Infrastructure Observed in Infostealer Logs (Sanitized)

The infostealer data referenced several enterprise systems associated with the affected organization. 
To adhere to responsible disclosure practices, all internal infrastructure hostnames have been generalized.

Observed system categories included:

• code-repository.[enterprise-domain]  
• collaboration.[enterprise-domain]  
• source-control.[enterprise-domain]  
• software-management.[enterprise-domain]  
• vpn-gateway.[enterprise-domain]  
• internal-portal.[enterprise-domain]  
• training-platform.[enterprise-domain]  

Note: Original hostnames have been removed to prevent disclosure of sensitive enterprise infrastructure.

---

# Installed Software Analysis

Installed applications provide insight into the role of the compromised system.

Examples identified:

• Citrix Workspace  
• Chrome browser  
• Foxit Reader  
• Microsoft Visual C++ libraries  
• Graphviz  

These applications suggest the device was used for:

• enterprise remote access  
• engineering work  
• development collaboration

---

# Initial Access Vector

The most likely initial access vector is **malicious file execution**.

Possible delivery methods include:

• phishing attachments  
• compromised vendor documents  
• malicious software downloads  
• trojanized engineering tools  

Once executed, the malware extracts credentials from:

• browser password stores  
• authentication cookies  
• enterprise login sessions

---

# MITRE ATT&CK Mapping

| Technique | Name | Description |
|---|---|---|
| T1566 | Phishing | Initial malware delivery |
| T1204 | User Execution | Victim executes malicious file |
| T1056 | Credential Harvesting | Malware captures credentials |
| T1555 | Credentials from Password Stores | Browser credential extraction |
| T1078 | Valid Accounts | Stolen credentials used for login |
| T1199 | Trusted Relationship | Supply chain compromise risk |

---

# Threat Actor Opportunity

An attacker possessing these credentials could potentially:

• Access internal engineering systems  
• Modify development workflows  
• Access intellectual property  
• Pivot into partner environments  
• Establish persistence through trusted access  

Because authentication uses valid credentials, malicious activity may appear indistinguishable from legitimate user behavior.

---

# Business Impact

The credential exposure identified in this investigation presents several potential operational and security risks for organizations involved in the affected engineering environment.

Because the compromised credentials belong to an enterprise engineering workstation, unauthorized access could allow attackers to interact with development infrastructure used for software collaboration and internal engineering workflows.

### Potential Organizational Risks

• Unauthorized access to internal development platforms  
• Exposure of proprietary engineering documentation  
• Unauthorized modification of development workflows  
• Intellectual property theft  

### Supply Chain Risk

The presence of credentials associated with engineering collaboration platforms introduces potential **third-party supply chain risk**.

If an attacker successfully authenticates using these credentials, they may gain access to systems used to collaborate with partner organizations.

This creates the possibility for attackers to:

• Access shared development environments  
• Manipulate software development artifacts  
• Introduce malicious code into trusted development pipelines  

### Detection Challenges

Because attackers authenticate using **valid credentials**, malicious activity may appear legitimate within authentication logs and user access records.

This makes credential exposure particularly dangerous, as traditional security controls designed to detect malware or exploits may not identify unauthorized activity performed through legitimate accounts.

### Strategic Security Considerations

Organizations should treat **credential exposure events as high-priority security incidents**, even when no persistent malware is detected within enterprise systems.

Rapid credential rotation, identity monitoring, and authentication anomaly detection are critical steps in mitigating the risk posed by credential harvesting malware.

---

# OSINT Investigation

Open-source intelligence techniques were used to identify:

• domain ownership  
• infrastructure purpose  
• enterprise system relationships  
• potential exposure risk  

OSINT analysis confirmed that many referenced domains correspond to **LG Electronics engineering infrastructure**.

---

# AI-Assisted Investigation

Generative AI prompt engineering was used to accelerate:

• log interpretation  
• infrastructure mapping  
• threat modeling  
• MITRE ATT&CK classification  
• investigative reporting

AI acted as an **analysis accelerator**, while human analysts maintained validation.

---

# Prompt Engineering Methodology

### Example Threat Intelligence Prompt

```
You are a cybersecurity threat intelligence analyst.

Analyze the following infostealer log data and determine:

1. Whether the credentials belong to a corporate environment
2. What enterprise systems the credentials may provide access to
3. Potential supply chain risk
4. Relevant MITRE ATT&CK techniques
```

---

### Example OSINT Prompt

```
Act as an OSINT analyst investigating enterprise infrastructure.

Analyze the domain:

jira.sdo.jlrmotor.com
```

---

# AI Prompt Bank

A shared prompt library guided analysis.

Categories included:

• threat intelligence prompts  
• OSINT prompts  
• credential exposure analysis  
• MITRE ATT&CK mapping prompts  
• risk assessment prompts

---

# Detection Opportunities

Organizations could detect similar incidents using:

• impossible travel authentication alerts  
• abnormal Jira login detection  
• new device authentication alerts  
• VPN anomaly detection  
• credential exposure monitoring

---

# Defensive Recommendations

### Identity Security

• enforce multi-factor authentication  
• implement conditional access policies  
• rotate compromised credentials

### Endpoint Security

• deploy EDR monitoring  
• detect infostealer malware indicators  
• disable browser credential storage

### Supply Chain Security

• enforce least privilege vendor access  
• monitor partner authentication activity  
• perform regular credential exposure scans

---

# Risk Assessment

The exposed credentials introduce several enterprise risks.

### Enterprise Risks

• unauthorized engineering system access  
• intellectual property exposure  
• development environment manipulation  

### Supply Chain Risks

Because the compromised environment contained engineering platform credentials, the exposure introduces **third-party supply chain risk**.

Attackers frequently exploit trusted development relationships to pivot into partner organizations.

---

# Lessons Learned

Infostealer malware is one of the **most effective credential theft techniques used by threat actors**.

Attackers increasingly rely on **credential theft rather than vulnerability exploitation**.

Supply chain relationships significantly expand attacker opportunity.

AI-assisted analysis can accelerate **threat intelligence investigations and reporting**.

---

# Technologies Used

• OSINT research tools  
• Infostealer log analysis  
• MITRE ATT&CK framework  
• Generative AI prompt engineering  
• Threat intelligence workflows

---

# Author

James Moore  
Cybersecurity Analyst  

Threat Intelligence • Vulnerability Management • Security Operations
