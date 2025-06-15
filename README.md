# azure-vm-backup-and-recovery-lab
Hands-on lab project that demonstrates how to configure backup, monitoring, and disaster recovery for Azure virtual machines using Recovery Services vaults and Azure Site Recovery.

# Azure VM Backup & Disaster Recovery Lab

## Overview

This project is a hands-on lab to demonstrate how to back up and replicate Azure virtual machines using:

- **Recovery Services vault**
- **Azure Backup Policies**
- **Azure Site Recovery for disaster recovery**

The lab was completed as part of my Azure learning journey and aligns with key responsibilities of a Cloud Infrastructure Engineer or Site Reliability Engineer (SRE).

---

## Lab Tasks

### Task 1: Provision Infrastructure
- Deployed a VM using ARM template.
- Region: East US.

### Task 2: Create Recovery Services Vault
- Created `az104-rsv-region1` in the same region.
- Configured backup storage type: **Geo-redundant**.
- Enabled Soft Delete.

### Task 3: Configure VM Backup
- Created a backup policy: `az104-backup`
- Frequency: Daily at 12:00 AM
- Retention: 2 Days
- Enabled backup for VM: `az104-10-vm0`

### Task 4: Monitor Backup
- Created a storage account to store logs.
- Enabled diagnostic settings to track:
  - Azure Backup Reporting
  - Backup Alerts
  - Site Recovery Events
- Verified backup status via Azure portal.

### Task 5: Enable VM Replication
- Created a second vault in West US for disaster recovery.
- Enabled replication of VM from East US to West US.
- Verified synchronization and replication health.

---

## Skills Demonstrated

- Azure ARM template deployment
- Recovery Services vault creation & configuration
- Backup policy design and VM protection
- Diagnostic settings & monitoring setup
- Azure Site Recovery (ASR) configuration
- Cross-region redundancy and disaster recovery planning

---

## 💡 Key Learnings

- How Azure handles backup, restore, and replication at the VM level
- Best practices for data protection in multi-region Azure environments
- How to monitor backups using diagnostic settings and Azure Monitor

