---
layout: default
title: "00 — Platform Overview"
nav_order: 2
description: "What Microsoft Engage Center is, the rollout timeline, key personas, and how it fits within Microsoft's broader support and customer success ecosystem."
permalink: /00-overview/
mermaid: true
---

# 00 — Engage Center: Platform Overview
{: .no_toc }

> 📁 [← Back to Home](/engage-center-notes/)

<details open markdown="block">
  <summary>Table of contents</summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

---

## What Is Engage Center?

**Microsoft Engage Center** (`engagecenter.microsoft.com`) is the next-generation customer experience portal for organisations with a **Microsoft Unified Support** agreement (and, progressively, select Premier customers). It is designed as the single, modernised destination for:

- Filing and tracking **support cases**
- Accessing **proactive services** (On-Demand Assessments, health checks, MIRP)
- Managing **contacts and account teams** (CSAMs, TAMs, DSEs)
- Consuming **learning paths** and Microsoft-curated content
- Viewing **analytics** on support consumption and service health

> **Key distinction:** Engage Center is not a new support *contract* — it is a new *portal experience* layered on top of existing Unified Support entitlements.

---

## Context & Rollout

Engage Center is part of Microsoft's broader initiative to modernise customer touchpoints following the **Unified Support rebrand** (which replaced Premier Support). Key milestones:

| Milestone | Detail |
|-----------|--------|
| **Premier → Unified transition** | New Premier contracts ceased; Microsoft Unified (Unified Enterprise Plan) launched |
| **Services Hub** | Web portal introduced as the primary interface for Unified customers |
| **Engage Center GA** | Rolling out from 2024–2025; progressively replacing Services Hub for most workflows |
| **Parallel operation** | Both portals remain active during transition; certain features still only in Services Hub |
| **Full migration** | No firm date published by Microsoft — both portals remain active; check with your CSAM for your organisation's status |

> ⚠️ The rollout is phased. Not all features are available to all customers simultaneously. Check your account team for your organisation's migration timeline.

---

## Key Personas

Understanding who uses Engage Center helps you navigate the platform effectively.

```mermaid
%%{init: {"theme":"dark"}}%%
flowchart TD
    subgraph Customer["Customer Organisation"]
        IT["IT Admin / Decision Maker\n(contract holder)"]
        ENG["Engineer / Architect\n(day-to-day user)"]
        PM["Project / Programme Manager\n(proactive services consumer)"]
    end
    subgraph Microsoft["Microsoft Account Team"]
        CSAM["CSAM\n(Customer Success Account Manager)"]
        TAM["TAM\n(Technical Account Manager — legacy title)"]
        DSE["DSE\n(Designated Support Engineer)"]
        CSA["CSA\n(Cloud Solutions Architect)"]
    end
    IT <--> CSAM
    ENG <--> DSE
    PM <--> CSA
    CSAM --- TAM
```

| Persona | Role | Primary Engage Center Activity |
|---------|------|-------------------------------|
| **IT Admin** | Contract & licence management | Account settings, contacts, contract details |
| **Engineer / Architect** | Hands-on workload owner | Support cases, On-Demand Assessments, learning |
| **CSAM** | Relationship + success planning | Account health, proactive service scheduling |
| **DSE** | Deep technical escalation | Case collaboration, advisory |
| **CSA** | Solution architecture guidance | Assessment reviews, MIRP, technical advisory |

---

## Platform Positioning

```mermaid
%%{init: {"theme":"dark"}}%%
flowchart LR
    subgraph Portals["Customer Portals"]
        EC["🌐 Engage Center\n(new, primary)"]
        SH["🏛️ Services Hub\n(legacy, parallel)"]
        M365["📊 M365 Admin Center\n(O365/M365 admins)"]
        AZ["⚙️ Azure Portal\n(infra/workloads)"]
    end
    subgraph Backend["Microsoft Backend"]
        ICM["ICM\n(Internal Case Mgmt)"]
        CMAP["CMAP\n(Account Plans)"]
    end
    EC --> ICM
    SH --> ICM
    M365 --> ICM
    EC -.->|"case sync"| AZ
    CSAM["CSAM / TAM"] --> CMAP
    CMAP --> EC
```

Engage Center sits at the intersection of **reactive support** (cases) and **proactive success** (services, learning), acting as the primary lens through which customers consume their Unified Support investment.

---

## How Engage Center Fits the Support Lifecycle

```mermaid
%%{init: {"theme":"dark"}}%%
flowchart TD
    PRE["📋 Pre-incident\nProactive Services\n(Assessments, MIRP planning)"]
    DURING["🚨 During Incident\nSupport Case + DSE\n(Severity A/B escalation)"]
    POST["📊 Post-incident\nReview & Analytics\n(lessons learned, health score)"]
    PLAN["🗓️ Success Planning\nCSAM-led\n(QBRs, roadmap alignment)"]

    PLAN --> PRE --> DURING --> POST --> PLAN
```

The platform is designed to support **all four phases** of the support lifecycle, not just reactive case management.

---

## Access & Authentication

| Requirement | Detail |
|-------------|--------|
| **Who can access** | Users associated with an active Unified Support contract |
| **Authentication** | Microsoft Entra ID (Azure AD) — organisational account required |
| **Admin provisioning** | Your IT Admin or CSAM must associate your account |
| **MFA** | Required (Microsoft Entra Conditional Access policies apply) |
| **Supported browsers** | Edge, Chrome, Firefox (latest versions); Safari supported |

> 💡 If you cannot access `engagecenter.microsoft.com`, contact your CSAM or raise a request through `support.microsoft.com` to get your account provisioned.

---

## Key Terminology

| Term | Definition |
|------|-----------|
| **Unified Support** | Microsoft's current support contract model (replaced Premier) — officially branded **Microsoft Unified** / Unified Enterprise Plan; entitlements defined per individual agreement |
| **Premier Support** | Legacy contract model, still active for existing customers but no longer sold as new |
| **CSAM** | Customer Success Account Manager — your primary Microsoft relationship contact |
| **DSE** | Designated Support Engineer — deep technical resource assigned under some contracts |
| **On-Demand Assessment** | Automated or guided technical health check (formerly called "Rapid Assessment Proactive Service") |
| **MIRP** | Microsoft Incident Response Planning — proactive service for IR readiness |
| **Proactive Service** | Any Microsoft-delivered service consumed from contract hours (not a break-fix case) |
| **Severity / Priority** | Case urgency level (A = business-critical, B = significant, C = general) |
| **ICM** | Internal Microsoft case management system — what CSAMs and DSEs use behind the scenes |

---

## What's Next?

- 🧭 [01 — Navigation & Features](/engage-center-notes/01-navigation-features/) — UI walkthrough, how to find everything
- 📄 [03 — Unified & Premier Contracts](/engage-center-notes/03-unified-premier-contracts/) — understand your entitlements
- 🔄 [05 — Services Hub vs Engage Center](/engage-center-notes/05-services-hub-comparison/) — what moved, what hasn't

---

[← Back to Home](/engage-center-notes/) | [01 — Navigation & Features →](/engage-center-notes/01-navigation-features/)
