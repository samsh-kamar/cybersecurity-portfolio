# Hi, I'm Samsh Kamar

**B.Tech CSE (Cyber Security) | BIT Sindri | 1st Year | Aspiring SOC Analyst**

## 👤 About Me

I am a first-year cybersecurity student focused on defensive security, SOC operations, and hands-on labs. I believe in learning by doing and documenting everything. This repository is my working portfolio: it tracks the labs, projects, and audits I complete as I progress through my studies and the Google Cybersecurity Professional Certificate. Everything listed here is student work, and I update it as I learn.

## 🛠️ Skills

- **Blue Team:** SOC Fundamentals, Log Analysis, Incident Response (Concepts), NIST CSF
- **Security Concepts:** CIA Triad, Encryption, Firewalls, IAM, Least Privilege, MFA
- **Tools:** Linux, Python, SQL, Git, VirtualBox, tcpdump - analyzing DNS / ICMP packet captures
- **Web Security** (Concepts - OWASP Top 10, SQL Injection, XSS)

## 📁 Projects

### 1. VoxGuard - Jan-Sahayak PS-04
Public grievance intake prototype with duplicate detection - Built for Bihar Police Cyber Hackathon

- Repo: https://github.com/samsh-kamar/voxguard
- Overview: [/projects/voxguard](./projects/voxguard/README.md)

### 2. Botium Toys - Internal Security Audit
Conducted a full internal security audit for a fictional toy company using NIST CSF.

- **Findings:** No Least Privilege, No Password Policy, No Encryption, No Disaster Recovery Plan, Non-compliant with PCI DSS and GDPR.
- **Recommendation:** Implement MFA, Encryption, Least Privilege, Regular Backups, and a Compliance Audit.
- Full report: [/audits/Botium-Toys-Audit.md](./audits/Botium-Toys-Audit.md)

### 3. Linux File Permissions Lab
Used `chmod`, `chown`, and `ls -la` to secure files and explained how misconfigured permissions cause privilege escalation.

- Write-up: [/labs/linux-file-permissions.md](./labs/linux-file-permissions.md)

### 4. SQL Filtering for SOC Analysis
Used SQL with `WHERE`, `AND`, and `OR` to filter suspicious login attempts like a SOC analyst.

- Write-up: [/labs/sql-filtering-lab.md](./labs/sql-filtering-lab.md)

### 5. YummyRecipes - Security Incident Investigation (Course Practice Scenario)
Investigated a simulated compromised website (yummyrecipesforme.com) using tcpdump packet analysis as part of Google Cybersecurity Certificate coursework.
Identified DNS, TCP, and HTTP protocols in the attack chain.

- **Findings:** Brute force attack via default admin password, malicious JavaScript injected to prompt malware download, users redirected to fake site greatrecipesforme.com.
- **Recommendation:** Enforce MFA/2FA, Limit login attempts, Enforce strong non-default passwords.
- Full report: [/incidents/yummyrecipes-incident-report.md](./incidents/yummyrecipes-incident-report.md)

## 🎓 Certifications

- Google Cybersecurity Professional Certificate - **In Progress** (3/8 courses completed)
  - Foundations of Cybersecurity (Google) - Completed
  - Play It Safe: Manage Security Risks (Google) - Completed
  - Connect and Protect: Networks and Network Security (Google) - Completed - Grade: 97.5% Module 1, 95% Module 2, 100% Module 3, 90% Module 4, 100% Portfolio Activity (NIST CSF)

### Additional Course

- Crash Course on Python (Google) - Completed

Details: [/certifications](./certifications)

## 🧪 Labs & Write-ups

Labs are documented in this repository - most in /labs, Lab 3 (YummyRecipes) in /incidents. Labs 5-6 are separate repositories linked below.

- [Linux File Permissions Lab](labs/linux-file-permissions.md) - Securing files with `chmod` and `chown`, and how misconfigured permissions lead to privilege escalation
- [SQL Filtering for SOC Analysis](labs/sql-filtering-lab.md) - Filtering suspicious login attempts with SQL
- [Lab 1: DNS and ICMP Analysis](labs/dns-icmp-analysis.md) - Troubleshooting DNS failure with packet capture
- [Lab 2: SYN Flood (DoS) Attack Analysis](labs/syn-flood-dos-analysis.md) - Analyzing a TCP SYN flood that took a travel agency web server offline
- [Lab 3: YummyRecipes Incident Response](incidents/yummyrecipes-incident-report.md) - Brute force and malware redirect investigation. See full report in /incidents/yummyrecipes-incident-report.md
- [Lab 4: OS Hardening](labs/os-hardening-lab.md) - Hardening Ubuntu Linux in VirtualBox: unused services, UFW firewall, patching, least privilege, default accounts
- Lab 5: Safe Practice Lab Setup - Built an isolated cybersecurity lab on Ubuntu 24.04 LTS using VirtualBox. Ubuntu Server VM with host-only networking and snapshots for safe, legal practice. Repo: https://github.com/samsh-kamar/safe-practice-lab-setup
- Lab 6: Linux Command Line Notebook - Linux CLI lab completed in 2 days - Ubuntu VM (VirtualBox) | 50+ commands | permissions with snapshots. Repo: https://github.com/samsh-kamar/linux-cli-notebook
- [Lab 7: Network Hardening Risk Assessment](labs/network-hardening-risk-assessment.md) - Analyzed a social media data breach with 4 vulnerabilities and recommended firewall filtering, MFA, and password policy. Write-up: /labs/network-hardening-risk-assessment.md
- [Lab 8: NIST CSF Incident Report](labs/nist-csf-dos-incident-report.md) - Analyzed an ICMP flood DoS attack using Identify, Protect, Detect, Respond, Recover. Write-up: /labs/nist-csf-dos-incident-report.md

## 📫 Contact

- GitHub: [samsh-kamar](https://github.com/samsh-kamar)
- LinkedIn: [Samsh Kamar](https://www.linkedin.com/in/samsh-kamar-158688380)
- Location: Ranchi, Jharkhand, India | Studying at BIT Sindri, Dhanbad

## 🗂️ Repository Structure

```
cybersecurity-portfolio/
├── labs/            # Hands-on lab write-ups
├── projects/        # Personal security projects (e.g. VoxGuard)
├── certifications/  # Certification progress and notes
├── audits/          # Security audit reports
├── incidents/       # Incident investigation reports
└── README.md
```
