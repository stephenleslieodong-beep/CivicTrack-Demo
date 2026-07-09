# CivicTrack – NDP IV Planning & Intelligence Platform

CivicTrack is a prototype government planning, monitoring and decision-support platform designed around Uganda's National Development Plan IV (NDP IV).

The objective is to improve planning, accountability, implementation monitoring, and evidence-based decision-making across all levels of government.

## Current Status

✅ Enterprise Design System Completed
✅ First Working Version (Phase 1) — this repository

Phase 1 is a real, running single-page application — not static mockups. It uses:

- **`index.html`** — the application shell
- **`tokens.css`** — the design system (colours, spacing, type, elevation, motion, dark mode)
- **`data.js`** — every data point used anywhere in the app, sourced from real documents (see below). Nothing is invented.
- **`app.js`** — the router, session handling, and reusable UI component builders (cards, status pills, breadcrumbs, drill tabs, expandable panels, toasts)
- **`views.js`** — one render function per screen, registered against the router

### What Phase 1 covers

- ✅ Working login (demo accounts only) and logout, with session persisted for the browser tab
- ✅ Five real, data-backed roles: Member of Parliament, LC5, LC3, LC2, LC1
- ✅ Interactive dashboards — NDP IV Programme-first (not budget-department-first), with expandable KPI tiles revealing real sub-data where it exists
- ✅ Project monitoring — full project lists, filterable by stage, with breadcrumb navigation
- ✅ Budget tracking — real district-level Programme performance for Kayunga District and Jinja District, pace-adjusted for differing report quarters; real Jinja City project budgets
- ✅ A flagship deep drill-down (Bbaale HC IV maternity ward, Kayunga) with tabbed Overview / Timeline / Related Facilities views, real PPDA procurement-timeline benchmarks, and an Advocacy & Lobbying Toolkit
- ✅ Dark mode (toggle in the top bar)
- ✅ "Demo Mode" confirmation toasts on every simulated submission (photo capture, blocker report, Parliamentary Question draft, outcome log)
- ✅ A constitutional guardrail built into both Advocacy Toolkits: MPs and District Councils are shown as performing oversight, coordination and advocacy — never as personally financing projects

### Upcoming phases

- Progressive disclosure extended to the remaining LC3/LC2/LC1 screens at the same depth as the MP/LC5 flagship chain
- Inspection workflows
- Community reporting at scale
- AI-assisted insights
- Additional institutional roles (Ministry, NPA, District Planner, CAO, RDC, Inspector, Development Partner) — deferred until real data feeds for each are confirmed, rather than demonstrated with invented information
- Mobile-first responsive refinement pass

## Data Sources

Every figure in `data.js` traces back to one of:

- NPA Annual Performance Report, FY2024/25 (October 2025)
- Kayunga District Local Government Quarterly Performance Report, FY2025/26 Q2
- Jinja District Local Government Performance Reports, FY2024/25 Q4 and FY2025/26 Q1
- Jinja City Approved Budget Estimates, FY2025/26
- PPDA Regulations on procurement timelines
- National Budget Speech, FY2026/27

Where a figure could not be confirmed from these sources, `data.js` records that gap explicitly rather than filling it in — see any field marked `notAvailable: true`.

## Design Principles

- Preserve a single shared design system
- Responsive by default
- Government-grade usability
- Accessible
- Professional
- Clean
- Maintainable
- Expandable

## Technology

- HTML5
- CSS3
- Vanilla JavaScript

(No backend. Session state lives in `sessionStorage` only, cleared when the browser tab closes — appropriate for a demo, not real authentication.)

## Running It

Open `index.html` directly in a browser, or serve the folder with any static file server. No build step, no dependencies.

## Project Vision

To become a modern Government Planning and Performance Intelligence Platform capable of supporting Parliament, Ministries, NPA, District Local Governments and Development Partners.
