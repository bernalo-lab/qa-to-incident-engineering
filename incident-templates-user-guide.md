# User Guide: Incident Engineering Templates on GitHub

This guide walks you from cloning the repo through to creating linked, working incident issues — using one worked example throughout (a checkout API latency spike) so you can see exactly what to click and type at each step.

---

## Part 1 — Getting the Repo

### Option A: Use it as a template for your own project repo (recommended for real use)

1. Go to `https://github.com/bernalo-lab/qa-to-incident-engineering`
2. Click the green **"Use this template"** button (top right) → **"Create a new repository"**
3. Name your new repo (e.g., `my-team-incidents`), choose public/private, click **Create repository**
4. This gives you a fresh repo with all 10 templates already in `.github/ISSUE_TEMPLATE/`, ready to use immediately

### Option B: Clone it directly (for editing the templates themselves)

```bash
git clone https://github.com/bernalo-lab/qa-to-incident-engineering.git
cd qa-to-incident-engineering
```

Use this option only if you're modifying the template files themselves, not for day-to-day incident logging.

---

## Part 2 — Worked Example: A Fictional Incident

We'll simulate the same scenario from earlier: **a checkout API latency spike**, walked through as three linked issues.

### Step 1: Create the Incident Timeline issue

1. Go to your repo → **Issues** tab → **New Issue**
2. Select **Incident Timeline** from the template list
3. Edit the title (click the pencil ✏️, or it's already editable before you submit):
   ```
   [TIMELINE] Incident #47 — Checkout API latency spike
   ```
4. Before clicking Create, fill in what you know so far in the body. Click into the text box and replace the empty table cells:

   ```
   | Field | Value |
   |---|---|
   | Incident ID | INC-047 |
   | Severity | SEV-2 |
   | Detected by | Alert |
   | Start time (UTC) | 14:02 |
   | Detection time (UTC) | 14:02 |
   | Resolution time (UTC) | |
   | Total duration | |
   | Incident Commander | @your-username |
   | Services affected | checkout-api |
   ```

5. Click **Create**. Note the issue number GitHub assigns — it'll show as `#1` if this is your repo's first issue (in the real example this was `#47`, but your test repo will likely start at `#1`).

### Step 2: Update the issue live, as the incident unfolds

1. Open the issue you just created
2. Click the **"..."** menu on your own comment (or click directly into the body) → **Edit**
3. Add rows to the Timeline table as things happen:

   ```
   | Time (UTC) | Event | Source | Action Taken |
   |---|---|---|---|
   | 14:02 | Alert fired — p99 latency >4s | Datadog | Paged on-call |
   | 14:04 | On-call acknowledged | PagerDuty | Started investigating |
   | 14:09 | Found unindexed query in recent deploy | GitHub | Formed hypothesis |
   | 14:18 | Decided to roll back the deploy | — | Opened rollback issue |
   ```

4. Click **Update comment** to save

### Step 3: Create the linked Rollback issue

1. Click **New Issue** again → select **Service Rollback**
2. Title:
   ```
   [ROLLBACK] checkout-api — unindexed query causing latency spike
   ```
3. In the body, find the "Related incident" field and type the issue number of your Timeline issue, e.g.:
   ```
   | Related incident | #1 |
   ```
   Typing `#1` (or whatever number your Timeline issue got) is what creates the automatic link — GitHub recognizes the `#` followed by a number as a reference to another issue in this repo.
4. Fill in the rest of the rollback checklist as you go, then **Create**

**What happens automatically:** once this issue is created with `#1` in its body, go back to Issue #1 (the Timeline) — scroll to the bottom of the conversation. You'll now see a line like:
> **bernalo-lab** mentioned this issue in #2

That's the automatic backlink. This is the mechanic doing its job — you don't need to manually connect anything.

### Step 4: Close the Rollback issue once resolved

1. Fill in the "Post-Rollback Verification" checkboxes as you confirm the fix
2. Scroll to the bottom of the issue → click **Close issue**
3. The issue badge turns from green "Open" to purple "Closed" — but it stays in the repo's history permanently, still linked to #1

### Step 5: Create the linked Postmortem issue

1. **New Issue** → **Postmortem**
2. Title:
   ```
   [POSTMORTEM] Incident #47 — Checkout API latency spike
   ```
3. In the body's "Incident ID" field, reference both prior issues:
   ```
   | Incident ID | #1 (Timeline), #2 (Rollback) |
   ```
4. Fill in Root Cause, Five Whys, and Action Items using what you logged in the Timeline
5. **Create**, then go back and check both #1 and #2 — both now show "mentioned this issue in #3" at the bottom

---

## Part 3 — Viewing the Linked Issues

Once all three issues reference each other, here's where to see the connections:

### Inline references (always visible, no setup needed)
Scroll to the bottom of any of the three issues — below the last comment, GitHub shows a timeline of activity including "mentioned this issue in #X" entries. This is automatic and always there once you've typed `#1`, `#2`, etc. anywhere in another issue.

### Development panel (right sidebar)
- This panel is mainly built for linking **pull requests** and **branches** to an issue, not other issues — so for issue-to-issue links (like your Timeline → Rollback → Postmortem chain), the bottom-of-page "mentioned this issue in" references are actually your primary view, not the Development panel.
- The Development panel becomes useful once you start linking actual code changes — e.g., if you create a branch or PR to add the missing database index from Step 5's action items, linking that PR to the Postmortem issue will show up here.

### Searching/filtering across all your incidents later
Once you've got a history of issues, use the Issues tab search bar:
```
label:incident is:closed
```
or click on a label (e.g., `postmortem`) from the Labels page to see every postmortem you've ever filed. This is where the real long-term value shows up — a searchable operational history, not just three connected issues.

---

## Part 4 — Quick Reference: The Habit

| When | Do this |
|---|---|
| Incident starts | New Issue → Incident Timeline. Fill in as you go, don't wait |
| Need to roll back | New Issue → Service Rollback. Reference the Timeline issue number |
| Comms needed | New Issue → Incident Status Update (or post as a comment on the Timeline) |
| Incident resolved | New Issue → Postmortem. Reference Timeline + Rollback issue numbers |
| End of on-call shift | New Issue → On-call Handover |
| Before a risky deploy | New Issue → Change Review or Production Readiness Review |

The core skill isn't the templates themselves — it's the habit of referencing issue numbers (`#1`, `#2`...) as you write, so GitHub builds the connective trail for you automatically.

---

*Tip: practice this exact flow in a throwaway test repo (like your `qa-testing-template` repo) a couple of times before using it on a real incident — the muscle memory of "type `#`, pick the issue, keep writing" is the main thing to get comfortable with.*
