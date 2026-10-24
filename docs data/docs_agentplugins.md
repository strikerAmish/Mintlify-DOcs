# PiyAPI - Agent Plugins Documentation

## 1. Top Configuration
* **Breadcrumb:** `Agent Plugins / Coding Agents / Claude Code`
* **Action:** `[Copy page]`

## 2. Left Sidebar Navigation
* **CODING AGENTS**
  * Claude Code
  * Cursor
  * Codex
  * OpenCode
  * Gemini CLI
  * Cline
  * Kimi Code
  * Antigravity
* **AGENT HARNESSES**
  * OpenClaw
  * Hermes Agent
  * Pi Agent
  * DeepSeek Harness
* **PLUGIN RESOURCES**
  * Plugin Overview
  * Installation
  * Configuration
  * Commands
  * Memory
  * Troubleshooting

## 3. Right Sidebar Navigation ("On this page")
* Prerequisites
* Quick start
* Managing the plugin
* What you can do
* Commands
* Search tool
* Sidekick agent
* How it works
* Memory scoping
* Search scope
* Settings
* Upgrading
* Troubleshooting
* Telemetry

---

# Claude Code

Persistent cross-session memory for Claude Code.

Connect the PiyAPI plugin to your Claude Code environment to persist relevant bitemporal context across sessions and retrieve it on demand. 

> **Current plugin version:** `v1.2.0`

## Prerequisites

1. **PiyAPI API key**: Required for authentication. Export this as `PIYAPI_API_KEY`.
2. **Supported agent environment**: The Claude Code CLI must be installed and accessible on your `$PATH`.
3. **Runtime dependencies**: Node.js 18+ and the `piyapi-cli`.

## Quick start

To install the plugin, bind it to your Claude Code session, and confirm the connection:

```bash
export PIYAPI_API_KEY="sk_live_your-api-key"
piyapi plugin install claude-code
piyapi plugin status
```

**Setup Flow:** `1. Install` → `2. Configure` → `3. Restart agent` → `4. Verify`

## Managing the plugin

Use the CLI to manage the plugin lifecycle:

```bash
piyapi plugin install claude-code
piyapi plugin update claude-code
piyapi plugin uninstall claude-code
piyapi plugin status
```

## What you can do

* **Automatic memory**: Captures relevant context from coding sessions in the background.
* **Commands**: Exposes explicit CLI commands for searching, checking status, forgetting, and pausing/resuming memory capture.
* **Search tool**: Query previous sessions and retrieve relevant context on demand via the UnifiedScorer.
* **Sidekick agent**: Spin up an isolated investigation or implementation workflow while preserving the primary working context.

## Commands

| COMMAND | DESCRIPTION |
|:---|:---|
| `/memory:search` | Search memories from earlier sessions. |
| `/memory:status` | Check current memory and configuration state. |
| `/memory:forget` | Delete or forget selected memories. |
| `/memory:pause` | Pause automatic memory capture. |
| `/memory:resume` | Resume automatic memory capture. |
| `/memory:remember` | Explicitly force-capture a specific input. |

## Search tool

Use the search tool to query prior sessions and retrieve context bounded by relevance and scope.

```javascript
memory.search('authentication flow', { scope: "project" })
```

```json
{
  "results": [
    {
      "memory_id": "8a1b2c3d-4e5f-6a7b-8c9d-0e1f2a3b4c5d",
      "content": "Authentication uses JWT tokens for the main API...",
      "score": 0.91
    }
  ]
}
```

## Sidekick agent

The sidekick agent handles isolated investigation or implementation work in a separate context, then returns its findings to the main agent without polluting the primary working memory.

*(Workflow: `Main Agent` → `Sidekick` → `Investigation` → `Result` → `Main Agent`)*

## How it works

1. **Capture**: Records relevant activity from the agent session.
2. **Flush**: Sends captured context to the PiyAPI engine after meaningful interaction boundaries.
3. **Extract**: Parses useful project context, architectural decisions, constraints, and preferences.
4. **Recall**: Retrieves relevant bitemporal memories during subsequent sessions.

*(Architecture: `Agent Session` → `Capture` → `PiyAPI Memory` → `Extract` → `Store` → `Recall` → `Next Session`)*

## Memory scoping

Memory is strictly scoped between shared project context and personal context. Relevant overlap is surfaced dynamically during retrieval via Context Assembly.

*(Data Flow: `Personal Memory` + `Project Memory` + `Session Context` → `Context Assembly (Retrieve, Filter, Combine)` → `Relevant Context`)*

## Search scope

| SCOPE | RETURNED CONTEXT |
|:---|:---|
| `repo` | Project-wide memory. |
| `dir` | Directory-specific memory. |
| `user` | Personal user memory. |
| `session` | Current task memory. |

*Example: Setting scope to `dir` restricts retrieval strictly to memories captured within the current working directory.*

## Settings

Configure the plugin via environment variables:

| SETTING | DEFAULT | DESCRIPTION |
|:---|:---|:---|
| `api_key` | `none` | Authenticates requests to the PiyAPI engine. |
| `user_id` | `none` | Identifies the memory owner. |
| `top_k` | `5` | Maximum number of memories returned per search. |
| `max_content_chars` | `4000` | Maximum characters captured per memory block. |
| `search_scope` | `repo` | Default scope used for retrieval. |
| `telemetry` | `true` | Enables anonymous usage telemetry. |

```bash
export PIYAPI_API_KEY="..."
export PIYAPI_USER_ID="..."
export PIYAPI_SEARCH_SCOPE="repo"
```

## Upgrading

Before upgrading to a new plugin version, verify the following checklist to avoid breaking your existing configuration or memory behavior:

* [x] Review changed configuration keys
* [x] Check command deprecations/changes
* [x] Verify memory compatibility
* [x] Re-run plugin setup
* [x] Confirm agent compatibility

## Troubleshooting

| PROBLEM | RESOLUTION |
|:---|:---|
| **Missing API key** | Export the `PIYAPI_API_KEY` and restart the plugin. |
| **Unauthorized** | Verify the API key and account permissions via `GET /api/v1/verify`. |
| **No memory after session** | Ensure memory capture is enabled and the plugin successfully flushed the session. |
| **Plugin won't start** | Verify your agent version is supported and the plugin installation succeeded. |
| **Search returns nothing** | Check the active search scope and verify memories exist within that boundary. |

## Telemetry

**What may be collected:**
* Event type
* Plugin version
* Runtime information
* Basic performance and error metadata

*Document the exact telemetry behavior here before production release.*

```bash
export PIYAPI_TELEMETRY=false
```

---

## Related agent plugins

* **PiyAPI MCP**: Connect PiyAPI memory through MCP-compatible workflows. `→`
* **Codex Integration**: Add persistent context to supported Codex workflows. `→`
* **Cursor**: Persistent memory for Cursor. `→`
* **OpenCode**: Context-aware OpenCode workflows. `→`
* **Gemini CLI**: Memory for Gemini CLI agents. `→`
* **Cline**: Persistent context for Cline. `→`

---

> **Building with PiyAPI?**
> Explore the open-source stack, contribute integrations, or browse the developer community.
> `[Join the community →]`

---

**Footer Actions:** `[Suggest edits]` | `[Raise issue]`

**Footer Navigation:** `← PREVIOUS: Agent Plugins Overview` | `NEXT: Cursor →`
