# Privilege Escalation & Persistence Lab

## Objective

Escalate privileges and maintain long-term access on compromised systems.

## Target Environment

VulnHub Linux VM ([Mr. Robot](https://www.vulnhub.com/entry/mr-robot-1,151/))

Target IP: 192.168.8.155

## Tools Used

Meterpreter

LinPEAS

PowerSploit

## Privilege Escalation Log

| Task ID | Technique    | Target IP       | Status  | Outcome    |
|--------|--------------|-----------------|---------|------------|
| 010    | SUID Exploit | 192.168.8.155   | Success | Root Shell |


## Persistence

Persistence was achieved by creating a malicious cron job executing a reverse shell at scheduled intervals. This ensured continued access even after system reboots, simulating real-world attacker persistence techniques commonly observed in advanced intrusions.
