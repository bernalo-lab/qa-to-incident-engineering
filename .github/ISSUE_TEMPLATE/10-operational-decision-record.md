---
name: Operational Decision Record
about: Record of a significant operational decision, its context, and rationale (an ADR for operations, not just architecture)
title: "[ODR] <decision title>"
labels: decision-record, operational
---

## Decision

One sentence stating the decision made.

| Field | Value |
|---|---|
| Status | Proposed / Accepted / Superseded |
| Date | |
| Decision maker(s) | |
| Related incident/review | (link if applicable) |

## Context

What situation led to needing this decision? What was the triggering event, question, or tension?

## Options Considered

| Option | Pros | Cons |
|---|---|---|
| Option A | | |
| Option B | | |
| Option C (do nothing) | | |

## Decision Rationale

Why was the chosen option selected over the alternatives? What tradeoffs were accepted knowingly?

## Consequences

- What does this decision make easier?
- What does this decision make harder, or what risk does it accept?
- What follow-up work does this create?

## Reversibility

- Is this decision easily reversible if it turns out wrong?
- If not, what would it take to reverse it?

## Review Date

When should this decision be revisited? (e.g., "in 6 months," "if traffic doubles," "if incident rate on X increases")

---
*Operational decisions made under pressure are often forgotten or reversed silently. This record exists so future engineers understand not just what was decided, but why — especially when the "why" isn't obvious in hindsight.*
