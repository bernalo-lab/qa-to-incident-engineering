---
name: Production Readiness Review
about: Pre-launch checklist to assess whether a service/feature is ready for production traffic
title: "[PRR] <service/feature name>"
labels: production-readiness, review
---

## Overview

| Field | Value |
|---|---|
| Service / Feature | |
| Owning team | |
| Launch date (target) | |
| Reviewer(s) | |
| Review date | |

## Reliability

- [ ] SLOs/SLIs defined and agreed with stakeholders
- [ ] Load/stress testing completed at expected (and 2x expected) traffic
- [ ] Graceful degradation behavior defined (what happens under overload?)
- [ ] Dependencies identified, with failure modes considered for each
- [ ] Timeout and retry policies configured for downstream calls

## Observability

- [ ] Dashboards exist for key metrics (latency, error rate, saturation, traffic)
- [ ] Alerts configured with sensible thresholds (not too noisy, not too quiet)
- [ ] Logs are structured and searchable
- [ ] Distributed tracing in place (if applicable)

## Operational Readiness

- [ ] Runbook exists for common failure scenarios (link it)
- [ ] On-call rotation covers this service
- [ ] Rollback procedure defined and tested
- [ ] Feature flags / kill switch available for risky components

## Data & Security

- [ ] Data migrations are backward-compatible / reversible
- [ ] Access controls reviewed
- [ ] Sensitive data handling reviewed (PII, secrets, encryption)
- [ ] Rate limiting / abuse protection in place if externally facing

## Change Management

- [ ] Rollout plan defined (canary / phased / big-bang, with justification)
- [ ] Stakeholders informed of launch window
- [ ] Related [Change Review](./07-change-review.md) completed

## Sign-off

| Reviewer | Area | Approved | Notes |
|---|---|---|---|
| | Reliability | ☐ | |
| | Security | ☐ | |
| | On-call/Ops | ☐ | |

---
*A PRR isn't a gate to slow teams down — it's a shared checklist so nothing critical is missed under launch pressure.*
