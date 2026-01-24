---
title: Claude Context - Banking PCF
type: reference
component_type: reference
version: 1.0.0
audience: contributor
status: pending
summary: AI context for Banking industry PCF analysis
keywords:
- APQC
- PCF
- banking
- claude-context
tokens: ~800
created: '2026-01-24'
updated: '2026-01-24'
tags:
- claude-context
- industry-pcf
---

# Banking PCF - Claude Context

## Purpose

This directory contains the APQC Process Classification Framework (PCF) for the Banking industry, pending decomposition into structured markdown for AI applicability analysis.

## Quick Reference

| Item | Value |
|------|-------|
| Industry | Banking |
| PCF Version | v7.2.2 |
| Status | Pending Decomposition |
| Source Files | `source/` directory |

## AI Applications Focus

- Fraud detection and prevention
- Credit risk assessment
- Regulatory compliance (Basel, AML)
- Customer onboarding automation

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
/agent pcf-decomposer "banking"
```

## Related

- [PROJECT-PLAN-DECOMPOSITION.md](../PROJECT-PLAN-DECOMPOSITION.md) - Decomposition workflow
- [Cross-Industry v7.4](../cross-industry-v7.4/) - Reference implementation

---

**Last Updated:** 2026-01-24
