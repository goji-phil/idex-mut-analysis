# Usability Test: Hunter Brown
**Date:** February 13, 2026
**Org:** City of Springfield, MO — Wastewater/Collection System
**Role:** Collection System Engineer; supervises flow monitoring team and private sewer team
**Session type:** Impression test — static Figma hi-fi designs
**Facilitator:** Phil (Goji Labs) with Yaman and JT (IDEX)

---

## Participant Context

Hunter is an engineer, not a field operations supervisor. His work involves analysis, project management, flow monitoring oversight, and condition assessment — not day-to-day crew dispatch. He works alongside a separate operations group (Brandon's group) that handles reactive dispatch and field work orders. His lens is more technical and system-wide than operational.

Current tech stack: ADS Prism (flow monitoring / blockage prediction), Fulcrum (field data entry), Doppler (reactive response management), n-4/in-for (asset management and work orders), Power BI (dashboards — static).

He explicitly noted he has ~8 separate logins to do his job.

---

## First Impressions

> *"The first thing I noticed was the work orders tab and the inspection footage this month. I liked that it was giving me an overview of what's going on."*

His first instinct was operational/overview — the tile-based summary gave him immediate situational awareness. He was also immediately curious about **map interactivity** — his first follow-up question was whether the map filtered the other data shown on the dashboard.

---

## Observations

### Map Interactivity — First and Recurring Question
Hunter's top concern across the session was map-data linkage: *"My first thought would be, can I filter based on this map? Does it change the work orders and the inspections footage?"* He returned to the map repeatedly. His mental model was that the map and the tiles should be bidirectionally linked — zoom to an area, see relevant data.

### Risk Score — Engineering Context, Not Daily Ops
*"Usually, I'm not looking at that until I'm diving deeper into something. If I customize it, I'd probably put the risk further in."*

Risk score wasn't his first-stop metric. He uses it during analysis and planning, not real-time operations. He also noted that risk tools can go stale — *"We can get to a point where nothing's categorized as high risk, or too many things are categorized as high risk."* He valued dynamic, recalibratable risk but was realistic about the limitations.

### Blockage Predictions — Familiar Concept
He noted this is already a feature in ADS Prism. He was interested in the implementation and whether this version could go deeper than what he already has. He saw it as a key feature to differentiate from static GIS-based systems.

### Asset Detail Panel — Depth Appreciated
Hunter liked the information density on the asset card:
- Liked install date (hard to find in current system)
- Liked the condition inspection summary and defect count: *"That's big. That's something and what would help us if we could drill farther into that tab and see the condition on the surrounding pipes."*
- Liked that it immediately flags priority defects and enables work order creation
- Wanted embedded CCTV footage: *"Can I zoom in and see the CCTV footage? Can I see what defects there were on the segment?"*

### Connected Assets — High Value
Hunter lit up on the connected assets/upstream neighbor concept: *"A lot of times, we've got someone who's backing up, and we need to know about the defect on the line three or four segments up. And in our current system, we gotta do a lot of digging to really pull all that info in. So that would be huge for us."*

This was one of his highest-signal moments — a specific workflow pain that this design directly addresses.

### Toolbar — Exploratory First Pass
He said he'd hover over icons to see tooltips. He recognized a layers icon and suspected selection tools, but wanted to expand the toolbar to see more. Not a blocker, but not immediately clear without tooltips.

### Work Orders Panel — Liked Backlog / Schedule Distinction
*"I really like how there's a create work order and add to the backlog."* He explained that his team documents things that need attention in 1–2 years but aren't urgent. The backlog feature matched a real workflow. He was slightly confused by the "to do" vs. "scheduled" split — interpreted "to do" as "needs to be scheduled."

He liked the ability to add to an existing open work order: *"I think that could be useful."*

### Risk Summary View
He liked the visual risk distribution (high/medium/low breakdown). His concern wasn't the visualization but the underlying equation: *"Things in the system will change, and we'll need to go in and tweak the equation... We have to go in and update that periodically."* He wanted the risk methodology to be configurable/maintainable.

### Export Feature
*"Something is I don't know. I like exporting and making memos."* A simple observation but consistent with his analytical, documentation-heavy role.

### AI-Generated Summary
He asked: *"The auto-generated details, is that just pulling things that — an AI tool that's pulling in a summary?"* He was curious about the intelligence layer and whether it was AI or rule-based aggregation.

### Rainfall Tile
Ambivalent: *"I don't know if I'd have today's rainfall on the front page, but at the same time, you could probably make an argument that that is really useful to have."* As someone who works on inflow/infiltration (I/I) analysis, he understood its value but wasn't certain it belonged on the primary dashboard.

He mentioned he's been thinking about building an R/I value (rainfall entering sewer as %) as a leakiness indicator — hinted that rainfall data tied to system response could be a useful future feature.

### Would He Use It?
*"I would use it. Seems like we're trying to always come up with dashboards for everyone, but then they're static and trying to... get something we can all use and not just these isolated dashboards."*

---

## Positive Signals

- Strong validation of the core unification concept: *"I've got, like, eight different logins. I had to look at eight different pages of things. So, I mean, this brings a lot of that together."*
- Connected assets feature landed as genuinely high-value for a real workflow
- Liked the work order + backlog structure
- *"It seems like it'd be pretty easy to navigate. 10 times easier than our old asset management system."*
- Gave strong intent to use: *"I would use it."*

---

## Pain Points / Friction

| Area | Observation |
|------|-------------|
| Map ↔ data linkage | Unclear if map filters the dashboard tiles (wanted bidirectional) |
| Risk placement | Would move it deeper; not a daily first-stop |
| Toolbar icons | Not self-explanatory; needs tooltips or expansion |
| "To do" vs. "Scheduled" | Distinction slightly unclear — thought "to do = needs scheduling" |
| CCTV access | Wants footage embedded or one-click from asset panel |
| Risk recalibration | Wants the risk scoring equation to be maintainable |
| AI/auto-generated label | Unclear whether it's rules-based or AI-driven |

---

## Notable Quotes

> *"The first thing I noticed was the work orders tab and the inspection footage this month. I liked that it was giving me an overview of what's going on."*

> *"I've got, like, eight different logins. I had to look at eight different pages of things. So, I mean, this brings a lot of that together."*

> *"A lot of times, we've got someone who's backing up, and we need to know about the defect on the line three or four segments up. And in our current system, we gotta do a lot of digging to really pull all that info in. So that would be huge for us."*

> *"I would use it. Seems like we're trying to always come up with dashboards for everyone, but then they're static."*

> *"I like exporting and making memos."*

> *"Can I zoom in and see the CCTV footage? Can I see what defects there were on the segment?"*

---

## Open Questions

- Is map filtering bidirectional with the dashboard tiles?
- How is the AI summary generated — rules-based or ML?
- Can the risk scoring equation be user-configurable?
- What is the path to embedding or linking CCTV footage in the asset panel?
- How does the connected assets feature behave — how many segments upstream/downstream?
- Will the platform replace all 8 of his current tools, or integrate with some?

---

## Facilitator Notes

Yaman sat out the first half of the session. Brandon (Hunter's colleague from the operations/dispatch group) was on standby and joined after this session. Hunter explicitly noted that Brandon would give better feedback on the reactive dispatch and work order routing side of things, as that's not his primary domain.
