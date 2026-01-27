---
title: APQC PCF Analysis & Documentation Project Plan
type: project-plan
component_type: documentation
version: 1.0.0
audience: contributor
status: complete
summary: Project plan documenting the analysis, breakdown, and documentation development for APQC PCF enterprise processes
keywords:
- APQC
- PCF
- project-plan
- documentation
- AI-applicability
tokens: ~2500
created: '2026-01-24'
updated: '2026-01-24'
tags:
- project-plan
- APQC-PCF
- research
apqc_license: royalty-free
apqc_attribution: "APQC Process Classification Framework® - Open Standard"
apqc_source: "www.apqc.org/pcf"
---

# APQC PCF Analysis & Documentation Project Plan

> **Project:** APQC Process Classification Framework - AI Applicability Analysis
> **Status:** Phase 1 Complete (104 documents, 2.1MB)
> **Date:** 2026-01-24

---

## 1. Project Overview

### 1.1 Objective

Transform the APQC Process Classification Framework (PCF) Cross-Industry Excel dataset into structured markdown documentation for AI applicability analysis, enabling identification of automation opportunities across enterprise processes.

### 1.2 Source Data

| Asset | Version | Format | Size |
|-------|---------|--------|------|
| Excel Dataset | v7.2.1 (April 2023) | XLSX, 19 sheets | ~2MB |
| PDF Reference | v7.4 (January 2025) | PDF, 35 pages | 775KB |

### 1.3 Scope

- 1,855 process elements across 13 major enterprise categories
- 1,856 glossary definitions
- 227 benchmarkable processes with APQC metrics
- Version change tracking (v7.2.1 vs v6.1.1)

---

## 2. Project Phases

### Phase 1: Source Data Analysis ✅ COMPLETE

**Duration:** Session 1

**Activities:**
1. Read and analyze Excel file structure (19 sheets)
2. Identify data schema and hierarchy levels
3. Map PCF ID system and numbering convention
4. Extract metadata (version, publisher, dates)

**Outputs:**
- Understanding of 5-level hierarchy (Category → Group → Process → Activity → Task)
- Identification of PCF ID numbering scheme (5-digit unique IDs)
- Change tracking columns identified (+NEW, -removed, cChanged)

---

### Phase 2: Master Document Generation ✅ COMPLETE

**Duration:** Session 1

**Activities:**
1. Create master overview document (apqc-pcf-overview.md)
2. Create 13 monolithic category documents
3. Create README.md with navigation
4. Create CLAUDE.md with context for AI assistants

**Outputs:**
| Document | Purpose | Size |
|----------|---------|------|
| apqc-pcf-overview.md | Master index, AI applicability summary | 6KB |
| category-{01-13}-*.md | Full category content | 13 files |
| README.md | Directory documentation | 6KB |
| CLAUDE.md | AI assistant context | 4KB |

---

### Phase 3: Hierarchical Document Breakdown ✅ COMPLETE

**Duration:** Session 1

**Activities:**
1. Create 13 category subdirectories
2. Generate README.md for each category
3. Create individual process group documents (72 files)
4. Maintain complete hierarchy in each document

**Outputs:**
```
category-{01-13}-*/
├── README.md           # Category overview
├── X.1-*.md           # Process group 1
├── X.2-*.md           # Process group 2
└── ...                 # All process groups
```

**Bug Fixed:**
- Regex pattern `f"^{cat_num}\\.\d+$"` incorrectly matched X.0 headers
- Fixed to `f"^{cat_num}\\.[1-9][0-9]*$"` for proper process group matching

---

### Phase 4: Completeness Verification ✅ COMPLETE

**Duration:** Session 1

**Activities:**
1. Build verification script to compare Excel vs generated docs
2. Count elements per category in both sources
3. Identify any missing or orphan elements
4. Generate completeness report

**Results:**
| Category | Excel Elements | Generated | Status |
|----------|---------------|-----------|--------|
| 1.0 | 123 | 123 | ✅ |
| 2.0 | 100 | 100 | ✅ |
| 3.0 | 202 | 202 | ✅ |
| 4.0 | 147 | 147 | ✅ |
| 5.0 | 67 | 67 | ✅ |
| 6.0 | 104 | 104 | ✅ |
| 7.0 | 135 | 135 | ✅ |
| 8.0 | 321 | 321 | ✅ |
| 9.0 | 270 | 270 | ✅ |
| 10.0 | 69 | 69 | ✅ |
| 11.0 | 56 | 56 | ✅ |
| 12.0 | 54 | 54 | ✅ |
| 13.0 | 207 | 207 | ✅ |
| **Total** | **1,855** | **1,855** | **✅ 100%** |

---

### Phase 5: Enhanced Data Extraction ✅ COMPLETE

**Duration:** Session 1

**Activities:**
1. Extract glossary definitions (1,856 terms)
2. Identify benchmarkable processes (227 with metrics)
3. Document version changes (NEW, additions, removals)
4. Integrate definitions into process group documents

**Outputs:**
| Document | Content | Size |
|----------|---------|------|
| apqc-pcf-glossary.md | All 1,856 definitions | 489KB |
| apqc-pcf-change-analysis.md | Version change tracking | 33KB |
| apqc-pcf-benchmarkable-metrics.md | 227 measurable processes | 32KB |

**Change Statistics:**
| Change Type | Count |
|-------------|-------|
| NEW elements in v7.2.1 | 845 |
| Additions (+) | 227 |
| Removals (-) | 24 |
| Modifications (c) | 74 |

---

### Phase 6: PDF Version Analysis 🔄 IN PROGRESS

**Duration:** Session 2 (current)

**Activities:**
1. Locate corresponding PDF document ✅
2. Read and parse 35-page PDF ✅
3. Convert to page-by-page markdown ⏳ PENDING
4. Compare v7.2.1 (Excel) vs v7.4 (PDF) ⏳ PENDING

**Status:**
- PDF successfully read (35 pages)
- Context limit reached during conversion
- Session compacted, work continuing

---

### Phase 7: Classification & Quality Assurance ⏳ PENDING

**Activities:**
1. Run `/classify` on all 104 generated documents
2. Verify frontmatter compliance
3. Update `moe_confidence` scores
4. Review AI applicability assessments

---

## 3. Deliverables Summary

### 3.1 Final Output

| Metric | Value |
|--------|-------|
| Total Documents | 104 |
| Total Size | 2.1 MB |
| Process Elements | 1,855 |
| Definitions | 1,856 |
| Benchmarkable | 227 (12%) |
| Categories | 13 |
| Process Groups | 72 |
| Hierarchy Depth | 5 levels |

### 3.2 Directory Structure

```
apqc-pcf-enterprise-processes/
├── apqc-pcf-overview.md              # Master index
├── apqc-pcf-glossary.md              # 489KB definitions
├── apqc-pcf-change-analysis.md       # Version tracking
├── apqc-pcf-benchmarkable-metrics.md # Measurable processes
├── README.md                          # Documentation
├── CLAUDE.md                          # AI context
├── project-plan-apqc-pcf-analysis.md # This document
├── category-01-develop-vision-and-strategy/
│   ├── README.md
│   ├── 1.1-*.md through 1.4-*.md
├── category-02-develop-and-manage-products-*/
│   ├── README.md
│   ├── 2.1-*.md through 2.3-*.md
... (13 category subdirectories, 72 process group files)
```

---

## 4. AI Applicability Analysis

### 4.1 High-Value Automation Targets

| Category | % Benchmarkable | AI Application |
|----------|-----------------|----------------|
| 9.0 Financial Resources | 32% | Transaction processing, reconciliation, reporting |
| 7.0 Human Capital | 23% | Resume screening, L&D personalization |
| 3.0 Marketing & Sales | 17% | Lead scoring, personalization, analytics |
| 6.0 Customer Service | 13% | Chatbots, ticket routing, sentiment analysis |

### 4.2 Automation Categories

| Category | AI Fit | Rationale |
|----------|--------|-----------|
| 8.0 IT Management | Full Automation | Rule-based, already digitized |
| 9.0 Financial | High Automation | High-volume transactions |
| 6.0 Customer Service | Chatbots + Routing | Repetitive inquiries |
| 3.0 Marketing | Analytics + Personalization | Data-driven decisions |
| 7.0 Human Capital | Augmentation | AI screens, humans decide |
| 1.0 Strategy | Augmentation | AI provides data, humans judge |
| 4.0 Physical Products | IoT + AI | Hybrid physical-digital |

---

## 5. Technical Implementation

### 5.1 Tools Used

| Tool | Purpose |
|------|---------|
| Python + pandas | Excel parsing and data extraction |
| openpyxl | Excel file reading |
| Claude Code | Document generation and analysis |
| CODITECT Framework | Document standards and classification |

### 5.2 Key Scripts

```python
# Excel reading pattern
import pandas as pd
df = pd.read_excel(file_path, sheet_name='Sheet Name')

# Hierarchy pattern matching
level_1 = df[df['Hierarchy ID'].astype(str).str.match(f"^{cat_num}\\.[1-9][0-9]*$")]
```

### 5.3 Bug Fixes

| Issue | Cause | Solution |
|-------|-------|----------|
| Only READMEs created | Regex matched X.0 headers | Changed to `[1-9][0-9]*` |
| Binary file error | Read tool can't read XLSX | Used pandas |
| Missing pandas | Module not installed | Activated venv, pip install |

---

## 6. Next Steps

### 6.1 Immediate (This Session)

- [ ] Convert PDF v7.4 to page-by-page markdown
- [ ] Compare v7.2.1 vs v7.4 changes
- [ ] Run `/classify` on generated documents

### 6.2 Future Enhancements

- [ ] Create process-to-occupation mapping (O*NET integration)
- [ ] Build AI applicability scoring model
- [ ] Generate automation ROI estimates per process
- [ ] Create interactive visualization of process hierarchy

---

## 7. References

### 7.1 Source Documents

- `k08897-cross-industry-v721-vs-v611-april-2023.xlsx` - Primary data source
- `k014750-apqc-process-classification-framework-(pcf)-cross-industry-pdf-version-7.4-january-2025.pdf` - Reference PDF

### 7.2 Related Research

- O*NET Occupation Database analysis (same parent directory)
- CODITECT AI Applicability research framework
- Process automation ROI methodology

### 7.3 APQC Resources

- Publisher: American Productivity & Quality Center (APQC)
- Website: apqc.org
- PCF Version: 7.2.1 Cross-Industry

---

**Document Version:** 1.0.0
**Created:** 2026-01-24
**Author:** CODITECT Research Team
**Status:** Phase 1 Complete, Phase 6-7 In Progress

---

## APQC Attribution

> This APQC Process Classification Framework® ("PCF") is an open standard developed by APQC, a nonprofit that promotes benchmarking and best practices worldwide. APQC grants a perpetual, worldwide, royalty-free license to use, copy, publish, modify, and create derivative works of the PCF with proper attribution.
>
> **Source:** [www.apqc.org/pcf](https://www.apqc.org/pcf)
