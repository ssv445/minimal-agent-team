# Agent agreement

A plain-markdown operating manual for AI coding agents. You copy it into a repo as `.project/`. It tells every agent (Claude Code, Codex, any of them) how to work together: who decides what, how to report, what "done" means, how review and git work, and what never happens without you.

There are no hooks, scripts or gates. Agents follow it the way a new hire follows a team handbook.

## Why

I spent about a year trying to build an autonomous AI company. I tried many agent stacks: skill packs, big global AGENTS.md files, enforcing hooks, multi-agent frameworks. Every one of them failed in its own way, and I spent more usage on the setup than on the product.

This small set of markdown files is what finally worked. Most of it is about what to remove.

Each rule has a dated incident behind it in `learnings.md`. Those rows cover only the last few weeks, when I started writing the failures down. The lessons behind them took the whole year.

## The core ideas

1. **One lead agent, and it never builds.** It talks to you, briefs workers, verifies their claims and keeps the log. Everything else goes to other agents.
2. **One fresh agent per task.** It does one task end to end, writes a handoff and stops. Long-lived workers drift.
3. **Only a few calls come to you:** money, anything sent or published, a new screen, a public release, changes to the rules. Every other call is the agent's. It logs the call as one line in `decisions.md` and keeps going.
4. **Incidents become rules.** Something breaks, then a dated row goes in `learnings.md` and a rule changes in `how-we-work.md`.
5. **The reviewer learns.** Each bug that gets past a review adds one check to `briefs/reviewer.md`.
6. **One heavy job at a time** on your machine. This alone saved more quota than any skill did.

## Files

Everything lives in [`template/`](template/):

| File | What it is |
|---|---|
| how-we-work.md | the agreement (roles, decisions, reporting, verification, review, git, machine etiquette, outbound, upkeep, schedule, checklists) |
| team.md | names and per-repo settings (agent cap, work hours, heavy jobs, models) |
| briefs/task-agent.md | prepended to every task agent's prompt |
| briefs/lead.md | what the lead reads when it starts or restarts |
| briefs/reviewer.md | prepended to every review request |
| learnings.md | incident → rule log, seeded with the incidents behind it |
| decisions.md | one-line decision log |
| schedule.md | every scheduled job; the lead's tick starts due ones |
| checklists/pr.md, checklists/pre-review-self-check.md | pasted into PRs / run before review |

## Install

1. Download this repo (Code → Download ZIP) or clone it.
2. Copy the `template/` folder into your repo and rename it `.project/`. From your repo's root:

   ```
   cp -Rn path/to/agent-agreement/template/ .project/
   ```

3. Fill the `<…>` placeholders in `.project/team.md` and the briefs. Leaving a default is fine.
4. Add this near the top of your `CLAUDE.md` or `AGENTS.md`:

   ```
   ## How agents work here
   Every agent follows `.project/how-we-work.md` (the operating agreement). Settings and names: `.project/team.md`. Task agents start from `.project/briefs/task-agent.md`; the lead restarts from `.project/briefs/lead.md`. The repo's rules beat private agent memory.
   ```

5. Add `.tmp/` to `.gitignore` (state, handoffs and run logs live there).
6. Start one lead agent and tell it to read `.project/briefs/lead.md`.

## Limits

1. It is written for one human owner running a small setup. A team with several humans will need to rework section 2.
2. Nothing enforces it. A careless agent can still ignore it. In practice, agents follow a short, specific rulebook far better than a long, vague one.
3. Some defaults assume Claude Code (subagents, background agents, in-session crons). The ideas carry over to other tools.
4. Delete what you don't need. My advice is to start with roles and the decision log. Add a rule only when something breaks.

## License

MIT. Copy it, change it, use it anywhere.
