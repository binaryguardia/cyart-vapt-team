# Full VAPT Report – PTES Methodology

A full penetration test was conducted against a Metasploitable2 system following
the Penetration Testing Execution Standard (PTES). Reconnaissance identified
multiple exposed services, including UnrealIRCd running on port 6667.

Vulnerability analysis revealed that UnrealIRCd 3.2.8.1 contained a known backdoor
that allows unauthenticated remote command execution. Exploitation was performed
using a public Perl proof-of-concept exploit, which successfully delivered a payload
and spawned a bind shell on the target system.

Post-exploitation activities confirmed root-level access. Sensitive system files
such as `/etc/passwd` and `/etc/shadow` were accessed, and password hashes were
extracted and cracked. Digital forensic analysis of system logs validated the
timeline of compromise.

The impact of this vulnerability is critical, as it allows complete system takeover.
Immediate remediation is recommended, including removal of vulnerable services,
patch management, firewall enforcement, and continuous monitoring.
