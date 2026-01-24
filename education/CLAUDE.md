---
title: Claude Context - Education PCF
type: reference
component_type: reference
version: 1.0.0
audience: contributor
status: pending
summary: AI context for Education industry PCF analysis
keywords:
- APQC
- PCF
- education
- claude-context
tokens: ~800
created: '2026-01-24'
updated: '2026-01-24'
tags:
- claude-context
- industry-pcf
---

# Education PCF - Claude Context

## Purpose

This directory contains the APQC Process Classification Framework (PCF) for the Education industry, pending decomposition into structured markdown for AI applicability analysis.

## Quick Reference

| Item | Value |
|------|-------|
| Industry | Education |
| PCF Version | v7.2.1 |
| Status | Pending Decomposition |
| Source Files | `source/` directory |

## AI Applications Focus

- Student enrollment automation
- Learning management optimization
- Grant and research administration
- Institutional compliance

## Common Tasks

### Check decomposition status

```bash
cat README.md | grep -A10 "Status"
```

### List source files

```bash
ls -la source/
```

### Start decomposition

```bash
/agent pcf-decomposer "education"
```

## Related

- [PCF-DECOMPOSITION-WORKFLOW.md](../PCF-DECOMPOSITION-WORKFLOW.md) - Decomposition workflow
- [Cross-Industry v7.4](../cross-industry-v7.4/) - Reference implementation

---

**Last Updated:** 2026-01-24
