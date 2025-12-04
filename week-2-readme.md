🚀 Week 2 – Entra ID + Intune Zero Trust Security Foundation

This week focused on building the identity and device management foundation required for an enterprise-grade Zero Trust architecture using Microsoft Entra ID and Microsoft Intune.
The objective was to design a secure identity model, enforce MFA, implement Conditional Access, configure device enrollment, and establish compliance controls that dictate how trusted devices access cloud resources.

🔐 1. Identity Architecture (Microsoft Entra ID)
📌 What I Did

Created a full identity hierarchy including:
Cloud Administrator
Intune Administrator
Helpdesk Technician
Standard Employees
Test Users

Created RBAC-driven security groups for scalable management:

grp-all-users
grp-intune-users
grp-windows-devices
grp-mfa-required
grp-cloud-admins
grp-autopilot-devices
Break-glass exclusion group

📘 What I Learned

Identity architecture must separate privileged and non-privileged accounts.
Administrators should always have a secondary emergency (break-glass) account with MFA/CA exclusions to avoid tenant lockouts.
Groups are the core of enterprise identity governance:
CA policies target groups
Compliance policies target groups
App assignments target groups
RBAC is built around groups
This ensures a scalable, secure, centralized identity model used in real organizations.

🔒 2. Conditional Access – Zero Trust Policy Framework
📌 What I Did

I implemented a modern CA security stack:
Policies Implemented
Require MFA for all users
Require compliant device
Block legacy authentication
Country-based access controls
Break-glass exclusions

Testing
Verified all policies through Entra Sign-In Logs
Observed MFA prompts, compliant-device requirements, and legacy auth blocks

📘 What I Learned

Conditional Access enforces Zero Trust by evaluating:
user identity
device posture
risk level
location
app being accessed
Legacy protocols bypass MFA and pose risk → must be blocked
CA decisions happen during token issuance, not during password entry
Sign-in logs are essential for troubleshooting misconfigurations
This is the same architecture major enterprises use to secure identity access.

💻 3. Intune Device Enrollment & Platform Restrictions
📌 What I Did

Configured Windows enrollment
Created enrollment restrictions:
Block personal Windows enrollment
Allow only Android Enterprise (block Android Device Admin)
Allow macOS & iOS
Created device categories:
Production
Non-Production
BYOD (Personal)

📘 What I Learned

Enrollment restrictions prevent unmanaged or outdated devices from entering the environment
Device categories help automate:
compliance targeting
app deployments
Autopilot assignments
CA enforcement
Modern device onboarding starts with clear governance: what is allowed vs blocked
This ensures corporate devices remain the only trusted endpoints.

🛡 4. Compliance Baseline – Enforcing Device Security
📌 What I Did

Created a Windows 10/11 compliance policy that requires:
BitLocker drive encryption
Secure Boot
Firewall enabled
Defender Antivirus + real-time protection
Password complexity
TPM presence
Device health attestation
Noncompliance marking after 1 day
Assigned to:
grp-intune-users
grp-windows-devices

📘 What I Learned

Compliance policies determine which devices are “trusted”
Conditional Access uses compliance state to allow or block access
This creates resource access that is identity + device + security posture aware
Device compliance is the backbone of Zero Trust endpoint security
This mirrors how enterprises validate device health before granting access.


<img width="1902" height="962" alt="CA_policy" src="https://github.com/user-attachments/assets/5914e235-d674-4159-ab92-1f0f24ba1af8" />
<img width="1918" height="960" alt="compliance_policy_details" src="https://github.com/user-attachments/assets/b4b64a51-661e-45d9-b43c-eb46b1660d75" />
<img width="1898" height="937" alt="device_Categories " src="https://github.com/user-attachments/assets/04eb7389-41e6-4977-99ce-f1a897a9b7e8" />
<img width="1912" height="954" alt="enrollment_restriction" src="https://github.com/user-attachments/assets/68eb162b-300a-42b6-80e5-523331706eb4" />
<img width="1903" height="953" alt="EntraID_ALlgrps" src="https://github.com/user-attachments/assets/c741f894-c92b-4e2e-a5b3-59ce2069c681" />
<img width="1884" height="935" alt="EntraID_users" src="https://github.com/user-attachments/assets/09f46f1d-a3aa-40f6-b932-4c900caadd0e" />
<img width="1894" height="939" alt="registration campaign" src="https://github.com/user-attachments/assets/7cd365e2-9c30-4f49-bb5d-0a7922112ffe" />
<img width="1885" height="964" alt="Required MFA_" src="https://github.com/user-attachments/assets/c015a93d-56a1-4cb9-af2e-e1eba1b25570" />
<img width="1910" height="959" alt="Required MFA_3" src="https://github.com/user-attachments/assets/c00fb322-6fc7-40b7-a7e4-e433a2efb084" />
<img width="1889" height="965" alt="RequiredMFA CA" src="https://github.com/user-attachments/assets/1f84a40a-fc63-424e-a20d-717e9b3ade7d" />
<img width="1897" height="938" alt="signinlogs" src="https://github.com/user-attachments/assets/ccf008f4-e3a5-4eea-ac27-98c881d7624c" />
