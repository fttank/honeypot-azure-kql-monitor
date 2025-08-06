# 🧠 KQL Queries – Azure Honeypot Monitoring

This file includes custom KQL queries used to detect suspicious behavior within the Azure-based honeypot and Active Directory environment.

---

## 🔐 Privilege Escalation Detection – Event ID 4672

```kql
SecurityEvent
| where EventID == 4672
| project TimeGenerated, Account, Computer, Activity = EventID
| sort by TimeGenerated desc
