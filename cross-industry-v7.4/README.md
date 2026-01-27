---
title: APQC PCF Enterprise Processes - AI Applicability Analysis
type: research-analysis
component_type: documentation
version: 2.0.0
audience: contributor
status: active
summary: APQC Process Classification Framework v7.2.1 - Complete analysis with definitions, metrics, and change tracking
keywords:
- APQC
- PCF
- enterprise-processes
- AI-automation
- process-framework
tokens: ~1000
created: '2026-01-24'
updated: '2026-01-24'
tags:
- research
- process-framework
- AI-applicability
apqc_license: royalty-free
apqc_attribution: "APQC Process Classification Framework® - Open Standard"
apqc_source: "www.apqc.org/pcf"
---
# APQC PCF Enterprise Processes

> **Source:** APQC Cross-Industry PCF v7.2.1 vs v6.1.1 (April 2023)
> **Created:** 2026-01-24 | **Version:** 2.0.0 (with definitions)

## Overview

Complete structured analysis of the APQC Process Classification Framework (PCF) Cross-Industry v7.2.1, including:

- **1,855 process elements** across 13 categories
- **1,856 full-text definitions** from APQC glossary
- **227 benchmarkable processes** with available metrics
- **845 NEW elements** added in v7.2.1
- **Version change tracking** (additions, removals, modifications)

## Quick Links

| Document | Description |
|----------|-------------|
| [apqc-pcf-overview.md](./apqc-pcf-overview.md) | Master overview with navigation |
| [apqc-pcf-glossary.md](./apqc-pcf-glossary.md) | Complete definitions (489KB) |
| [apqc-pcf-change-analysis.md](./apqc-pcf-change-analysis.md) | Version change tracking |
| [apqc-pcf-benchmarkable-metrics.md](./apqc-pcf-benchmarkable-metrics.md) | 227 measurable processes |
| [project-plan-apqc-pcf-analysis.md](./project-plan-apqc-pcf-analysis.md) | Project plan & methodology |

## Category Index

| # | Category | Elements | Benchmarkable | Subdirectory |
|---|----------|----------|---------------|--------------|
| 1.0 | Develop Vision and Strategy | 123 | 3 | [category-01-develop-vision-and-strategy/](./category-01-develop-vision-and-strategy/) |
| 2.0 | Develop and Manage Products and Services | 100 | 12 | [category-02-develop-and-manage-products-and-services/](./category-02-develop-and-manage-products-and-services/) |
| 3.0 | Market and Sell Products and Services | 202 | 34 | [category-03-market-and-sell-products-and-services/](./category-03-market-and-sell-products-and-services/) |
| 4.0 | Deliver Physical Products | 147 | 20 | [category-04-deliver-physical-products/](./category-04-deliver-physical-products/) |
| 5.0 | Deliver Services | 67 | 6 | [category-05-deliver-services/](./category-05-deliver-services/) |
| 6.0 | Manage Customer Service | 104 | 14 | [category-06-manage-customer-service/](./category-06-manage-customer-service/) |
| 7.0 | Develop and Manage Human Capital | 135 | 31 | [category-07-develop-and-manage-human-capital/](./category-07-develop-and-manage-human-capital/) |
| 8.0 | Manage Information Technology (IT) | 321 | 8 | [category-08-manage-information-technology-it/](./category-08-manage-information-technology-it/) |
| 9.0 | Manage Financial Resources | 270 | 87 | [category-09-manage-financial-resources/](./category-09-manage-financial-resources/) |
| 10.0 | Acquire, Construct, and Manage Assets | 69 | 3 | [category-10-acquire-construct-and-manage-assets/](./category-10-acquire-construct-and-manage-assets/) |
| 11.0 | Manage Enterprise Risk, Compliance, Remediati | 56 | 3 | [category-11-manage-enterprise-risk-compliance-remediation-and/](./category-11-manage-enterprise-risk-compliance-remediation-and/) |
| 12.0 | Manage External Relationships | 54 | 2 | [category-12-manage-external-relationships/](./category-12-manage-external-relationships/) |
| 13.0 | Develop and Manage Business Capabilities | 207 | 4 | [category-13-develop-and-manage-business-capabilities/](./category-13-develop-and-manage-business-capabilities/) |

## Statistics

| Metric | Value |
|--------|-------|
| Total Process Elements | 1,855 |
| Total Definitions | 1,856 |
| Major Categories | 13 |
| Process Groups | 72 |
| Benchmarkable Processes | 227 (12%) |
| NEW in v7.2.1 | 845 elements |
| Maximum Hierarchy Depth | 5 levels |

## Document Structure

```
apqc-pcf-enterprise-processes/
├── apqc-pcf-overview.md              # Navigation index
├── apqc-pcf-glossary.md              # All 1,856 definitions
├── apqc-pcf-change-analysis.md       # v7.2.1 vs v6.1.1 changes
├── apqc-pcf-benchmarkable-metrics.md # 227 measurable processes
├── README.md                          # This file
├── CLAUDE.md                          # Claude context
├── category-01-develop-vision-and-strategy/
│   ├── README.md
│   ├── 1.1-define-the-business-concept-*.md
│   ├── 1.2-develop-business-strategy.md
│   └── ...
├── category-02-develop-and-manage-products-*/
│   └── ...
... (13 category subdirectories)
```

## AI Automation Insights

### High-Value Automation Targets

1. **9.0 Financial Resources** - 32% benchmarkable, high transaction volume
2. **7.0 Human Capital** - 23% benchmarkable, repetitive screening
3. **3.0 Marketing & Sales** - 17% benchmarkable, analytics-heavy

### Process Categories by AI Fit

| Category | AI Application | Rationale |
|----------|----------------|-----------|
| 8.0 IT Management | Full Automation | Rule-based, digitized |
| 9.0 Financial | High Automation | Transactions, reconciliation |
| 6.0 Customer Service | Chatbots + Routing | FAQs, ticket handling |
| 3.0 Marketing | Analytics + Personalization | Data-driven decisions |
| 7.0 Human Capital | Augmentation | Screening + human judgment |
| 1.0 Strategy | Augmentation | AI data, human decisions |

## Usage

```bash
# View complete glossary
cat apqc-pcf-glossary.md

# Find processes with metrics
cat apqc-pcf-benchmarkable-metrics.md

# Search for automation targets
grep -r "automation" . --include="*.md"

# View specific process group
cat category-09-manage-financial-resources/9.3-perform-general-accounting-and-reporting.md
```

## Source Data

**Original Excel:** `../k08897-cross-industry-v721-vs-v611-april-2023.xlsx`

---

**Owner:** CODITECT Research Team
**License:** APQC Content - See original Excel for copyright

---

## APQC Attribution

> This APQC Process Classification Framework® ("PCF") is an open standard developed by APQC, a nonprofit that promotes benchmarking and best practices worldwide. APQC grants a perpetual, worldwide, royalty-free license to use, copy, publish, modify, and create derivative works of the PCF with proper attribution.
>
> **Source:** [www.apqc.org/pcf](https://www.apqc.org/pcf)
