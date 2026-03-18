# Last Session

The last few significant actions in detail.
Always replaced — this is a window, not a log.
<!-- Entry format: **[Date]** — [Action] [namespace:name?] -->
<!-- attribution: [user:name], [agent:name], or [system:process] — who originated this. Optional. -->

**2026-03-19** — v1.6.0 git tag created and pushed to GitHub; v1.6.0 GitHub release published at https://github.com/NominexHQ/poor-man-memory/releases/tag/v1.6.0 with title "v1.6.0 — context-first recall, recall_beyond_window config", marked as latest. [system:process]

**2026-03-19** — PR #30 (feat: v1.6.0 — context-first recall, recall_beyond_window config) reviewed by raffi-ismail: context-first pattern well-executed, Phase 4 and /pmm-query gates sound, beyond-window consistency correct, 'don't ask me again' persistence proper UX, safe defaults. PR merged to main. [user:raffi]

**2026-03-19** — v1.5.0 Released: Read-Only Model & Lazy Session Start — readonly_model: haiku config (default) for all read-only agents (~95% cost reduction vs Opus); session_start: lazy config (default) skips Phase 2 when bootstrap_wired: true (~33k token savings per session); Early-exit bug fix in pmm-save (always dispatch). PR #29 merged by raffi-ismail. [user:raffi] [agent:leith]
