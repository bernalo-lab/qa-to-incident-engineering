# Incident Engineering Template Pack

10 templates covering the full lifecycle of operational work: before an incident (readiness, risk, change), during an incident (timeline, status updates, rollback), and after (postmortem, decision records), plus the connective tissue that keeps teams calibrated (runbooks, on-call handover).

## The 10 Templates

| # | Template | Use When |
|---|---|---|
| 1 | [Incident Timeline](./01-incident-timeline.md) | An incident is declared — start this immediately, update live |
| 2 | [Service Rollback](./02-service-rollback.md) | You need to revert a service to a known-good state |
| 3 | [Postmortem](./03-postmortem.md) | After an incident is resolved, to extract learning |
| 4 | [Incident Status Update](./04-incident-status-update.md) | Communicating incident status to stakeholders/customers |
| 5 | [Production Readiness Review](./05-production-readiness-review.md) | Before launching a new service or major feature |
| 6 | [Operational Risk Assessment](./06-operational-risk-assessment.md) | Evaluating risk of a system, dependency, or upcoming change |
| 7 | [Change Review](./07-change-review.md) | Before deploying a change with meaningful production risk |
| 8 | [Runbook](./08-runbook.md) | Documenting how to diagnose/resolve a specific failure scenario |
| 9 | [On-call Handover](./09-on-call-handover.md) | End of every on-call shift |
| 10 | [Operational Decision Record](./10-operational-decision-record.md) | Recording the "why" behind a significant operational decision |

## Who is this for?

This repository is designed for:

1. QA Engineers transitioning into Reliability Engineering
2. Test Engineers moving towards SRE
3. Incident Engineers
4. Platform Engineers
5. Engineering Managers building operational capability
6. Teams introducing incident management practices

## How to Use These

### Option A — GitHub Issue Templates
Drop these files into `.github/ISSUE_TEMPLATE/` in any repo. The YAML frontmatter (`name`, `about`, `title`, `labels`) is already formatted for GitHub's issue template system — they'll appear automatically when someone clicks "New Issue."

### Option B — Standalone Docs
Keep them in a `/docs/templates/` or `/runbooks/` folder and copy-paste content into issues, PRs, or wiki pages as needed. Strip the YAML frontmatter if you don't need it.

### Option C — Repo Template
Turn a repo containing all 10 into a GitHub Template Repository (Settings → Template repository), so new projects can be scaffolded with all of this baked in from day one.

## Suggested Adoption Path for QA → Reliability Teams

1. Start with **Runbook**, **On-call Handover**, and **Incident Timeline** — these have the fastest payoff and lowest barrier to adoption.
2. Add **Postmortem** and **Incident Status Update** once your team runs its first couple of real incidents with the above three.
3. Introduce **Production Readiness Review**, **Change Review**, and **Operational Risk Assessment** as your team starts influencing decisions *before* incidents happen — this is the shift from reactive QA to proactive reliability engineering.
4. **Operational Decision Record** and **Service Rollback** round things out once the team has enough operational history to want a memory of past decisions.

## Notes

- All templates use tables and checklists deliberately — they're built to be filled in under time pressure, not read as prose.
- Cross-references between templates (e.g., Rollback → Incident Timeline) are intentional — link actual issues once you're using these live, so incidents form a connected trail rather than isolated documents.
- Customize severity definitions (SEV-1/2/3/4), escalation paths, and team names to match your organization before rolling these out.

## Continue your learning

- **[Incident Engineering Hub](https://hub.bernalo.com/)**
The complete platform for learning, practising and applying Incident Engineering through interactive simulations, engineering games, AI-assisted diagnosis and enterprise tools.

- **[Bernalo](https://www.bernalo.com/)** - Helping engineering teams make better operational decisions.

- **[Incident Ladder](https://incidentladder.com)** – Learn how production systems fail.

- **[ExplainError Daily](https://www.explainerror.dev/)** - Wordle-style game for engineers that trains incident diagnosis and failure interpretation.

- **[ExplainError](https://www.incidentatlas.io/)** -
ExplainError is an API that interprets production failures and returns structured incident judgement — classification, severity and recommended action.
It reduces the time engineers spend diagnosing incidents.

- **[Operational Knowledge]** - Coming soon....

- **[Production Failure Patterns](https://github.com/bernalo-lab/incident-pattern-free)** -
Production failure patterns for SREs, DevOps, and platform engineers — real-world incident behaviours, misleading signals, root causes, and operational troubleshooting guidance for distributed systems.

- **[AWS ClodWatch Search](https://github.com/bernalo-lab/aws-log-search-preview)** -
Selected AWS CloudWatch Logs Insights patterns for incident triage under pressure

- **[YouTube]** - In progress

- **[LinkedIn]** -</br>
Author (https://www.linkedin.com/in/bosun-sogeke-a1413713b/)</br>
Company (https://www.linkedin.com/company/19836464/)

- **[explainerror-pilot](https://explainerror-pilot.vercel.app/)** -
Reduce incident misclassification before it slows down your response.
ExplainError pilot landing page – structured error classification and confidence-driven incident triage for SRE and engineering teams.


- **[Submit a Redacted Incident Example](https://incident-dataset.onrender.com)** -
A curated dataset of real-world production errors used for calibrating incident classification systems.
Share a production incident example to help grow the Open Production Incident Dataset.

- **[Skool](https://www.skool.com/incident-engineering-academy-3597)**

- **[Incident Engineeer (Reddit)](https://www.reddit.com/r/IncidentEngineering/)**

## Mission

Our goal is simple:

Help QA Engineers become Reliability Engineers by providing practical tools, operational knowledge, and hands-on exercises that can be used immediately in production environments.

Small improvements in operational judgement prevent big incidents.