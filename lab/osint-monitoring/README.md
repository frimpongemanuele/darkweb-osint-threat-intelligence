# OSINT & Dark Web Monitoring Lab

## Overview

This environment represents the **external intelligence collection component** of the project laboratory.

A dedicated Ubuntu virtual machine was created to separate OSINT and Dark Web research activities from the other components of the lab. The environment was used to access external intelligence sources, investigate potentially exposed organizational information, and correlate collected data using OSINT and link-analysis tools.

The VM forms the first stage of the broader investigation workflow:

```text
External Sources
       ↓
OSINT / Dark Web Research
       ↓
Information Collection
       ↓
Entity & Link Analysis
       ↓
Relevant Indicators
       ↓
Further Security Investigation
```

---

## Lab Environment

The environment was deployed as a dedicated virtual machine using **Oracle VM VirtualBox**.

| Component | Configuration |
|---|---|
| **VM Name** | OSINT DW MONITORING |
| **Hypervisor** | Oracle VM VirtualBox |
| **Operating System** | Ubuntu Linux (64-bit) |
| **Memory** | 8 GB RAM |
| **Processors** | 2 vCPUs |
| **Storage** | 40 GB VDI |
| **Network** | NAT |
| **Graphics Controller** | VMSVGA |
| **Shared Folders** | None |

The use of a dedicated VM provides separation between OSINT/Dark Web research and the host system while allowing the environment to be independently configured for security-research activities.

<p align="center">
  <img src="../../assets/lab/osint-monitoring/virtualbox-vm-configuration.png"
       alt="VirtualBox configuration for the OSINT and Dark Web monitoring virtual machine"
       width="700">
</p>

<p align="center">
  <em>VirtualBox configuration of the dedicated Ubuntu OSINT and Dark Web monitoring environment.</em>
</p>

---

## Purpose

The environment was designed to support three main activities:

### 1. OSINT Collection

Open-source information was collected and analyzed to identify information potentially relevant to the simulated organization and security incident.

The investigation considered indicators such as:

- organization and domain information;
- email addresses;
- usernames and identities;
- publicly exposed technical information;
- relationships between discovered entities.

### 2. Dark Web Monitoring

Dark Web sources were investigated to determine whether organizational information or credentials could potentially appear in sources outside the conventional indexed web.

The purpose of this stage was **defensive intelligence gathering**, not interaction with malicious services or use of exposed credentials.

### 3. Entity & Link Analysis

Collected information was analyzed to identify relationships between entities such as:

```text
Person
  │
  ├── Email Address
  ├── Organization
  ├── Domain
  └── Public Web Presence
```

This helped transform individual OSINT findings into structured investigative context.

---

## Tools Used

| Tool | Role in the Lab |
|---|---|
| **Ubuntu Linux** | Base operating system for the dedicated research environment |
| **Tor Browser** | Access to Tor-based resources and Dark Web research |
| **DarkOwl Vision** | Search and analysis of Dark Web intelligence |
| **Maltego** | Entity correlation and link analysis |

> **Note:** The thesis evaluates a broader set of OSINT and cybersecurity technologies. This page focuses only on technologies directly associated with the practical OSINT and Dark Web environment. See [`../../docs/tools-evaluated.md`](../../docs/tools-evaluated.md) for the complete technology assessment.

---

## Environment Setup

### Tor Environment

Tor and Tor Browser were used to support Dark Web research from within the dedicated Ubuntu virtual machine.

The installation documented during the project included:

```bash
sudo apt install -y tor torbrowser-launcher
```

This allowed Dark Web research activities to remain within the dedicated research VM rather than being performed directly from the host environment.

### Network Configuration

The VirtualBox network adapter was configured using **NAT**.

```text
Internet
   │
   ↓
VirtualBox NAT
   │
   ↓
Ubuntu OSINT VM
   │
   ↓
Tor / OSINT Resources
```

NAT provided network connectivity to the VM without directly exposing the virtual machine as another independently reachable device on the physical LAN.

> **Security Note:** NAT should not be interpreted as a complete security boundary or sandbox. The virtual machine provides an additional layer of separation for the academic research environment, while potentially risky material and services should still be handled cautiously.

---

## Investigation Workflow

The practical OSINT investigation followed a structured workflow.

### Step 1 — Define the Investigation Target

Identify the organization, domain, account, email address, or other indicator relevant to the simulated incident.

### Step 2 — Collect Open-Source Information

Search available public sources for information related to the target and establish an initial intelligence baseline.

### Step 3 — Investigate Dark Web Exposure

Use Dark Web monitoring resources to search for potentially exposed information relevant to the investigation.

### Step 4 — Correlate Entities

Use Maltego to visualize and analyze relationships between discovered entities and establish additional investigative context.

### Step 5 — Validate Relevant Findings

Evaluate the relevance and reliability of collected information before treating it as evidence of compromise.

### Step 6 — Escalate Relevant Indicators

Indicators considered relevant to the simulated incident can then support subsequent stages of the investigation, including SIEM analysis and controlled technical validation.

```text
        OSINT Sources
             │
             ├──────────────┐
             ↓              ↓
        Public Web       Dark Web
             │              │
             └──────┬───────┘
                    ↓
          Information Collection
                    ↓
           Entity Correlation
                    ↓
               Validation
                    ↓
          Relevant Indicators
                    ↓
          SIEM Investigation
```

---

## Practical Evidence

### Dark Web Intelligence

DarkOwl Vision was used during the research to demonstrate how Dark Web information could be searched and evaluated as part of an external intelligence investigation.

<p align="center">
  <img src="../../assets/case-study/darkowl-search-results.png"
       alt="DarkOwl Vision search results used during the case study"
       width="700">
</p>

<p align="center">
  <em>Example of Dark Web intelligence research performed using DarkOwl Vision.</em>
</p>

### Entity & Link Analysis

Maltego was used to visualize relationships between entities discovered during OSINT research, helping transform individual findings into a structured investigation graph.

<p align="center">
  <img src="../../assets/case-study/maltego-link-analysis.png"
       alt="Maltego entity and link analysis performed during the OSINT investigation"
       width="700">
</p>

<p align="center">
  <em>Example of entity correlation and link analysis performed with Maltego.</em>
</p>

> **Privacy Note:** Screenshots published in this repository should contain only sanitized or non-sensitive information. Personal information, credentials, identifiers, or unnecessary third-party data should be redacted before publication.

---

## Observations

The OSINT environment demonstrated that individual pieces of publicly available or externally exposed information become more useful when they are **correlated and placed into investigative context**.

A discovered email address, domain, username, IP address, or other indicator does not independently prove that an organization or account has been compromised.

Instead, information should move through a validation process:

```text
Collected → Correlated → Validated → Contextualized
```

This distinction is particularly important when working with OSINT and Dark Web sources, where information may be incomplete, outdated, duplicated, misleading, or unrelated to the current investigation.

The output of this environment therefore represents **external intelligence** that can support subsequent investigation rather than automatically constituting evidence of compromise.

Relevant indicators can then be compared with internal telemetry collected by the SIEM environment.

```text
External Intelligence
         ↓
Relevant Indicators
         ↓
Internal Telemetry
         ↓
SIEM Investigation
         ↓
Technical Validation
```

---

## Limitations

This environment represents an **academic security-research laboratory** and should not be interpreted as a production threat-intelligence platform.

Notable limitations include:

- intelligence collection was primarily manual;
- automated indicator ingestion was not implemented;
- no production threat-intelligence feed integration was deployed;
- no automated enrichment or confidence-scoring pipeline was implemented;
- collected intelligence required manual analysis and validation;
- the reliability and freshness of external information cannot always be guaranteed;
- Dark Web information may be incomplete, outdated, duplicated, intentionally misleading, or unrelated to the investigated organization.

These limitations also provide opportunities for future development, particularly around intelligence automation, enrichment, correlation, and SIEM integration.

See [`../../docs/future-work.md`](../../docs/future-work.md) for the proposed development roadmap.

---

## Security & Ethical Considerations

OSINT and Dark Web research can expose researchers to sensitive, personal, misleading, or potentially unlawfully obtained information.

The environment and investigation were therefore approached according to several principles:

- use dedicated research environments;
- collect only information relevant to the investigation;
- do not use exposed credentials to access systems;
- avoid unnecessary interaction with potentially malicious services;
- do not execute unknown files obtained from untrusted sources;
- validate intelligence before drawing conclusions;
- minimize collection and retention of personal information;
- sanitize sensitive information before publishing research material;
- perform security testing only within authorized environments;
- respect applicable privacy, legal, and authorization requirements.

The project uses OSINT and Dark Web intelligence for **academic research and defensive-security purposes**.

For the complete discussion of privacy, authorization, responsible OSINT, Dark Web research, and sensitive-data handling, see [`../../docs/ethics-and-legal.md`](../../docs/ethics-and-legal.md).

---

## Related Documentation

| Document | Description |
|---|---|
| [Project Architecture](../../docs/architecture.md): Complete laboratory architecture and separation of environments |
| [Methodology](../../docs/methodology.md): Investigation methodology and workflow |
| [Case Study](../../docs/case-study.md): Complete simulated security incident |
| [Results](../../docs/results.md): Findings and conclusions from the investigation |
| [Tools Evaluated](../../docs/tools-evaluated.md): Technologies demonstrated, evaluated, and referenced |
| [Ethics & Legal](../../docs/ethics-and-legal.md): Responsible research, privacy, and legal considerations |
| [Future Work](../../docs/future-work.md): Proposed technical extensions to the laboratory |

---

[← Back to main project](../../README.md)
