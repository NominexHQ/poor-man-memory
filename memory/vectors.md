# Vectors

Semantic similarities, concept clusters, and embedding provenance.
The soft companion to graph.md — implicit weighted relationships rather than explicit typed edges.
Similarities and clusters are living documents. Embedding registry is append-only.

Use formats from references/vector-syntax.md.

## Similarities

[[graph.md]] ↔ [[vectors.md]] | score: 0.85 | basis: both capture relationships between concepts, different modalities — graph is explicit typed edges, vectors is weighted similarities
[[last.md]] ↔ [[progress.md]] | score: 0.65 | basis: both track recent state, but last.md is a high-fidelity window and progress.md is structured milestones
[[decisions.md]] ↔ [[standinginstructions.md]] | score: 0.58 | basis: both record committed positions, but decisions are about choices made and instructions are about behaviour mandated
[[SKILL.md]] ↔ [[processes.md]] | score: 0.55 | basis: both describe how operations are performed, but SKILL.md is executable dispatch logic and processes.md is human-readable documentation
[[Agent Dispatch]] ↔ [[Subprocess]] | score: 0.88 | basis: agent dispatch IS subprocess execution — nearly identical concepts in this context
[[config.md]] ↔ [[preferences.md]] | score: 0.62 | basis: both store user-facing settings, but config.md is operational control (cadence, windows, active files) and preferences.md is style/workflow preferences
[[summaries.md]] ↔ [[timeline.md]] | score: 0.80 | basis: same temporal data at different compression levels — fine-grained events vs narrative rollups
[[preferences.md]] ↔ [[voices.md]] | score: 0.70 | basis: both about user identity — preferences captures style/workflow, voices captures communication patterns and reasoning lenses
[[Tier-based Dispatch]] ↔ [[SKILL.md]] | score: 0.76 | basis: both are operational dispatch logic — tier-based dispatch is the Phase 3 implementation pattern, SKILL.md documents the higher-level skill semantics
[[Single Maintain]] ↔ [[Tiered Maintain]] | score: 0.74 | basis: both are Maintain Strategy modes in v1.4.0 — single is default (minimal overhead), tiered is opt-in (faster execution), represent different optimization targets
[[Bootstrap Check Cache]] ↔ [[Pre-check Agent Removal]] | score: 0.68 | basis: both v1.4.0 overhead reductions — cache skips file reads, pre-check moves detection to main context; both eliminate agent dispatch overhead at different phases
[[Token Economy]] ↔ [[Maintain Strategy]] | score: 0.72 | basis: both relate to cost: Token Economy documents per-save costs, Maintain Strategy is user-configurable lever to control token spend
[[Batch Hydration]] ↔ [[Concurrent Pre-check]] | score: 0.65 | basis: both consolidate file operations — batch hydration reads populated files once for multiple targets, concurrent pre-check replaces sequential template checks with single agent read

## Clusters

Cluster: recent-context → [[[last.md]], [[progress.md]], [[timeline.md]]] | theme: files that track temporal state and recency
Cluster: append-only → [[[decisions.md]], [[timeline.md]], [[standinginstructions.md]], [[graph.md]]] | theme: files with immutable history — never delete entries
Cluster: identity → [[[preferences.md]], [[voices.md]], [[assets.md]], [[memory.md]]] | theme: files that define who/what this project is, how the user communicates, and how to work with them
Cluster: semantic-layer → [[[graph.md]], [[vectors.md]]] | theme: structural and semantic relationships between concepts — explicit edges and implicit similarities
Cluster: self-referential → [[[SKILL.md]], [[memory.md]], [[processes.md]]] | theme: the poor-man-memory skill is its own project — these files describe and govern themselves
Cluster: temporal-memory → [[[timeline.md]], [[summaries.md]], [[last.md]]] | theme: three tiers of temporal resolution — fine-grained events, compressed rollups, recent window
Cluster: operational → [[[config.md]], [[BOOTSTRAP.md]], [[standinginstructions.md]]] | theme: system behaviour controls — configuration, initialization, persistent rules
Cluster: concurrency → [[[Tier-based Dispatch]], [[Concurrent Pre-check]], [[Tier 1+2 Agents]], [[Tier 3 Agent]]] | theme: Phase 3 Maintain parallelism patterns — dispatch strategy, pre-checks, tiered execution
Cluster: overhead-reduction → [[[Bootstrap Check Cache]], [[Pre-check Agent Removal]], [[Batch Hydration]], [[Maintain Strategy]]] | theme: v1.4.0 optimizations reducing token/message cost — cache logic, agent elimination, I/O consolidation, configurable strategy

## Embedding Registry

| Entity | Model | Dimensions | Location | Date | Notes |
|---|---|---|---|---|---|
| | | | | | |
