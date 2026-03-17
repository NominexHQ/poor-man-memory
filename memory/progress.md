# Progress

Current state, milestones, and what's next.
Updated whenever state changes meaningfully.

## Current State

v1.0.0 released on GitHub. Repository is live at https://github.com/NominexHQ/poor-man-memory as a clone-and-go project. All 17 memory files implemented. 5 phases operational (Init, Session Start, Maintain, Recall, Hydrate). 3 skills built (poor-man-memory, pmm-settings, pmm-viz). System stable and undergoing dog-fooding.

## Completed

- Memory system initialisation (13 files, git repo, first commit)
- Added vectors.md — semantic similarities, clusters, embedding registry
- Rewrote SKILL.md to use agent-based dispatch for all four phases (init, session start, maintain, recall)
- Added config.md — operational settings controlling save cadence, commit behaviour, window sizes, verbosity, active files
- Created /pmm-settings skill — re-presents preference prompts at any time
- Rewrote Phase 1 (init) with first-run preference prompt (5 interactive questions)
- Added summaries.md — periodic rollups with sliding window, two-tier temporal memory
- Changed timeline.md to sliding window (max 50 entries per config)
- Reorganised repo as clone-and-go project (skills in .claude/skills/, settings.json, CLAUDE.md, README.md)
- Updated README with installation instructions and Nominex branding
- Decided: agents edit files only, main context handles git
- Decided: config.md controls phase behaviour, not preferences.md
- Decided: repo is clone-and-go, not drop-in skill files
- Created GitHub repo and pushed v1.0
- Commit author switched to Leith identity for public-facing commits
- v1.0.0 release published
- Configurable maintain agent model (haiku default)
- PR workflow established (PRs #1-7)
- voices.md added — tone profiles and reasoning lenses
- Phase 5 "Hydrate" added for non-greenfield installs
- Standing instructions: no attribution in docs, proactive memory saves
- User voice captured in preferences.md
- Git history rewritten to remove private emails
- /pmm-viz added — ASCII visualization
- Major memory reconstruction from recovered conversation history

## In Progress

<!-- Nothing currently in progress -->

## Blocked

<!-- Nothing currently blocked -->

## Next

- Further dog-fooding across real projects
- Community feedback on v1.0
- Potential v1.1 features
- Evaluate whether taxonomies.md needs initial population
