# Capstone – Full VAPT Cycle (PTES)

## Target
DVWA – 192.168.8.144

## SQL Injection Test
```bash
sqlmap -u "http://192.168.8.144/dvwa/vulnerabilities/sqli/?id=1&Submit=Submit" \
--cookie="PHPSESSID=6a812f993ea7b337c2fe2ad7f3491e09; security=low" \
--dbs --level=5 --risk=3 --batch
```
### Payload used
```bash
1'+AND+(SELECT+3899+FROM+(SELECT(SLEEP(5)))AYSl)--+dDxS
```
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/4ba30e08-7422-4c27-96db-d6387b92dd9f" />

## Remediation
- Input sanitization
- Prepared SQL statements
- Re-scan after patching

## PTES Report (200 words)
The penetration test was conducted against the Damn Vulnerable Web Application (DVWA) hosted at 192.168.8.144, following the Penetration Testing Execution Standard (PTES). The engagement began with scoping and reconnaissance to identify exposed web application components. During the scanning and vulnerability analysis phase, the SQL Injection module within DVWA was identified as a potential attack surface.

Exploitation was performed using the sqlmap automated tool with a valid authenticated session and low security configuration. The SQL injection vulnerability was successfully confirmed through time-based blind injection, as demonstrated by delayed server responses using crafted payloads. Further exploitation allowed enumeration of available databases on the target system, confirming unauthorized access to backend database resources.

Post-exploitation analysis demonstrated the potential impact of the vulnerability, including unauthorized data disclosure and database manipulation. Although no destructive actions were performed, the findings confirm that an attacker could extract sensitive information, modify application data, or escalate the attack to other components of the system.

The vulnerability poses a significant risk to confidentiality and integrity due to improper input validation. Immediate remediation is recommended, including the use of prepared statements, proper input sanitization, and regular security testing. A follow-up scan should be conducted after applying fixes to ensure the vulnerability has been fully mitigated.

## Non-Technical Summary (100 words)
Critical vulnerabilities were identified that allow attackers to access sensitive data...

