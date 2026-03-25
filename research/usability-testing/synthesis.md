# Synthesis: IDEX Usability Testing — Impression Tests
**Sessions:** Brad Phillips (Feb 12), Hunter Brown (Feb 13), Juan Bedoya (Feb 26)
**Test type:** Impression tests — static Figma hi-fi designs
**Product:** Perispek (IDEX Intelligent Water platform)
**Synthesized by:** Claude (Goji Labs UX research workflow)

---

## Executive Summary

Three wastewater utility professionals — spanning operations supervisors, field engineers, and senior managers — reviewed the Perispek hi-fi designs and responded with strong positive reactions to the overall direction. The unified dashboard concept resonates clearly: every participant identified fragmented tooling as a current pain, and all three expressed intent or enthusiasm to use a product like this. The highest-signal feedback centered on **risk of overflow as a priority metric**, **the need to see connected/upstream pipe history**, and **the gap between asset-centric design and crew/personnel management needs**. The designs communicate professional competence and spatial intelligence, but several labeling and scoping ambiguities caused hesitation across multiple participants.

---

## Key Themes

### Theme 1: Risk of Overflow is the Highest-Priority Signal
**Appeared in:** Brad (strong), Hunter (moderate), Juan (implied)

Brad made this the clearest: he would move "Risk of Overflow" to the far left of the dashboard — *"we read left to right"* — and said it was *"probably the most important thing I see up here right now."* He described a morning routine built around it: check overflow risk first, build the crew's day around addressing those assets.

Hunter noted it could be tied to live flow monitoring or a hydraulic model and wanted to understand the data source. Juan understood overflow risk within the broader context of consequence-of-failure scoring, though he didn't single it out the same way.

**Design implication:** Overflow risk should be the dominant, leftmost tile. Its prominence in the design is partially correct, but position and visual weight should be maximized. The data basis (flow meter thresholds? AI prediction?) should be surfaced at the tile level.

---

### Theme 2: The Unified Platform Concept Directly Addresses a Real Pain
**Appeared in:** Hunter (explicit), Brad (explicit), Juan (contextual)

> *"I've got, like, eight different logins. I had to look at eight different pages of things. So, I mean, this brings a lot of that together."* — Hunter

> *"I like what you guys have come a long way. I'm impressed."* — Juan, comparing to IN4

> *"I hate Lucidity. And I'm just done with it at this point."* — Brad, on his current platform

All three participants are using fractured tool ecosystems: Lucidity, Doppler, Fulcrum, n-4, Power BI, ADS Prism, GIS — none of which talk to each other. Perispek's consolidation is the single most validating aspect of the design.

**Design implication:** The integration story is the strongest pitch. The prototype's value isn't any single feature — it's the synthesis. This should be foregrounded in any stakeholder presentation.

---

### Theme 3: Connected / Upstream Asset History is a High-Value Differentiator
**Appeared in:** Hunter (very strong), Juan (implicit in lifecycle focus), Brad (adjacent)

> *"A lot of times, we've got someone who's backing up, and we need to know about the defect on the line three or four segments up. And in our current system, we gotta do a lot of digging."* — Hunter

> *"What's missing here is work order history. Life cycle history."* — Juan

Hunter's reaction to the "connected assets" tab was one of the highest-signal moments across all three sessions. The ability to see upstream and downstream pipe condition without switching systems or doing GIS queries is a specific, unmet need. Juan framed the same need through the lens of lifecycle costing and work order history per asset.

**Design implication:** The connected assets / pipe network view needs to be prominent and easily accessible from the asset panel. This is potentially a key differentiator vs. competitors.

---

### Theme 4: Dashboard KPI Tiles Lack Scope Context
**Appeared in:** Brad (explicit), Juan (explicit), Hunter (implicit)

Brad: *"71 open — is that engineering work orders? Construction? Maintenance?"*
Juan: *"Is that based on the image in the screen? What's it based on?"*

Both participants hit a similar moment of friction: a tile showing a number without clear scoping (is this the whole system? My work group? The map area?). The design needs to signal scope at-a-glance.

**Design implication:** Each KPI tile should include a visible scope label (e.g., "System-wide" or "Your work group" or the area visible on the map). Work order counts in particular should be filterable/scoped to the logged-in user or their assigned group by default.

---

### Theme 5: Role-Based Views — Ops vs. Engineering
**Appeared in:** Juan (explicit), Brad (contextual), Hunter (implicit)

> *"Maybe you could have an operations dashboard and an engineering dashboard."* — Juan

> *"Risk scores are for decision making. Not for operational decision making, but for R&R decision making."* — Juan

Juan articulated this most precisely, but all three participants represent different roles (senior manager, field supervisor, engineer) — and they use the dashboard differently. Brad doesn't need deep risk analysis on a daily basis. Hunter doesn't need crew overtime tracking. Juan wants both.

**Design implication:** Consider role-based dashboard defaults or a configurable tile layout. At minimum, document which tiles are relevant to which role and design with that in mind. A two-persona split (Ops vs. Engineering) may cover the majority of use cases.

---

### Theme 6: Condition Change Labels Caused Confusion
**Appeared in:** Brad (strong), Hunter (mild)

Brad: *"Worsened since last inspection — that kinda throws me. I don't know if it worsened... what is the indicator? Why did it? How do we know it worsened?"*

Brad was uncertain about: (a) what data source drives this, (b) what "improved" means without a new inspection, and (c) what "no significant change" actually means for maintenance planning.

Hunter was less confused but also less explicit about his understanding. Juan did not comment directly on this section.

**Design implication:** The basis for condition change labels needs to be legible either in the label itself or via a tooltip/info icon. "Worsened since last inspection" should clarify the inspection type and data source. Consider a help icon with a one-line explanation.

---

### Theme 7: CCTV Video Access Should Be Embedded
**Appeared in:** Brad (explicit), Hunter (explicit), Juan (implicit)

> *"If there's a way to integrate those videos when you click on an asset, that'd be something that's highly, highly helpful."* — Brad

> *"Can I zoom in and see the CCTV footage? Can I see what defects there were on the segment?"* — Hunter

Both Brad and Hunter specifically called out wanting CCTV inspection footage accessible from within the asset panel — not a link that opens another system. Juan referenced CCTV data quality throughout but didn't ask for embedded video explicitly.

**Design implication:** CCTV footage access (even as a quick-link button to the video source) should be designed into the asset panel's condition section. This feature is explicitly expected and should be prioritized on the roadmap.

---

### Theme 8: Crew and Personnel Management is Outside Current Scope but Expected
**Appeared in:** Juan (very strong), Brad (moderate), Hunter (not raised)

> *"This is a great asset-centric dashboard, but I would think that what this is missing is that component [crew productivity KPIs]."* — Juan

Juan spent significant time on this: overtime tracking, crew assignments per work order, contractor management, field activity windows. Brad touched on it with "inspections this month" KPIs and wanting to know which crew owns a work order. Hunter, being an engineer, didn't raise it.

For ops managers (Juan, Brad), the crew dimension is essential — you can't manage a utility just by looking at assets. You also have to manage people and budget.

**Design implication:** This is likely roadmap-level feedback, not current-sprint. But the current design should not imply completeness if crew management is absent — the framing should make it clear this is Phase 1 of a larger vision. Work order assignment (to a crew/contractor) is the minimum viable version of this for the current release.

---

## Frequency Matrix

| Finding | Brad | Hunter | Juan |
|---------|------|--------|------|
| Risk of overflow = top priority | ✓✓ | ✓ | – |
| Tool fragmentation as pain | ✓✓ | ✓✓ | ✓ |
| Connected/upstream asset history | ✓ | ✓✓ | ✓✓ |
| Dashboard tile scope unclear | ✓✓ | ✓ | ✓✓ |
| Work order type / assignment missing | ✓ | – | ✓✓ |
| Condition change labels confusing | ✓✓ | ✓ | – |
| CCTV footage access wanted | ✓✓ | ✓✓ | ✓ |
| Role-based views (ops vs. engineering) | ✓ | ✓ | ✓✓ |
| Crew/personnel KPIs missing | ✓ | – | ✓✓ |
| Map ↔ dashboard data linkage | ✓ | ✓✓ | ✓ |
| Asset lifecycle / work order history | ✓ | ✓ | ✓✓ |
| Strong overall positive reaction | ✓✓ | ✓✓ | ✓✓ |

✓✓ = primary feedback / unprompted  ✓ = mentioned / secondary  – = not raised

---

## Design Implications (Prioritized)

### High Priority (Affects all 3 participants)
1. **Tile scope labels** — Every KPI tile needs a legible scope indicator. Work orders should default to the logged-in user's work group.
2. **Risk of overflow prominence** — Move to leftmost / most visually dominant position.
3. **Connected/upstream asset panel** — Make this highly accessible from the asset card; frame it as "area history" not just "connected assets."
4. **Strong overall positive signal** — The design is working. Don't over-pivot. Refinement, not redesign.

### Medium Priority (Affects 2 participants)
5. **Condition change labels** — Add data source and basis to "worsened / improved / no change" labels. Add tooltips or info icons.
6. **CCTV footage access** — Design a video-access pattern into the asset panel condition tab (even a placeholder link).
7. **Map ↔ data linkage** — Make it legible (or explicit) whether the map viewport filters the dashboard tiles.
8. **Role-based dashboard** — At minimum, document the ops vs. engineering persona split and design default tile sets for each.

### Lower Priority / Roadmap
9. **Work order type and assignment fields** — Add to work order creation form for current release.
10. **Crew/personnel productivity module** — Roadmap item; acknowledged as essential by ops managers but not necessarily current scope.
11. **Lifecycle costing / asset cost history** — "Holy grail" feature; acknowledged as aspirational.

---

## Open Questions for Follow-Up

- What is the technical basis for "condition worsened" — is this CCTV re-inspection, sensor-based, or inference?
- Will user authentication support role-based dashboard defaults (ops vs. engineering persona)?
- What is the integration path for CCTV footage (WinCan, Granite Net, vendor-agnostic)?
- How does the current design handle work order assignment and crew routing — is this a current or future feature?
- Is the map viewport intended to filter dashboard tile data, or are they intentionally decoupled?
- How should the product handle large utilities (WYCO, JEA) with hundreds of open work orders vs. smaller utilities?
