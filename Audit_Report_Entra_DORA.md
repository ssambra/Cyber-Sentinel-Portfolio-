# Audit Report: Identity Governance & Insider Threat Detection (Microsoft Entra)
**Alignment:** DORA Article 9 (Protection and Prevention)
**Scope:** Behavioral Identity Auditing for Critical Financial Systems

## 1. Audit Methodology
Evaluated the implementation of 'Least Privilege' and 'Zero Trust' within the Microsoft Entra ID (formerly Azure AD) environment. Audit focused on the detection of anomalous behavior indicative of insider threats.

## 2. Configured Controls (Simulated)
- **Conditional Access (CA) Policies:** Implemented "Location-Based MFA" and "Device Compliance Verification" for all accounts with Administrative Roles.
- **Privileged Identity Management (PIM):** Enforced Just-In-Time (JIT) access for Global Admin and Security Admin roles to minimize the permanent attack surface.
- **Identity Protection:** Configured alert thresholds for "Impossible Travel" and "Leaked Credentials."

## 3. Behavioral Detection Log (Sample)
| Timestamp | Identity | Event Type | Risk Level | Action Taken |
| :--- | :--- | :--- | :--- | :--- |
| 2026-04-25 14:22 | admin_jt_01 | Unusual login location (Tor Exit Node) | High | Account Blocked / MFA Reset |
| 2026-04-25 16:05 | svc_pwr_shell | Excessive Permission Escalation Attempt | Critical | Service Principal Disabled |

## 4. Auditor Conclusion
The current Entra configuration satisfies DORA requirements for robust identity management. Recommendations include quarterly access reviews for all users with 'critical function' permissions.
