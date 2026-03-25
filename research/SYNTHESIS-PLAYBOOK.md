# Usability Research Synthesis Playbook
**For:** IDEX x Goji Labs — Moderated Usability Testing
**Toolchain:** Granola MCP + Claude + Figma MCP

A repeatable step-by-step process for turning moderated usability test sessions into structured findings, synthesis, prototype comparison, and a FigJam board — ready for stakeholder review.

---

## Prerequisites

Before starting a synthesis session, confirm:

- [ ] **Granola MCP connected** — `.mcp.json` exists in the repo root; workspace reloaded in Claude Code so Granola tools appear
- [ ] **Figma MCP enabled** — for writing to FigJam boards (`figma-use` skill)
- [ ] **Scope constraint active** — Granola access is limited to the **IDEX folder only** (folder ID: `bb1bdbd0-6da6-4ff8-978e-8dc3a4e51dc2`). Never access other folders.
- [ ] **UX skills available** — `transcript-analysis`, `ux-researcher`, `ux-design-thinking` (installed globally in `~/.claude/skills/`)

---

## Step 1: Protocol Alignment (Before Sessions)

Hold a brief alignment meeting with the research team to agree on:
- What is being tested (specific screens, flows, or prototypes)
- Session type: **impression** (static screens, no clicking), **click-through** (prototype navigation), or **task-based** (complete a specific goal)
- Core questions you're trying to answer
- Success criteria for the sessions
- Who is the facilitator, who takes notes, who observes

> **Why this matters:** Session type changes what you look for. Impression tests surface first reactions and comprehension. Click-through tests reveal navigation and mental models. Task-based tests surface completion rates and friction.

Save the alignment meeting notes in Granola → IDEX folder so they're accessible alongside the session transcripts.

---

## Step 2: Finding Sessions in Granola

```
1. List IDEX folder meetings:
   → list_meetings(folder_id: "bb1bdbd0-6da6-4ff8-978e-8dc3a4e51dc2", time_range: "last_30_days")

2. If sessions are older than 30 days:
   → list_meetings(folder_id: ..., time_range: "custom", custom_start: "YYYY-MM-DD", custom_end: "YYYY-MM-DD")

3. Confirm participant names match expected attendees before fetching.
```

Also locate the **alignment meeting** (usually held 1–2 weeks before sessions) — it's the protocol context you'll need in Step 4.

---

## Step 3: Fetch Transcripts

Use `get_meeting_transcript` for:
- The alignment meeting
- Each usability session

**Fetch all in parallel** for speed. Read the alignment transcript first — it tells you what was being tested and what questions were asked, which frames everything that follows.

---

## Step 4: Per-Participant Analysis

Create one markdown file per participant at:
```
research/usability-testing/[first-last].md
```

Each file should contain these sections:

```markdown
# Usability Test: [Name]
**Date:** ...
**Org:** ...
**Role:** ...
**Session type:** Impression / Click-through / Task-based
**Facilitator:** Phil (Goji Labs) with [IDEX attendees]

## Participant Context
[Role summary, current tools they use, mental model / prior experience]

## First Impressions
[Immediate reaction — what they said in the first 60 seconds]

## Observations
[Grouped by screen/area — what they noticed, what confused them, where they paused]

## Positive Signals
[What resonated, what they liked, what they'd use]

## Pain Points / Friction
| Area | Observation |
|------|-------------|
| ... | ... |

## Notable Quotes
> "verbatim quote here"

## Open Questions
[Things they asked or were uncertain about]

## Facilitator Notes
[Anything notable about how the session ran, who else was present, tangents]
```

**Tip:** Work through the transcript chronologically on first pass, then reorganize into sections.

---

## Step 5: Cross-Participant Synthesis

Create `research/usability-testing/synthesis.md`.

**Only include themes that appeared in 2 or more sessions.** Single-participant observations belong in their individual files, not the synthesis.

Structure:

```markdown
## Executive Summary
[3–5 sentences covering: overall reaction, top finding, most surprising insight, biggest gap]

## Key Themes
[One section per theme: description, which participants raised it, evidence quotes, design implication]

## Frequency Matrix
| Finding | Participant A | Participant B | Participant C |
|---------|--------------|--------------|--------------|
| ...     | ✓✓ / ✓ / –  | ...          | ...          |

✓✓ = primary / unprompted   ✓ = mentioned / secondary   – = not raised

## Design Implications (Prioritized)
### High Priority (3+ participants or critical path)
### Medium Priority (2 participants or secondary flows)
### Roadmap (valid but out of scope for current sprint)

## Open Questions for Follow-Up
```

---

## Step 6: Prototype Comparison

Create `research/usability-testing/prototype-comparison.md`.

For each issue raised in testing, map it to the current prototype's status:

| Issue | Raised By | Prototype Status | Evidence / Notes |
|-------|-----------|-----------------|------------------|
| ...   | ...       | ✅ Addressed     | ... |
| ...   | ...       | ⚠️ Partial       | ... |
| ...   | ...       | ❌ Not yet       | ... |

**Status definitions:**
- ✅ **Addressed** — The prototype directly solves this; you can point to specific UI evidence
- ⚠️ **Partial** — The feature exists but is incomplete or missing edge cases
- ❌ **Not yet** — Valid finding; not in the current prototype; roadmap candidate

---

## Step 7: FigJam Visualization

Open the IDEX x Goji Research Whiteboard and navigate to the relevant page (e.g., "Moderated Usability Tests").

**Always load the `figma-use` skill before calling `use_figma`.**

### Layout
Place sections left-to-right with ~100px gaps:

| Section | Suggested Color | Contents |
|---------|----------------|----------|
| Participant A | Blue | Header + impressions + positives + pain points + quotes + questions |
| Participant B | Violet/Purple | Same structure |
| Participant C | Orange | Same structure |
| Synthesis | Yellow | Executive summary + 1 sticky per theme + priority tiers |
| Prototype Comparison | Green | 3 columns: ✅ / ⚠️ / ❌ |

### Sticky note structure per participant section
1. **Section header** — name, role, org, date (large sticky, section color)
2. **First impressions** — 1–2 stickies
3. **Positive signals** — light green or lighter shade, one per finding
4. **Pain points** — light red/pink, one per friction point
5. **Notable quotes** — yellow, verbatim in quotation marks
6. **Open questions** — light gray, one per question

### Accessibility rule
> **No dark text on a very dark sticky note.** Always ensure text color and sticky color have sufficient contrast. Use pastel/light backgrounds with dark text, or dark backgrounds with white text.

---

## Step 8: File Structure

```
research/
  SYNTHESIS-PLAYBOOK.md          ← this file
  usability-testing/
    [participant-slug].md         ← one per session
    synthesis.md
    prototype-comparison.md
```

---

## Step 9: Commit, Push, and PR

```bash
git add research/
git commit -m "Add [round name] usability test research and synthesis"
git push -u origin [branch-name]
gh pr create --base main --title "..." --body "..."
```

PR description should include:
- What sessions were analyzed
- Top 3 findings
- What files were created

Then post a **chat summary** of the top 5 findings for quick reference without opening files.

---

## Quick Checklist

- [ ] Protocol alignment meeting notes saved in Granola IDEX folder
- [ ] All session transcripts fetched
- [ ] Per-participant file created for each session
- [ ] "Yoman" / "Yomar" — verify names are spelled correctly throughout
- [ ] Synthesis covers only cross-participant themes (2+ participants)
- [ ] Prototype comparison has status for every finding from synthesis
- [ ] FigJam board updated (all sections visible, text readable/accessible)
- [ ] All files committed and PR opened
