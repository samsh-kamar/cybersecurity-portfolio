# YummyRecipes - Security Incident Investigation

> Course Practice Scenario: this is a simulated incident from the Google Cybersecurity Certificate coursework, not a real incident.

## Summary
Investigated a simulated compromised website (yummyrecipesforme.com) using tcpdump packet analysis. The analysis identified DNS, TCP, and HTTP protocols in the attack chain.

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
