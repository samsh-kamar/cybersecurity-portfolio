# Lab 8: NIST CSF Incident Report - ICMP Flood DoS Attack

Scenario from the Google Cybersecurity Certificate course - practice activity, not a real incident.

## Summary
A multimedia company that offers web design, graphic design, and social media marketing services experienced a DoS attack that lasted 2 hours. Network services stopped responding because of a flood of incoming ICMP packets. Normal traffic could not reach network resources. The team blocked incoming ICMP packets, stopped non-critical services, and restored critical services.

## Identify
- **Type of attack:** DoS attack using an ICMP flood (ping flood)
- **Systems impacted:** Internal network, network services, firewall, and all internal devices
- **Cause:** An unconfigured firewall with no ICMP filtering and no source IP verification
- **Business impact:** Services were disrupted for 2 hours

## Recommendations

### Protect
- Configure the firewall to limit the rate of incoming ICMP packets
- Enable source IP verification to check for spoofed IP addresses
- Use an IDS/IPS to filter ICMP traffic
- Apply least privilege for firewall changes
- Train staff
- Audit the firewall monthly

### Detect
- Use network monitoring software to spot abnormal patterns
- Use a SIEM to collect firewall and IDS logs
- Use an IDS to flag suspicious ICMP traffic
- Set alerts for high ICMP volume and spoofed sources
- Review logs daily

### Respond
- **Containment:** Block ICMP packets and isolate network segments
- **Neutralization:** Stop non-critical services and filter malicious traffic
- **Communication:** Inform the incident team, IT, management, and employees
- **Analysis:** Collect firewall, IDS/IPS, and traffic logs, and preserve evidence
- **Improvements:** Update the response plan, add a DoS playbook, and hold a lessons-learned review

### Recover
- Restore critical services first, then non-critical services
- Verify that the new firewall rule, IP verification, monitoring, and IDS/IPS work
- Test employee access
- Communicate recovery status
- Document the recovery steps
- Back up firewall configurations
- Test the recovery plan every 3 months

## Source
Google Cybersecurity Certificate, Course 3 - Networks and Network Security. Activity: Incident Report Analysis using NIST CSF
