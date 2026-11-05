---
name: remocode-cli
description: >-
  Operate Remocode projects, sessions, terminals, browser tabs, automations,
  and Computer Use through the `remocode` CLI. Use when the user asks for
  Remocode state, wants an agent to continue work in a Remocode workspace,
  needs terminal or browser control, or asks to hand work to another session.
---

# Remocode CLI

This discovery stub loads the version-matched guide from the Remocode executable used for this session.

## Resolve the CLI for this session

Choose the executable once and reuse it for every later command:

- If the `REMOCODE_CLI_COMMAND` environment variable is set, use its value. Accept legacy
  `ORCA_CLI_COMMAND` when migrating an older environment.
- Otherwise, in a dev checkout whose session exposes `REMOCODE_DEV_REPO_ROOT` or
  `ORCA_DEV_REPO_ROOT`, use `remocode-dev`.
- Otherwise, use `remocode`. Use legacy `orca` only when `remocode` is unavailable.

Below, `REM` is a placeholder for the executable you resolved. Substitute it before
running anything; do not create a shell variable or run `REM` literally. This works the
same way in POSIX shells, PowerShell, and cmd.exe.

If the selected executable cannot run, report its exact error and stop.

## Load the version-matched guide before running Remocode commands

```text
REM skills get remocode-cli
```

Prefer `--json`. Use the selected executable's `--help` for commands or flags the guide does
not cover. If a command reports that Remocode is not running, start it with `REM open --json`
and retry. If it fails with `runtime_access_denied`, your sandbox blocked the connection:
re-run it with escalated permissions, and do not run `REM open` or restart Remocode. If
`skills get` is unknown, explain that updating Remocode restores the guide; use `--help` for
read-only discovery and do not guess unsupported commands.
