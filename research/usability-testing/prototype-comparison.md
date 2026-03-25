# Prototype Comparison: Issues Raised in Testing vs. Current Prototype
**Sessions:** Brad Phillips (Feb 12), Hunter Brown (Feb 13), Juan Bedoya (Feb 26)
**Prototype repo:** https://github.com/goji-phil/Idexprototype.git
**Analysis date:** March 2026

This document maps each issue surfaced during usability testing to its status in the current Perispek prototype, based on code review of the GitHub repository.

---

## ✅ Fully Addressed

| Issue | Raised By | Evidence in Prototype |
|-------|-----------|----------------------|
| CCTV footage embedded in asset panel | Brad (explicit), Hunter (explicit) | "View CCTV" button on each defect in asset Condition tab; opens video modal with playback, scrubber, defect navigation (1 of N), PACP code display |
| PACP ratings in condition tab | Brad | Defects show PACP code (e.g., RMJ, DMS), grade 1–5, NASSCO standards reference |
| Work order type field | Juan (strong), Brad | Types: Inspection, Repair, Deployment, Cleaning — present in WO detail and Kanban grouping |
| Work order assignment field | Juan (strong), Brad | Assignee dropdown in WO detail; Kanban can be grouped by Assignee |
| Backlog vs. scheduled distinction | Hunter | Full status pipeline: Backlog → To Do → Scheduled → In Progress → Complete |
| Map color-coded by risk | Brad | Assets color-coded Green/Yellow/Red/Critical; pipe network overlays; 3 view modes (Risk, Condition, Performance) |
| Map insight filtering | Hunter | Insight Category Filter on map: All, Risk Score, Overflow, Blockage Predict, Condition Change, Maint. Suggested |
| Asset detail: material, diameter, length, install date | Brad, Juan | Overview tab in asset drawer and full asset detail page includes all fields |
| Search by asset ID / address | Hunter | Map search supports ID, name, material, basin; global command palette (Cmd+K) |
| Polygon selection on map | Hunter (implicit) | Polygon select tool on map toolbox for drawing area selection; multi-select mode with shift-click |
| Alerts / real-time notifications | Brad, Hunter | Full alerts page with severity (Critical/High/Medium/Low/Info), category (Overflow/Blockage/Condition/Sensor), status workflow |
| Risk of overflow tile present | Brad | KPI tile on dashboard — present with d/D ratio monitoring and threshold alerts |

---

## ⚠️ Partially Addressed

| Issue | Raised By | Current State | Gap |
|-------|-----------|---------------|-----|
| Risk of overflow tile position (leftmost) | Brad | Tile exists; dashboard has 4 KPI tiles | Position/order on dashboard may not place it far left as requested |
| Export capability | Hunter | Export button on work orders page; WinCan sync | CSV export explicitly marked "coming soon" |
| Work order history per asset | Juan, Hunter | Work Orders tab in asset detail shows linked work orders | No cost tracking, no lifecycle costing, no frequency analysis |
| Risk scoring recalibration | Hunter | Risk is deterministic from material, age, condition | No user-configurable risk equation editor; settings has data config but not equation weighting |
| Last active date vs. last inspected | Brad | "Last Inspected" date shown in asset overview | "Last active" (most recent work order date) not surfaced as a distinct field |
| Connected/upstream asset history | Hunter (very strong), Juan | Work Orders tab links assets; map shows pipe network | Dedicated upstream neighbor condition history not confirmed as a distinct UI panel |

---

## ❌ Not Yet Addressed

| Issue | Raised By | Notes |
|-------|-----------|-------|
| Dashboard tile scope context | Brad, Juan | Tiles show system-wide totals; no scope label ("System-wide" / "Your work group") or user-based filtering |
| Work order count scoped to work group | Brad | No per-user/group default; a supervisor would see all WOs, not just their group's |
| Map ↔ dashboard tile bidirectional linking | Hunter | Map and dashboard are separate pages; map viewport does not filter dashboard KPI tiles |
| Role-based dashboard views (ops vs. engineering) | Juan (explicit), Brad, Hunter | Users & Roles framework exists in settings but no separate Ops vs. Engineering dashboard defaults |
| Condition change label basis | Brad (strong), Hunter | "Worsened since last inspection" has no tooltip, data source reference, or explanation of methodology |
| Crew/personnel productivity KPIs | Juan (strong), Brad | No crew productivity dashboard: work orders closed per day, footage per crew, overtime, contractor tracking |
| Asset burial depth | Juan | Material, diameter, and length shown; burial depth (important for repair difficulty/safety) not visible |
| As-built PDF links | Juan | No document linking from asset detail to as-built drawings |
| Lifecycle costing / cost per work order | Juan | No financial data in work order detail; acknowledged as roadmap ("holy grail") |
| Capital projects view | Juan | No CIP/capital project module or tracking |
| Work group / crew filter on asset risk list | Brad | Insights and risk lists don't filter by owning work group (maintenance vs. construction vs. engineering) |

---

## Summary

| Status | Count |
|--------|-------|
| ✅ Fully addressed | 12 |
| ⚠️ Partially addressed | 6 |
| ❌ Not yet addressed | 11 |
| **Total issues tracked** | **29** |

The prototype has made strong progress on the most technically complex feedback (CCTV integration, PACP ratings, work order structure, map visualization). The remaining gaps are primarily around **personalization and scoping** (user-level filtering, role-based views, tile scope labels) and **operational management features** (crew productivity, lifecycle costing) that require product scope decisions before design.
