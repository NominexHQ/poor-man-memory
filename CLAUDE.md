# Poor Man's Memory

This project uses a structured memory system backed by markdown files and git.

## First Run

If the `memory/` directory doesn't exist, initialise the memory system:

```
init memory
```

This will prompt you for preferences (save cadence, verbosity, active files, etc.) and scaffold the memory files.

## Commands

- `/pmm-settings` — Change memory system configuration at any time
- `update memory` — Trigger a manual memory update
- `summarise memory` — Get a summary of what's in memory

## How It Works

Memory operations run in background agents — the main context window stays clean. Git commits after every update create an immutable audit trail. See `memory/config.md` for current settings.
