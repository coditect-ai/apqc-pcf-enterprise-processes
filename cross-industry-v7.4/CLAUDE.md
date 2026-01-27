---
title: Claude
type: reference
component_type: reference
version: 1.0.0
audience: contributor
status: draft
summary: Auto-classified reference document
keywords:
- reference
tokens: ~1000
created: '2026-01-24'
updated: '2026-01-26'
tags:
- reference
apqc_license: royalty-free
apqc_attribution: "APQC Process Classification Framework® - Open Standard"
apqc_source: "www.apqc.org/pcf"
ai_indexing: prohibited
compliance_status: human-reference-only
---
# APQC PCF Enterprise Processes - Claude Context

## CRITICAL: Compliance Restrictions

> **DO NOT INDEX FOR AI/ML SYSTEMS**
>
> Per APQC Terms of Service (August 2025):
> "Use any of APQC's Online Resources to create, train, or test any
> large language models or other artificial intelligence or machine
> learning systems" - **PROHIBITED**
>
> **This content is for HUMAN REFERENCE ONLY:**
> - DO NOT index in platform.db
> - DO NOT generate embeddings
> - DO NOT include in semantic search
> - DO NOT use for agent discovery
> - DO NOT process with AI/ML tools
>
> **For AI-enabled process framework, use:**
> - CODITECT Process Framework (CPF) at `frameworks/cpf/`
> - CPF is a compliant derivative work with proper attribution
> - See: ADR-122 for legal analysis

---

## APQC Attribution

> This APQC Process Classification Framework® ("PCF") is an open standard developed by APQC, a nonprofit that promotes benchmarking and best practices worldwide. APQC grants a perpetual, worldwide, royalty-free license to use, copy, publish, modify, and create derivative works of the PCF with proper attribution.
>
> **Source:** [www.apqc.org/pcf](https://www.apqc.org/pcf)

## Purpose

This directory contains the APQC Process Classification Framework (PCF) v7.2.1 transformed into markdown for AI applicability analysis. The PCF is the world's most widely used process framework for business process benchmarking.

## Quick Reference

| Item | Value |
|------|-------|
| Total Elements | 1,855 process elements |
| Categories | 13 major enterprise process areas |
| Hierarchy Depth | Up to 5 levels (X.X.X.X.X) |
| Source | APQC Cross-Industry PCF v7.2.1 (April 2023) |

## Document Structure

```
apqc-pcf-enterprise-processes/
├── apqc-pcf-overview.md           # Master index and summary
├── README.md                       # Directory documentation
├── CLAUDE.md                       # This file
└── category-{NN}-{name}.md         # 13 category documents
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

## PCF Hierarchy Structure

The PCF uses a hierarchical numbering system:

```
1.0       = Category (e.g., "Develop Vision and Strategy")
1.1       = Process Group
1.1.1     = Process
1.1.1.1   = Activity
1.1.1.1.1 = Task (deepest level)
```

## Key Fields in Each Document

| Field | Description |
|-------|-------------|
| PCF ID | Unique identifier (e.g., 10002, 17040) |
| Hierarchy ID | Position in tree (e.g., 1.1.1) |
| Name | Process/activity name |
| Change details | Version changes (+NEW, -removed, cChanged) |
| Metrics available? | Y/N for benchmarking data |

## Common Tasks

### Find processes related to a topic

```bash
grep -r "automation" . --include="*.md" -l
grep -r "customer" category-06-*.md
```

### View a specific category

```bash
cat category-08-manage-information-technology-it.md
```

### Search by PCF ID

```bash
grep "PCF ID.*17040" *.md
```

## AI Applicability Analysis Notes

### High Automation Potential (>70% automatable)

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

## Related Research

This analysis connects to CODITECT's AI applicability research:
- O*NET occupation analysis
- Industry-specific automation potential
- Process-to-occupation mapping

## Usage in CODITECT

Use this framework for:
1. **Agentic Platform Design** - Map agents to process categories
2. **Automation ROI** - Identify high-value automation targets
3. **Enterprise Sales** - Speak customer's process language
4. **Benchmark Comparisons** - Use standard PCF terminology

---

**Last Updated:** 2026-01-24

---

## APQC Attribution

> This APQC Process Classification Framework® ("PCF") is an open standard developed by APQC, a nonprofit that promotes benchmarking and best practices worldwide. APQC grants a perpetual, worldwide, royalty-free license to use, copy, publish, modify, and create derivative works of the PCF with proper attribution.
>
> **Source:** [www.apqc.org/pcf](https://www.apqc.org/pcf)
