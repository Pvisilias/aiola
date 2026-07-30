# Aiola Use Cases

Real-world ways people use Aiola — the local agentic desktop app for Claude Code, Codex, Cursor, Grok CLI, and OpenCode.

> Aiola requires at least one supported provider to be installed locally: **Claude Code SDK / CLI**, **Codex SDK / CLI**, **Cursor (`cursor-agent`)**, **Grok CLI (`grok`)**, or **OpenCode (`opencode`)**. It does not bundle an LLM.

---

## Running agentic workflows across many repos

You have eight projects — a SaaS, two client apps, three side projects, and two abandoned-but-still-shipping experiments. The Claude Code, Codex, Cursor, Grok CLI, or OpenCode CLIs need a separate session per repo, and you constantly lose context.

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

You ship multiple products. Comparing growth across them is slow, and ordinary traffic totals do not tell you whether AI systems are citing, indexing, or training on your content.

With Aiola: the analytics dashboard splits into Traffic and AI tabs. Per-project analytics live in `/analytics`, and `/central/analytics` rolls them up with stats, trends, geography, breakdowns, referrers, funnels, journeys, heatmaps, goals, realtime visitors, currency conversion, and segment filters. The AI layer recognizes 70 AI and search crawlers by vendor and splits bot traffic by purpose: AI answers, indexing, training, and other fetchers. It tracks human AI Referrals separately, computes a deterministic 0–100 AI Visibility Score from crawl coverage, crawler breadth, referral volume, assistant breadth, and discovery-file health, and surfaces broken pages, robots.txt / llms.txt / sitemap health, page coverage, and popular pages no AI crawler has touched.

---

## Knowing whether AI recommends your product

You cannot tell from search rankings or crawler traffic whether assistants recommend your product to buyers.

With Aiola: the deterministic 0–100 AI Visibility Score measures crawl coverage of popular pages, AI-crawler breadth, AI-answer referral volume, assistant breadth, and discovery-file health. The prebuilt AI visibility check automation runs buyer-style questions on whichever supported CLI the automation uses, through your existing provider subscription with no extra API cost, and anchors the result on the computed score. Agents can retrieve the same score through the `get_analytics_overview` MCP tool.

---

## Finding pages AI crawlers ask for that do not exist yet

AI and search crawlers repeatedly request URLs that return 404, but ordinary crawl totals hide the content demand behind those failures.

With Aiola: broken-page tracking lists those requested URLs separately so they never inflate crawl totals. Repeated requests become a content-roadmap signal: the AI already thinks the page exists, so you can decide whether to build it.

---

## Telling AI citations apart from AI training

A crawler hit can mean an assistant is citing your content in a live answer, a search engine is indexing it, or a model builder is collecting training data. Those events do not have the same commercial meaning.

With Aiola: bot traffic is classified by purpose. AI answers covers ChatGPT-User, Claude-User, and Perplexity-User fetching a page live for someone's question; Indexing covers search crawlers; Training covers model-training crawlers; Other covers ad and link-preview fetchers. AI Referrals separately count human visitors who clicked through from an AI answer, so live citation, future discoverability, training access, and attributable visits are not lumped together.

---

## Plan, take notes, track todos, queue, and ship from one app

You plan in Notion, jot notes in Apple Notes, keep todos somewhere else, queue work in Linear, and run prompts in a terminal — every round-trip wastes time.

With Aiola: use `/notebook` to write the plan (nested blocks, rich formatting), keep searchable Notes beside it, and track per-workspace Todos — all three are modes of one surface. #note-mention any note into a chat turn, capture stray thoughts in the Quick Note scratchpad (⌘⇧J), break the plan into tasks on `/tasks`, run agents from the dashboard, and ship via the auto-PR pipeline. No round-trips.

---

## Agency / freelance project isolation

You have several client codebases. Mixing context — or letting an agent touch the wrong project — is a real risk.

With Aiola: each workspace is fully isolated. Threads, tasks, plans, knowledge, and settings stay scoped to their workspace. Central views stay read-only aggregations.

---

## Keeping five agent CLIs side-by-side

Some projects work better with Claude Code, Codex, Cursor, Grok CLI, or OpenCode. Switching CLIs and config every time is fragile.

With Aiola: install the Claude Code SDK / CLI, Codex SDK / CLI, Cursor (`cursor-agent`), Grok CLI (`grok`), OpenCode (`opencode`), or any combination. The model picker hides providers that aren't installed. Pick a default and override per thread. Claude Opus 5 is available with 1M-token context by default, selectable 200K context, Fast mode, and reasoning up to Extra High. Codex's model list is hydrated at runtime from the SDK so it does not go stale. Cursor runs with Git cloning support. Grok models, currently including grok-4.5, and OpenCode's configured provider/model pairs are discovered live from the installed CLI.

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
