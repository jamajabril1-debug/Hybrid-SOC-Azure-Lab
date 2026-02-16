# Attack Simulation

## Linux Brute Force Simulation

Command used:
ssh fakeuser@192.168.83.147

Repeated failed password attempts triggered Wazuh detection.

## Detection Result

- Rule ID: 2502
- MITRE ATT&CK: T1110 (Brute Force)
- Category: Credential Access
- Log source: /var/log/auth.log
