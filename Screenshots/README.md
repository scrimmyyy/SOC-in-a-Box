## Wazuh SIEM Dashboard

![Wazuh Dashboard](./wazuhdash.png)

## Windows Endpoint Integration

![Active Windows Agent](./wazuhactiveagent.png)

### Sysmon Integration and Event Monitoring

Successfully integrated Microsoft Sysmon with Wazuh to monitor Windows endpoint activity.

Configured the Wazuh agent to collect events from the `Microsoft-Windows-Sysmon/Operational` channel.

Verified successful event ingestion and alert generation through the Wazuh Threat Hunting dashboard.

**Validation Results:**
- Monitored endpoint: Win11Lab
- Sysmon event collection: Operational
- Process creation monitoring: Event ID 1
- Wazuh alerts observed: 44 within a 15-minute monitoring window
- Sysmon-related alert groups: `sysmon`, `sysmon_eid1_detection`

![Sysmon Integration](alerts.png)
