---
name: Runbook
about: Step-by-step operational guide for diagnosing and resolving a specific failure scenario
title: "[RUNBOOK] <scenario name, e.g. 'API latency spike'>"
labels: runbook, documentation
---

## Scenario

**What this runbook covers:** (e.g., "Elevated p99 latency on the checkout API")

**When to use this runbook:** What alert, symptom, or report should trigger someone to open this document?

## Severity Guidance

| Symptom | Likely Severity |
|---|---|
| | SEV-1 |
| | SEV-2 |
| | SEV-3 |

## Quick Diagnosis

A short decision tree or checklist to narrow down the cause fast.

1. Check ___ dashboard — is ___ elevated?
2. Check recent deploys — was anything deployed in the last ___ minutes?
3. Check upstream dependencies — is ___ healthy?
4. Check ___ logs for error pattern ___

## Common Causes & Fixes

| Cause | How to Confirm | Fix |
|---|---|---|
| | | |
| | | |
| | | |

## Step-by-Step Resolution

1. 
2. 
3. 
4. Verify resolution: what does "healthy" look like on the dashboard?

## Escalation

- If not resolved within ___ minutes, escalate to: ___
- If this affects ___, notify: ___ (see [Incident Status Update](./04-incident-status-update.md))

## Related Resources

- Dashboard: 
- Related runbooks: 
- Owning team: 

## Last Verified

| Date | Verified By | Notes |
|---|---|---|
| | | |

---
*Runbooks go stale fast. Review this after every incident it's used in, and set a calendar reminder to re-verify it quarterly even if unused.*
