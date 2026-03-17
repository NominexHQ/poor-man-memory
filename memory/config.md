# PMM Configuration

Settings that control how Poor Man's Memory behaves.
Run `/pmm-settings` at any time to change these.

## Save Cadence

<!-- How often memory is updated -->
- Mode: every-milestone
<!-- Options: every-milestone | every-N-messages (specify N) | on-request-only -->
<!-- Note: For fine-grained control, use /loop to run a save prompt on a recurring interval -->

## Commit Behaviour

<!-- When changes are committed to git -->
- Mode: auto-commit
<!-- Options: auto-commit | session-end | manual -->

## Sliding Window Size

<!-- Max entries in windowed files (timeline, summaries) before trimming -->
- Timeline max: 50
- Summaries max: 10
<!-- Presets: light (30/5) | moderate (50/10) | heavy (100/20) | unlimited -->

## Verbosity

<!-- How memory updates are communicated -->
- Mode: silent
<!-- Options: silent | summary | verbose -->

## Maintain Agent Model

<!-- Which model handles memory updates (maintain phase) -->
- Model: haiku
<!-- Options: haiku (default, cheapest) | sonnet (balanced) | opus (most capable) -->
<!-- Session-start and recall agents always use the parent model -->

## Active Files

<!-- Which memory files are active. Deactivated files are not created or loaded. -->
<!-- config.md and BOOTSTRAP.md are always active. -->
- memory.md: active
- assets.md: active
- decisions.md: active
- processes.md: active
- preferences.md: active
- voices.md: active
- lessons.md: active
- timeline.md: active
- summaries.md: active
- progress.md: active
- last.md: active
- graph.md: active
- vectors.md: active
- taxonomies.md: active
- standinginstructions.md: active
