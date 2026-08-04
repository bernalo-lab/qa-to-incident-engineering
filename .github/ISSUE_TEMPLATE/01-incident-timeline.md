---
name: Incident Timeline
about: Chronological record of an incident from detection to resolution
title: "[TIMELINE] Incident #<incident-id> — <short description>"
labels: incident, timeline
---

## Incident Summary

| Field | Value |
|---|---|
| Incident ID | |
| Severity | SEV-1 / SEV-2 / SEV-3 / SEV-4 |
| Detected by | Alert / Customer report / Internal / Other |
| Start time (UTC) | |
| Detection time (UTC) | |
| Resolution time (UTC) | |
| Total duration | |
| Incident Commander | |
| Services affected | |

## Timeline

> Log every meaningful event with a UTC timestamp. Include false starts and dead ends — they matter for the postmortem.

| Time (UTC) | Event | Source | Action Taken |
|---|---|---|---|
| | Alert fired / issue first observed | | |
| | On-call acknowledged | | |
| | Initial hypothesis formed | | |
| | Mitigation attempt #1 | | |
| | Mitigation attempt #2 (if needed) | | |
| | Root cause identified | | |
| | Fix deployed / rollback initiated | | |
| | Service confirmed stable | | |
| | Incident closed | | |

## Communication Log

| Time (UTC) | Channel | Message Sent | Audience |
|---|---|---|---|
| | Status page / Slack / Email | | Internal / Customers / Both |

## Notes for Postmortem

- What slowed down detection or diagnosis?
- What worked well and should be repeated?
- What links to the [Postmortem template](./03-postmortem.md) once this is filled in?

---
*This timeline should be started the moment an incident is declared and updated live — don't wait until resolution to fill it in from memory.*
