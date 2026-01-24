---
title: Claude Context - Healthcare Provider PCF
type: reference
component_type: reference
version: 1.0.0
audience: contributor
status: pending
summary: AI context for Healthcare Provider industry PCF analysis
keywords:
- APQC
- PCF
- healthcare-provider
- claude-context
tokens: ~800
created: '2026-01-24'
updated: '2026-01-24'
tags:
- claude-context
- industry-pcf
---

# Healthcare Provider PCF - Claude Context

## Purpose

This directory contains the APQC Process Classification Framework (PCF) for the Healthcare Provider industry, pending decomposition into structured markdown for AI applicability analysis.

## Quick Reference

| Item | Value |
|------|-------|
| Industry | Healthcare Provider |
| PCF Version | v7.2.1 |
| Status | Pending Decomposition |
| Source Files | `source/` directory |

## AI Applications Focus

- Clinical decision support
- Patient scheduling optimization
- Medical coding automation (ICD-10, CPT)
- Revenue cycle management

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
/agent pcf-decomposer "healthcare-provider"
```

## Related

- [PCF-DECOMPOSITION-WORKFLOW.md](../PCF-DECOMPOSITION-WORKFLOW.md) - Decomposition workflow
- [Cross-Industry v7.4](../cross-industry-v7.4/) - Reference implementation

---

**Last Updated:** 2026-01-24
