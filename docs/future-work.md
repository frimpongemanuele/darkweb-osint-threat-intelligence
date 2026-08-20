# Future Work

## Overview

The current project demonstrates a research-oriented workflow combining OSINT, Dark Web intelligence, SIEM analysis and controlled vulnerability assessment.

Future development could extend the laboratory into a more automated and integrated threat-intelligence environment while preserving the same principles of controlled testing, validation and responsible handling of security data.

## Automation & Data Collection

A first area of improvement would be reducing the amount of manual work required during intelligence collection and correlation.

Potential extensions include:

- scheduled collection of relevant OSINT indicators;
- automated normalization of domains, IP addresses, email addresses and usernames;
- enrichment of indicators using multiple intelligence sources;
- deduplication and basic confidence scoring;
- repeatable workflows for processing newly collected information.

Automation should support the analyst rather than replace validation. Collected intelligence would still require contextual review before being treated as reliable evidence.

## Threat Intelligence Integration

The laboratory could be expanded with a more structured threat-intelligence layer.

Possible improvements include:

- integration of additional threat-intelligence feeds;
- centralized storage of indicators of interest;
- tracking relationships between indicators and investigations;
- maintaining historical information about indicator changes;
- distinguishing source reliability and confidence levels.

This would create a clearer bridge between external intelligence collection and internal security monitoring.

## SIEM & Detection Engineering

The Splunk environment could be developed beyond exploratory log analysis by introducing more structured detection capabilities.

Future work could include:

- custom dashboards for authentication and security events;
- detection rules for suspicious authentication activity;
- alerts related to potential credential misuse;
- correlation between externally discovered indicators and internal logs;
- ingestion of additional endpoint and network telemetry.

This would allow the SIEM component to become a more active part of the investigation workflow.

## Security Validation

The controlled vulnerability-assessment environment could also be expanded.

Potential improvements include:

- validation of additional vulnerabilities and exposed services;
- broader reconnaissance and asset discovery;
- repeatable vulnerability-assessment procedures;
- integration of vulnerability findings with threat-intelligence investigations;
- additional intentionally vulnerable systems for authorized testing.

The objective would remain **validation of security hypotheses**, rather than exploitation for its own sake.

## Network & Endpoint Visibility

The current environment could benefit from additional telemetry sources to provide a broader view of simulated organizational activity.

Possible additions include:

- centralized Windows event collection;
- network monitoring and IDS/IPS telemetry;
- endpoint security events;
- authentication and access logs;
- additional simulated enterprise systems.

These sources could improve correlation between external indicators and events occurring inside the laboratory.

## Data Analysis & Prioritization

As the volume of collected intelligence increases, additional analytical techniques could help prioritize relevant findings.

Future research could explore:

- indicator classification and prioritization;
- relationship and graph analysis;
- historical trend analysis;
- anomaly detection;
- statistical or machine-learning techniques where they provide measurable value.

Any automated classification should remain subject to human review because OSINT and Dark Web sources can contain incomplete, misleading or unreliable information.

## Laboratory Expansion

The virtualized environment could evolve into a broader security-monitoring laboratory containing additional components such as:

- a dedicated threat-intelligence platform;
- centralized logging;
- additional endpoint and network telemetry;
- containerized security services;
- multiple simulated enterprise hosts;
- intentionally vulnerable targets;
- automated attack-and-detection scenarios.

This would provide a more representative environment for studying how different defensive and investigative systems interact.

## Long-Term Direction

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
Controlled Validation
          ↓
Response & Remediation
