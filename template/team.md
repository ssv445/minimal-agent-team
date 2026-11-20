# Team and settings

Who does what in this repo, and the per-repo choices that [how-we-work.md](how-we-work.md) points to. Fill every `<…>` at install time. Leaving the default is fine.

## People and agents

| Name | Kind | Does | Reports to |
|---|---|---|---|
| <owner name> | owner (human) | big calls (how-we-work §2) | — |
| <repo>-lead | lead, long-lived | talks to owner, decides, briefs, verifies | owner |
| <repo>-task-<slug> | task agent, short-lived | one task end to end, then stops | <repo>-lead |
| reviewer | subagent per gate | one independent review | the agent that started it |

Name task agents `<repo>-task-<slug>`, so they never clash with scheduled job names.

## Settings

| Setting | This repo | Default if blank |
|---|---|---|
| Owner's editor for review files | <e.g. `open -a Zed <path>`> | the owner's usual editor |
| Max live task agents | <n> | 3 |
| Parallel work | <serial / light-parallel> | light-parallel: one heavy job, light work alongside |
| Heavy jobs in this repo | <builds, Docker stack, e2e, VM, renders…> | builds, full suites, e2e, VMs, Docker, video |
| Verify command | <command or skill that starts the app and drives the changed path; "none"> | none |
| Load ceiling before a heavy job | <1-min load, free RAM> | load < 8 |
| Work hours | <e.g. 08:00–20:00, or "any"> | any time |
| Build window (app code) | <e.g. after 20:00, or "any"> | any time |
| Silence watchdog cadence | <minutes> | 20 |
| Schedule tick cadence | <minutes> | 30 |
| Lead model / account | <model> / <account> | strongest model / main account |
| Task agents model / account | <model> / <account> | cheapest tier that can be right / a secondary account if you have one; no silent fallback to the main one, tell the owner |
| Reviewer model | <model + effort> | Opus, high effort |
| Release style | <straight to main / release branch> | straight to main |
| Rule changes (.project/, CLAUDE.md) | <straight to main / PR, owner merges> | straight to main, with an issue as the record |
| Decision log | decisions.md | decisions.md |
| Issue tracker | <GitHub repo> | GitHub Issues, Inbox milestone |

## Standing approvals

Exact owner quote, date, and scope. Nothing outside the scope is covered.

| Date | Owner's words | Covers | Excludes |
|---|---|---|---|
| | | | |
