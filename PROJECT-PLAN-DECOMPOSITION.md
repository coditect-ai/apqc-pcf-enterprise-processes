---
title: APQC PCF Decomposition Process Plan
type: project-plan
component_type: documentation
version: 1.0.0
audience: contributor
status: active
summary: Repeatable process for decomposing APQC PCF documents into structured markdown
keywords:
- APQC
- PCF
- decomposition
- project-plan
tokens: ~2000
created: '2026-01-24'
updated: '2026-01-24'
tags:
- project-plan
- decomposition
- process-framework
---

# APQC PCF Decomposition Process Plan

## Purpose

This document defines the repeatable process for converting APQC Process Classification Framework (PCF) source documents (PDF and Excel) into structured markdown for AI applicability analysis.

## Decomposition Workflow

```
┌─────────────────────────────────────────────────────────────────┐
│                    PCF DECOMPOSITION PIPELINE                    │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│ PHASE 1: SOURCE ANALYSIS                                         │
│ • Identify source files (PDF, XLSX)                              │
│ • Determine PCF version and industry                             │
│ • Count pages/sheets and estimate elements                       │
│ • Create industry subfolder structure                            │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│ PHASE 2: EXCEL DECOMPOSITION (Primary - Contains Full Data)     │
│ • Extract all sheets to markdown                                 │
│ • Parse hierarchy structure (X.X.X.X.X)                          │
│ • Extract PCF IDs, names, change tracking                        │
│ • Generate category files (category-NN-*.md)                     │
│ • Generate process group files (N.N-*.md)                        │
│ • Extract glossary, metrics, changes                             │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│ PHASE 3: PDF DECOMPOSITION (Secondary - Visual Reference)       │
│ • Convert page-by-page to markdown                               │
│ • Apply naming convention: PCF-MM-NN-Name.md                     │
│ • Extract framework diagrams and visual elements                 │
│ • Cross-reference with Excel data                                │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│ PHASE 4: DOCUMENTATION                                           │
│ • Create README.md for each folder                               │
│ • Create CLAUDE.md for AI context                                │
│ • Update parent-level indexes                                    │
│ • Verify completeness (element counts)                           │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│ PHASE 5: COMMIT & PUBLISH                                        │
│ • Stage all generated files                                      │
│ • Commit with conventional message                               │
│ • Push to repository                                             │
│ • Update session log                                             │
└─────────────────────────────────────────────────────────────────┘
```

## Directory Structure Template

```
{industry-name}/
├── README.md                           # Industry overview
├── CLAUDE.md                           # AI context for industry
├── v{version}/                         # Version-specific folder
│   ├── README.md                       # Version overview
│   ├── source/                         # Original source files
│   │   ├── {xlsx-file}.xlsx            # Excel source
│   │   └── {pdf-file}.pdf              # PDF source
│   ├── {industry}-overview.md          # Master index
│   ├── {industry}-glossary.md          # Term definitions
│   ├── {industry}-change-analysis.md   # Version changes
│   ├── {industry}-metrics.md           # Benchmarkable processes
│   ├── category-01-*.md                # Category documents
│   ├── category-01-*/                  # Process group breakdown
│   │   ├── 1.1-*.md
│   │   ├── 1.2-*.md
│   │   └── README.md
│   └── pdf-pages/                      # PDF page-by-page (optional)
│       ├── PCF-00-01-Overview.md
│       └── PCF-01-00-*.md
└── DECOMPOSITION-STATUS.md             # Conversion status tracker
```

## Naming Conventions

### Folder Names

| Pattern | Example | Description |
|---------|---------|-------------|
| `{industry-slug}/` | `aerospace-defense/` | Lowercase, hyphenated |
| `v{major}.{minor}/` | `v7.2.2/` | Version folder |
| `source/` | `source/` | Original files |
| `category-NN-*/` | `category-08-manage-it/` | Process group folders |

### File Names

| Type | Pattern | Example |
|------|---------|---------|
| Category | `category-NN-{name}.md` | `category-01-develop-vision-and-strategy.md` |
| Process Group | `N.N-{name}.md` | `1.1-define-business-concept.md` |
| PDF Page | `PCF-MM-NN-{Name}.md` | `PCF-01-00-Develop-Vision-and-Strategy.md` |
| Overview | `{industry}-overview.md` | `aerospace-defense-overview.md` |
| Glossary | `{industry}-glossary.md` | `aerospace-defense-glossary.md` |

### PDF Page Naming

```
PCF-MM-NN-Name.md

Where:
  PCF = Fixed prefix
  MM  = Category (00=meta, 01-13=category)
  NN  = Sequence (00=main, 01-99=pages)
  Name = Descriptive title
```

## YAML Frontmatter Template

```yaml
---
title: {Document Title}
type: research-analysis
component_type: documentation
version: 1.0.0
audience: contributor
status: active
summary: {One-line description}
keywords:
- APQC
- PCF
- {industry}
tokens: ~{estimate}
created: '{YYYY-MM-DD}'
updated: '{YYYY-MM-DD}'
tags:
- {industry}
- process-framework
pcf_version: '{X.X.X}'
pcf_industry: '{Industry Name}'
---
```

## Excel Sheet Processing

| Sheet Name | Output | Description |
|------------|--------|-------------|
| `Main Framework` | category-*.md, N.N-*.md | Process hierarchy |
| `Glossary` | {industry}-glossary.md | Term definitions |
| `Changes` | {industry}-change-analysis.md | Version delta |
| `Metrics` | {industry}-metrics.md | Benchmarkable flags |
| `Overview` | {industry}-overview.md | Summary stats |

## Quality Checklist

### Phase 1: Source Analysis
- [ ] Source files identified and inventoried
- [ ] Version determined from filename/content
- [ ] Industry classification confirmed
- [ ] Element count estimated

### Phase 2: Excel Decomposition
- [ ] All sheets extracted
- [ ] Hierarchy structure preserved (X.X.X.X.X)
- [ ] PCF IDs captured
- [ ] Change tracking preserved (+NEW, -removed, cChanged)
- [ ] Element count verified

### Phase 3: PDF Decomposition
- [ ] All pages converted
- [ ] Naming convention applied
- [ ] Framework diagrams described
- [ ] Cross-referenced with Excel

### Phase 4: Documentation
- [ ] README.md created at each level
- [ ] CLAUDE.md created with AI context
- [ ] Parent indexes updated
- [ ] Completeness verified

### Phase 5: Publish
- [ ] All files staged
- [ ] Commit message follows convention
- [ ] Pushed to repository
- [ ] Session log updated

## Industry PCF Inventory

| Industry | PDF Version | Excel Version | Status |
|----------|-------------|---------------|--------|
| Cross-Industry | v7.4 (Jan 2025) | v7.2.1 (Apr 2023), v7.4 | ✅ Complete |
| Aerospace & Defense | v7.2.2 (Mar 2025) | v7.2.2 | ⏳ Pending |
| Airline | v7.2.2 (Mar 2025) | v7.2.2 | ⏳ Pending |
| Automotive | v7.2.2 (Mar 2025) | v7.2.2 | ⏳ Pending |
| Banking | v7.2.2 (Mar 2025) | v7.2.1 | ⏳ Pending |
| Broadcasting | v7.2.2 (Mar 2025) | v7.2.2 | ⏳ Pending |
| City Government | v7.2.1 (Apr 2023) | v7.2.1 | ⏳ Pending |
| Consumer Electronics | v7.2.1 (Apr 2023) | v7.2.1 | ⏳ Pending |
| Consumer Products | v7.2.2 (Mar 2025) | v7.2.2 | ⏳ Pending |
| Downstream Petroleum | v7.2.2 (Mar 2025) | v7.2.2 | ⏳ Pending |
| Education | v7.2.1 (Apr 2023) | v7.2.1 | ⏳ Pending |
| Healthcare Provider | v7.2.1 (Apr 2023) | v7.2.1 | ⏳ Pending |
| Health Insurance Payor | v7.2.1 (Apr 2023) | v7.2.1 | ⏳ Pending |
| Life Sciences | v7.2.2 (Mar 2025) | v7.2.2 | ⏳ Pending |
| Property & Casualty Insurance | v7.2.2 (Mar 2025) | v7.2.1 | ⏳ Pending |
| Retail | v7.2.1 (Apr 2023) | v7.2.1 | ⏳ Pending |
| Telecom | v5.0.2 (2025) | - | ⏳ Pending |
| Upstream Petroleum | v7.2.2 (Mar 2025) | v7.2.1 | ⏳ Pending |
| Utilities | v7.2.2 (Mar 2025) | v7.2.1 | ⏳ Pending |

## Automation Commands

### Clone This Process

```bash
# 1. Create industry folder
mkdir -p {industry-slug}/v{version}/source

# 2. Move source files
mv "{pdf-file}" {industry-slug}/v{version}/source/
mv "{xlsx-file}" {industry-slug}/v{version}/source/

# 3. Run decomposition agent
/agent pcf-decomposer "{industry-slug} v{version}"

# 4. Verify and document
/classify {industry-slug}/
```

### Batch Processing

```bash
# Process all pending industries
for industry in aerospace-defense airline automotive banking; do
  /agent pcf-decomposer "$industry"
done
```

## Related Documents

- [README.md](./README.md) - Repository overview
- [CLAUDE.md](./CLAUDE.md) - AI context
- [cross-industry-v7.4/README.md](./cross-industry-v7.4/README.md) - Reference implementation

---

**Owner:** CODITECT Research Team
**Created:** 2026-01-24
**Template Version:** 1.0.0
