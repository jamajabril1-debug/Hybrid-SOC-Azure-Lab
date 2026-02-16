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

## Wazuh – SSH Brute Force Detection

### Attack Simulation

The following screenshot shows the simulated SSH brute force attempts against the Linux endpoint:

![SSH Failed Login](Screenshots/wazuh/wazuh_ssh_failed_login.png)

### Authentication Failure Overview

Wazuh dashboard showing authentication failures:

![Wazuh Dashboard Authentication](Screenshots/wazuh/wazuh_dashboard_authentication.png)

### Event Details – Rule 2502

Detailed view of the triggered alert, showing rule 2502 and MITRE mapping (T1110 – Brute Force):

![Wazuh Event Details – Rule 2502](Screenshots/wazuh/wazuh_event_details_rule_2502.png)

### Brute Force Alert Summary

Summary of brute force alerts logged by Wazuh:

![Wazuh Brute Force Alert](Screenshots/wazuh/wazuh_bruteforce_alert.png)

## Azure Entra ID – Failed Sign-in Detection

### Failed Sign-in List

The list shows multiple failed login attempts in Azure Sign-in logs:

![Azure Failed Sign-ins List](Screenshots/azure/azure_failed_signins_list.png)

### Failed Sign-in Details

Detailed event view showing failure status, error code, and failure reason:

![Azure Sign-in Failure Details](Screenshots/azure/azure_signin_failure_details.png)

---

## Key Learnings

- End-to-end SIEM troubleshooting (Agent → Manager → Indexer → Dashboard)
- Log ingestion debugging (401 Unauthorized / Filebeat issues)
- Azure identity attack simulation and log validation
- Practical MITRE ATT&CK mapping in real detection scenarios
- Hybrid monitoring (On-prem + Cloud)

---

## Author

Jabril Jama  
Aspiring SOC Analyst | Cloud Security  
---

## Key Learnings

- End-to-end SIEM troubleshooting (Agent → Manager → Indexer → Dashboard)
- Log ingestion debugging (401 Unauthorized / Filebeat issues)
- Azure identity attack simulation and log validation
- Practical MITRE ATT&CK mapping in real detection scenarios
- Hybrid monitoring (On-prem + Cloud)

---

## Author

Jabril Jama  
Aspiring SOC Analyst | Cloud Security  



