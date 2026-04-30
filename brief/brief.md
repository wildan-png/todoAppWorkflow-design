# aTodo — Client Brief

**Date**: April 30, 2026
**Client**: Wildan
**Project type**: UI / frontend — product implemented in the browser; no separate Figma file required (design lives in code / components).

---

## Background

For small-scale or individual freelance teams, tools like Linear, Plane, and ClickUp are often expensive, and their feature sets don’t match what this audience actually needs — paying for breadth they won’t use.

aTodo addresses that gap: a simple task tracker focused on status / progress (list + board), closer to the workflow than bloated suites, without chasing parity.

---

## What We're Building

A focused web app with three main surfaces:

**1. Task list**

A clear list of tasks so freelancers can see everything in flight at a glance, add items quickly, and open a task for more detail.

**2. Board by status**

A board grouped by status so the team can see how work is moving across stages. This complements the list: same tasks, status-oriented view.

**3. Task detail**

Each task supports editable description / notes, image attachments, priority, assignee / user assignment, and other core fields needed for the MVP. The goal is an obvious picture of where each task stands and who owns it.

This phase targets a desktop / fixed-layout MVP: responsive layout and multi-breakpoint polish are explicitly deferred to a later phase.

---

## Target Users

Small-scale freelancers, typically 1–3 people (solo or tiny collaboration).

---

## Business Model

The core product stays free to use, aligned with a simpler scope than paid competitors.

Monetization is optional donations: e.g. a popup reminder to support the project. It must not block usage — no forced payment; users can dismiss and continue. Gentle reminder, opt-in support, no paywall on core features.

---

## References / Inspiration

- **Linear** — speed, minimal UI (aspirational; aTodo MVP stays smaller).
- **Plane** — project/issue-style tasks without copying the full feature set.
- **ClickUp** — depth users may expect there; aTodo stays intentionally lighter.

---

## What We're NOT Building (V1 scope)

- No in-app agent (no AI agent inside the product for V1).
- MVP first — super simple: defer heavy automation, enterprise features, and deep customization until after validation.
- Responsive web / mobile layouts: out of scope for this phase; next phase (desktop / non-responsive delivery first).
- Not matching full docs/wiki products or ClickUp-scale customization in V1.

---

## Open Questions

- Backend / API contract and auth.
- Image storage (upload flow, limits).
- Exact default statuses / columns on the board.

---

## Deliverables Expected from Agency

- Frontend ready to integrate (with backend/API when wired): implementation-ready UI in code — not a Figma-first handoff.

---

*Contact: wildan*
