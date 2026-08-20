# Ethics, Legal & Responsible Use

## Overview

OSINT, Dark Web monitoring and security testing can provide valuable information for cybersecurity investigations, but these activities also introduce important **ethical, privacy and legal responsibilities**.

Information being technically accessible does not automatically mean that it should be collected, processed, redistributed or used without restriction.

This project therefore considers responsible information gathering, data protection and authorization as fundamental parts of the security workflow.

The practical activities documented in this repository were developed for an **academic case study and controlled laboratory environment**. The project does not authorize or encourage security testing against systems without explicit permission, unauthorized access to accounts or systems, credential misuse, or unlawful collection and redistribution of personal information.

---

# Responsible OSINT

Open Source Intelligence involves collecting and analyzing information available through publicly or openly accessible sources.

The ability to discover information, however, does not remove the responsibility to consider:

* why the information is being collected;
* whether the collection is necessary for the investigation;
* whether personal or sensitive information is involved;
* how the information will be stored;
* who should have access to it;
* whether it is appropriate to redistribute or publish it;
* whether the information is accurate and sufficiently validated.

The project therefore treats OSINT as a **purpose-driven intelligence activity**, rather than indiscriminate information collection.

A responsible investigation should define its objectives before collection and limit the information gathered to what is relevant to those objectives.

---

## Publicly Accessible Does Not Mean Risk-Free

OSINT can involve information obtained from sources such as:

* websites;
* search engines;
* public documents;
* social networks;
* online communities;
* technical infrastructure information;
* publicly accessible databases;
* Dark Web sources.

Some of this information may contain personal, confidential or sensitive data.

Even when information can be accessed without bypassing a technical security control, its collection and processing can still have privacy, ethical or legal implications.

Researchers should therefore consider both **accessibility and appropriate use**.

---

# Dark Web Research

Dark Web research introduces additional risks compared with conventional web research.

Dark Web environments may contain:

* stolen credentials;
* leaked personal information;
* illegally obtained corporate data;
* malware;
* fraudulent services;
* malicious links or files;
* illegal content;
* misleading or fabricated information.

The presence of such information creates both technical and ethical risks.

The project therefore approaches Dark Web monitoring as a **defensive intelligence activity**, focused on identifying information potentially relevant to organizational security.

---

## Safe Research Environment

The practical architecture uses a dedicated virtualized environment for OSINT and Dark Web activities.

This separation is intended to reduce exposure of the host system and other lab environments to potentially malicious content.

Relevant precautions include:

* using isolated virtual machines;
* separating Dark Web research from normal workstation activity;
* controlling network communication;
* avoiding unnecessary downloads or execution of unknown files;
* minimizing interaction with potentially malicious services;
* avoiding the use of personal accounts or credentials during research.

Isolation reduces technical risk, but it does not remove the legal or ethical responsibilities associated with accessing and processing information.

---

# Handling Exposed Credentials

Credential exposure is central to the simulated incident explored by the case study.

The discovery of credentials through a breach source, Dark Web platform or OSINT investigation **does not authorize their use**.

Exposed credentials should be treated as sensitive security information.

Appropriate defensive actions may include:

* documenting the exposure securely;
* notifying the responsible organization or security team through appropriate channels;
* forcing password resets;
* invalidating existing sessions;
* investigating associated account activity;
* monitoring for additional indicators of compromise.

Credentials should not be used to authenticate to systems without explicit authorization, even when the credentials are already publicly exposed or available through a third party.

The repository therefore does not publish functional credentials obtained from external sources.

---

# Personal Data & Privacy

OSINT investigations may involve information relating to identifiable individuals.

The thesis considers privacy regulation — particularly the **General Data Protection Regulation (GDPR)** in the European context — as an important constraint when collecting, processing and storing personal information.

Relevant principles include:

### Purpose Limitation

Information should be collected for a defined and legitimate investigative purpose rather than simply because it is available.

### Data Minimization

Only information necessary for the investigation should be collected and retained.

### Accuracy

Information gathered from public or Dark Web sources may be incomplete, outdated or incorrect.

Where decisions depend on collected information, appropriate efforts should be made to verify its accuracy.

### Storage and Access

Sensitive research material should be stored securely and made accessible only to those who require it.

### Retention

Information should not be retained indefinitely when it is no longer required for the purpose for which it was collected.

These principles are particularly important when OSINT findings contain email addresses, usernames, identities, credentials or other personal information.

---

# Security Testing & Authorization

The penetration-testing component of this project is based on a fundamental rule:

> **Security testing should only be performed against systems that you own or for which you have explicit authorization to test.**

The practical vulnerability-assessment activities documented in this repository were performed within a controlled academic/laboratory context.

Tools such as Kali Linux and Metasploit are legitimate security technologies, but their legality and ethical use depend heavily on **scope, authorization and intent**.

Before performing a real-world security assessment, appropriate authorization should define elements such as:

* systems included in scope;
* systems explicitly excluded from testing;
* permitted testing techniques;
* testing period;
* handling of discovered vulnerabilities;
* handling of sensitive data;
* reporting and escalation procedures.

The presence of an exposed service or suspected vulnerability does not provide permission to test or exploit it.

---

# Vulnerability Validation vs Exploitation

The practical case study uses Metasploit to assess whether a controlled target appeared susceptible to the SMB vulnerability associated with MS17-010.

The objective was **technical validation**, not unauthorized exploitation.

The target was not identified as vulnerable.

This distinction is important throughout the project:

```text
Potential Weakness
        ↓
Authorized Validation
        ↓
Evidence
        ↓
Security Finding
        ↓
Remediation
```

A potential vulnerability identified through OSINT, scanning or security monitoring should not automatically lead to exploitation.

Validation should remain within the authorized scope and use the minimum level of interaction necessary to answer the security question being investigated.

---

# Reliability of Intelligence

Another ethical concern is the reliability of information collected through OSINT and Dark Web sources.

Information discovered online may be:

* inaccurate;
* outdated;
* duplicated;
* taken out of context;
* deliberately manipulated;
* falsely attributed;
* fabricated.

A username, email address, domain or IP address appearing in a dataset does not by itself prove malicious activity or compromise.

The methodology therefore emphasizes **correlation and validation before conclusions are drawn**.

This is especially important when findings could affect individuals or organizations.

Incorrect attribution can itself cause reputational, privacy and security harm.

---

# Responsible Disclosure

If research reveals a genuine vulnerability or sensitive exposure affecting a real organization, the appropriate response is not to immediately publish the technical details.

Responsible handling should consider:

1. validating the finding without exceeding the authorized scope;
2. preserving only the evidence necessary to support the finding;
3. notifying the appropriate organization or security contact;
4. allowing reasonable time for investigation and remediation;
5. avoiding unnecessary disclosure of sensitive technical or personal information.

Any disclosure process must also respect the applicable authorization, organizational policies and legal requirements.

---

# Publication & Repository Sanitization

The public GitHub repository intentionally contains less sensitive information than the original research material.

Before publication, project assets should be reviewed for:

* personal email addresses;
* usernames;
* credentials;
* access tokens and API keys;
* personal identifiers;
* private organizational information;
* sensitive IP addresses or infrastructure details;
* third-party information collected during OSINT research;
* Dark Web material that should not be redistributed.

Where necessary, screenshots should be **redacted, cropped or recreated using fictional data**.

For example, the original Maltego demonstration used during the academic work contained personal and university-related information. The public portfolio version should instead use a sanitized representation that demonstrates the analytical technique without unnecessarily exposing personal information.

The objective is to preserve the technical value of the project while minimizing unnecessary disclosure.

---

# Ethical Principles Applied to the Project

The project's approach can be summarized through the following principles:

| Principle                  | Application                                                                    |
| -------------------------- | ------------------------------------------------------------------------------ |
| **Authorization**          | Security testing is restricted to owned or explicitly authorized systems       |
| **Purpose Limitation**     | Intelligence is collected to answer defined security questions                 |
| **Data Minimization**      | Only information relevant to the investigation should be retained              |
| **Isolation**              | Potentially risky research is separated into dedicated environments            |
| **Validation**             | Intelligence is correlated before conclusions are drawn                        |
| **Privacy**                | Personal and sensitive information should be protected                         |
| **Non-Exploitation**       | Exposed credentials or vulnerabilities do not provide authorization for misuse |
| **Responsible Disclosure** | Genuine findings should be handled through appropriate reporting channels      |
| **Sanitization**           | Public documentation should avoid unnecessary exposure of sensitive data       |

---

# Legal Context

The original thesis examines privacy and cybersecurity regulation within both European and international contexts.

In particular, the research considers the importance of frameworks such as the **General Data Protection Regulation (GDPR)** when personal information is collected and processed during OSINT activities.

Different jurisdictions may impose different requirements concerning:

* personal-data processing;
* monitoring activities;
* unauthorized access;
* interception of communications;
* security testing;
* breach information;
* retention and disclosure of collected data.

Researchers and security practitioners are responsible for understanding the requirements applicable to the jurisdiction, organization and systems involved in a specific investigation.

This repository does not attempt to provide a complete interpretation of those laws.

---

# Disclaimer

This repository documents an **academic cybersecurity research project** focused on OSINT, Dark Web threat intelligence, security monitoring and controlled vulnerability assessment.

The information and examples are provided for **educational, research and defensive-security purposes**.

Nothing in this repository should be interpreted as authorization to:

* access systems or accounts without permission;
* use leaked or stolen credentials;
* bypass security controls;
* collect personal information unlawfully;
* perform vulnerability testing against unauthorized targets;
* redistribute stolen, confidential or unlawfully obtained data.

Users are responsible for ensuring that their activities comply with applicable laws, regulations, organizational policies and authorization requirements.

This documentation is not legal advice.

---

## Related Documentation

* [Architecture](architecture.md) — isolation and separation of security environments
* [Methodology](methodology.md) — responsible intelligence and investigation workflow
* [Case Study](case-study.md) — controlled application of the methodology
* [Results](results.md) — findings and project limitations
* [Tools Evaluated](tools-evaluated.md) — technologies used and researched
