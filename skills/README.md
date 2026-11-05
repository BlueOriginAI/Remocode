# Remocode Agent Skills

Install the public Remocode agent skills with the `skills` CLI:

```bash
npx skills@1.7.2 add https://github.com/BlueOriginAI/Remocode/tree/skills \
  --skill remocode-cli \
  --skill computer-use \
  --global
```

`remocode-cli` is the guide for operating projects, sessions, terminals, browser tabs, automations, and Computer Use through the Remocode CLI.

Each skill directory contains a `SKILL.md` discovery stub. The stub loads the version-matched full guide from the Remocode executable running on the current host.
