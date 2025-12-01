# ☁️ Azure Cloud Architect Portfolio — Enterprise Landing Zone Project

This repository documents my end-to-end Azure Cloud Architect project, where I am building a full enterprise Landing Zone from scratch.  
The project follows Microsoft’s Cloud Adoption Framework (CAF) and mirrors how real cloud platform teams build identity, governance, networking, and security in production.

---

# 🧱 Week 1 – Enterprise Cloud Foundation (Identity → Intune → Azure)

Week 1 focused on establishing the **complete identity and governance foundation** using Microsoft Entra ID, Intune groundwork, and Azure Management Groups.  
This page outlines exactly what I built, what I learned, and how this matches real cloud architecture work.

---

## 1️⃣ Microsoft Entra ID – Identity Foundation

### ✔ What I did
- Set up my dedicated Microsoft Entra tenant (**NextLevel Cloud Lab**).
- Reviewed tenant details (tenant ID, domain, objects, apps, devices).
- Created security groups for:
  - Intune device targeting  
  - Role-based access  
  - Conditional Access alignment  
- Verified my admin account has **Global Administrator** rights and Azure resource access.

### ✔ What I learned
Identity is always the first step in cloud architecture.  
Everything (Azure access, Intune policies, Conditional Access, RBAC, MFA) depends on a solid identity configuration.

---

## 2️⃣ Intune Foundation – Preparing for Device & User Management

### ✔ What I did
- Prepared Entra security groups for:
  - Autopilot devices  
  - Intune-managed users  
  - Application and compliance targeting  
- Validated identity structure for later Intune enrollment & Zero Trust policies.

### ✔ What I learned
Intune relies heavily on Entra ID.  
A clean group and identity design makes device management scalable and secure.

---

## 3️⃣ Azure Management Group Hierarchy (CAF Model)

### ✔ What I built
A complete Microsoft Cloud Adoption Framework (CAF) hierarchy:
Tenant Root Group
│
├── Landing Zones
│ ├── Non-Production
│ └── Production
│
├── Platform
│ ├── Identity
│ ├── Connectivity (Networking)
│ └── Management
│
└── Sandbox


### ✔ What I learned
Management groups are the backbone of Azure governance.  
They control:
- Policy inheritance  
- Subscription organization  
- Access control  
- Environment separation  

This matches real enterprise architecture.

---

## 4️⃣ Subscription Placement – Non-Production Landing Zone

### ✔ What I did
Moved my Azure subscription under:
Landing Zones → Non-Production


### ✔ What I learned
Subscription placement defines which:
- Policies apply  
- RBAC roles flow down  
- Governance rules are enforced  

This is exactly how cloud platform teams manage large environments.

---

## 5️⃣ Resource Group Strategy – Enterprise-Level Structure

### ✔ Resource groups created
- `rg-identity`
- `rg-security`
- `rg-monitoring`
- `rg-platform`
- `rg-networking-hub`
- `rg-network-prod`
- `rg-network-nonprod`
- `rg-apps-prod-eastus`
- `rg-apps-nonprod-eastus`

### ✔ What I learned
A strong RG strategy helps with:
- Security boundaries  
- Cost allocation  
- Monitoring  
- Automation  
- Lifecycle management  
- Production vs non-production separation  

---

## 6️⃣ Governance with Azure Policy

### ✔ Policies implemented
- **Required Tag: environment (prod / nonprod)**
- **Allowed Locations: restrict deployments to East US**
- **Security baseline initiative**
- **Not allowed resource types**

### ✔ What I learned
Azure Policy enforces rules automatically, which ensures:
- Compliance  
- Security  
- Standardized deployments  
- Proper tagging  
- Region control  

This is exactly how enterprises prevent cloud sprawl.

---

## 7️⃣ Policy Compliance – Monitoring Governance

### ✔ What I did
- Used Azure Policy → Compliance to verify:
  - Compliant vs non-compliant resources  
  - Policy evaluation  
  - Enforcement effectiveness  

### ✔ What I learned
Compliance is ongoing.  
Cloud governance must be continuously monitored to detect drift.

---

## 8️⃣ RBAC at Tenant Root – Access Security

### ✔ What I did
- Verified **Owner** and **User Access Administrator** roles at the Root Management Group.
- Reviewed permission inheritance to Landing Zones and subscriptions.

### ✔ What I learned
RBAC scope is everything:
- The higher the scope, the more powerful the permissions.
- Real companies use strict least-privilege assignment.
- Root-level access is typically limited to platform engineers.

---

## 9️⃣ Documentation & Evidence

### ✔ What I did
- Captured screenshots of:
  - Entra ID tenant overview  
  - Entra groups  
  - Management groups  
  - Resource groups  
  - Policy assignments  
  - Policy compliance  
  - RBAC configuration  

Stored them in `/screenshots` for verification.

### ✔ What I learned
Documentation is how cloud engineers prove their work.  
This transforms hands-on architecture into a portfolio employers can evaluate.

---

# 🎉 Week 1 Completed Deliverables

- Entra ID identity foundation  
- Intune group structure  
- CAF management group hierarchy  
- Non-Production landing zone  
- Enterprise resource group strategy  
- Azure Policy governance  
- Tag & region restrictions  
- RBAC at root  
- Compliance validation  
- Full GitHub documentation + screenshots  

This completes the entire foundation layer of the Azure Landing Zone.

---

# ⏭️ Week 2 (Next)
**Zero Trust:**  
MFA, Conditional Access, Device Compliance, Intune Enrollment, and security baselines.

Stay tuned!

md
# Screenshots
This folder contains all architecture screenshots for my Azure Cloud Architect lab.

<img width="938" height="469" alt="01-entra-overview" src="https://github.com/user-attachments/assets/3a66c87c-99f9-4958-ad76-71e925f12d80" />
<img width="950" height="415" alt="01-management-groups-hierarchy" src="https://github.com/user-attachments/assets/7385bb69-482f-430f-8276-faf939c5ef8d" />
<img width="956" height="351" alt="02-resource-groups-list" src="https://github.com/user-attachments/assets/283d460b-e5f2-4664-8fa9-7d5ab00500cd" />
<img width="946" height="374" alt="04-azure-policy-compliance" src="https://github.com/user-attachments/assets/a65c2cf3-8910-4f10-88ee-9d90f1d4e9af" />
<img width="949" height="325" alt="05-rbac-role-assignments" src="https://github.com/user-attachments/assets/c9519483-4739-4fa8-8847-832606295c1e" />
<img width="950" height="326" alt="06-required-tag-environment-root" src="https://github.com/user-attachments/assets/13a634a8-e5ab-4182-b623-ac08f7ac79de" />
<img width="947" height="298" alt="07-allowed-locations-root" src="https://github.com/user-attachments/assets/89d2c780-51cd-427b-aff4-6d38967cfa0f" />


















