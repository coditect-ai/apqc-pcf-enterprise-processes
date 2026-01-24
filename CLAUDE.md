# APQC PCF Enterprise Processes - Claude Context

## Purpose

This repository contains the APQC Process Classification Framework (PCF) transformed into markdown for AI applicability analysis. The PCF is the world's most widely used process framework for business process benchmarking.

## Quick Reference

| Item | Value |
|------|-------|
| Total Elements | 1,855 process elements |
| Categories | 13 major enterprise process areas |
| Hierarchy Depth | Up to 5 levels (X.X.X.X.X) |
| Source | APQC Cross-Industry PCF v7.2.1 (April 2023), v7.4 (August 2024) |

## Directory Structure

```
apqc-pcf-enterprise-processes/
├── README.md                      # Repository overview
├── CLAUDE.md                      # This file
└── cross-industry-v7.4/           # Cross-Industry PCF
    ├── APQC-PCF-OVERVIEW.md       # Master index
    ├── category-*.md              # 13 category documents
    ├── category-*/                # Process group breakdowns
    └── K014750-APQC-PCF-*/        # PDF v7.4 conversion
```

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

### View a specific category

```bash
cat cross-industry-v7.4/category-08-manage-information-technology-it.md
```

### Search by PCF ID

```bash
grep "PCF ID.*17040" cross-industry-v7.4/*.md
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
