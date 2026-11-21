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
Public grievance intake prototype with duplicate detection - Built for Bihar Police Cyber Hackathon (Private Repo)

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

- Google Cybersecurity Professional Certificate - **In Progress** (2/8 courses completed)
- Foundations of Cybersecurity (Google) - Completed - Credential ID: Z31U3YLLPT7H
- Play It Safe: Manage Security Risks (Google) - Completed - Credential ID: I1NEB761VC9S
- Crash Course on Python (Google) - Completed - Credential ID: FZN2TALBCNU2

Details: [/certifications](./certifications)

## 🧪 Labs & Write-ups

All labs are documented in the [/labs](./labs) folder.

- [Linux File Permissions Lab](labs/linux-file-permissions.md) - Securing files with `chmod` and `chown`, and how misconfigured permissions lead to privilege escalation
- [SQL Filtering for SOC Analysis](labs/sql-filtering-lab.md) - Filtering suspicious login attempts with SQL
- [Lab 1: DNS and ICMP Analysis](labs/dns-icmp-analysis.md) - Troubleshooting DNS failure with packet capture
- [Lab 2: SYN Flood (DoS) Attack Analysis](labs/syn-flood-dos-analysis.md) - Analyzing a TCP SYN flood that took a travel agency web server offline
- [Lab 3: YummyRecipes Incident Response](incidents/yummyrecipes-incident-report.md) - Brute force and malware redirect investigation. See full report in /incidents
- [Lab 4: OS Hardening](labs/os-hardening-lab.md) - Hardening Ubuntu Linux in VirtualBox: unused services, UFW firewall, patching, least privilege, default accounts

## 📫 Contact

- GitHub: [samsh-kamar](https://github.com/samsh-kamar)
- LinkedIn: [Samsh Kamar](https://www.linkedin.com/in/samsh-kamar-158688380)
- Location: Ranchi, Jharkhand, India

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
