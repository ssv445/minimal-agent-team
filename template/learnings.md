# Learnings

Dated incident → rule lines. Each line says why a rule exists. Newest at the bottom. Terse.

Seed rows: the incidents the agreement was built from (Oct–Nov 2026). Add this repo's own below them.

| Date | What happened | Rule (how-we-work §) |
|---|---|---|
| 2026-10-07 | Agents waited on owner approvals for mechanical steps; 4 adversarial review rounds chased loopholes | never ask mechanical steps §2; honest-agent threat model §7 |
| 2026-10-14 | 20 screens built without owner approval of the design | new screen = mock first §2 §3 |
| 2026-10-23 | 5–7 parallel gate runs pushed load to ~290; pre-push 7–14 min, tests flaked | one heavy job at a time §9 |
| 2026-10-23 | Reviewers failed on launch; a builder waited ~2 h for a verdict line | wait on exit, not on a verdict §4 |
| 2026-10-26 | ~45 min of idle builders between steps; one decision lost to compaction | agents chain next step; log D-numbers §4 |
| 2026-10-28 | Manager built things itself; owner's questions waited during its push loop | lead manages, does not build §1 |
| 2026-10-28 | Owner rejected a bulk "apply the safe ones" approach | one decision per question, Apply/Discuss/Keep open §3 |
| 2026-10-28 | A 393-line safety check and 3 review rounds for a small change | safety only for material risk §7 |
| 2026-10-29 | A small change re-ran a 45-min e2e three times; release-note facts untrue on release day | test what changed; fact-check words early §6 |
| 2026-10-29 | A reviewer ran pkill and killed unrelated processes | never touch what you didn't start §9 |
| 2026-10-30 | Owner: "remove all the git hooks… convert repo standards into a guideline" | guideline, not gate (header) |
| 2026-10-30 | A reviewer ran `git checkout -- .` in a builder's worktree | reviewers only read §7 |
| 2026-10-31 | Owner: "long term memory should be put in .project always, you can update there in particular checklist/instructions yourself" | lead changes checklists without asking §13 |
| 2026-11-02 | The e2e was reported "all pass" from grep FAIL \| head; a second failure sat past the cut | read the runner's final line §5 |
| 2026-11-02 | A runaway self-re-exec hit ~4,400 processes, the per-user limit | depth guard on self-re-run §9 |
| 2026-11-02 | Owner: "I don't need every update" | quiet by default §5 |
| 2026-11-02 | An agent downloaded both takes of a metered resource | spend only what they picked §10 |
| 2026-11-03 | A peer relayed a discussion as a decision; work was pulled | peer relay ≠ decision §1 |
| 2026-11-04 | 12 full builds queued after "let's prepare all these" (meant mocks) | a mock is not a go §3 |
| 2026-11-04 | About half of the research tool's cited view counts and links were wrong | third-party research is a claim §6 |
| 2026-11-04 | A PR shipped on a self-read while the review slot was busy | the review always runs §7 |
| 2026-11-05 | 3 variants queued at once: "doing a lot of stuff in parallel does not add value" | parallel-work setting (team.md) |
| 2026-11-05 | Owner: "Maintain a schedule list as a table in a markdown file… you also need that" | every job written down in schedule.md §12 |
| 2026-11-06 | One cron trigger per job; owner: "one singular cron job which check our schedule.md" | one tick reads the file §12 |
| 2026-11-09 | A post slot was missed while the session waited on an open question | never hold a blocking question near a timed job §3 |
| 2026-11-10 | PR bodies clobbered through a shared temp file; verdicts sent by message were lost | own scratch folder; report files §4 |
| 2026-11-10 | A heredoc was used to append code; a browser credential leaked to 4 hosts | commands are data; never use credential-everywhere browser features §9 §10 |
| 2026-11-11 | Ships ran into the daily full-regression run | a heavy job holds its window §12 |
| 2026-11-12 | A large, uncertain infrastructure ticket cost two 2-hour runs and ~4 h of blocked Mac | smallest first; give cost and odds §8 |
| 2026-11-13 | Long-lived helpers drifted (false "worktree removed", inverted relay) | only the lead is long-lived §1 |
| 2026-11-13 | A process-only change took ~9 h through the full ship pipeline | rule changes straight to main §11 |
| 2026-11-14 | Three idle agents left alive for hours | stop finished agents §4 |
| 2026-11-15 | A handoff was lost when stopping the agent deleted its job folder | handoff to a surviving path, verify, then stop §4 |
| 2026-11-15 | Agents kept their own crons alongside the lead's tick | only the lead triggers jobs §12 |
| 2026-11-16 | Backticks inside a quoted agent prompt ran a deploy script | write long briefs to a file §4 |
| 2026-11-16 | An agent overwrote a reply the owner had already edited | live state differs → stop and report §10 |
| 2026-11-16 | Tickets filed that duplicated parked ones | search before filing §8 |
| 2026-11-17 | Owner: scheduled jobs are written down and the lead triggers them by observing; "they do not go to any other ways" | no other trigger path §12 |
