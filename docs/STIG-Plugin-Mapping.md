# 📊 Nessus Plugin to STIG Control Mapping

This table maps Nessus vulnerability plugin IDs to DISA STIG IDs and NIST 800-53 control families.  
It supports POA&M documentation, ISSO reporting, and traceability of remediation efforts.

| #  | Plugin ID | Vulnerability Title                          | STIG ID    | NIST Control | Status          | Evidence File                           | Notes |
|----|-----------|----------------------------------------------|------------|--------------|------------------|-------------------------------------------|-------|
| 1  | 26920     | SMBv1 Enabled                                | V-254276   | CM-7         | ✅ Resolved      | finding_smb_post.png                      | Disabled SMBv1 via Ansible. Verified by PowerShell and Nessus scan. |
| 2  | 65796     | Weak Password Policy                          | V-254445   | AC-2         | ✅ Resolved      | finding_passwordpolicy_post.png           | Password policy updated. |
| 3  | 20007     | TLS 1.0 Enabled                               | V-254354   | SC-7         | ✅ Resolved      | tls_ssl_multiple_issues_post.png          | TLS 1.0 disabled in registry. |
| 4  | 19506     | Windows Defender Not Up to Date               | V-254521   | SI-2         | ❌ Open (POA&M)  | windows_defender_update_post.png         | Will be remediated through enterprise WSUS. |
| 5  | 103440    | RDP NLA Not Enforced (Example)                | V-254289   | SC-7         | ✅ Resolved      | finding_rdp_post.png                      | NLA enforced and confirmed. |

## 📎 Status Legend
- ✅ **Resolved:** Finding remediated and validated.  
- ❌ **Open (POA&M):** Finding remains open and tracked in POA&M documentation.  
- ⏳ **Planned:** Mitigation planned for a future date.  
