# Aiola Use Cases

Real-world ways people use Aiola — the local agentic desktop app for Claude Code and Codex.

> Aiola requires the **Claude Code SDK** and/or **Codex SDK** to be installed locally. It does not bundle an LLM.

---

## Running agentic workflows across many repos

You have eight projects — a SaaS, two client apps, three side projects, and two abandoned-but-still-shipping experiments. The Claude Code or Codex CLIs need a separate session per repo, and you constantly lose context.

With Aiola: every repo is a workspace in one local agentic desktop app. The `/central/home` command center aggregates today's tasks, recent app-log spikes, incoming feedback, open PRs, and scheduled automations across every workspace. Pick a global default model, override per thread when a project needs different capability.

---

## Auto-PR pipeline from a task

You finish steering an agent through a feature task. Now you have to commit, push, open a PR, and write a description.

With Aiola: move the task to `create_pr`. The auto-PR pipeline checks out the task branch in a worktree, commits any dirty changes, merges subtask branches if present, pushes the branch, and runs `gh pr create`. If a step fails too many times the task lands in `human_review` with a `pr-failed` label and the recovery sweep retries it later. Crashes and transient git failures don't permanently wedge the task.

---

## Agentic PR review on incoming pull requests

A teammate or contractor opens a PR. Reviewing it manually means pulling the branch, running it, reading the diff, and writing thoughtful comments.

With Aiola: open the PR in `/github` or `/central/github`. Trigger an AI review with the PR's files and history, or a fix flow that creates a worktree-backed thread on the PR branch using the same provider/model as the rest of the workspace. Optionally auto-comment a concise summary back on the PR. Duplicate detection can auto-close PRs that retread closed ones.

---

## Live app-log triage instead of inbox-zeroing Sentry

Errors stream in across multiple products. Manually grouping them, deciding which are urgent, and routing fixes is a full-time chore.

With Aiola: `/app-logs` and `/central/app-logs` group errors live, with stats, filters, and detail panels. From a log group you can run AI analyze (root cause) or AI fix (which opens a thread on the relevant code). Realtime updates keep the queue current without refresh.

---

## Closing the user-feedback loop

Feedback piles up in spreadsheets, Discord, and email and turns into a graveyard.

With Aiola: `/feedback` captures bugs and feature requests with customizable issue and feature field definitions. From a feedback item you can open a coding thread that references the feedback. The central `/central/feedback` view rolls everything up across workspaces while keeping each project's field config separate.

---

## Scheduled agentic automations across the portfolio

You have repetitive agentic chores — daily error digest, weekly PR cleanup, monthly analytics summary.

With Aiola: `/automations` builds recurring jobs. Scope to one workspace or all of them. Mention files, agents, tasks, logs, feedback, workspaces, GitHub issues, and PRs in the prompt. Live updates while running. The calendar shows every scheduled run alongside scheduled tasks.

---

## Per-project knowledge base for agents

Agents do better with context. Repeating that context every conversation is friction.

With Aiola: every workspace has `/info` — an editable project profile (app name, email, URL, goal, audience, brand voice, values, GTM), `brief.md`, and `rules.md`. The agents read from these. One-click "Analyze project" populates them by reading the code.

---

## MCP servers managed per workspace

Different projects need different tool integrations.

With Aiola: `/settings/mcp` installs, enables, and disables MCP servers per workspace. Tool connectivity is standardized without you maintaining a config file by hand for every repo.

---

## Portfolio analytics in one app

You ship multiple products. Comparing growth across them by hand — flipping between dashboards — is slow.

With Aiola: per-project analytics live in `/analytics`, and `/central/analytics` rolls them up. Stats, trends, geography, breakdowns, referrers, funnels, journeys, heatmaps, goals, realtime visitors. Currency conversion and segment filters work across the whole portfolio. Aiola's pricing scales with the analytics event volume you actually use (100k / 500k / 1M / 5M tiers).

---

## Plan, queue, and ship from one app

You plan in Notion, queue work in Linear, and run prompts in a terminal — every round-trip wastes time.

With Aiola: write the plan in `/plan` (nested blocks, rich formatting), break it into tasks on `/tasks`, run agents from the dashboard, and ship via the auto-PR pipeline. No round-trips.

---

## Agency / freelance project isolation

You have several client codebases. Mixing context — or letting an agent touch the wrong project — is a real risk.

With Aiola: each workspace is fully isolated. Threads, tasks, plans, knowledge, and settings stay scoped to their workspace. Central views stay read-only aggregations.

---

## Keeping Claude Code and Codex side-by-side

Some projects work better with Claude. Others work better with Codex. Switching CLIs and config every time is fragile.

With Aiola: install the Claude Code SDK, the Codex SDK, or both. The model picker hides providers that aren't installed. Pick a default and override per thread. Codex's model list is hydrated at runtime so it doesn't go stale.

---

## Env-file safety check across many repos

You're never sure which repos are leaking `.env` files.

With Aiola: `/settings/environment` finds exposed `.env` files, lets you compare and edit them, and adds missing files to `.gitignore` with one click — repeat per workspace.

---

## Calendar and terminals across workspaces

You forget when scheduled work runs and lose track of which terminal session belongs to which project.

With Aiola: `/calendar` and `/central/calendar` show scheduled tasks and recurring automations on one timeline. `/terminals` and `/central/terminals` give you a thread-linked terminal canvas with split and canvas modes — every command stays tied to the right workspace.

---

## Links
- Website: [aiola.app](https://aiola.app)
- Download: [aiola.app/download](https://aiola.app/download)
- Pricing: [aiola.app/pricing](https://aiola.app/pricing)
- Docs: [docs.aiola.app](https://docs.aiola.app)
