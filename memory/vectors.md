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

## Clusters

Cluster: recent-context → [[[last.md]], [[progress.md]], [[timeline.md]]] | theme: files that track temporal state and recency
Cluster: append-only → [[[decisions.md]], [[timeline.md]], [[standinginstructions.md]], [[graph.md]]] | theme: files with immutable history — never delete entries
Cluster: identity → [[[preferences.md]], [[voices.md]], [[assets.md]], [[memory.md]]] | theme: files that define who/what this project is, how the user communicates, and how to work with them
Cluster: semantic-layer → [[[graph.md]], [[vectors.md]]] | theme: structural and semantic relationships between concepts — explicit edges and implicit similarities
Cluster: self-referential → [[[SKILL.md]], [[memory.md]], [[processes.md]]] | theme: the poor-man-memory skill is its own project — these files describe and govern themselves
Cluster: temporal-memory → [[[timeline.md]], [[summaries.md]], [[last.md]]] | theme: three tiers of temporal resolution — fine-grained events, compressed rollups, recent window
Cluster: operational → [[[config.md]], [[BOOTSTRAP.md]], [[standinginstructions.md]]] | theme: system behaviour controls — configuration, initialization, persistent rules

## Embedding Registry

| Entity | Model | Dimensions | Location | Date | Notes |
|---|---|---|---|---|---|
| | | | | | |
