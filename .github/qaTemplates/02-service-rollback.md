---
name: Service Rollback
about: Structured request and record for rolling back a service to a previous known-good state
title: "[ROLLBACK] <service-name> — <reason>"
labels: rollback, incident-response
---

## Rollback Request

| Field | Value |
|---|---|
| Service / Repo | |
| Current (bad) version / commit | |
| Target (rollback) version / commit | |
| Requested by | |
| Approved by | |
| Related incident | (link to Incident Timeline issue) |

## Why Rollback (not forward-fix)

- [ ] Root cause is not yet understood
- [ ] Fix would take longer than acceptable downtime allows
- [ ] Previous version is confirmed stable
- [ ] Other: ___

## Pre-Rollback Checklist

- [ ] Confirmed target version is a known-good, previously deployed build
- [ ] Checked for schema/data migrations between current and target version (are they backward-compatible?)
- [ ] Checked for feature flags or config that may not roll back cleanly
- [ ] Notified affected teams / on-call
- [ ] Confirmed rollback mechanism (redeploy, revert commit, infra-level toggle)

## Rollback Steps

1. 
2. 
3. 

## Post-Rollback Verification

- [ ] Service health checks passing
- [ ] Key user flows manually verified
- [ ] Error rates / latency back to baseline
- [ ] Monitoring dashboards reviewed for 15–30 min post-rollback
- [ ] Stakeholders notified of completion

## Follow-up Actions

| Action | Owner | Due |
|---|---|---|
| Root cause investigation | | |
| Forward-fix plan | | |
| Update rollback runbook if process broke down | | |

---
*A rollback is a mitigation, not a fix. Always pair this with a follow-up task to address the underlying cause.*
