# Last Session

The last few significant actions in detail.
Always replaced — this is a window, not a log.
<!-- Entry format: **[Date]** — [Action] [namespace:name?] -->
<!-- attribution: [user:name], [agent:name], or [system:process] — who originated this. Optional. -->

**2026-03-18** — v1.4.0 Token/Message Overhead Reduction shipped: (1) Bootstrap Check cache via `bootstrap_wired` flag eliminates CLAUDE.md read on every Bootstrap Check once wired. (2) Pre-check agent removed — template-only detection moved to main context Read tool calls, counts content lines per file, saves 1 agent per /pmm-save. (3) Batch hydration in Phase 5: single-file mode (1 target) vs batch mode (2+ targets), batch dispatches ONE agent reading all populated files once and writing all templates. (4) Configurable maintain strategy: `single` (default, 1 agent for all files) vs `tiered` (3-agent tier dispatch, opt-in). Files updated: SKILL.md, pmm-save/SKILL.md, pmm-hydrate/SKILL.md, pmm-settings/SKILL.md, templates, config.md, version 1.4.0. [user:raffi]
**2026-03-18** — PR #28 opened (feat/v1.4.0-token-reduction) with review comment from raffi-ismail approving core logic; bootstrap cache sound, pre-check correct tradeoff, batch hydration handles templates gracefully, single maintain right for audience, follow-up noted for v1.5.0 (Phase 2 lazy session-start). PR #28 merged by raffi-ismail to main (6c65e96), first run of new single-agent dispatch path confirms working. [system:process]
