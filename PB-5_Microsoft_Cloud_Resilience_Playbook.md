# Playbook 5: Microsoft Cloud Resilience (DORA-Aligned)
**Author:** Ssambra | Resilience Architect & Identity Auditor
**Framework:** EU DORA (Regulation 2022/2554) mapped to Microsoft Azure/M365

## 1. Identity & Access (DORA Article 9)
**Objective:** Prevent unauthorized access to critical financial functions.
- **Enforcement:** Implement Microsoft Entra Conditional Access.
- **Control:** Block all legacy authentication; enforce Phishing-Resistant MFA (FIDO2) for 'Finance' and 'IT Admin' groups.
- **Audit:** Weekly PIM (Privileged Identity Management) activation reviews.

## 2. Detection & Reporting (DORA Article 17)
**Objective:** Standardize incident reporting across the EU.
- **Tooling:** Microsoft Sentinel (SIEM) + Defender for Cloud.
- **Logic:** Automated triggers for 'Impossible Travel' and 'Brute Force' on critical service accounts.
- **Workflow:** Sentinel Playbooks automatically notify the Risk Management function upon detection of a 'High' severity alert.

## 3. Resilience Testing (DORA Article 24)
**Objective:** Prove the ability to withstand ICT disruptions.
- **Method:** Annual TLPT (Threat-Led Penetration Testing) using Azure Chaos Studio.
- **Verification:** Quarterly "Soft-Failover" tests using Azure Site Recovery to validate RTO/RPO metrics.

## 4. Third-Party Risk (DORA Article 28)
**Objective:** Manage CTPP (Critical Third-Party Provider) concentration risk.
- **Artifact:** Microsoft Products and Services Data Protection Addendum (DPA) Review.
- **Strategy:** Maintain "Exit Strategy" documentation for critical workloads in case of regional cloud termination.
- 
