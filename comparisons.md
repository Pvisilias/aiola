# Aiola vs Other Tools

How Aiola — the local agentic desktop app for Claude Code, Codex, and Cursor — compares to the tools people often use alongside or instead of it.

> Aiola requires the **Claude Code SDK**, the **Codex SDK**, and/or **Cursor (`cursor-agent`)** to be installed locally. It does not bundle an LLM. The model picker hides providers that aren't installed.

---

## Aiola vs Claude Code (CLI)

| | Aiola | Claude Code CLI |
|---|---|---|
| Type | Local agentic desktop app | CLI-first agentic coding tool |
| Provider stack | Claude Code SDK + Codex SDK + Cursor side-by-side | Claude Code SDK only |
| Project model | Workspaces + central cross-workspace command center | Single working directory per session |
| Task system | Board with state machine and auto-PR pipeline | None |
| GitHub PR review | Built-in AI review and AI fix flows | Manual via prompts |
| App-log triage | Live grouping with AI analyze and AI fix | None |
| Feedback triage | Capture + customizable fields | None |
| Automations | Scheduled agentic jobs across workspaces | None |
| MCP server manager | Yes — per workspace | Per-config-file |
| Knowledge base | `/info` profile + `brief.md` + `rules.md` per workspace | `CLAUDE.md` per repo |
| Analytics | Per-project + portfolio-level | None |
| Calendar | Scheduled tasks and automations | None |
| Runs locally | Yes (Electron) | Yes (CLI) |

**Summary:** Claude Code is the agentic coding runtime. Aiola is the agentic desktop app that wraps the Claude Code SDK (and Codex SDK), turns its output into tracked tasks and pushed PRs, and surfaces every signal — errors, feedback, PRs, analytics — in one command center.

---

## Aiola vs Codex (CLI)

| | Aiola | Codex CLI |
|---|---|---|
| Type | Local agentic desktop app | CLI-first agentic coding tool |
| Provider stack | Codex SDK + Claude Code SDK + Cursor side-by-side | Codex SDK only |
| Multi-project | Workspaces + central views | Single working directory per session |
| Auto-PR pipeline | Yes — worktree commit, push, `gh pr create`, recovery sweep | None |
| AI PR review and fix flows | Yes | None |
| MCP server management | Per workspace | Per-config-file |
| Knowledge base per project | Yes | Limited |

**Summary:** Codex is one provider. Aiola runs the Codex SDK, Claude Code SDK, and Cursor (`cursor-agent`) side-by-side in a local agentic desktop app, and adds the task system, PR pipeline, log/feedback triage, automations, and analytics on top.

---

## Aiola vs Cursor

> Note: Cursor is also a **supported provider** inside Aiola via `cursor-agent`. This comparison is about Cursor *the editor* — the two work well together, and Aiola can run Cursor's agent as one of its providers.

| | Aiola | Cursor |
|---|---|---|
| Type | Agentic desktop app (can run Cursor's agent as a provider) | AI-native code editor (VS Code fork) |
| Multi-project | Workspaces + central views | One project per window |
| Task system | Yes | No |
| Auto-PR pipeline | Yes | No |
| AI PR review on incoming PRs | Yes | No |
| App-log triage | Yes | No |
| Feedback / Analytics / Automations | Yes | No |
| MCP server manager | Yes | No |

**Summary:** Cursor is an excellent agentic editor for inline coding. Aiola is not an editor — it is the agentic operations layer for everything that happens *around* the code: tasks, PRs, errors, feedback, automations, analytics. They work well together.

---

## Aiola vs VSCode

| | Aiola | VSCode |
|---|---|---|
| Type | Agentic desktop app | General-purpose editor |
| Built-in agentic stack | Yes — Claude Code SDK + Codex SDK + Cursor | Via extensions only |
| Multi-project command center | Yes | No |
| Task system + auto-PR pipeline | Yes | No |
| App-log / feedback / analytics triage | Yes | No |
| MCP server manager | Yes | No |

**Summary:** VSCode is a free extensible editor. Aiola is a dedicated local agentic workspace. They serve different purposes and pair well.

---

## Aiola vs Linear / Jira (project trackers)

| | Aiola | Linear / Jira |
|---|---|---|
| Agentic execution | Yes — tasks run via Claude Code SDK, Codex SDK, or Cursor | No — tracker only |
| Auto-PR creation from tasks | Yes | No |
| AI PR review | Yes | No |
| App-log triage | Yes | No |
| Feedback triage | Yes | No |
| Cross-workspace command center | Yes | Yes (cross-team) |

**Summary:** Linear and Jira track work; Aiola also *executes* work. A task in Aiola can move from todo to a pushed PR by an agent without leaving the app.

---

## Pricing note

Aiola is priced by analytics event volume — 100k / 500k / 1M / 5M events on Pro Monthly ($24, $49, $89, $249) and Pro Yearly (10× monthly, 2 months free). 7-day free trial on the 100k tier. Teams plan coming soon. There is no free plan. See [aiola.app/pricing](https://aiola.app/pricing).

---

## Links
- Website: [aiola.app](https://aiola.app)
- Full comparison page: [Aiola vs Claude Code](https://aiola.app/comparisons/claude)
