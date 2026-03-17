# Assets

Key entities this project involves — people, tools, systems, organisations.
Updated when new entities are introduced.

## People

| Name | Role | Notes |
|---|---|---|
| Raffi (raffi-ismail) | Admin, reviewer, PMM creator | Reviews and merges PRs, admin of NominexHQ |
| Leith (leith-dev) | Public-facing identity | Creates PRs, commits use leith-dev@users.noreply.github.com |

## Tools & Systems

| Name | Purpose | Notes |
|---|---|---|
| poor-man-memory | Git-backed structured memory for Claude Code | 17 files, clone-and-go repo, v1.0 shipped |
| SKILL.md | Agent dispatch logic for memory operations | Governs init, session-start, maintain, recall, hydrate phases |
| vectors.md | Semantic similarities, clusters, embedding registry | Companion to graph.md — implicit weighted relationships |
| graph.md | Explicit typed relationship graph | Uses edge vocabulary from references/graph-syntax.md |
| config.md | PMM operational configuration | Save cadence, commit behaviour, window sizes, verbosity, active files |
| /pmm-settings | Skill to re-present preference prompts | Lives at .claude/skills/pmm-settings/ |
| /pmm-viz | ASCII visualization of memory state | Visualizes graph.md, vectors.md, timeline.md |
| GitHub repo | https://github.com/NominexHQ/poor-man-memory | Public repo, clone-and-go project |

## Organisations

| Name | Relationship | Notes |
|---|---|---|
| NominexHQ | Creator/owner | GitHub org (https://github.com/NominexHQ), @nominex_ai on X |
| Nominex | Product | "The memory layer for AI agents" — PMM is the open-source prototype |

## Other

<!-- Anything that doesn't fit above -->
