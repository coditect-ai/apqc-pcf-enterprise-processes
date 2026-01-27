---
title: Claude Context - Downstream Petroleum PCF
type: reference
component_type: reference
version: 1.0.0
audience: contributor
status: pending
summary: AI context for Downstream Petroleum industry PCF analysis
keywords:
- APQC
- PCF
- downstream-petroleum
- claude-context
tokens: ~800
created: '2026-01-24'
updated: '2026-01-24'
tags:
- claude-context
- industry-pcf
---

# Downstream Petroleum PCF - Claude Context

## Purpose

This directory contains the APQC Process Classification Framework (PCF) for the Downstream Petroleum industry, pending decomposition into structured markdown for AI applicability analysis.

## Quick Reference

| Item | Value |
|------|-------|
| Industry | Downstream Petroleum |
| PCF Version | v7.2.2 |
| Status | Pending Decomposition |
| Source Files | `source/` directory |

## AI Applications Focus

- Refinery optimization
- Supply chain scheduling
- Pricing optimization
- Environmental compliance

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
/agent pcf-decomposer "downstream-petroleum"
```

## Related

- [pcf-decomposition-workflow.md](../pcf-decomposition-workflow.md) - Decomposition workflow
- [Cross-Industry v7.4](../cross-industry-v7.4/) - Reference implementation

---

**Last Updated:** 2026-01-24
