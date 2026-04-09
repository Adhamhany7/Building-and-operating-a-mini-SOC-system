# Mini SOC Home Lab - Wazuh vs ELK Detection Comparison

## Overview
This project demonstrates building a home-based Security Operations Center (SOC) lab using both Wazuh and the Elastic Stack (ELK). The main goal is to compare how each platform handles log collection, detection rules, and alert generation.

The lab focuses specifically on the difference in detection logic:
- Wazuh uses built-in rules and decoders
- ELK requires custom detection rules created by the analyst or downloaded from Elastic rules

---

## Objectives
- Build a SOC lab using Wazuh and ELK
- Monitor endpoints and collect logs
- Compare detection mechanisms between the two solutions
- Understand rule-based alerting vs custom detection engineering
- Practice alert analysis and triage

---

## Lab Environment

### Components
- Wazuh Manager (Docker)
- Elastic Stack (Elasticsearch, Logstash, Kibana)
- Windows Endpoint
- Windows Server
  Linux

---

## Architecture
![Lab Architecture](images/architecture.png)

---

## Implementation Steps

### Wazuh Setup
- Deployed Wazuh using Docker
- Installed agents on Windows and Linux machines
- Connected agents to Wazuh Manager
- Verified log collection and agent status
- Observed alerts generated automatically by built-in rules

### ELK Setup
- Deployed Elasticsearch, Logstash, and Kibana
- Configured data ingestion (Winlogbeat / Filebeat)
- Created index patterns and data views
- Built custom detection rules manually
- Generated alerts based on custom queries

---

## Detection Approach Comparison

### Wazuh (Rule-Based Detection)
- Uses prebuilt rules and decoders
- Automatically generates alerts when conditions match
- Minimal setup required for detection
- Good for quick deployment and baseline monitoring

### ELK (Custom Detection Engineering)
- No default detection logic (requires manual rule creation)
- Analyst builds detection rules using queries (KQL / ES|QL)
- More flexible and customizable
- Requires a deeper understanding of logs and attack patterns

---

## Key Difference (Important Insight)

In this lab:
- Wazuh provided **out-of-the-box detection** using predefined rules
- ELK required **manual creation of detection logic**

This highlights a critical SOC concept:

> Detection in SIEM can be either:
> - Prebuilt (Wazuh-style)
> - Analyst-driven (ELK-style)

---

## Screenshots

### Wazuh Alerts
![Wazuh Alerts](images/wazuh-alerts.png)

### ELK Detection Rule
![ELK Rule](images/elk-rule.png)

### ELK Alerts
![ELK Alerts](images/elk-alerts.png)

---

## Challenges Faced
- Understanding how Wazuh rules are triggered
- Writing detection queries in ELK
- Troubleshooting data ingestion in Elastic Stack
- Handling field mapping and index issues
- Differentiating between logs and alerts

---

## What I Learned
- Difference between SIEM and detection engine behavior
- How rules work internally in Wazuh
- How to build detection logic manually in ELK
- Importance of log normalization and field mapping
- Basics of detection engineering in SOC environments

---

## Future Improvements
- Create advanced detection use cases (brute force, lateral movement)
- Integrate Sysmon for enhanced Windows visibility
- Map detections to MITRE ATT&CK framework
- Add alert tuning and false positive reduction
- Build automated response (SOAR concepts)

---

## Conclusion
This lab provided hands-on experience in comparing two different approaches to security monitoring and detection:

- Wazuh simplifies detection with built-in rules
- ELK provides flexibility through custom detection engineering

Understanding both approaches is essential for working in modern SOC environments.

---

## Author
Adham Hani  
SOC Analyst Trainee | IT Specialist  
