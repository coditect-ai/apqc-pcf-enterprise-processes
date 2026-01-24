# APQC PCF Enterprise Processes - Claude Context

## Purpose

This repository contains the APQC Process Classification Framework (PCF) transformed into markdown for AI applicability analysis. The PCF is the world's most widely used process framework for business process benchmarking.

## Quick Reference

| Item | Value |
|------|-------|
| Total Elements | 1,855+ process elements per industry |
| Categories | 13 major enterprise process areas |
| Hierarchy Depth | Up to 5 levels (X.X.X.X.X) |
| Industries | 19 (1 complete, 18 pending) |
| Source Versions | v7.2.1, v7.2.2, v7.4 |

## Directory Structure

```text
apqc-pcf-enterprise-processes/
├── README.md                           # Repository overview
├── CLAUDE.md                           # This file
├── PCF-DECOMPOSITION-WORKFLOW.md       # Decomposition workflow
│
├── cross-industry-v7.4/                # ✅ Complete
│   ├── source/                         # Original PDF/Excel
│   ├── APQC-PCF-OVERVIEW.md
│   ├── category-*.md
│   └── K014750-APQC-PCF-*/
│
├── aerospace-defense/                  # ⏳ Pending
│   ├── source/
│   ├── README.md
│   └── CLAUDE.md
│
├── [17 more industry folders]          # ⏳ Pending
└── utilities/
```

## Industry Status

| Industry | Status | AI Focus |
|----------|--------|----------|
| Cross-Industry | ✅ Complete | Universal enterprise processes |
| Aerospace & Defense | ⏳ Pending | Defense contracts, supply chain traceability |
| Airline | ⏳ Pending | Revenue management, crew scheduling |
| Automotive | ⏳ Pending | Manufacturing, supply chain, quality |
| Banking | ⏳ Pending | Fraud detection, credit risk, compliance |
| Broadcasting | ⏳ Pending | Content recommendation, ad placement |
| City Government | ⏳ Pending | Citizen services, permits, public works |
| Consumer Electronics | ⏳ Pending | Product lifecycle, warranty, support |
| Consumer Products | ⏳ Pending | Demand forecasting, trade promotion |
| Downstream Petroleum | ⏳ Pending | Refinery optimization, supply chain |
| Education | ⏳ Pending | Enrollment, learning management, grants |
| Healthcare Provider | ⏳ Pending | Clinical decision support, coding |
| Health Insurance Payor | ⏳ Pending | Claims adjudication, fraud detection |
| Life Sciences | ⏳ Pending | Drug discovery, clinical trials, regulatory |
| Property & Casualty Insurance | ⏳ Pending | Underwriting, claims, fraud |
| Retail | ⏳ Pending | Demand forecasting, inventory, pricing |
| Telecommunications | ⏳ Pending | Network optimization, churn prediction |
| Upstream Petroleum | ⏳ Pending | Reservoir optimization, drilling |
| Utilities | ⏳ Pending | Grid optimization, demand response |

## The 13 Categories

### Operating Processes (1.0 - 6.0)

| # | Category | Elements | Key AI Applications |
|---|----------|----------|---------------------|
| 1.0 | Develop Vision and Strategy | 123 | Market analysis, scenario planning |
| 2.0 | Develop and Manage Products and Services | 100 | R&D analytics, patent search |
| 3.0 | Market and Sell Products and Services | 202 | Lead scoring, personalization |
| 4.0 | Deliver Physical Products | 147 | Supply chain optimization, logistics |
| 5.0 | Deliver Services | 67 | Service automation, scheduling |
| 6.0 | Manage Customer Service | 104 | Chatbots, ticket routing, sentiment |

### Management and Support Processes (7.0 - 13.0)

| # | Category | Elements | Key AI Applications |
|---|----------|----------|---------------------|
| 7.0 | Develop and Manage Human Capital | 135 | Resume screening, L&D personalization |
| 8.0 | Manage Information Technology (IT) | 321 | AIOps, incident response, monitoring |
| 9.0 | Manage Financial Resources | 270 | Fraud detection, reconciliation |
| 10.0 | Acquire, Construct, and Manage Assets | 69 | Predictive maintenance |
| 11.0 | Manage Enterprise Risk, Compliance | 56 | Compliance monitoring, risk scoring |
| 12.0 | Manage External Relationships | 54 | PR monitoring, investor relations |
| 13.0 | Develop and Manage Business Capabilities | 207 | Process mining, analytics |

## Common Tasks

### Find processes related to a topic

```bash
grep -r "automation" cross-industry-v7.4/ --include="*.md" -l
grep -r "customer" cross-industry-v7.4/category-06-*.md
```

### View decomposition workflow

```bash
cat PCF-DECOMPOSITION-WORKFLOW.md
```

### Start industry decomposition

```bash
/agent pcf-decomposer "banking"
```

### List pending industries

```bash
ls -d */ | grep -v cross-industry
```

## AI Applicability Analysis Notes

### High Automation Potential (>70%)

- 8.0 IT Management - Already digitized, rule-based
- 9.0 Financial Resources - Transaction processing
- Subprocesses in 6.0 Customer Service - FAQ, routing

### Human-AI Collaboration Focus

- 1.0 Strategy - AI for data, humans for judgment
- 2.0 Product Development - AI assists ideation
- 7.0 Human Capital - AI screens, humans decide

### Physical-Digital Hybrid

- 4.0 Physical Products - IoT + AI optimization
- 10.0 Asset Management - Predictive maintenance

---

**Last Updated:** 2026-01-24
