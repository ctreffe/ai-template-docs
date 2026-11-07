# Project-local Codex profile

## Keep enough to restore

Confirm the exact project-local `.codex/config.toml` and current Desktop mode.
Keep a short ignored `RESTRICTED_STORAGE.local.md` with the mode, any affected
defaults and a pointer to the exact original config bytes or a record of prior
absence. Use an approved ignored backup such as
`.codex/restricted-storage.original.toml`. Check that these local files are
untracked and ignored before storing private settings. Preserve existing
recovery records. If the change could prevent startup or tool access, arrange
bounded independent recovery before applying it.

## Prepare the approved change

Name the profile `<full-repository-slug>-restricted` and extend the approved
baseline. Preserve unrelated settings and the current default. Use exact
absolute paths under the selected project root and any additional approved
denies. Confirm that the effective workspace roots cover ordinary project
work. If needed, add only the exact approved project root using the profile’s
`workspace_roots` setting. Review conflicting overrides and managed rules.

New project profiles enable command networking unless the maintainer specifies
a restriction or a governing rule requires one. Keep approved network rules
when changing an existing profile. Access and transmission remain separately
authorized. Adapt this example to the selected project.

```toml
[permissions."example-repository-restricted"]
extends = ":workspace"

[permissions."example-repository-restricted".filesystem]
'D:/APPROVED-PROJECT/input/intake' = "deny"
'D:/APPROVED-PROJECT/input/restricted' = "deny"
'D:/APPROVED-PROJECT/temp/restricted' = "deny"

[permissions."example-repository-restricted".network]
enabled = true
```

## Restart before each check

1. Save the approved change and retain a fingerprint of the applied config for
   conflict-safe rollback. The maintainer fully quits and reopens Desktop,
   then selects the profile in the intended local chat if needed.
2. In a fresh ordinary tool turn, check the profile marker and the declared
   scope for the intended denies, workspace roots and network setting when
   available. Record the active scope or the specific gap in the local record.
3. On rollback, check for concurrent edits and stop for reconciliation if any
   are found. Restore the original bytes or prior absence. The maintainer
   fully restarts Desktop and restores the original mode if needed. In a fresh
   ordinary tool turn, confirm the recovered configuration and scope.

Routine scope checks use declared permissions. Required workflow checks use
the procedure below; unresolved behavior questions go to Governance for
separately scoped invented-only tests. Local command scope
does not establish isolation for other tools, devices or approved escalation.

See the [permission profile](https://learn.chatgpt.com/docs/permissions) and
[Desktop sandbox](https://learn.chatgpt.com/docs/sandboxing) documentation for
the supported settings and controls.

## Required workflows

Complete the [usability procedure](profile-usability.md) alongside the selected
profile setup. Keep missing authority or failed required operations pending.
Domain-specific credential and execution boundaries remain authoritative.

