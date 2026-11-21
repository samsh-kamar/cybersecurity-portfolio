# Lab 7: Network Hardening Risk Assessment - Social Media Data Breach

## Scenario
A social media organization had a major data breach. Customer personal information, such as names and addresses, was compromised.

Scenario from the Google Cybersecurity Certificate course - practice activity, not a real incident.

## Vulnerabilities Found
1. Employees share passwords
2. The admin password for the database is set to the default
3. Firewalls have no rules to filter inbound and outbound traffic
4. MFA is not used

## Hardening Methods Applied

### 1. Firewall Rule Configuration / Port Filtering
Configure firewall rules to filter inbound and outbound traffic. Allow only necessary ports and block all else by default. Review the rules monthly.

### 2. Multi-Factor Authentication (MFA)
Enforce MFA for all employees, especially admin and database accounts. A password alone is not enough.

### 3. Password Policy and Access Control
Enforce strong, unique passwords. Prohibit password sharing. Change all default passwords immediately. Apply least privilege access.

## Why Effective
- The firewall reduces the attack surface
- MFA blocks a login even if a password is stolen
- The password policy stops brute force attacks and credential reuse

Together, these controls help prevent another breach.

## Source
Google Cybersecurity Certificate, Course 3 - Networks and Network Security. Activity: Analysis of Network Hardening
