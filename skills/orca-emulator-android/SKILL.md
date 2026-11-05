---
name: orca-emulator-android
description: >-
  Android device and emulator control from inside Orca over adb, with the live
  device view in Orca's emulator pane. Use when driving an adb-connected emulator
  or phone on Windows, Linux, or macOS: booting AVDs, taps, swipes, typing,
  hardware buttons, rotation, app install and launch, runtime permissions, the
  accessibility tree, and logcat. For an iOS simulator use the iOS emulator
  skill; build the APK with Gradle first.
license: Apache-2.0
---

# Orca Emulator (Android)

This discovery stub loads the version-matched guide from the Orca executable used for this session.

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
ORCA skills get orca-emulator-android
```

Prefer `--json`. Use the selected executable's `--help` for commands or flags the guide does
not cover. If a command reports that Remocode is not running, start it with `REM open --json`
and retry. If it fails with `runtime_access_denied`, your sandbox blocked the connection:
re-run it with escalated permissions, and do not run `REM open` or restart Remocode. If
`skills get` is unknown, explain that updating Remocode restores the guide; use `--help` for
read-only discovery and do not guess unsupported commands.
