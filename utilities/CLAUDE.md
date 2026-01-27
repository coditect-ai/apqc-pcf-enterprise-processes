---
title: Claude Context - Utilities PCF
type: reference
component_type: reference
version: 1.0.0
audience: contributor
status: pending
summary: AI context for Utilities industry PCF analysis
keywords:
- APQC
- PCF
- utilities
- claude-context
tokens: ~800
created: '2026-01-24'
updated: '2026-01-24'
tags:
- claude-context
- industry-pcf
---

# Utilities PCF - Claude Context

## Purpose

This directory contains the APQC Process Classification Framework (PCF) for the Utilities industry, pending decomposition into structured markdown for AI applicability analysis.

## Quick Reference

| Item | Value |
|------|-------|
| Industry | Utilities |
| PCF Version | v7.2.2 |
| Status | Pending Decomposition |
| Source Files | `source/` directory |

## AI Applications Focus

- Grid optimization
- Demand response management
- Predictive maintenance
- Customer service automation

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
/agent pcf-decomposer "utilities"
```

## Related

- [pcf-decomposition-workflow.md](../pcf-decomposition-workflow.md) - Decomposition workflow
- [Cross-Industry v7.4](../cross-industry-v7.4/) - Reference implementation

---

**Last Updated:** 2026-01-24
