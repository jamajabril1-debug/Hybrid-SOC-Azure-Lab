# Environment Setup

## Hypervisor
VMware

## SIEM
- Ubuntu Server 22.04
- 4GB RAM
- 2 CPUs
- 50GB Disk

## Endpoint
- Ubuntu 22.04 LTS
- SSH enabled
- Wazuh agent installed

## Lessons Learned
- Duplicate agent names prevent enrollment
- Misconfigured ossec.conf breaks log ingestion
- Filebeat authentication must be correct
