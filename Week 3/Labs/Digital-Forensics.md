# Digital Forensics and Log Analysis

## Objective
To identify evidence of exploitation and attacker activity through system logs.

## Logs Analyzed
- Authentication logs
- System logs
- Network service logs

## Commands Used
```bash
ls /var/log
cat /var/log/auth.log
cat /var/log/syslog
```
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/0297a6a4-9d25-4c67-8b3b-2c53d84dd50c" />

```
last
```
<img width="676" height="248" alt="image" src="https://github.com/user-attachments/assets/592ddf05-e937-4ccb-a096-6572843d3807" />

## Findings
Evidence of unauthorized service interaction
IRC service activity corresponding to exploitation timeframe
Root access sessions recorded

### Integrity Verification
```
sha256sum shadowed.txt
```
<img width="1920" height="1080" alt="week3-log-and-integrity check" src="https://github.com/user-attachments/assets/78e3e2eb-e0db-4f86-9db7-aea970c2e0b4" />

Conclusion

Logs confirmed successful exploitation and privilege escalation,
supporting the penetration test findings.
