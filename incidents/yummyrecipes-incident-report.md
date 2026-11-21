# YummyRecipes - Security Incident Investigation

> Course Practice Scenario: this is a simulated incident from the Google Cybersecurity Certificate coursework, not a real incident.

## Summary
Investigated a simulated compromised website (yummyrecipesforme.com) using tcpdump packet analysis. Identified DNS, TCP, and HTTP protocols in the attack chain.

## Timeline
- **T0:** Attacker starts a brute force attack on the admin panel, trying known default passwords.
- **T1:** Attacker gains access and injects JavaScript into the website's source code.
- **T2:** Attacker changes the admin password, locking out the owner.
- **T3 (several hours later):** Customers email the helpdesk. They report being prompted to download a file and being redirected to greatrecipesforme.com. They also report that their PCs are running slowly.
- **T4:** The owner tries to log in, fails, and contacts the hosting provider.
- **T5:** An analyst runs tcpdump in a sandbox environment, visits yummyrecipesforme.com, and reproduces the redirect.

## Protocol-Stage Table

| Stage | Protocol | What Happened |
| --- | --- | --- |
| 1. Name Resolution | DNS (UDP 53) | Browser asks DNS for yummyrecipesforme.com IP |
| 2. Connection | TCP | 3-way handshake between browser and web server |
| 3. Web Request | HTTP (TCP 80) | Browser requests webpage, gets malicious JavaScript |
| 4. Malware Download | HTTP | Browser downloads executable file |
| 5. Redirect | DNS + HTTP | Browser asks DNS for greatrecipesforme.com, then HTTP request to fake site |

## Findings
- Brute force attack via the default admin password
- Malicious JavaScript injected into the website to prompt visitors to download malware
- Users redirected to a fake site, greatrecipesforme.com

## Recommendations
- Enforce MFA/2FA
- Limit login attempts
- Enforce strong, non-default passwords

## Related Lab
Related Lab: See [Lab 1 - DNS and ICMP Analysis](../labs/dns-icmp-analysis.md) for the earlier DNS failure stage of the same scenario.
