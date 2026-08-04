---
name: Postmortem
about: Blameless review of an incident to extract learning and prevent recurrence
title: "[POSTMORTEM] <incident-id> — <short description>"
labels: postmortem, incident
---

> This document is blameless. The goal is to understand systems and processes, not to assign fault to individuals.

## Summary

| Field | Value |
|---|---|
| Incident ID | (link to Incident Timeline) |
| Date | |
| Severity | |
| Duration | |
| Customer impact | |
| Author(s) | |
| Status | Draft / In Review / Final |

## Impact

- Who/what was affected (users, internal teams, revenue, SLA)?
- Quantify where possible (requests failed, users affected, minutes of downtime).

## Root Cause

Describe the technical and/or process root cause. Distinguish the **trigger** (what set it off) from the **root cause** (why the system was vulnerable to that trigger).

## Detection

- How was this detected — alert, customer report, internal discovery?
- Time to detect (from start of impact to detection)?
- Could/should this have been caught sooner? By what?

## Response

- Time to acknowledge, time to mitigate, time to resolve.
- What went well in the response?
- What was slow, confusing, or missing (tooling, access, documentation)?

## The Five Whys (optional but recommended)

1. Why did X happen? →
2. Why did that happen? →
3. Why did that happen? →
4. Why did that happen? →
5. Why did that happen? →

## Action Items

| Action | Type (Prevent / Detect / Mitigate) | Owner | Due Date | Status |
|---|---|---|---|---|
| | | | | |
| | | | | |

## Lessons Learned

- What surprised us?
- What assumptions turned out to be wrong?
- What would we do differently if this happened again tomorrow?

---
*Publish this internally even when the story isn't flattering — the value of a postmortem is proportional to how honestly it's written.*
