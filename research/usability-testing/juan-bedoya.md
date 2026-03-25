# Usability Test: Juan Bedoya
**Date:** February 26, 2026
**Org:** JEA (Jacksonville Electric Authority) — Wastewater
**Role:** Operations Manager / Director level (manages both in-house crews and contractors)
**Session type:** Impression test — static Figma hi-fi designs
**Facilitator:** Phil (Goji Labs) with Yaman (IDEX)

---

## Participant Context

Juan is a senior operations manager at a large utility (JEA, Jacksonville). He oversees field operations including in-house sewer crews, vac crews, customer response, capital infrastructure (CIP) contractors, and specialty contractors (manhole coating, CCTV). He is simultaneously managing people, assets, and budgets — and constantly thinking about crew productivity, overtime, and contractor accountability. He has previously used more advanced platforms (IN4 at Miami-Dade) and has a mature mental model for what an enterprise asset management system should do.

JEA is currently mid-way through an asset management gap analysis (recently hired a consultant) and evaluating platforms like CityWorks and Hexagon.

---

## First Impressions

Juan jumped in immediately with questions rather than general reactions. He oriented quickly by asking what each data point was "based on" — he was trying to understand the scope and methodology behind the numbers (is the data system-wide? Polygon-based? What algorithm drives the risk score?). This reflects someone with deep domain expertise who evaluates data quality before acting on it.

His overall first reaction was positive: *"It looks great. I mean, that's a lot of great information."*

---

## Observations

### Dashboard Scope / Context — First Question
Before evaluating anything else, Juan asked: *"The information on the screen — is that based on the image in the screen? What's it based on?"* He was trying to understand whether the KPIs reflected the full system or just what was visible on the map. This is a critical question for usability — the scope of the data displayed was not immediately legible.

### Work Orders — Missing Type and Assignment
Juan noted two key missing fields from the work order tile and creation flow:

1. **Work order type** — *"You're missing a work order type. That's for sure."* Types include: investigate cave-in, appointment repair, customer complaint, manhole overflow, mainline blockage. Without type, you can't route, prioritize, or track by category.

2. **Assignment** — *"All work orders are assigned to somebody. Right? Is this assigned to the in-house sewer crew? Is this being assigned to an outside contractor? Or is this being assigned to, you know, what crew?"* He wanted explicit assignment to a crew, contractor, or contract number.

### Crew Productivity KPIs — Missing Entirely
This was Juan's most persistent and detailed piece of feedback. He felt the dashboard was excellent for asset-level visibility but completely missing the **personnel and crew management** dimension:

> *"What's missing here as a manager is productivity metrics. How many work orders have been closed out every day? What is the average? How much CCTV footage did the crews perform yesterday?"*

He also flagged:
- **Overtime tracking**: *"Am I getting an ROI on it? Am I getting good productivity for it?"*
- **Contractor activity window**: How many contractors in the field today? Which contract are they working under?
- **In-house crew window**: What is each crew working on today?

He suggested a "field activities" or "field crews" window, or even a customizable section of the dashboard for each section/supervisor.

### Risk Scores — For Engineering, Not Ops
Juan articulated the clearest role-based framing of risk of any participant: *"Risk score is one of those things where transitioning from an operational manager... is he gonna look at risk scores? I don't think so. Who's gonna look at risk scores is the engineer of that utility or of that section."*

He gave a specific use case: an engineer using risk scores to select which manholes to line when given a budget for 100. Or a polygon query when FDOT notifies them of an upcoming repaving project.

He proposed separate dashboards: **operations dashboard** and **engineering dashboard**, with each role seeing what's relevant to them.

### Asset Detail Panel — Needs More and Deeper
Juan walked through what he'd expect in a full attribute table from GIS:
- Material, length, diameter, depth, asset type
- Street address
- **As-built PDF link** (key — he mentioned it twice)
- Upstream/downstream manhole ID
- Priority defect, last inspected, property defect

**Depth** was specifically called out as critical for safety and repair decision-making: *"If you have a 10-foot deep line and you're showing indications of a cave-in, then immediately... my radar's focused on that."*

### Work Order History / Lifecycle — The Holy Grail
Juan repeatedly came back to **lifecycle costing and work order history per asset**: *"The first thing as a manager when you look at an asset is how many — the historical activity here. Have I visited and cleaned blockages at this line eight times in the last one year?"*

He outlined what a complete asset history would look like: work order type + monetary value + linked inspection results + condition assessment over time. He called this *"the holy grail of an asset management platform."*

He noted most utilities don't have the data infrastructure to do this yet (connected to storeroom, equipment pricing, etc.), but it's the target state.

### Customizable Nomenclature
Each utility uses different naming conventions. He gave the example of JEA's level monitors (named by nearest street/cross-street) vs. Miami's pump station numbers. He wanted the platform to support whatever nomenclature is meaningful to the utility, not just one fixed naming system.

### Blockage Predictions / Sensors
He understood the sensor-based data and overflow risk framing. *"This is based on probably scheduled cleaning routes."* He asked clarifying questions but didn't express confusion — more curiosity about the algorithm and data source.

### Overall Architecture
Despite the detailed gaps he called out, Juan was consistently positive about the design direction: *"I think the architecture's there, man. I really do."* He acknowledged the product was clearly well-developed and comparable to or exceeding platforms like IN4.

---

## Positive Signals

- Strong overall endorsement: *"I love it. I like it. I like what you guys have come a long way. I'm impressed. It's purty."*
- The risk/consequence framework (consequence of failure vs. likelihood of failure) was well-received: *"I like it."*
- Appreciated the linked work order creation from the asset panel
- Saw a direct gap his utility is currently trying to fill: *"We're in the process of doing asset management gap analysis. We don't have... user-friendly... spatial... [tools like this]."*
- Said the product *"compares to or exceeds"* IN4 visually.

---

## Pain Points / Friction

| Area | Observation |
|------|-------------|
| Dashboard scope | Unclear whether KPIs are system-wide or map-area-specific |
| Work order type | Missing — makes routing and categorization impossible |
| Work order assignment | No visibility into who/what team receives the work |
| Crew productivity KPIs | Entirely absent — major gap for ops managers |
| Contractor management | No field to indicate which contractor or which contract |
| As-built links | No link to PDF as-built documents from asset panel |
| Asset depth | Not visible at summary level (important for repair priority) |
| Lifecycle costing | Not present — acknowledged as advanced but worth targeting |
| Capital projects | No view for CIP activity in the system |
| Nomenclature flexibility | System needs to support utility-specific naming conventions |

---

## Notable Quotes

> *"What's missing here as a manager is productivity metrics."*

> *"This is a great asset-centric dashboard, but I would think that what this is missing is that component [crew/personnel KPIs]."*

> *"Risk scores are for decision making. Not for operational decision making, but for R&R decision making."*

> *"If you have a 10-foot deep line and you're showing indications of a cave-in, then immediately, my radar's focused on that."*

> *"That's the holy grail of an asset management platform."*

> *"I love it... I think the architecture's there, man."*

> *"You're missing a work order type. That's for sure."*

> *"The first thing as a manager when you look at an asset is how many — the historical activity here."*

---

## Open Questions

- What is the scope of each dashboard tile — full system or map viewport?
- Will there be a crew/field activity module, or is this purely asset-centric?
- How does work order assignment and contractor management work?
- Can the risk view produce polygon-based queries for engineering planning?
- Is there a roadmap for as-built document linking?
- Will there be role-based dashboard views (ops vs. engineering)?

---

## Facilitator Notes

Yaman sat out the first half of the session. Juan was very engaged and thorough — more of a domain expert interview than a passive usability impression. He was clearly evaluating the platform against his own detailed requirements, not just reacting. His feedback represents a senior enterprise buyer perspective. Dave (presumably from Goji Labs) joined briefly.
