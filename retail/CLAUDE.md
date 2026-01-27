---
title: Claude Context - Retail PCF
type: reference
component_type: reference
version: 1.0.0
audience: contributor
status: pending
summary: AI context for Retail industry PCF analysis
keywords:
- APQC
- PCF
- retail
- claude-context
tokens: ~800
created: '2026-01-24'
updated: '2026-01-24'
tags:
- claude-context
- industry-pcf
---

# Retail PCF - Claude Context

## Purpose

This directory contains the APQC Process Classification Framework (PCF) for the Retail industry, pending decomposition into structured markdown for AI applicability analysis.

## Quick Reference

| Item | Value |
|------|-------|
| Industry | Retail |
| PCF Version | v7.2.1 |
| Status | Pending Decomposition |
| Source Files | `source/` directory |

## AI Applications Focus

- Demand forecasting
- Inventory optimization
- Price optimization
- Customer personalization

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
/agent pcf-decomposer "retail"
```

## Related

- [pcf-decomposition-workflow.md](../pcf-decomposition-workflow.md) - Decomposition workflow
- [Cross-Industry v7.4](../cross-industry-v7.4/) - Reference implementation

---

**Last Updated:** 2026-01-24
