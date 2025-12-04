Week 2 – Entra ID + Intune Zero Trust Security Foundation

This week focuses on implementing identity protection, device compliance, and Zero Trust controls using Microsoft Entra ID and Microsoft Intune.

🔐 1. Identity Architecture (Entra ID)
Users & Identity Roles Created

Cloud Administrator

Intune Administrator

Helpdesk Technician

Standard Employees

Test Users for CA validation

Key Learnings

Role separation improves security

Test users help validate real-world policy behavior

Administrative accounts must be isolated

Security Groups Created

grp-all-users

grp-intune-users

grp-windows-devices

grp-mfa-required

grp-cloud-admins

grp-autopilot-devices

Break-glass exclusion group

Key Learnings

Identity governance relies heavily on group-based targeting

CA, compliance, and app deployments become scalable with RBAC groups

MFA Registration (Tenant-Wide)

Mandatory MFA registration enabled

Authentication Methods → Registration Campaign configured

Break-glass accounts excluded

Key Learnings

MFA is the first pillar of Zero Trust

Emergency accounts must bypass MFA to avoid lockout scenarios

🔒 2. Conditional Access Security Model
Policies Implemented

Require MFA for all users

Require compliant device

Block legacy authentication

Location-based filtering

Break-glass exclusions

Testing

Verified enforcement using Entra Sign-In Logs

Checked grant controls, session controls, and policy evaluation paths

Key Learnings

CA is enforced after authentication, during token issuance

Policy layering ensures secure access based on device + identity

Sign-in logs are critical for troubleshooting

💻 3. Intune Device Enrollment & Compliance
Enrollment Steps Completed

Windows enrollment

Enrollment restrictions configured

Device Categories:

Production

Non-Production

BYOD

Key Learnings

Device categories help automate app deployments & CA targeting

Blocking personal Windows improves corporate governance

Windows Compliance Baseline

Policy Name: NL-Windows-Compliance-Baseline

Compliance Checks Enabled

BitLocker required

Secure Boot enabled

TPM required

Firewall enabled

Antivirus + Real-time protection

Password complexity

Device health attestation

Assignments

grp-intune-users

grp-windows-devices

Verification

Devices correctly marked compliant / noncompliant

CA policies enforced based on compliance state

📸 Included Screenshots

Entra Users

Entra Groups

MFA Registration

Conditional Access list

Individual CA Policies

Sign-In logs

Windows Enrollment

Enrollment Restrictions

Device Categories

Compliance Policy + Assignments


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
