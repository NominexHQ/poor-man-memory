---
name: pmm-viz
description: "Visualize PMM memory state as ASCII art in the terminal. Renders relationship graphs, file activity heatmaps, and vector similarity maps. Use when the user runs /pmm-viz or asks to visualize, map, or see their memory."
---

# PMM Viz

Render PMM memory state as inline ASCII visualizations. No dependencies, no browser — pure terminal output.

## Invocation

- `/pmm-viz` — all three visualizations
- `/pmm-viz graph` — relationship map only
- `/pmm-viz heatmap` — file activity only
- `/pmm-viz vectors` — similarity matrix and clusters only

## Visualization 1: Graph — Relationship Map

**Source:** `memory/graph.md`

**Steps:**
1. Read `memory/graph.md`
2. Parse all `[[A]] → relationship → [[B]]` lines
3. Group edges by section headers (## headings in graph.md)
4. Render each group as an ASCII subgraph

**Rendering rules:**
- Nodes are boxed: `┌──────┐ │ name │ └──────┘`
- Edges use box-drawing arrows: `───relationship──▶`
- Vertical edges use `│` with label beside
- Group subgraphs under their section name
- If graph.md has more than 15 edges, show top-level structure only (collapse leaf nodes)
- If graph.md is empty/template, say: "No relationships recorded yet."

**Example output:**

```
## Structure

  ┌─────────────┐  extends   ┌───────────┐
  │ vectors.md  │───────────▶│ graph.md  │
  └─────────────┘            └───────────┘

  ┌──────────┐  uses    ┌────────────────┐  enables  ┌───────────────┐
  │ SKILL.md │─────────▶│ Agent Dispatch │─────────▶│ Clean Context │
  └──────────┘          └────────────────┘           └───────────────┘

## Dependencies

  ┌────────────────┐  depends-on  ┌──────────────────┐
  │ Agent Dispatch │────────────▶│ Bash Permissions │
  └────────────────┘              └──────────────────┘
```

## Visualization 2: Heatmap — File Activity

**Source:** `memory/config.md` (active files list) + `git log`

**Steps:**
1. Read `memory/config.md` to get the list of active files
2. For each active file, run: `git log -1 --format="%ar|%at" -- memory/<filename>`
3. Map the unix timestamp to a heat level:
   - `████` = modified < 5 minutes ago
   - `███░` = modified < 30 minutes ago
   - `██░░` = modified < 2 hours ago
   - `█░░░` = modified < 24 hours ago
   - `░░░░` = modified > 24 hours ago or never
4. Check if file is empty/template-only (only has comments and headers, no real content)
5. Sort by recency (most recent first)
6. Render as aligned table

**Example output:**

```
PMM File Activity

  ████ last.md               2 min ago
  ███░ progress.md          15 min ago
  ███░ preferences.md       18 min ago
  ██░░ decisions.md          1 hr ago
  ██░░ voices.md             1 hr ago
  █░░░ timeline.md           3 hr ago
  █░░░ graph.md              3 hr ago
  █░░░ vectors.md            3 hr ago
  ░░░░ taxonomies.md         never (empty)
  ░░░░ summaries.md          never (empty)

  Legend: ████ <5m  ███░ <30m  ██░░ <2h  █░░░ <24h  ░░░░ stale
```

## Visualization 3: Vectors — Similarity Matrix & Clusters

**Source:** `memory/vectors.md`

**Steps:**
1. Read `memory/vectors.md`
2. Parse similarity lines: `[[A]] ↔ [[B]] | score: X.XX | basis: ...`
3. Parse cluster lines: `Cluster: name → [[[A]], [[B]]] | theme: ...`
4. Build a sparse similarity matrix from the pairs
5. Render as aligned ASCII table with abbreviated column headers
6. Render clusters as indented tree

**Rendering rules:**
- Use `·` for no data (pairs without a recorded similarity)
- Abbreviate node names to fit columns (max 6 chars)
- Show scores to 2 decimal places
- Below the matrix, render clusters as a tree with `┌├└` chars
- If vectors.md is empty/template, say: "No similarities or clusters recorded yet."

**Example output:**

```
Similarity Matrix

              graph  vectr  last   prog   decis  stand  SKILL  proc   summ   timel
  graph.md      ·    0.72    ·      ·      ·      ·      ·      ·      ·      ·
  vectors.md  0.72     ·     ·      ·      ·      ·      ·      ·      ·      ·
  last.md       ·      ·     ·    0.65     ·      ·      ·      ·      ·      ·
  progress.md   ·      ·   0.65     ·      ·      ·      ·      ·      ·      ·
  decisions.md  ·      ·     ·      ·      ·    0.58     ·      ·      ·      ·
  standing.md   ·      ·     ·      ·    0.58     ·      ·      ·      ·      ·
  SKILL.md      ·      ·     ·      ·      ·      ·      ·    0.55     ·      ·
  processes.md  ·      ·     ·      ·      ·      ·    0.55     ·      ·      ·
  summaries.md  ·      ·     ·      ·      ·      ·      ·      ·      ·    0.74
  timeline.md   ·      ·     ·      ·      ·      ·      ·      ·    0.74     ·

Clusters
  ┌ recent-context ──── last.md, progress.md, timeline.md
  ├ append-only ─────── decisions.md, timeline.md, standinginstructions.md, graph.md
  ├ identity ────────── preferences.md, assets.md, memory.md
  ├ relationship ────── graph.md, vectors.md
  └ self-referential ── SKILL.md, memory.md, processes.md
```

## Notes

- This is a prompt-only skill — Claude reads the files and generates the ASCII art. No scripts or binaries.
- All data comes from the memory files. If a file is empty, the viz says so.
- The heatmap requires git history — if the project has no commits yet, show all files as `░░░░`.
- Keep output compact. If the terminal is narrow, prefer vertical layouts over wide tables.
