# OSINT & Dark Web Threat Intelligence for Corporate Security

> An academic cybersecurity project exploring the integration of Dark Web
> monitoring, OSINT, SIEM analysis and controlled vulnerability assessment
> within a simulated corporate security incident.

<p align="center">
  <img src="assets/architecture/lab-architecture.svg"
       alt="OSINT and Dark Web Threat Intelligence Lab Architecture"
       width="600">
</p>

## Overview

The continuous evolution of cyber threats requires organizations to adopt a proactive approach to protecting their information, systems, and digital assets. The **Dark Web** represents a particularly relevant source of threat intelligence, as compromised credentials, stolen data, and other sensitive information may be exchanged through services accessible via specialized networks such as Tor.

This project explores how **Open Source Intelligence (OSINT)** and **Dark Web monitoring** can be integrated into a broader corporate cybersecurity strategy to support threat identification, investigation, and incident response.

Developed as part of my Bachelor's thesis in Computer Science, the project combines theoretical research with a practical case study based on a simulated technology and financial startup affected by a security incident involving compromised employee credentials.

The case study investigates an integrated security workflow involving:

* **Dark Web monitoring and OSINT** to identify potentially exposed information and investigate external threat indicators.
* **Entity and relationship analysis** to correlate information collected from different sources.
* **SIEM and log analysis** to investigate security events within the monitored environment.
* **Controlled vulnerability assessment** to validate potential weaknesses identified during the investigation.
* **Mitigation and continuous monitoring** to reduce exposure and improve the organization's security posture.

The practical environment was implemented as an isolated virtualized lab, separating **OSINT/Dark Web monitoring**, **SIEM and log management**, and **penetration-testing activities** into dedicated environments.

The project demonstrates how external threat intelligence can complement internal security monitoring and technical validation, while also highlighting the importance of employee awareness, security policies, continuous monitoring, and responsible handling of sensitive information.

## Key Areas

The project brings together several complementary areas of cybersecurity research and practical investigation:

- **OSINT & Dark Web Intelligence**: collection and analysis of potentially exposed organizational information from open and Dark Web sources.
- **Threat Intelligence**: investigation and correlation of external indicators to identify potential security risks.
- **Entity & Link Analysis**: connecting people, organizations, domains, email addresses and other indicators to build investigative context.
- **SIEM & Log Analysis**: collection and investigation of Windows security events using Splunk Enterprise.
- **Vulnerability Assessment**: controlled validation of potential security weaknesses using Kali Linux and Metasploit Framework.
- **Security Research Lab**: isolated virtualized environments designed to separate OSINT, monitoring and security-testing activities.
- **Incident Response & Mitigation**: analysis of potential response, remediation and continuous-monitoring measures.
- **Ethics & Privacy**: consideration of authorization, data minimization, responsible OSINT and safe handling of sensitive information.

## Architecture

The practical environment was designed as an isolated virtualized security lab, with different activities separated into dedicated environments.

The architecture is organized around three main security functions:

- **OSINT & Dark Web Monitoring**: dedicated environment for OSINT research, Dark Web access and external intelligence collection.
- **SIEM & Log Management**: environment used to collect and analyze security-related events generated within the monitored systems.
- **Penetration Testing**: dedicated environment for controlled reconnaissance and vulnerability assessment.

This separation helps reduce interaction between potentially risky research activities and the other components of the laboratory while providing a structured workflow from external intelligence collection to internal investigation and technical validation.

### Investigation Flow

```text
External Intelligence
        ↓
OSINT / Dark Web Research
        ↓
Information Correlation
        ↓
SIEM & Log Analysis
        ↓
Controlled Vulnerability Assessment
        ↓
Mitigation & Continuous Monitoring
```

## Technologies

The practical implementation combines virtualization, Linux-based security environments, OSINT and Dark Web intelligence, SIEM analysis, and controlled vulnerability assessment.

| Category | Technologies |
|---|---|
| Virtualization | Oracle VM VirtualBox |
| Operating Systems | Ubuntu Linux, Kali Linux |
| Dark Web Access | Tor Browser |
| Dark Web Intelligence | DarkOwl Vision |
| OSINT & Link Analysis | Maltego |
| SIEM & Log Analysis | Splunk Enterprise |
| Vulnerability Assessment | Metasploit Framework |

> **Note:** The thesis also evaluates and discusses additional OSINT and cybersecurity technologies, including OSINT Framework, SpiderFoot, Shodan, Have I Been Pwned, Nmap, Burp Suite, Scrapy, Zeek, Suricata and others. These are documented separately and should not be interpreted as technologies all implemented hands-on in the practical case study.
>
> See [`docs/tools-evaluated.md`](docs/tools-evaluated.md) for the complete technology assessment and the distinction between practically demonstrated, evaluated, and referenced technologies.

## Methodology

The project follows a structured investigation workflow that combines external intelligence collection, information correlation, internal monitoring, and controlled technical validation.

<br>
<p align="center">
  <img src="assets/methodology/methodology-flow.svg"
       alt="Methodology investigation workflow and scope"
       width="300">
</p>
</br>

## Case Study

The practical component of the thesis is based on a **simulated security incident affecting a technology and financial startup**.

The scenario begins with a phishing and social-engineering attack resulting in the compromise of an employee's corporate credentials. The investigation then follows the potential exposure and technical implications of the compromise through multiple security layers.

### Investigation Workflow

```text
Phishing / Social Engineering
             ↓
      Credential Compromise
             ↓
      Dark Web Monitoring
             ↓
       OSINT Correlation
             ↓
       SIEM Investigation
             ↓
   Controlled Vulnerability
          Assessment
             ↓
     Mitigation & Monitoring
```

<p align="center"> <img src="assets/case-study/darkowl-search-results.png" alt="DarkOwl Vision search results" width="800"> </p>
<p align="center"> <img src="assets/case-study/splunk-event-analysis.png" alt="Splunk Windows event analysis" width="800"> </p>
<p align="center"> <img src="assets/case-study/metasploit-ms17-010-scan.png" alt="Metasploit MS17-010 vulnerability assessment" width="800"> </p>

## Results

The case study demonstrated how external intelligence and internal security monitoring can be combined to investigate a simulated credential-compromise scenario.

| Area | Result |
|---|---|
| Dark Web Intelligence | Demonstrated the identification and analysis of potentially exposed organizational information |
| OSINT Correlation | Demonstrated how information from multiple sources can be correlated to build investigative context |
| SIEM Investigation | Used Splunk Enterprise to analyze Windows security events and investigate activity within the monitored environment |
| Vulnerability Assessment | Assessed the simulated target for the MS17-010 SMB vulnerability using Metasploit Framework |
| Vulnerability Outcome | The tested target was not identified as vulnerable to the assessed MS17-010 condition |
| Defensive Response | Identified monitoring, credential protection, hardening and continuous security-awareness measures as relevant mitigation strategies |

### Key Findings

- **External intelligence can provide an early indication of potential organizational exposure**, before or alongside internal security investigations.
- **OSINT findings become more valuable when correlated with other sources**, rather than being treated as isolated indicators.
- **SIEM-based log analysis provides an internal perspective** that can be used to investigate and validate suspicious activity.
- **Technical validation should remain controlled and authorized**, using the minimum level of interaction necessary to assess a security hypothesis.
- **Continuous monitoring and preventive measures are essential** because exposed information and emerging threats can change over time.

The case study therefore supports the thesis' central proposition: **combining OSINT, Dark Web monitoring and internal security telemetry can improve an organization's ability to identify, investigate and respond to potential security threats.**

For the detailed findings, evidence and limitations, see [`docs/results.md`](docs/results.md).

## Skills Demonstrated

This project demonstrates a combination of cybersecurity research, technical investigation, system administration and analytical skills.

| Area | Skills Demonstrated |
|---|---|
| **Cybersecurity Research** | OSINT, Dark Web intelligence, threat monitoring, security research |
| **Threat Intelligence** | Information collection, indicator correlation, threat analysis, investigative workflows |
| **Security Analysis** | Log analysis, event investigation, vulnerability assessment |
| **OSINT** | Open-source information gathering, entity correlation, link analysis |
| **SIEM** | Windows event collection and analysis using Splunk Enterprise |
| **Vulnerability Assessment** | Controlled vulnerability validation using Kali Linux and Metasploit Framework |
| **Linux & Security Environments** | Linux-based security tooling and isolated virtualized laboratory environments |
| **Virtualization** | Design and configuration of a multi-environment security laboratory using VirtualBox |
| **Problem Solving** | Structured investigation, hypothesis validation, evidence correlation and technical troubleshooting |
| **Technical Documentation** | Research methodology, architecture documentation, technical analysis and security reporting |
| **Security & Privacy** | Responsible OSINT, data minimization, authorization, ethical handling of sensitive information |

### Key Competencies

- **OSINT & Dark Web Research**
- **Cybersecurity Analysis**
- **SIEM & Log Analysis**
- **Threat Intelligence**
- **Vulnerability Assessment**
- **Linux Security Environments**
- **Virtualization**
- **Information & Entity Correlation**
- **Technical Research & Documentation**
- **Responsible Security Practices**

## Challenges & Lessons Learned

Developing the case study required combining several areas of cybersecurity that are normally addressed independently. One of the main challenges was designing a coherent investigation workflow that connected external intelligence with internal security telemetry and technical validation.

### Key Challenges

- **Connecting heterogeneous information sources**  
  OSINT and Dark Web sources provide information in different formats and with different levels of reliability. Establishing meaningful relationships between collected information required correlation and validation rather than relying on individual findings.

- **Building an isolated research environment**  
  Dark Web research and security testing introduce additional technical risks. The laboratory therefore required separation between the different activities and dedicated virtualized environments.

- **Correlating external and internal evidence**  
  External intelligence alone does not necessarily confirm a security incident. Combining OSINT findings with Windows security events and SIEM analysis provided an additional perspective for investigating the simulated compromise.

- **Validating security hypotheses safely**  
  Potential vulnerabilities identified during an investigation should be validated within an authorized and controlled environment. The vulnerability-assessment stage therefore focused on testing the MS17-010 hypothesis without treating exploitation as the objective.

- **Handling sensitive information responsibly**  
  Research involving exposed credentials, personal information and Dark Web sources requires careful consideration of privacy, authorization, data minimization and publication practices.

### Lessons Learned

The project highlighted several important principles:

1. **Security investigations benefit from multiple sources of evidence.**  
   OSINT, Dark Web intelligence, system logs and vulnerability assessment provide different perspectives that become more useful when correlated.

2. **Information collection is only the beginning of an investigation.**  
   Findings must be analyzed, validated and placed into context before they can support a security decision.

3. **Isolation is an important part of security research.**  
   Separating research activities into controlled environments reduces unnecessary exposure and provides a safer platform for experimentation.

4. **A negative security finding is still a useful result.**  
   The absence of the tested MS17-010 vulnerability demonstrates the importance of validating assumptions rather than treating an initial hypothesis as fact.

5. **Technical capability must be combined with responsible security practices.**  
   Authorization, privacy and appropriate handling of sensitive information are fundamental when working with OSINT and cybersecurity tools.

> These lessons influenced the final methodology and the recommendations presented in the project.

## Future Improvements

The current project provides a foundation for combining OSINT, Dark Web intelligence, SIEM analysis and controlled vulnerability assessment. Several extensions could make the environment more representative of a real-world threat-intelligence and security-monitoring workflow.

### Automation

- Automate the collection and normalization of OSINT indicators from multiple sources.
- Introduce scheduled Dark Web monitoring for relevant organizational indicators.
- Develop automated workflows for correlating newly discovered indicators with existing security data.
- Reduce manual investigation steps through repeatable data-processing and enrichment pipelines.

### Threat Intelligence Integration

- Integrate additional threat-intelligence feeds and enrichment services.
- Develop a structured indicator repository for domains, IP addresses, email addresses, usernames and other relevant indicators.
- Introduce mechanisms for tracking changes to indicators over time.
- Improve correlation between external intelligence and internal security events.

### SIEM & Detection Engineering

- Expand the Splunk environment with custom dashboards and detection rules.
- Develop alerts for suspicious authentication activity and potential credential compromise.
- Correlate external threat intelligence with internal Windows security events.
- Introduce additional log sources to provide broader visibility across the laboratory environment.

### Security Testing

- Expand the controlled vulnerability-assessment phase to cover additional vulnerabilities and services.
- Introduce a broader reconnaissance and vulnerability-management workflow.
- Integrate vulnerability findings with the threat-intelligence investigation process.
- Develop repeatable testing procedures for the laboratory environment.

### Data Analysis

- Introduce automated classification and prioritization of collected intelligence.
- Apply statistical or machine-learning techniques where they provide measurable value for identifying patterns or anomalies.
- Improve visualization of relationships between entities and indicators.
- Develop historical analysis to identify changes and emerging trends.

### Laboratory Expansion

The laboratory could be extended with additional components such as:

- a dedicated threat-intelligence platform;
- additional endpoint and network telemetry;
- centralized log collection;
- containerized security services;
- additional simulated enterprise hosts;
- automated attack-and-detection scenarios.

These additions would allow the environment to evolve from a primarily research-oriented laboratory into a more comprehensive **threat-intelligence and security-monitoring platform**.

### Long-Term Direction

A future version of the project could focus on building a more automated end-to-end workflow:

```text
OSINT / Dark Web Sources
          ↓
Automated Collection
          ↓
Normalization & Enrichment
          ↓
Threat Intelligence
          ↓
Correlation with SIEM
          ↓
Detection & Alerting
          ↓
Investigation
          ↓
Response & Remediation
```

