# 🛡 STIG Hardening & Continuous Vulnerability Validation Lab

## 📌 Project Overview
This lab demonstrates how to harden a Windows Server 2022 host using DISA STIGs and validate remediation through credentialed Nessus scans. It simulates a controlled vulnerability management workflow that connects technical hardening with compliance controls and POA&M tracking.

### **Objectives**
- Apply STIG controls to a Windows Server 2022 machine.  
- Run baseline and post-hardening Nessus credentialed scans.  
- Validate vulnerability closure.  
- Generate STIG and POA&M artifacts suitable for ISSO reporting.

### **Stack**
- Windows Server 2022 (Admin + Standard user)  
- Nessus Professional (Linux host)  
- DISA STIG Viewer  
- PowerShell  
- Ansible (control node for automation)

✅ **Mapped Controls:** AC-2, AC-3, CM-7, SI-2, SC-7  

```mermaid
flowchart TD
    A[Start] --> B[Step 1: Baseline ACAS Scan]
    B --> C[Step 2: Import Findings & Map to STIGs]
    C --> D[Step 3: Develop Ansible Playbook for Remediation]
    D --> E[Step 4: Execute Playbook on Target Host]
    E --> F[Step 5: Verify Remediation Locally]
    F --> G[Step 6: Run Post-Hardening ACAS Scan]
    G --> H{All Findings Closed?}
    H -- Yes --> I[Step 7: Archive Artifacts & Document in POA&M]
    H -- No --> D
    I --> J[End]
