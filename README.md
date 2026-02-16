# Hybrid SOC Lab – Azure & Linux Identity Monitoring

## Project Goal
Build a hybrid SOC lab to detect and analyze identity-based attacks 
across on-prem Linux systems and Microsoft Entra ID.

Target Role: SOC Analyst / Cloud Security Intern

---

## Architecture

**On-Prem:**
- Ubuntu Server (Wazuh SIEM)
- Ubuntu Endpoint (SSH log source)
- Log source: /var/log/auth.log

**Cloud:**
- Microsoft Entra ID
- Azure sign-in logs
- Azure audit logs

---

## Attack Simulated

### Linux
- SSH brute force attempts
- MITRE ATT&CK: T1110 (Brute Force)
- Detection via Wazuh rule 2502

### Azure
- Failed Entra ID sign-in attempts
- Identity-based attack validation

---

## Detection Pipeline

Linux Endpoint  
→ Wazuh Agent  
→ Wazuh Manager  
→ Filebeat  
→ Wazuh Indexer (OpenSearch)  
→ Wazuh Dashboard  

---

## Skills Demonstrated

- SIEM deployment (Wazuh)
- Linux log analysis
- File Integrity Monitoring (FIM)
- SSH brute force detection
- Azure Entra ID log analysis
- Troubleshooting log ingestion pipeline
- MITRE ATT&CK mapping

---

## Documentation

Detailed setup and analysis available in `/Documentation`
