# Last Session

The last few significant actions in detail.
Always replaced — this is a window, not a log.
<!-- Entry format: **[Date]** — [Action] [namespace:name?] -->
<!-- attribution: [user:name], [agent:name], or [system:process] — who originated this. Optional. -->

**2026-03-18** — Bootstrap Check reminder system implemented: added reusable utility to SKILL.md that detects missing @memory/BOOTSTRAP.md in CLAUDE.md and prompts user with three options (fix now with auto-commit, remind next time, or suppress permanently) [agent:leith]
**2026-03-18** — Bootstrap Check integrated across all 6 PMM surfaces (init memory, /pmm-save, /pmm-hydrate, /pmm-update, /pmm-status, /pmm-query): ensures users are aware of critical wiring step for memory auto-load [agent:leith]
**2026-03-18** — BOOTSTRAP.md self-reference removed from live file and templates.md template; bootstrap_reminder config flag added (on/off control) [agent:leith]
**2026-03-18** — README.md "Adding to an Existing Project" step 3 updated with note about wiring @memory/BOOTSTRAP.md into CLAUDE.md [agent:leith]
**2026-03-18** — PR #20 created, reviewed by raffi-ismail, and merged to main: v1.3.1 release with Bootstrap Check implementation [user:raffi]
**2026-03-18** — v1.3.1 GitHub release published: https://github.com/NominexHQ/poor-man-memory/releases/tag/v1.3.1 [system:process]
