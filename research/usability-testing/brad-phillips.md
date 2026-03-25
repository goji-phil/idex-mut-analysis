# Usability Test: Brad Phillips
**Date:** February 12, 2026
**Org:** Wyandotte County/Kansas City, KS (WYCO) — Public Works, Wastewater
**Role:** Supervisor / Operations Manager
**Session type:** Impression test — static Figma hi-fi designs
**Facilitator:** Phil (Goji Labs) with Yaman and JT (IDEX)

---

## Participant Context

Brad is an operations supervisor overseeing wastewater collection crews at WYCO. He manages field crews dispatched daily, monitors KPIs regularly, and is actively frustrated with their current platform (Lucidity/Central Square). His public works director has already expressed openness to exploring alternatives. Brad is a hands-on, early-morning decision-maker — he described coming in an hour before shift to plan the day.

Current tech stack: Lucidity (work orders), Power BI (dashboards), Android tablets in field (problematic — switching to iPads).

---

## First Impressions

Brad's immediate reaction was positive. He said *"Wow. This looks a lot different. It looks pretty good to me."* He was oriented quickly by the dashboard layout and moved methodically across tiles left-to-right, narrating what each meant to him before asking follow-up questions.

---

## Observations

### Risk of Overflow — Highest Attention
Brad zeroed in on **Risk of Overflow** immediately and said he would move it to the far left of the dashboard because *"we read left to right."*

He articulated a clear operational scenario: *"I could come in at 6:00 in the morning, you know, an hour before shift, and say, hey. We've got nine assets that are at risk of overflow. Let's try to get out there and knock out two or three of them today."*

He explained the regulatory pressure: overflows trigger mandatory paperwork to the state, EPA, and other agencies, plus fines. Catching them early eliminates that burden entirely.

### Average Risk Score — Secondary Priority
Brad said average risk score "is not gonna change too much unless we really get something from an inspection crew." He'd check it second, after overflow risk. He understood it as a slow-moving indicator, not a daily operational trigger.

### Work Orders — Needs Scoping by Work Group
Brad noted that "71 open" is too vague for a utility their size. *"Right now, we have probably several hundred work orders open just depending on where we're at throughout the city."* He wanted the count scoped to whichever supervisor or work group is logged in — making it meaningful rather than overwhelming.

### Inspections This Month — Actively Tracked
He liked this tile and connected it to his current KPI practice: *"We monitor our KPIs on a daily and weekly basis."* He currently has to leave the app and open Power BI to see this. Having it on the main dashboard was a noted improvement.

### Map — Expected Color-Coded Layer
When Phil clarified the map wasn't live data, Brad explained his mental model: he expected the map to visually reflect the dashboard data — green/yellow/red segments tied to risk levels. *"Red meaning okay, red's gonna be those 12 assets. Yellow meaning... risk of overflow."* He was slightly recalibrating his understanding mid-session.

### Blockage Predictions / Condition Changes — Mostly Clear, Some Confusion
- Blockage predictions: understood intuitively, liked the color categories.
- "Worsened since last inspection" — confused him: *"That kinda throws me... I don't know if it had worsened... what is the indicator? Why did it? How do we know it worsened?"*
- "Improved" — speculated it might mean a repair was done, but wasn't certain.
- "Needs maintenance records" — read as "no data available, haven't been out there."

### System Insights — Read as AI/Predictive
Brad interpreted System Insights as the AI/algorithmic layer: *"Stop doing this willy nilly pick wherever you want to go. You need to get your butt over here and take care of these problems."* This resonated with him as solving a real workflow pain.

### Asset Detail Panel
Wanted:
- **Pipe type / material** ✓ (confirmed it was there)
- **Footage / length** ✓ (confirmed)
- **Depth** — specifically requested; install date was lower priority
- **Last active date** — preferred over "last inspected": *"Last active saying, this is the last time activity or work order was done on that."*
- **Subnetwork type** — wanted to remove if map uses color-coding by system type

**Priority defect** was highly valued: *"That saves them time in the field"* — if crew knows roots were pulled last time, they can bring the right nozzle.

### Condition Tab — Expected PACP Ratings + Embedded Video
He referenced PACP (Pipe Assessment Certification Program, NASSCO standard) as the universal language for condition rating. *"If there's a way to integrate those videos when you click on an asset, that'd be something that's highly, highly helpful."* He wanted either embedded video or a single-click link to CCTV footage, rather than switching to another system.

### Work Group Filtering on Risk Panel
When viewing the list of flagged assets, he couldn't tell which work group owned the work. Wanted a filter: *"Set up a filter — one for maintenance... one for construction... one for engineering."* This would make it actionable: maintenance crews can flush, construction handles excavations, etc.

### Work Order Creation — Assignment + Project Type
He asked about who gets assigned the work order — in-house crew vs. contractor. Wanted project type field (CIP, DOT, O&M) and a freehand notes field.

---

## Positive Signals

- Strongly positive on the overall direction: *"I like it, Phil, because this is what we're looking for. We're looking for where should we go next."*
- Gave a **4/5 usability rating** and **4/5 overall**: *"This is definitely better than what we have... I'd stick at a 4 right now."*
- Excited about the platform as an alternative to Lucidity: *"Does this get me excited? Yeah. Because I hate Lucidity."*
- His utility's leadership has already signaled openness to new platforms: public works director said they'd *"be doing our citizens a favor by going out and looking for more efficient products."*

---

## Pain Points / Friction

| Area | Observation |
|------|-------------|
| Risk of overflow tile position | Wanted it moved further left (highest priority visually) |
| Work orders count | Too vague without work group scoping |
| Condition change basis | "Worsened" label unclear — no indication of *why* |
| Asset panel — required work group | No visibility into which team/crew a flagged item belongs to |
| Toolbar | No feedback — *"I don't know what any of those mean. I'm sure I could figure it out here within a few minutes."* |
| Condition tab | Expected PACP rating system to be present |
| Video access | Wants embedded CCTV video, not a link to another system |

---

## Notable Quotes

> *"Risk of overflow... that's probably the most important thing I see up here right now."*

> *"When we reach an overflow, when we have sewage on the ground, Phil, that means we have to do a lot of paperwork, send it to the states. Send it to the EPA. If we can catch those beforehand, that can basically cancel out the paperwork."*

> *"Does this get me excited? Yeah. Because I hate Lucidity. And I'm just done with it at this point."*

> *"This is what we're looking for. We're looking for where should we go next. Where should we get to next rather than just waiting for those phone calls to come in."*

> *"The hardest decisions for us to make is the collective ones on what pipes or what area of the city do we take care of first."*

> *"If you guys can model that in there [budget allocation / ROI], that's gonna be the toughest decision."*

---

## Open Questions

- How does the system determine "worsened since last inspection" without a new CCTV run?
- How does work order assignment/routing to specific crews/contractors work?
- Can the dashboard be personalized per logged-in user to scope work orders?
- Will it work on Android tablets (or require iOS)?
- What is the PACP integration path?

---

## Facilitator Notes

Yaman was present but largely stayed quiet, allowing Phil to run the session. Brad was very forthcoming and detailed — clearly an experienced operator with strong opinions about what tools should do. At the end, Yaman asked a broader question about the hardest decision Brad faces each year, which generated the budget allocation / ROI framing — very quotable for leadership.
