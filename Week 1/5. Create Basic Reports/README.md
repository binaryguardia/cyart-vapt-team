# Reporting and Documentation

This section documents the findings from exploiting the **vsftpd vulnerability** on the Metasploitable target system and presents a structured security assessment report.

---

## Objective
- Summarize identified vulnerabilities
- Document exploitation evidence
- Provide clear remediation guidance
- Prepare a comprehensive report suitable for submission as a PDF

---

## Sources Consulted
- NVD (National Vulnerability Database)
- Exploit-DB
- Metasploit Framework documentation
- CVSS Calculator
- Vendor security advisories

---

## Executive Summary

During the penetration testing exercise, a critical vulnerability was identified in the **vsftpd service** running on the Metasploitable machine.  
The vulnerable version allows **unauthenticated remote code execution**, enabling an attacker to gain shell access to the system.

### Key Risks Identified
- Full system compromise
- Unauthorized remote access
- Potential pivoting to internal network assets

**Overall Risk Level:** Critical

---

## Technical Details

### Target Information
- Target IP: `192.168.8.144`
- Service: FTP
- Port: `21`
- Software: `vsftpd 2.3.4`

---

### Vulnerability Description

The vsftpd 2.3.4 version contains a **backdoor vulnerability** that allows attackers to spawn a shell by sending a specially crafted username during FTP authentication.

- CVE ID: `CVE-2011-2523`
- Vulnerability Type: Remote Code Execution
- Authentication Required: No

---

### Exploitation Process

1. Identify FTP service running on port 21.
2. Confirm vulnerable vsftpd version via service banner.
3. Use Metasploit Framework to exploit the vulnerability.
4. Successful exploitation results in shell access on port 6200.

### Evidence
- Metasploit session established
- Command execution confirmed
- Screenshots captured for:
  - Exploit execution
  - Shell access
  - System user context

---

### CVSS Scoring

- Base Score: **10.0**
- Severity: **Critical**
- Attack Vector: Network
- Privileges Required: None
- User Interaction: None
- Impact: Complete compromise (CIA)

---

## Remediation and Mitigation

### Recommended Fixes
- Upgrade vsftpd to the latest secure version
- Disable FTP if not required
- Use SFTP or FTPS instead of FTP
- Restrict service exposure using firewall rules

### Patch References
- Official vsftpd website
- Linux distribution security advisories
- Vendor patch management guidelines

---

## Conclusion

The exploitation of the vsftpd vulnerability demonstrates the severe risk posed by outdated and misconfigured services.  
Immediate remediation is required to prevent unauthorized access and system compromise.

This report highlights the importance of:
- Regular vulnerability scanning
- Timely patch management
- Secure service configurations
