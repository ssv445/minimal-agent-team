# Schedule

Every scheduled job in this repo. The lead reads this table on each tick and starts the due jobs (how-we-work section 12). A job not in this table does not run.

Runs are logged in `.tmp/schedule-runs.md` (gitignored), not here.

| ID | Job | When | Latest useful | Heavy | Account | State | Brief / command |
|---|---|---|---|---|---|---|---|
| S1 | Renew the lead's tick (in-session crons expire after 7 days) | every 6 days | 7 days | no | lead | active | lead renews its own tick |

State is `active` or `paused (date, owner's words)`.
