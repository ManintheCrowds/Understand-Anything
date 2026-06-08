# Harness integration map (MiscRepos)

Links from this UA fork to the **operational** harness in [ManintheCrowds/MiscRepos](https://github.com/ManintheCrowds/MiscRepos). Edit harness code in MiscRepos, not here.

## SSOT documents

| Doc | Path in MiscRepos |
|-----|------------------|
| Integration guide | `local-proto/docs/integrations/UNDERSTAND_ANYTHING_INTEGRATION.md` |
| Audit (2026-05-24) | `local-proto/docs/integrations/UNDERSTAND_ANYTHING_AUDIT_2026-05-24.md` |
| Repo boundaries | `local-proto/docs/REPO_BOUNDARY_INDEX.md` |
| Backlog | `.cursor/state/pending_tasks.md` § `PENDING_UNDERSTAND_ANYTHING` |
| Wave 17 | `local-proto/docs/WAVED_PENDING_TASKS.md` |

## Scripts (MiscRepos)

| Script | Purpose |
|--------|---------|
| `local-proto/scripts/Invoke-UnderstandAutoUpdate.ps1` | Stale graph check (exit 0/1/2) |
| `local-proto/scripts/Run-UnderstandDashboard.ps1` | Code graph dashboard |
| `local-proto/scripts/Run-UnderstandDashboard-Wiki-StreamDeck.cmd` | Wiki graph dashboard |
| `local-proto/scripts/ua-wiki-*.py` | Wiki graph pipeline helpers |

## Graph artifacts (committed in MiscRepos)

| Graph | Path | Policy |
|-------|------|--------|
| Code | `local-proto/.understand-anything/knowledge-graph.json` | Committed (UA-6 Ben onboarding) |
| Wiki | `local-proto/Arc_Forge/ObsidianVault/LLM-Wiki/.understand-anything/knowledge-graph.json` | Option A — graph only |
| Local scratch | `meta.json`, `fingerprints.json` | **Never commit** |

## Plugin install (this repo)

```
%USERPROFILE%\.understand-anything\repo\understand-anything-plugin
```

Auto-update hook prompt: `understand-anything-plugin/hooks/auto-update-prompt.md`

## Collaborator onboarding (Ben)

- Fast track: `local-proto/docs/collaboration/ben-eilers-fast-track.md`
- Tier 2 checklist: `local-proto/docs/collaboration/tier2-fast-track-provision-checklist.md`
- **UA-7** blocked on **BEN-004** [MEATSPACE]

## Verification

```powershell
cd C:\Users\Dell\Documents\GitHub\MiscRepos
.\local-proto\scripts\Invoke-UnderstandAutoUpdate.ps1   # expect 0 or 2, not 1
Test-Path .\local-proto\docs\integrations\UNDERSTAND_ANYTHING_INTEGRATION.md
```

Reconciled on `main`: 2026-06-08 (`feat/ua-reconcile-main` → PR #21).
