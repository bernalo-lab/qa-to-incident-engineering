---
name: Operational Risk Assessment
about: Structured evaluation of operational risk for a change, system, or dependency
title: "[RISK ASSESSMENT] <system/change name>"
labels: risk-assessment, operational-review
---

## Scope

| Field | Value |
|---|---|
| System / Change under review | |
| Assessed by | |
| Date | |
| Trigger (why now?) | New launch / Architecture change / Incident follow-up / Periodic review |

## Risk Identification

List specific ways this system/change could fail. Be concrete — "the database could go down" is less useful than "a single region outage would take checkout offline with no failover."

| # | Risk | Likelihood (Low/Med/High) | Impact (Low/Med/High) | Risk Score |
|---|---|---|---|---|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |

## Single Points of Failure

- Are there components with no redundancy?
- Are there dependencies (internal or third-party) that, if they fail, take this system down entirely?

## Blast Radius

If this fails, what else is affected? Map the dependency chain — upstream and downstream.

## Existing Mitigations

What controls, safeguards, or fallbacks already exist for the risks above?

## Recommended Mitigations

| Risk # | Mitigation | Owner | Priority | Status |
|---|---|---|---|---|
| | | | | |

## Residual Risk

After mitigations, what risk remains, and is it acceptable? Who is accountable for accepting it?

**Risk accepted by:** ______________ **Date:** ______________

---
*The goal isn't zero risk — it's making risk visible and deciding deliberately what to accept, mitigate, or avoid.*
