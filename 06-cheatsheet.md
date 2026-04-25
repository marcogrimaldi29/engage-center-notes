---
layout: default
title: "06 — Quick Reference Cheatsheet"
nav_order: 8
description: "Engage Center quick reference: key URLs, severity reference, Microsoft Unified offering, escalation paths, MIRP checklist, and CSA tips."
permalink: /06-cheatsheet/
mermaid: false
---

# 06 — Quick Reference Cheatsheet
{: .no_toc }

> 📁 [← Back to Home](/engage-center-notes/)

*Reference for Cloud Solutions Architects — everything on one page.*

<details open markdown="block">
  <summary>Table of contents</summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

---

## 🔗 Key URLs

| Portal / Resource | URL |
|------------------|-----|
| **Engage Center** | [engagecenter.microsoft.com](https://engagecenter.microsoft.com/) |
| **Services Hub** (legacy) | [serviceshub.microsoft.com](https://serviceshub.microsoft.com) |
| **Azure Portal** | [portal.azure.com](https://portal.azure.com) |
| **M365 Admin Center** | [admin.microsoft.com](https://admin.microsoft.com) |
| **Microsoft Support** | [support.microsoft.com](https://support.microsoft.com) |
| **Unified Support info** | [microsoft.com/unifiedsupport](https://www.microsoft.com/en-us/unifiedsupport) |
| **Microsoft Secure Score** | [security.microsoft.com/securescore](https://security.microsoft.com/securescore) |
| **Defender for Cloud** | [portal.azure.com → Defender for Cloud](https://portal.azure.com/#blade/Microsoft_Azure_Security/SecurityMenuBlade/0) |
| **Azure Status** | [status.azure.com](https://status.azure.com) |
| **Microsoft Entra ID** | [entra.microsoft.com](https://entra.microsoft.com) |

---

## ⏱️ Severity Reference

| Severity | Business Impact | Microsoft Unified | Legacy Premier |
|----------|----------------|:-----------------:|:--------------:|
| **A — Critical** | Business down, no workaround | ≤ 1h 24/7 | ≤ 1h 24/7 |
| **B — High** | Major impact, partial workaround | ≤ 2h 24/7 | ≤ 2h 24/7 |
| **C — General** | Minor / question | ≤ 4h BH | ≤ 4h BH |

**BH** = Business Hours · **24/7** = Around the clock

> ⚠️ Initial response time only — not resolution time. Resolution is not contractually guaranteed.

---

## 📄 Microsoft Unified — What's Officially Documented

| Attribute | Detail |
|-----------|--------|
| **Official name** | Microsoft Unified / Unified Enterprise Plan |
| **Service categories** | **Value Acceleration Services** (proactive, strategic) · **Mission Critical Services** (reactive break-fix, incident response) |
| **CSAM** | Included — named account manager for relationship and success planning |
| **DSE** | Available — scope defined in the individual agreement |
| **On-Demand Assessments** | Available — scope defined in the individual agreement |
| **Proactive hours** | Annual pool — volume defined in the individual agreement |
| **Portal** | Engage Center (`engagecenter.microsoft.com`) |
| **Entitlements** | Response SLAs as per Severity Reference above; proactive hours, named resources (CSAM, DSE), and additional services defined per negotiated contract |

> 💡 For the specifics of what a customer is entitled to, navigate to **Customer Activity** in Engage Center or ask their CSAM. The contract document is the authoritative source.

---

## 🔑 Key Personas at a Glance

| Role | Abbreviation | What They Do |
|------|:------------:|-------------|
| Customer Success Account Manager | **CSAM** | Relationship owner, success planning, escalation coordinator |
| Designated Support Engineer | **DSE** | Deep technical resource for complex issues |
| Cloud Solutions Architect | **CSA** | Architecture advisory, proactive services delivery |
| Technical Account Manager | **TAM** | Legacy Premier title, equivalent to CSAM |
| Premier Field Engineer | **PFE** | Legacy Premier title, equivalent to DSE |
| Detection & Response Team | **DART** | Reactive security incident response (separate engagement) |

---

## 🎫 Case Creation Checklist

Before submitting a support case, gather:

| Item | Example |
|------|---------|
| ☐ Azure Subscription ID | `xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx` |
| ☐ Tenant / Directory ID | `xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx` |
| ☐ Resource Group name | `rg-prod-eastus` |
| ☐ Resource name / ID | `vm-appserver-01` |
| ☐ Exact error message | Copy full error text + code |
| ☐ Steps to reproduce | Numbered, repeatable steps |
| ☐ Time of first occurrence | UTC preferred |
| ☐ Recent changes (last 48h) | Deployments, config changes, patches |
| ☐ Business impact statement | "X users cannot access Y, impacting Z process" |
| ☐ Relevant logs attached | Diagnostic logs, screenshots |

---

## 🚨 Escalation Path

```
Issue unresolved / response inadequate
    ↓
1. Update case severity in Engage Center
    ↓
2. Add escalation comment in case thread (document business impact)
    ↓
3. Contact CSAM directly (Teams / phone)
    ↓
4. CSAM escalates to Microsoft support manager
    ↓
5. CSAM escalates to Account Executive / Engineering (subject to agreement)
```

---

## 🛡️ Digital MIRP Quick Reference

**Major Incident Response Plan** — self-service portal tool in Engage Center, not a consulting engagement.

| Section | Purpose |
|---------|---------|
| **Cloud Solutions** | Inventory of business-critical workloads + key contacts; attest when current |
| **Your Account Team** | Microsoft contact info and support portal links |
| **Response Guidelines** | Before / During / After a service incident guidance |
| **Azure Health** | Services Dashboard + Resiliency Recommendations + Azure Advisor link |

**Azure workloads:** auto-populated via the Proactive Resiliency Program · **M365 / D365 / Power Platform:** added manually · **Contacts:** managed by customer admins only · **Attest** after any significant change

**Access:** requires appropriate Engage Center role — confirm with CSAM

---

## 🔄 Services Hub vs Engage Center: One-Line Summary

| Portal | Status | Use For |
|--------|--------|---------|
| **Engage Center** (`engagecenter.microsoft.com`) | ✅ Primary (current) | All new workflows |
| **Services Hub** (`serviceshub.microsoft.com`) | ⚠️ Legacy (parallel) | Legacy cases / service types only |

---

## 📊 On-Demand Assessment — Top Picks for CSAs

| Assessment | What It Checks | Typical Time |
|-----------|---------------|-------------|
| **Azure Well-Architected Review** | Reliability, Security, Cost, Performance, Ops Excellence | 2–4h questionnaire |
| **Microsoft Defender for Cloud** | Azure security posture, Secure Score gaps | Automated + 1h review |
| **Identity Security** | Entra ID config, MFA coverage, CA policies | 2h questionnaire |
| **Business Continuity** | Backup, DR, RTO/RPO posture | 2–3h questionnaire |
| **Microsoft 365 Security** | Exchange, Teams, SharePoint security config | 2h questionnaire |
| **Endpoint Security** | Defender for Endpoint coverage & config | 2h questionnaire |

---

## 📝 CSA Role Tips

| Situation | Tip |
|-----------|-----|
| First call with a new Unified customer | Start in **Customer Activity** in Engage Center to understand their entitlements and hours pool |
| Customer says "our cases take too long" | Check severity assigned and whether "Waiting for Customer" time is inflating perceived response time |
| Customer wants to know what proactive services they can use | Go to **Services catalogue** in Engage Center — available services reflect what's included in their agreement |
| Customer asks about Services Hub retirement | "No firm date yet. Both portals work. Default to Engage Center, Services Hub still there if needed." |
| Customer wants to expand their Unified entitlements | Key additions to ask CSAM about: 24/7 Sev A response, dedicated CSAM, DSE, On-Demand Assessments — entitlements are contract-specific, not a fixed published tier |
| Preparing for a QBR | Pull 90-day case and service consumption reports from **Analytics** |
| Customer has a security incident | Do NOT use MIRP — open a **Severity A security case** and/or engage DART |

---

## 🧩 Engage Center Navigation Shortcuts

| Section | Path |
|---------|------|
| Create new case | Support → New Request |
| View all open cases | Support → All Requests → filter by Status: Open |
| Browse proactive services | Services → Catalogue |
| View my CSAM contact | People & Contacts → Account Team |
| Check contract hours | Account → Entitlements |
| Pull case analytics | Analytics → Case Volume |
| Configure notifications | Settings → Notifications |

---

## 🔐 Common Entra ID / Security Quick Checks

For use during MIRP or advisory sessions:

| Check | Where |
|-------|-------|
| MFA coverage % | Entra ID → Identity Protection → MFA registration report |
| CA policy gaps | Entra ID → Security → Conditional Access → Policies |
| PIM configured? | Entra ID → Privileged Identity Management |
| Break-glass accounts set up? | Entra ID → Users → filter for emergency access accounts |
| Secure Score | security.microsoft.com/securescore |
| Defender for Cloud score | portal.azure.com → Defender for Cloud → Overview |
| Azure Policy compliance | portal.azure.com → Policy → Compliance |

---

## ©️ Notes

> *Not affiliated with or endorsed by Microsoft. Content based on publicly available documentation. Always verify against the latest [Microsoft documentation](https://learn.microsoft.com/en-us/). Last reviewed: April 2026.*

---

[← 05 — Services Hub vs Engage Center](/engage-center-notes/05-services-hub-comparison/) | [Back to Home →](/engage-center-notes/)
