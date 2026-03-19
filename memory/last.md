# Last Session

The last few significant actions in detail.
Always replaced — this is a window, not a log.
<!-- Entry format: **[Date]** — [Action] [namespace:name?] -->
<!-- attribution: [user:name], [agent:name], or [system:process] — who originated this. Optional. -->

**2026-03-19** — Investigation: PreCompact hook is non-blocking in Claude Code — Exit code 2 marks the hook as "failed" but compact always proceeds. The v1.7.0 block-signal-retry design was based on a false assumption. SessionEnd hook also non-blocking — no hook mechanism in Claude Code can gate compact or session exit. Corrected documentation across: SKILL.md When-to-Update, pmm-settings Q14, memory/config.md comments, references/templates.md config template. Removed vestigial marker code (touch /tmp/pmm-compact-ready*) from pmm-save step 5b and Phase 3 post-commit. [system:process]

**2026-03-19** — New explicit save trigger: "Before ending the session" (user says goodbye, closes conversation, or signals they are done). Added to BOOTSTRAP.md, SKILL.md When-to-Update, and templates.md BOOTSTRAP template. [system:process]

**2026-03-19** — Decision ratified: PreCompact and SessionEnd hooks are non-blocking in Claude Code; compact/exit saves rely on soft instruction only (honored by Claude following BOOTSTRAP.md triggers). Session-exit added as explicit PMM save trigger. [user:raffi]

**2026-03-19** — PR #32 merged by raffi-ismail; v1.7.1 released at https://github.com/NominexHQ/poor-man-memory/releases/tag/v1.7.1 with title "v1.7.1 — correct hook blocking claims, add session-exit save trigger". [system:process]
