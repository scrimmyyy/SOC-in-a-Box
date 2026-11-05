# SOC-in-a-Box
A home SOC lab using Wazuh, OpenSearch, and Windows endpoint monitoring to develop and test custom security detection rules.

# SOC-in-a-Box: SIEM & Detection Engineering Lab

**Status:** In Progress  
**Focus:** Blue Team | Security Operations | SIEM | Detection Engineering

## Overview

This project involves building a home-based Security Operations Center (SOC) using Wazuh, OpenSearch, and Windows endpoint monitoring.

The goal is to simulate a real-world SOC environment capable of collecting, analyzing, and monitoring security events while developing custom detection rules to identify suspicious activity.

The lab will be used to investigate security alerts, analyze system logs, identify potential threats, and understand how security analysts monitor and respond to incidents.

## Project Objectives

- Deploy and configure a functional SIEM environment.
- Centralize security event collection and monitoring.
- Configure Windows endpoint monitoring using Wazuh agents.
- Integrate Sysmon for detailed Windows event logging.
- Develop custom detection rules using Wazuh XML.
- Map detection rules to the MITRE ATT&CK framework.
- Generate controlled security events to test detection capabilities.
- Investigate alerts and document findings.
- Develop practical SOC analyst and detection engineering skills.

## Technologies & Tools

| Technology | Purpose |
|---|---|
| Wazuh | SIEM and security monitoring |
| OpenSearch | Security event indexing and storage |
| Ubuntu Server 24.04 LTS | SOC server operating system |
| Windows 11 | Monitored endpoint |
| Sysmon | Windows system activity monitoring |
| VirtualBox | Virtualization and lab infrastructure |
| MITRE ATT&CK | Threat behavior classification |
| GitHub | Project documentation and version control |

## Lab Architecture

The environment consists of two primary virtual machines:

**1. SOC Server (Ubuntu Server)**
- Hosts Wazuh Manager.
- Hosts Wazuh Indexer.
- Hosts Wazuh Dashboard.
- Collects and analyzes endpoint security events.

**2. Windows Endpoint**
- Runs the Wazuh Agent.
- Uses Sysmon to collect detailed system activity.
- Forwards security events to the SOC server.

## Planned Detection Engineering

The following detection use cases will be developed and tested:

| Detection Use Case | Description |
|---|---|
| Failed Login Attempts | Identify repeated authentication failures. |
| Suspicious Login Activity | Identify unusual authentication patterns. |
| Account Creation | Monitor the creation of new user accounts. |
| Privilege Escalation | Detect unexpected privilege changes. |
| PowerShell Monitoring | Identify suspicious PowerShell activity. |
| Windows Service Creation | Monitor newly installed services. |
| File Integrity Monitoring | Identify unauthorized file modifications. |
| Security Configuration Changes | Monitor changes to security-related settings. |

Each detection will include:
- Detection logic.
- Relevant Windows Event IDs.
- Custom Wazuh rules.
- MITRE ATT&CK technique mapping.
- Test scenarios.
- Expected and observed results.

## Project Structure

```text
SOC-in-a-Box/
└── Screenshots/
    ├── 01-infrastructure/
    │   ├── virtualbox-vms.png
    │   └── ubuntu-server.png
    │
    ├── 02-wazuh-installation/
    │   ├── dashboard-home.png
    │   └── wazuh-services.png
    │
    ├── 03-endpoint-monitoring/
    │   └── connected-windows-agent.png
    │
    └── 04-detection-engineering/
        ├── failed-login-alert.png
        └── file-integrity-alert.png
|
|
├── README.md
│
├── Architecture/
│   ├── architecture.png
│   └── network-diagram.png
│
├── Installation/
│   ├── wazuh-installation.md
│   ├── windows-agent-setup.md
│   └── sysmon-configuration.md
│
├── Detection-Rules/
│   ├── authentication/
│   ├── account-monitoring/
│   ├── powershell/
│   ├── privilege-escalation/
│   └── file-integrity/
│
├── Testing/
│   ├── test-cases.md
│   └── detection-results.md
│
├── MITRE-Mapping/
│   └── attack-mapping.md
│
└── Screenshots/
    ├── dashboard.png
    └── detection-alerts/
```

## Testing & Validation

Controlled security events will be generated within the isolated lab environment to evaluate detection capabilities.

Testing will include:
- Generating authentication failures.
- Creating test user accounts.
- Modifying monitored files.
- Performing controlled PowerShell activity.
- Monitoring Windows security events.
- Validating custom detection rules against generated logs.

Detection results will be documented with screenshots, relevant event information, and investigation notes.

## Learning Outcomes

Through this project, I aim to develop practical experience with:

- Security Information and Event Management (SIEM).
- Security event collection and log analysis.
- Windows endpoint monitoring.
- Detection engineering.
- Custom rule development.
- MITRE ATT&CK mapping.
- Security alert investigation.
- SOC operations and incident analysis.

## Disclaimer

This project is intended for educational and defensive cybersecurity purposes. All testing and simulated security activity will be conducted within an authorized, controlled virtual lab environment.

---

**Project Status:** Infrastructure setup in progress. Detection development and testing will be documented as the project progresses.
