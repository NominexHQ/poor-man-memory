# Decisions

Committed decisions. Append-only — never delete or modify past entries.
Each entry is ratified and should be treated as ground truth unless explicitly reversed.

## Format

**[Date] — [Decision]**
Context: why this was decided
Ratified by: [user / consensus / default]

---

**2026-03-17 — Phase 5 "Hydrate" for non-greenfield installs**
Context: When PMM is installed in an existing project (not a fresh clone), memory files need to be seeded from existing context. Phase 5 handles this — new files are populated from whatever memory already exists.
Ratified by: user

**2026-03-16 — User voice captured in preferences.md, not a separate file**
Context: Considered a dedicated user-voice file but decided preferences.md is the right home. Keeps identity info co-located with other user preferences.
Ratified by: user

**2026-03-16 — Maintain agent defaults to haiku model**
Context: Maintain phase work is mechanical — read file, append entry, replace section. Doesn't need opus-level reasoning. Haiku is ~10x cheaper. Configurable via config.md if needed.
Ratified by: user

**2026-03-16 — Sliding windows with git history as backing store**
Context: Timeline and summaries use fixed-size sliding windows (configurable in config.md). When entries are trimmed, they're not lost — git history preserves the full record. Bounded memory with full audit trail.
Ratified by: user

**2026-03-16 — Two-tier temporal memory: timeline (fine-grained) + summaries (compressed rollups)**
Context: timeline.md captures individual events. summaries.md compresses batches into narrative rollups. Two resolutions of the same temporal data — high-fidelity and compressed.
Ratified by: user

**2026-03-16 — No transcript.md — last.md covers recent context**
Context: Considered adding transcript.md for conversation history. User said "bin it" — last.md already serves as the recent context window. No need for a second file covering similar ground.
Ratified by: user

**2026-03-16 — Repository structured as clone-and-go, not drop-in skill files**
Context: poor-man-memory-repo/ is a complete project directory with .claude/, CLAUDE.md, settings.json, and README. Users clone and start using — no manual file shuffling required.
Ratified by: user

**2026-03-16 — config.md controls all phase behaviour (not preferences.md)**
Context: preferences.md stores user style/workflow preferences. config.md is the operational control file — save cadence, commit behaviour, window sizes, verbosity, active file list. All phases read config.md first.
Ratified by: user

**2026-03-16 — Agents edit files only, main context handles all git commits**
Context: Agent subprocesses write memory file changes but never run git commands. The main context is responsible for staging, committing, and pushing. This avoids permission issues and keeps git history clean.
Ratified by: user

**2026-03-16 — vectors.md added as semantic companion to graph.md**
Context: graph.md captures explicit typed edges but can't represent implicit weighted relationships. vectors.md fills that gap — semantic similarities with scores, concept clusters, and embedding provenance tracking.
Ratified by: user

**2026-03-16 — Use agents (subprocesses) for all memory operations**
Context: Main context window was getting polluted with file I/O and git ops during memory phases. Dispatching agents keeps the main window clean — agents do the heavy lifting and return concise results.
Ratified by: user
