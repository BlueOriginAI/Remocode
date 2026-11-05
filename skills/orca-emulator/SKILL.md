---
name: orca-emulator
description: >-
  iOS Simulator control from inside Orca, with the live device view in Orca's
  emulator pane. Use when driving a booted Apple Simulator on macOS: taps,
  gestures, typing, hardware buttons, rotation, and the accessibility tree, or
  when an iOS change needs simulator evidence. For an Android device or emulator
  use the Android emulator skill; build and install the app with xcodebuild or
  simctl first.
license: Apache-2.0
---

# Orca Emulator

This discovery stub loads the version-matched guide from the Orca executable used for this session.

Prefer Orca over raw `serve-sim` or direct `simctl` for simulator control inside Orca; it
handles device scoping, helper lifecycle, and worktree context.

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

## Load the version-matched guide before running Orca commands

```text
ORCA skills get orca-emulator
```

Prefer `--json`. Use the selected executable's `--help` for commands or flags the guide does
not cover. If a command reports that Remocode is not running, start it with `REM open --json`
and retry. If it fails with `runtime_access_denied`, your sandbox blocked the connection:
re-run it with escalated permissions, and do not run `REM open` or restart Remocode. If
`skills get` is unknown, explain that updating Remocode restores the guide; use `--help` for
read-only discovery and do not guess unsupported commands.
