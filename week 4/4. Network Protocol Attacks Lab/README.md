# Network Protocol Attacks Lab

## Objective

Exploit insecure network protocols using Man-in-the-Middle techniques.

## Target Environment

TryHackMe Network Lab

Target IP: 192.168.8.160

## Tools Used

Responder

Ettercap

Wireshark

## Attack Log
Attack ID	Technique	Target IP	Status	Outcome
015	SMB Relay	192.168.8.160	Success	NTLM Hash

## MITM Summary
ARP spoofing was performed using Ettercap to intercept network traffic. Responder successfully captured NTLM hashes through SMB relay attacks, demonstrating the risks of weak authentication protocols and lack of network segmentation in enterprise environments.
