---
title: APQC PCF Decomposition Workflow
type: workflow
component_type: documentation
version: 1.1.0
audience: contributor
status: active
summary: Repeatable 7-phase workflow for decomposing APQC PCF documents into structured markdown
keywords:
- APQC
- PCF
- decomposition
- workflow
- process-framework
- ai-applicability
tokens: ~2500
created: '2026-01-24'
updated: '2026-01-24'
tags:
- workflow
- decomposition
- process-framework
- enterprise-processes
agent: pcf-decomposer
---

# APQC PCF Decomposition Workflow

## Purpose

This workflow defines the repeatable process for converting APQC Process Classification Framework (PCF) source documents (PDF and Excel) into structured markdown for AI applicability analysis.

## Agent Invocation

```bash
# Execute decomposition for a specific industry
/agent pcf-decomposer "{industry-slug} v{version}"

# Example
/agent pcf-decomposer "banking v7.2.2"
```

## Decomposition Workflow

```text
┌─────────────────────────────────────────────────────────────────┐
│                    PCF DECOMPOSITION PIPELINE                    │
│                        (7 Phases)                                │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│ PHASE 0: PREREQUISITES                                          │
│ • Verify source files exist (PDF and/or XLSX)                   │
│ • Confirm read access to source directory                       │
│ • Check industry folder structure exists                        │
│ • Verify cross-industry reference is available                  │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│ PHASE 1: SOURCE ANALYSIS                                         │
│ • Identify source files (PDF, XLSX)                              │
│ • Determine PCF version and industry                             │
│ • Count pages/sheets and estimate elements                       │
│ • Create industry subfolder structure                            │
│ • Document source file metadata                                  │
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
│ • Preserve change tracking (+NEW, -removed, cChanged)            │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│ PHASE 3: PDF DECOMPOSITION (Secondary - Visual Reference)       │
│ • Convert page-by-page to markdown                               │
│ • Apply naming convention: PCF-MM-NN-Name.md                     │
│ • Extract framework diagrams and visual elements                 │
│ • Cross-reference with Excel data                                │
│ • Document any PDF-only content                                  │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│ PHASE 4: DOCUMENTATION                                           │
│ • Create README.md for each folder                               │
│ • Create CLAUDE.md for AI context                                │
│ • Update parent-level indexes                                    │
│ • Add YAML frontmatter to all generated files                    │
│ • Cross-link related documents                                   │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│ PHASE 5: VALIDATION                                              │
│ • Verify element counts match source                             │
│ • Check all 13 categories are represented                        │
│ • Validate hierarchy completeness (no gaps in X.X.X.X.X)         │
│ • Run markdown lint checks                                       │
│ • Verify YAML frontmatter on all files                           │
│ • Cross-reference Excel and PDF outputs for consistency          │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│ PHASE 6: COMMIT & PUBLISH                                        │
│ • Stage all generated files                                      │
│ • Commit with conventional message                               │
│ • Push to repository                                             │
│ • Update DECOMPOSITION-STATUS.md                                 │
│ • Update session log                                             │
│ • Run /classify on generated directory                           │
└─────────────────────────────────────────────────────────────────┘
```

## Directory Structure Template

```text
{industry-name}/
├── README.md                           # Industry overview
├── CLAUDE.md                           # AI context for industry
├── DECOMPOSITION-STATUS.md             # Conversion status tracker
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
```

## Naming Conventions

### Folder Names

| Pattern | Example | Description |
|---------|---------|-------------|
| `{industry-slug}/` | `aerospace-defense/` | Lowercase, hyphenated |
| `v{major}.{minor}/` | `v7.2.2/` | Version folder |
| `source/` | `source/` | Original files |
| `category-NN-*/` | `category-08-manage-it/` | Process group folders |
| `pdf-pages/` | `pdf-pages/` | PDF conversion output |

### File Names

| Type | Pattern | Example |
|------|---------|---------|
| Category | `category-NN-{name}.md` | `category-01-develop-vision-and-strategy.md` |
| Process Group | `N.N-{name}.md` | `1.1-define-business-concept.md` |
| PDF Page | `PCF-MM-NN-{Name}.md` | `PCF-01-00-Develop-Vision-and-Strategy.md` |
| Overview | `{industry}-overview.md` | `aerospace-defense-overview.md` |
| Glossary | `{industry}-glossary.md` | `aerospace-defense-glossary.md` |
| Metrics | `{industry}-metrics.md` | `aerospace-defense-metrics.md` |
| Changes | `{industry}-change-analysis.md` | `aerospace-defense-change-analysis.md` |

### PDF Page Naming Convention

```text
PCF-MM-NN-Name.md

Where:
  PCF = Fixed prefix
  MM  = Category (00=meta, 01-13=category)
  NN  = Sequence (00=main, 01-99=pages)
  Name = Descriptive title (PascalCase)

Examples:
  PCF-00-01-Overview.md           # Meta: Overview
  PCF-01-00-Develop-Vision.md     # Category 1 main
  PCF-08-02-IT-Operations.md      # Category 8, page 2
```

## YAML Frontmatter Template

```yaml
---
title: '{Document Title}'
type: research-analysis
component_type: documentation
version: 1.0.0
audience: contributor
status: active
summary: '{One-line description}'
keywords:
- APQC
- PCF
- '{industry}'
tokens: ~{estimate}
created: '{YYYY-MM-DD}'
updated: '{YYYY-MM-DD}'
tags:
- '{industry}'
- process-framework
- enterprise-processes
pcf_version: '{X.X.X}'
pcf_industry: '{Industry Name}'
pcf_category: '{Category Number}'
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

### Hierarchy Extraction Rules

```text
Level 1: X.0       = Category (e.g., "8.0 Manage Information Technology")
Level 2: X.Y       = Process Group (e.g., "8.1 Manage IT Strategy")
Level 3: X.Y.Z     = Process (e.g., "8.1.1 Define IT Strategy")
Level 4: X.Y.Z.W   = Activity (e.g., "8.1.1.1 Align IT with business strategy")
Level 5: X.Y.Z.W.V = Task (e.g., "8.1.1.1.1 Document strategic alignment")
```

## Quality Checklist

### Phase 0: Prerequisites

- [ ] Source files located in `source/` directory
- [ ] PDF file readable (not password protected)
- [ ] Excel file readable (not corrupted)
- [ ] Industry folder created
- [ ] Cross-industry v7.4 reference available

### Phase 1: Source Analysis

- [ ] Source files identified and inventoried
- [ ] Version determined from filename/content
- [ ] Industry classification confirmed
- [ ] Element count estimated
- [ ] Source metadata documented

### Phase 2: Excel Decomposition

- [ ] All sheets extracted
- [ ] Hierarchy structure preserved (X.X.X.X.X)
- [ ] PCF IDs captured for all elements
- [ ] Change tracking preserved (+NEW, -removed, cChanged)
- [ ] Element count verified against source
- [ ] All 13 categories represented

### Phase 3: PDF Decomposition

- [ ] All pages converted
- [ ] Naming convention applied (PCF-MM-NN-Name.md)
- [ ] Framework diagrams described
- [ ] Cross-referenced with Excel data
- [ ] PDF-only content documented

### Phase 4: Documentation

- [ ] README.md created at each folder level
- [ ] CLAUDE.md created with AI context
- [ ] Parent indexes updated
- [ ] YAML frontmatter on all files
- [ ] Cross-links verified

### Phase 5: Validation

- [ ] Element count matches source
- [ ] All 13 categories present
- [ ] No hierarchy gaps
- [ ] Markdown lint passes
- [ ] YAML frontmatter valid
- [ ] Excel/PDF consistency verified

### Phase 6: Publish

- [ ] All files staged
- [ ] Commit message follows convention
- [ ] Pushed to repository
- [ ] DECOMPOSITION-STATUS.md updated
- [ ] Session log updated
- [ ] /classify executed on directory

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

### Execute Decomposition

```bash
# 1. Verify prerequisites
ls {industry-slug}/source/

# 2. Run decomposition agent
/agent pcf-decomposer "{industry-slug} v{version}"

# 3. Validate and classify
/classify {industry-slug}/
```

### Manual Decomposition Steps

```bash
# 1. Create industry folder structure
mkdir -p {industry-slug}/v{version}/source

# 2. Copy/move source files
cp "{pdf-file}" {industry-slug}/v{version}/source/
cp "{xlsx-file}" {industry-slug}/v{version}/source/

# 3. Execute decomposition (manual)
# Follow phases 1-5 manually

# 4. Commit results
git add {industry-slug}/
git commit -m "feat(pcf): decompose {industry} PCF v{version}"
git push

# 5. Update status
echo "| {Industry} | v{version} | v{version} | ✅ Complete |" >> PCF-DECOMPOSITION-WORKFLOW.md
```

### Batch Processing

```bash
# Process multiple industries in sequence
for industry in aerospace-defense airline automotive banking; do
  echo "Processing: $industry"
  /agent pcf-decomposer "$industry"
  /classify "$industry/"
done
```

## Success Criteria

| Metric | Target | Validation |
|--------|--------|------------|
| Element Count | 100% of source | Compare vs Excel row count |
| Category Coverage | 13/13 | Verify category-01 to category-13 exist |
| Hierarchy Depth | All 5 levels | Check for X.X.X.X.X patterns |
| Documentation | README + CLAUDE at each level | File existence check |
| Frontmatter | 100% of .md files | YAML lint validation |
| Markdown Quality | 0 lint errors | markdownlint check |

## Related Documents

- [README.md](./README.md) - Repository overview
- [CLAUDE.md](./CLAUDE.md) - AI context
- [cross-industry-v7.4/](./cross-industry-v7.4/) - Reference implementation

---

**Owner:** CODITECT Research Team
**Created:** 2026-01-24
**Updated:** 2026-01-24
**Workflow Version:** 1.1.0
