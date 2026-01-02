# Capstone – Full VAPT Cycle (PTES)

## Target
DVWA – 192.168.1.200

## SQL Injection Test

sqlmap -u http://dvwa/login.php
--dbs


📸 Screenshot: `Screenshots/sqlmap-dvwa.png`

## OpenVAS Detection Log
| Time | Target | Vulnerability | PTES Phase |
|----|--------|---------------|-----------|
| 12:00 | 192.168.1.200 | XSS | Exploitation |

## Remediation
- Input sanitization
- Prepared SQL statements
- Re-scan after patching

## PTES Report (200 words)
The penetration test followed PTES methodology... *(write full paragraph here)*

## Non-Technical Summary (100 words)
Critical vulnerabilities were identified that allow attackers to access sensitive data...

