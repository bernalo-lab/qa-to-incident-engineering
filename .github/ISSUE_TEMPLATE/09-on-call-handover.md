---
name: On-call Handover
about: Structured handoff between outgoing and incoming on-call engineers
title: "[HANDOVER] <date range> — <outgoing> to <incoming>"
labels: on-call, handover
---

## Handover Details

| Field | Value |
|---|---|
| Outgoing on-call | |
| Incoming on-call | |
| Handover date/time (UTC) | |
| Shift period covered | |

## Open Incidents

| Incident | Status | Next Action | Owner |
|---|---|---|---|
| | | | |

*If none, state "No open incidents" explicitly — don't leave this blank.*

## Recent Incidents (this shift)

Brief summary of anything that happened, even if resolved — patterns matter.

| Incident | Resolution | Postmortem needed? |
|---|---|---|
| | | Yes / No |

## Watch Items

Things that aren't incidents yet but are worth the next on-call's attention:

- [ ] E.g., "Error rate on X has been creeping up, not yet alert-worthy"
- [ ] E.g., "Deploy of Y is scheduled for tomorrow, may need monitoring"
- [ ] E.g., "Known flaky alert on Z, low priority but noisy"

## System State Notes

- Any manual mitigations currently in place that need to be remembered/reverted?
- Any feature flags toggled that aren't in their normal state?
- Any scheduled maintenance or deploys coming up?

## Access & Tooling Check

- [ ] Incoming on-call has access to all required dashboards/alerts
- [ ] Incoming on-call has tested paging/notification works
- [ ] Incoming on-call knows current escalation contacts

## Questions / Notes from Outgoing

Free text — anything not captured above.

---
*A good handover means the incoming on-call could handle a page in the first 5 minutes of their shift without needing to ask "wait, what's going on?"*
