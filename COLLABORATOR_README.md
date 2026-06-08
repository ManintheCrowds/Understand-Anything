# Understand-Anything — Collaborator Guide (ManintheCrowds fork)

This fork is a **distribution mirror** for collaborators onboarding to the MiscRepos harness. It is **not** an upstream contribution fork — we do not open PRs to [Lum1104/Understand-Anything](https://github.com/Lum1104/Understand-Anything).

## What this repo is

- **Upstream tool:** [Lum1104/Understand-Anything](https://github.com/Lum1104/Understand-Anything) — desk-first code + wiki intelligence (knowledge graphs, dashboard, `/understand` skills).
- **This fork:** Annotated mirror with harness integration pointers for Ben and other collaborators.
- **Operational SSOT:** [ManintheCrowds/MiscRepos](https://github.com/ManintheCrowds/MiscRepos) — scripts, graphs, auto-update, backlog.

## Install (Windows)

1. Clone **this fork** (or use the operator vendor path):

   ```powershell
   git clone https://github.com/ManintheCrowds/Understand-Anything.git "$env:USERPROFILE\.understand-anything\repo"
   ```

2. Clone **MiscRepos** and open a multi-root workspace (MiscRepos + `local-proto`).

3. Build the plugin (first run):

   ```powershell
   cd "$env:USERPROFILE\.understand-anything\repo\understand-anything-plugin"
   pnpm install
   pnpm --filter @understand-anything/core build
   ```

4. Read harness integration: [docs/HARNESS_INTEGRATION.md](docs/HARNESS_INTEGRATION.md) and MiscRepos [UNDERSTAND_ANYTHING_INTEGRATION.md](https://github.com/ManintheCrowds/MiscRepos/blob/main/local-proto/docs/integrations/UNDERSTAND_ANYTHING_INTEGRATION.md).

## Git remotes (operator)

| Remote | URL | Use |
|--------|-----|-----|
| `upstream` | `Lum1104/Understand-Anything` | Pull upstream releases only |
| `origin` | `ManintheCrowds/Understand-Anything` | Push collaborator docs only |

**Do not push to `upstream`.**

## Upstream pin

```
upstream_tracking: Lum1104/Understand-Anything @ 5c1e35f
```

Refresh after `git pull upstream main` and update this line.

## jcodemunch vs UA

| Tool | Who | When |
|------|-----|------|
| **jcodemunch** | Agents | Per-query symbol retrieval (MCP) |
| **Understand-Anything** | Humans / collaborators | Batch graphs, dashboard, onboarding tours |

Agents use jcodemunch; humans use UA for “how does this fit together?”
