# 🕵️ Honeypot Log Monitoring – Azure + KQL

## 📌 Overview
This project simulates a production-like network using a deployed **honeypot in Microsoft Azure** (including an Ubuntu server and Active Directory setup). Logs were analyzed using **KQL (Kusto Query Language)** through Azure Monitor and Elastic Stack.

Due to Azure subscription expiration, live access is no longer available — but key screenshots and detection insights were preserved.

## 🧰 Tools & Stack
- Microsoft Azure (VMs, Active Directory)
- Ubuntu Honeypot
- Azure Monitor + KQL
- Elastic Stack (Kibana)
- Linux logging tools

## 🎯 Goals
- Simulate a real-world attack surface for security monitoring
- Analyze failed logins, top attacker IPs, and attack patterns
- Practice blue team techniques and KQL log analysis

## 📸 Screenshots

### 🌍 Global Honeypot Activity Dashboard
![Global Honeypot Dashboard](screenshots/dashboard-global-summary.jpg)

### 📊 Failed Logins & Attack Attempts
![Attack Graphs](screenshots/dashboard-attack-graphs.jpg)

### 🔒 Privilege Escalation – Event ID 4672
![Privilege Escalation Events](screenshots/privilege-escalation-events.jpg)

## 🔍 Detection Use Cases

| Threat | Detection Logic |
|--------|------------------|
| Privilege Escalation | Multiple Event ID 4672 entries from SYSTEM or single account |
| SSH brute-force | High frequency of failed logins from single IPs |
| Port scanning | Spike in multi-port access attempts |
| AD misuse | Logon attempts to disabled/privileged users |
| Time-based analysis | Attacks during off-hours or holidays |

## 📂 Project Structure
- `README.md` – Project overview (this file)
- `kql_queries.md` – Actual KQL used to detect threats
- `honeypot_setup_notes.md` – Notes on honeypot/AD deployment

## 🧠 What I Learned
- How to deploy an AD-enabled honeypot in Azure
- Creating dashboards from log ingestion
- Detecting and interpreting brute-force and scanning behavior
- Writing detection logic in KQL for real-world use cases

> Built independently for cybersecurity hands-on learning. Inspired by YouTube tutorial, extended for custom testing and documentation.
