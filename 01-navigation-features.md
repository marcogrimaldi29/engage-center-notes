---
layout: default
title: "01 — Navigation & Features"
nav_order: 3
description: "Engage Center walkthrough: left-nav sections, workspaces, support, MIRP, Support Insights, learning, user management, settings, and productivity tips for daily use."
permalink: /01-navigation-features/
mermaid: false
---

# 01 — Navigation & Features
{: .no_toc }

> 📁 [← Back to Home](/engage-center-notes/)

<details open markdown="block">
  <summary>Table of contents</summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

---

## Portal Layout Overview

Engage Center uses a **left navigation + main content** layout. What you see in the left nav depends on your **workspace type**, the **services** associated with that workspace's agreements, the **features** turned on in Settings, and your **roles**.

> 💡 Microsoft groups Engage Center features into four areas: **Management & settings** (User and group management, Manage workspaces, Manage agreements, External resources), **Support & activity** (Customer activity, Support insights, Case creation, Shared files), **Health & readiness** (Digital MIRP, Azure health, On-demand assessments), and **Learning & updates** (Learning, Newsletter). See [Engage Center features](https://learn.microsoft.com/en-us/services-hub/microsoft-engage-center/get-started/features).

---

## Left Navigation Sections

| Section | Icon | What You Do Here |
|---------|------|-----------------|
| **Support** | 🎫 | **Help + Support** (Support AI Assistant, case creation, phone support) and the **Support Requests** list |
| **Support Insights** | 📊 | Dashboards, AI-assisted **Ask & Explore**, and **Custom Reports** on support activity |
| **Shared Files** | 📁 | Download (and, if permitted, delete) files shared by your CSAM or Incident Manager |
| **Customer Activity** | 📄 | Agreement packages, the services in each, and their usage |
| **Major Incident Response Plan** | 🛡️ | MIRP — Cloud Solutions, Your Account Team, Response Guidelines, Azure Health |
| **On-Demand Assessments** | 🔍 | Run automated health assessments across your Microsoft environments (under **IT Health**) |
| **Learning** | 🎓 | All Titles, On-Demand Learning, Scheduled Services, My Learning, Learning Management |
| **Newsletter** | 📰 | Browse and subscribe to newsletters and Microsoft security briefings |
| **User Management** | 👤 | Users, Microsoft Entra groups, roles, and (optionally) **Reactive Services** |
| **External Resources** | 🔗 | Per-tenant Support Request Visibility, Login Access, and MIRP availability |
| **Manage Agreements** / **Manage Workspaces** | 🗂️ | Agreement and service associations for a workspace; child workspaces (Rollup only) |
| **Settings** | ⚙️ | **Features** toggles (MIRP, Newsletter, Granular Reactive Services) and **Newsletter settings** |

> ⚠️ Navigation availability varies by rollout phase, workspace type, and role. Features transition progressively from Services Hub — not all sections may be visible until your workspace is fully migrated. See [05 — Services Hub vs Engage Center](/engage-center-notes/05-services-hub-comparison/) for the rollout phase order.

---

## Workspaces

Everything in Engage Center happens inside a **workspace**. Microsoft recommends a **single workspace** for most customers: all cases for the agreement land in one place, and tenant consent in External Resources is given once.

| Workspace type | Purpose |
|---------------|---------|
| **Support Services** | Day-to-day support work for a specific set of agreements and services; shows only data assigned to it |
| **Rollup** | Parent workspace aggregating multiple child Support Services workspaces — Support Management, Support Insights, Customer Activity, optional Digital MIRP, and **Manage Workspaces**. **Cases can't be created in a Rollup workspace** |
| **Unified for Partner** | Operational workspace for partners enrolled in the Unified for Partner offering (no Rollup) |

**Manage Workspaces** (Rollup only) lets administrators create, edit, link, and delete child workspaces, choose which agreements and services each child gets, and assign **Managed Administrators** (at least two per new workspace). In multi-workspace setups, some cases can't be auto-assigned — Rollup users use **Case Assignment** to route them to the right child workspace.

**Manage Agreements** shows the agreements, packages, and services associated with the current workspace, and lets you add eligible agreements, enable or remove service associations, rename the workspace, or create a Rollup workspace.

> 💡 See [Engage Center workspaces](https://learn.microsoft.com/en-us/services-hub/microsoft-engage-center/get-started/workspaces) and [Manage Workspaces](https://learn.microsoft.com/en-us/services-hub/microsoft-engage-center/roles/manage-workspaces).

---

## Support Section

The Support section is where you manage reactive break-fix cases. See [02 — Support Requests](/engage-center-notes/02-support-requests/) for full detail.

**Key areas:**
- **Help + Support** — the **Support AI Assistant**: pick a product and problem type, get guided self-help, answer a few scoping questions, then select **Create support request**. A **Phone support** option lists regional numbers.
- **Support Requests** — a filterable list (State, Severity, Product, Product family, Primary contact, Created date) of cases assigned to the workspace. Each case opens to **Overview**, **Communications**, **Attachments**, and **Sharing** tabs; the list can be exported.

> 💡 Only users with the **Support User** role can create support cases. Administrators alone cannot open cases without also having the Support User role assigned. Microsoft users (including CSAMs) can't open cases on behalf of customers.

---

## Major Incident Response Plan

The **Major Incident Response Plan (MIRP)** is a self-service portal tool with its own dedicated section in the left nav. It is not a consulting engagement — it is a digital tool for maintaining shared readiness between your organisation and Microsoft. See [04 — Digital MIRP](/engage-center-notes/04-digital-mirp/) for full detail.

| Sub-section | What It Contains |
|-------------|-----------------|
| **Cloud Solutions** | Inventory of business-critical Azure, M365, D365, and Power Platform workloads + key contacts; attestation |
| **Your Account Team** | Microsoft contact info and support portal links — maintained by Microsoft |
| **Response Guidelines** | Before / During / After incident guidance; searchable by topic |
| **Azure Health** | Services Dashboard (subscription health alerts) and Resiliency Recommendations (links to Azure Advisor) |

> 💡 MIRP is controlled in **Settings → Features** and is **on by default**. In a **Rollup** workspace the toggle starts off — turn it on there to run one MIRP across all child workspaces, or manage it per workspace. Customers with a **single workspace** can't toggle MIRP off. Turning MIRP off removes the feature and its plans from the workspace.

> 💡 Managing contacts within MIRP requires the **Mirp Manager** role. The **Mirp Viewer** role can create and edit solutions and toggle tenants, but cannot add tenants, add contacts, or attest the plan.

---

## Incident Readiness

The **Incident Readiness** guidance (under the Health area) helps you prepare for and respond to the three types of cloud incidents Microsoft categorises:

| Incident Type | Description |
|--------------|-------------|
| **Service incidents** | Unplanned downtime, outages, performance degradation affecting Microsoft services |
| **Privacy incidents** | Potential unauthorised use or disclosure of customer data |
| **Security incidents** | Confirmed breaches resulting in data destruction, loss, or unauthorised access |

The guidance is product-specific:
- **Azure Incident Readiness** — preparation steps and response actions for Azure workloads
- **Microsoft 365, Dynamics 365 & Power Platform Incident Readiness** — equivalent guidance for those product families

> 💡 Incident Readiness complements MIRP: MIRP maintains your workload inventory and contacts; Incident Readiness provides the product-specific guidance on what to do when an incident occurs. See [Incident Readiness](https://learn.microsoft.com/en-us/services-hub/microsoft-engage-center/health/incident-readiness/incident-readiness).

---

## External Resources

**External Resources** is a per-tenant dashboard that controls which tenant data and capabilities appear in the workspace:

| Toggle | What It Controls |
|--------|-----------------|
| **Support** (Support Request Visibility) | Whether that tenant's support requests — including those from Azure subscriptions trusting the tenant — appear in the workspace. Turning it on counts as consent to show them |
| **Login** (Login Access) | Whether users from that tenant can sign in to the workspace |
| **MIRP** | Whether the tenant can be selected when creating MIRP cloud solutions |

You can also add a tenant manually (by Tenant ID) or remove manually added tenants. CSMs and Administrators have full access; CSAMs and Mirp Managers have partial access.

> 💡 If expected cases are missing from Support Requests or Support Insights, or a tenant is missing from the MIRP dropdown, check External Resources first. Newly enabled tenants can take up to an hour to appear in Support Insights. See [aka.ms/ec-externalresources](https://aka.ms/ec-externalresources).

---

## Shared Files

The **Shared Files** section provides a centralised location to securely access support-related files shared by your CSAM or Incident Manager.

| Action | Who Can Do It |
|--------|--------------|
| **View & download files** | Users with the **Shared Files User** role |
| **Delete files** | Users with the **Shared Files User** role (deletion is permanent) |
| **Upload files** | CSAMs and Incident Managers only — not available to customers |

> 💡 If you cannot see Shared Files in the nav, ask your Customer Support Manager, Administrator, or User Access Administrator to assign the **Shared Files User** role. Customers manage their own access — Microsoft doesn't assign it on your behalf.

---

## Customer Activity

**Customer Activity** gives a centralised view of the services in your Microsoft support agreement and how they're being used. It requires the **Contract Manager** role (or another administrative role with access).

| Element | What It Shows |
|---------|---------------|
| **Agreement number** dropdown | Switch between agreements associated with the workspace |
| **Enterprise-wide packages** | Shared services for the purchasing entity — one tile per service |
| **Add-on packages** | Purchased add-ons, shown within their parent package |
| **Service tiles** | Title, description, and usage count (when available) |
| **Detailed usage views** | Per-service usage detail; format and download options vary by service |

> 💡 What appears can be narrowed per workspace using **Manage Agreements** (single workspace) or **Manage Workspaces** (from the Rollup). A few services that can be turned on may not display yet — Microsoft has flagged this as a known gap.

---

## Proactive Services & On-Demand Assessments

> 💡 **Two distinct types of "services" exist in Engage Center — they are separate:**
> - **Learning → Scheduled Services**: instructor-led learning sessions and workshops you can browse in the Learning section and request enrolment for via your CSAM (see below)
> - **Consulting / advisory proactive services**: advisory sessions, custom engagements, and similar contract-based services are coordinated through your **CSAM**, not via a self-service catalogue

**On-Demand Assessments** use the Engage Center Connector and Azure Log Analytics. Initial setup requires an Azure subscription and Log Analytics workspace (~2 hours to configure), plus a collector machine (Azure VM or Azure Arc-enabled server with the Azure Monitor Agent). Collector VMs configured before **September 2024** should be replaced or reimaged. For CSA-led deliveries, the customer grants Microsoft personnel **Log Analytics Reader** access. See [Get started with On-Demand Assessments](https://learn.microsoft.com/en-us/services-hub/microsoft-engage-center/health/get-started-with-on-demand-assessments).

> 💡 The **Assessment User** role grants access to the **Offline Assessment** tab for customers who purchased an Offline package, and only appears after the CSAM turns on the Assessments feature for the workspace.

Advisory sessions, workshops, and custom consulting engagements are scheduled in coordination with your CSAM. Availability and scope depend on your agreement — check **Customer Activity** and confirm scope with your CSAM.

---

## Learning Section

The Learning section brings together discovery, participation, and progress tracking in a single location:

| Sub-section | What It Provides |
|-------------|-----------------|
| **All Titles** | Browse all available learning and service offerings — on-demand and scheduled; search by keyword, filter by product and service type |
| **On-Demand Learning** | Self-paced Microsoft Learn modules, learning paths, and interactive hands-on labs; progress is automatically tracked |
| **Scheduled Services** | Instructor-led sessions and guided workshops; review descriptions, timing, and formats, then **request enrolment by emailing your CSAM** |
| **My Learning** | Personalised view — Not Started / In Progress / Completed; shows assigned learning and lets you resume where you left off |
| **Learning Management** | Assign on-demand learning to individuals or groups, set due dates, and track completion and overdue assignments |

> 💡 **Learning Management** requires the **Learning Manager** role; general access requires the **Learning User** role. Only on-demand courses from **Microsoft Learn** and the **Microsoft Learning Campus** can be assigned and tracked.

---

## Account Team Contacts

Microsoft account team contact details are accessible within **Major Incident Response Plan → Your Account Team**. This section is maintained by Microsoft and contains support contact information and portal links.

| Contact Type | Role | Where to Find |
|-------------|------|--------------|
| **CSAM** | Primary relationship manager, success planning | MIRP → Your Account Team; also via email / Teams |
| **Incident Manager (IM)** | Incident coordination on your cases | System-assigned in Engage Center |
| **DSE** | Deep technical resource for complex issues | Availability defined per agreement |
| **CSA** | Cloud architecture advisory | Engaged through proactive services via CSAM |
| **Premier Field Engineer (PFE)** | Legacy title (some still active) | As per existing Premier contract |

User and role management is handled through **User Management**.

> 💡 If your account team has changed and contact details appear stale, ask your CSAM to update the Your Account Team section in MIRP.

---

## Support Insights

**Support Insights** gives an interactive view of support activity for the workspace. It only includes cases that are (1) tied to agreements assigned to the workspace, (2) from tenants made visible in External Resources, and (3) assigned to the workspace. Access requires the **Reporting User** role (or **Problem Manager**, which also includes access to all case details).

| Area | What It Shows |
|------|--------------|
| **Global filters** | State, Date range, Cloud, Product / product family, Severity, Status, Tenant |
| **Detailed statistics** | Total cases, Open cases, Average aging, Critical cases, Critical case time, Initial response performance |
| **Support case summary charts** | Cases by current / initial / max severity, Initial response (IR) met, Case count by product and by product family, Overall case distribution, Cases opened by country/region |
| **Support Requests table** | Case-level drill-down to spot aging or inactive cases |
| **Ask & Explore** (AI) | Natural-language questions — "what needs attention today?", "which cases are aging?", QBR prep, case hygiene reviews |
| **Custom Reports** (AI) | Describe a report in plain language or start from a template (executive summary, SLA tracking, CritSit monitoring, product health) and refine it conversationally |

> 💡 Export is available to customer users. Validate AI-generated insights (data source, refresh time) before sharing them externally.

---

## User Management & Reactive Services

**User Management** is where Administrators and **User Access Administrators** add, edit, and remove users and Microsoft Entra groups and assign roles. Invited users stay **Pending** until their first sign-in.

**Reactive Services** (optional) restricts which reactive support services specific users or groups can use to open cases or create Access IDs. It only appears after an administrator turns on **Settings → Features → Support (Granular Reactive Services)**, which is off by default. Saving a selection replaces the previous one, and Microsoft recommends leaving it off unless your agreement has multiple reactive services that must be split between teams.

> 💡 See [Engage Center roles and permissions](https://learn.microsoft.com/en-us/services-hub/microsoft-engage-center/roles/) for the full role list and [Reactive Services](https://learn.microsoft.com/en-us/services-hub/microsoft-engage-center/user-management/services).

---

## Settings, Profile & Newsletter

| Where | What You Can Do |
|-------|----------------|
| **Settings → Features** | Workspace administrators toggle **MIRP** (on by default), **Newsletter** (on by default), and **Support (Granular Reactive Services)** (off by default) |
| **Settings → Newsletter settings** | Administrators enable or disable distribution of individual newsletters in the workspace |
| **My Profile** | Set and verify the **preferred email** used for newsletters (delivery is paused until verified); subscribe to Engage Center updates |
| **Newsletter** | Browse newsletters and Microsoft security briefings, filter by language or topic, and subscribe |

> 💡 See [Features](https://learn.microsoft.com/en-us/services-hub/microsoft-engage-center/settings/features-page) and [Manage and subscribe to newsletters](https://learn.microsoft.com/en-us/services-hub/microsoft-engage-center/resources/newsletter-subscription-management).

---

## Productivity Tips for CSAs

| Tip | How |
|-----|-----|
| **Bookmark frequently used sections** | Browser bookmarks for Support, Support Insights, Customer Activity, and MIRP |
| **Start with External Resources when data looks missing** | Tenant visibility drives what appears in Support Requests and Support Insights |
| **Use Custom Reports before QBRs** | Start from the executive-summary or SLA template, then refine for the audience |
| **Check MIRP → Your Account Team after account team changes** | Reflects current CSAM and Microsoft contact details |
| **Customer Activity as a conversation starter** | Walk through packages, services, and usage counts with the customer |

---

## During the Transition

Some features may still live in Services Hub until your workspace completes its rollout. See [05 — Services Hub vs Engage Center](/engage-center-notes/05-services-hub-comparison/) and Microsoft's [What to expect as Engage Center rolls out](https://learn.microsoft.com/en-us/services-hub/microsoft-engage-center/get-started/what-to-expect).

---

[← 00 — Platform Overview](/engage-center-notes/00-overview/) | [02 — Support Requests →](/engage-center-notes/02-support-requests/)
