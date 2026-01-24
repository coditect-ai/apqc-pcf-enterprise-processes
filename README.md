---
title: Readme
type: guide
component_type: guide
version: 1.0.0
audience: contributor
status: draft
summary: Auto-classified guide document
keywords:
- guide
tokens: ~1000
created: '2026-01-24'
updated: '2026-01-24'
tags:
- guide
---
# APQC PCF Enterprise Processes

APQC Process Classification Framework (PCF) transformed into structured markdown for AI applicability analysis.

## Overview

The APQC PCF is the world's most widely used process framework for business process benchmarking, containing 1,855+ process elements across 13 major enterprise categories.

## Directory Structure

```text
apqc-pcf-enterprise-processes/
├── README.md                           # This file
├── CLAUDE.md                           # AI context
├── PROJECT-PLAN-DECOMPOSITION.md       # Repeatable decomposition workflow
│
├── cross-industry-v7.4/                # ✅ Complete - Reference implementation
│   ├── source/                         # Original PDF and Excel files
│   ├── APQC-PCF-OVERVIEW.md            # Master index
│   ├── category-01-*.md ... category-13-*.md
│   ├── category-01-*/ ... category-13-*/
│   └── K014750-APQC-PCF-*/             # PDF v7.4 pages
│
├── aerospace-defense/                  # ⏳ Pending
│   ├── source/                         # PDF v7.2.2 + Excel
│   ├── README.md
│   └── CLAUDE.md
│
├── airline/                            # ⏳ Pending
├── automotive/                         # ⏳ Pending
├── banking/                            # ⏳ Pending
├── broadcasting/                       # ⏳ Pending
├── city-government/                    # ⏳ Pending
├── consumer-electronics/               # ⏳ Pending
├── consumer-products/                  # ⏳ Pending
├── downstream-petroleum/               # ⏳ Pending
├── education/                          # ⏳ Pending
├── healthcare-provider/                # ⏳ Pending
├── health-insurance-payor/             # ⏳ Pending
├── life-sciences/                      # ⏳ Pending
├── property-casualty-insurance/        # ⏳ Pending
├── retail/                             # ⏳ Pending
├── telecom/                            # ⏳ Pending
├── upstream-petroleum/                 # ⏳ Pending
└── utilities/                          # ⏳ Pending
```

## Industry PCF Summary

| Industry | PDF | Excel | Status |
|----------|-----|-------|--------|
| **Cross-Industry** | v7.4 | v7.2.1, v7.4 | ✅ Complete |
| Aerospace & Defense | v7.2.2 | v7.2.2 | ⏳ Pending |
| Airline | v7.2.2 | v7.2.2 | ⏳ Pending |
| Automotive | v7.2.2 | v7.2.2 | ⏳ Pending |
| Banking | v7.2.2 | v7.2.1 | ⏳ Pending |
| Broadcasting | v7.2.2 | v7.2.2 | ⏳ Pending |
| City Government | v7.2.1 | v7.2.1 | ⏳ Pending |
| Consumer Electronics | v7.2.1 | v7.2.1 | ⏳ Pending |
| Consumer Products | v7.2.2 | v7.2.2 | ⏳ Pending |
| Downstream Petroleum | v7.2.2 | v7.2.2 | ⏳ Pending |
| Education | v7.2.1 | v7.2.1 | ⏳ Pending |
| Healthcare Provider | v7.2.1 | v7.2.1 | ⏳ Pending |
| Health Insurance Payor | v7.2.1 | v7.2.1 | ⏳ Pending |
| Life Sciences | v7.2.2 | v7.2.2 | ⏳ Pending |
| Property & Casualty Insurance | v7.2.2 | v7.2.1 | ⏳ Pending |
| Retail | v7.2.1 | v7.2.1 | ⏳ Pending |
| Telecommunications | v5.0.2 | - | ⏳ Pending |
| Upstream Petroleum | v7.2.2 | v7.2.1 | ⏳ Pending |
| Utilities | v7.2.2 | v7.2.1 | ⏳ Pending |

## The 13 Enterprise Process Categories

| # | Category | Elements | Focus |
|---|----------|----------|-------|
| 1.0 | Develop Vision and Strategy | 123 | Strategic planning |
| 2.0 | Develop and Manage Products/Services | 100 | R&D, innovation |
| 3.0 | Market and Sell Products/Services | 202 | Sales, marketing |
| 4.0 | Deliver Physical Products | 147 | Supply chain, logistics |
| 5.0 | Deliver Services | 67 | Service operations |
| 6.0 | Manage Customer Service | 104 | Customer support |
| 7.0 | Develop and Manage Human Capital | 135 | HR, talent |
| 8.0 | Manage Information Technology | 321 | IT operations |
| 9.0 | Manage Financial Resources | 270 | Finance, accounting |
| 10.0 | Acquire, Construct, Manage Assets | 69 | Facilities, assets |
| 11.0 | Manage Enterprise Risk/Compliance | 56 | Risk, compliance |
| 12.0 | Manage External Relationships | 54 | Partnerships, PR |
| 13.0 | Develop and Manage Business Capabilities | 207 | Process improvement |

## PCF Hierarchy Structure

```text
1.0       = Category (e.g., "Develop Vision and Strategy")
1.1       = Process Group
1.1.1     = Process
1.1.1.1   = Activity
1.1.1.1.1 = Task (deepest level)
```

## Quick Start

### View completed Cross-Industry decomposition

```bash
ls cross-industry-v7.4/
cat cross-industry-v7.4/APQC-PCF-OVERVIEW.md
```

### Start industry decomposition

```bash
# Follow the decomposition process plan
cat PROJECT-PLAN-DECOMPOSITION.md

# Or use the decomposer agent
/agent pcf-decomposer "aerospace-defense"
```

## Usage

This framework supports:
- **AI Applicability Analysis** - Map AI capabilities to enterprise processes
- **Automation ROI** - Identify high-value automation targets
- **Enterprise Sales** - Speak customer's process language
- **Benchmark Comparisons** - Use standard PCF terminology

## Related Research

- O*NET occupation analysis
- Industry-specific automation potential
- Process-to-occupation mapping

## License

APQC Content - See individual files for copyright and attribution.

---

**Repository:** [coditect-ai/apqc-pcf-enterprise-processes](https://github.com/coditect-ai/apqc-pcf-enterprise-processes)
**Owner:** AZ1.AI INC
**Created:** 2026-01-24
