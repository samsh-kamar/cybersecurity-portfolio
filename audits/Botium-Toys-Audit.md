# Botium Toys - Internal Security Audit

> **Note:** Botium Toys is a fictional company used in a learning scenario. This audit is a student exercise completed as part of my cybersecurity studies, not a professional engagement.

## Scope

The audit covers Botium Toys' security posture, assessed against the **NIST Cybersecurity Framework (CSF)**, with attention to compliance requirements under **PCI DSS** and **GDPR**.

## Goals

- Assess existing security controls against NIST CSF
- Identify gaps and risks to company assets
- Check compliance with PCI DSS and GDPR
- Recommend prioritized improvements

## Findings

| # | Finding | Why it matters |
|---|---|---|
| 1 | No Least Privilege | Users have more access than their role needs, increasing the impact of mistakes or compromised accounts |
| 2 | No Password Policy | Weak or reused passwords make account compromise easier |
| 3 | No Encryption | Sensitive data, including customer payment information, is exposed if intercepted or stolen |
| 4 | No Disaster Recovery Plan | The business cannot reliably recover from data loss or an outage |
| 5 | Non-compliant with PCI DSS and GDPR | Exposes the company to regulatory and financial risk |

## Recommendations

1. **Implement MFA** to reduce the risk of account takeover.
2. **Implement Encryption** for data at rest and in transit, especially payment and customer data.
3. **Enforce Least Privilege** so access matches job responsibilities.
4. **Perform Regular Backups** and establish a tested disaster recovery plan.
5. **Conduct a Compliance Audit** against PCI DSS and GDPR and close the gaps found.

## Framework Reference

Framework: NIST CSF 2.0 - Govern, Identify, Protect, Detect, Respond, Recover

The findings above mainly fall under **Protect** (access control, encryption, password policy) and **Recover** (disaster recovery and backups).

## Takeaways

This exercise helped me practice structuring an audit, mapping findings to a framework, and writing recommendations that a non-technical stakeholder can act on.
