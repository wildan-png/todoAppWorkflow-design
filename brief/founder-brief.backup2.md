# Founder brief — synthesized from `/brief/`

**Sources:** `brief/brief.md` (client brief for **aTodo**, dated April 30, 2026; client Wildan). **Founder clarifications** and **recommended defaults** (where labeled) are merged below.

---

## 🎯 Product & Vision

- **What is the product and what problem does it solve?**  
  **aTodo** is a simple task tracker for small freelance teams, focused on **status / progress** via a **list** and a **board**, closer to day-to-day workflow than bloated suites. It addresses **Linear, Plane, and ClickUp** being **often expensive** for this audience, with **feature sets that don’t match what they actually need** — i.e. paying for breadth they won’t use.

- **Who is the target user? (demographics, behavior, context of use)**  
  **Small-scale freelancers**, typically **1–3 people** (solo or tiny collaboration). Context: they need to see work in flight, move tasks by status, and see ownership — without enterprise-scale tooling.

- **What is the core value proposition — why would someone choose this over alternatives?**  
  A **focused** web app: **simple** task tracking (list + board + task detail), **without chasing parity** with large PM suites; **aligned with a simpler scope** than paid competitors (per brief).

- **What does success look like in 6 months? In 1 year?**  
  **6 months:** **~100 active users** (founder target).  
  **1 year:** **Founder:** no concrete goal yet — **intentionally deferred** (not blocking MVP).

---

## 🏁 Competitors & Market

- **Who are the direct competitors? (name them)**  
  **Linear**, **Plane**, and **ClickUp** (named explicitly as tools in the same problem space).

- **Who are the indirect competitors? (different product, same problem)**  
  **Founder:** no indirect competitors in mind / none identified for now.

- **What do competitors do well that we should match or beat?**  
  - **Linear:** **speed**, **minimal UI** (brief calls this **aspirational**; aTodo MVP stays smaller).  
  - **Plane:** **project/issue-style tasks** (without copying the full feature set).  
  - **ClickUp:** **depth** that users may expect there — aTodo **stays intentionally lighter** (per brief).

- **What do competitors do poorly that we can exploit?**  
  Stated gaps for this audience: **cost** (often expensive) and **mismatch** between **breadth of features** and **what small freelance teams actually need** (paying for unused breadth).

- **Is there a product the founder admires as a reference? (even outside the category)**  
  **Linear** — cited for **speed** and **minimal UI** as reference / inspiration (aspirational).

---

## ⚙️ Product Scope

- **What are the must-have features for launch (MVP)?**  
  **Surfaces (from brief)**  
  1. **Task list** — all tasks in one scannable view; quick add; open row → detail.  
  2. **Board by status** — same tasks as the list, **columns = statuses**; moving a task **changes its status** (exact gesture: drag vs menu — implementation detail).  
  3. **Task detail** — single place to edit rich fields and see full context.

  **Task model — MVP fields (brief + minimum viable shape)**  
  | Area | MVP scope |
  |------|-----------|
  | Identity | **Title** (required), stable **task id** internally. |
  | Workflow | **Status** (must align with board columns; see *Decisions* below for defaults). |
  | Content | **Description / notes** (rich text optional later; plain text OK for MVP). |
  | Attachments | **Images** on the task (see storage limits in *Decisions*). |
  | Ownership | **Assignee** tied to a **user** in the workspace (supports 1–3 people). |
  | Urgency | **Priority** (e.g. low / medium / high — exact enum flexible). |
  | Audit | **Created at** / **Updated at** (for “what’s moving” without building activity feeds). |

  **Workspace & people**  
  - **One workspace** for the tiny team is enough for MVP: **invite-only members** (small cap, e.g. ≤5 accounts, matches “1–3 people” with headroom).  
  - **Assignee** = pick from workspace members.

  **Core behaviors**  
  - **CRUD** tasks (create, read, update, delete/archive — **archive** preferred over hard delete for safety).  
  - **List ↔ board ↔ detail** stay in sync (same underlying tasks).  
  - **Donation reminder** (from business model): **non-blocking**, dismissible, no paywall.

  **Explicitly not MVP** (per brief + above)  
  - In-app AI agent; heavy automation; enterprise features; deep customization; full mobile responsive polish; docs/wiki parity; ClickUp-level configuration.

- **What is explicitly out of scope for now?**  
  - **No in-app agent** (no AI agent inside the product for V1).  
  - **Defer:** heavy automation, enterprise features, deep customization until after validation; **super simple** MVP first.  
  - **Responsive web / mobile layouts** and **multi-breakpoint polish** — **deferred to a later phase** (this phase is **desktop / fixed-layout** first).  
  - **Not** matching **full docs/wiki products** or **ClickUp-scale customization** in V1.

- **Are there any AI features planned? (copilot, agent, automation)**  
  **No in-app agent for V1** — explicitly stated. Nothing else about AI/copilot/automation beyond that.

- **What platforms? (web, iOS, Android, desktop)**  
  **Web app in the browser** (UI/frontend product). This phase is **desktop / fixed-layout**; responsive layouts are **not** in this phase.

---

## 🎨 Design Direction

- **Is there any existing brand identity? (logo, colors, fonts)**  
  **None** (no locked logo, palette, or type system). UI direction instead: **dark**, **compact**, **clean**, **professional** (founder preference).

- **What visual style feels right? (references, adjectives)**  
  **Founder:** **dark**, **compact**, **clean**, **professional**. Still aligned with brief’s **Linear**-like aspiration: **speed**, **minimal UI**; MVP **stays smaller** than Linear’s scope. **Plane** / **ClickUp** in the brief are mainly product positioning, not visual specs.

- **What should the product feel like to use? (fast, trustworthy, playful, professional)**  
  From brief: **clear**, **obvious picture** of status and ownership; **simple**; **minimal** (Linear reference). **Founder:** **professional**, **clean**, **compact** (dense layout), **dark** theme.

- **Is there anything design-wise the founder dislikes or wants to avoid?**  
  **Founder:** avoid a **raw, generic “blank template”** look (unstyled defaults that feel like a throwaway demo). **At minimum** use a **Tailwind-first** system (this repo: **Tailwind CSS 4** + component primitives) so spacing, type, and **dark** density are **intentional and consistent** — not naked HTML defaults.

---

## 🔧 Technical Constraints

- **Has a tech stack been decided?**  
  **UI (this codebase — decided):** **Next.js** (16.x), **React** (19.x), **TypeScript**, **Tailwind CSS** (v4), **shadcn**-style / shared UI primitives (`package.json`).  
  **Backend / auth / DB (recommended default — confirm when wiring):** keep a **clear HTTP or typed server boundary** (e.g. **Route Handlers** or a small **REST** surface) + **relational DB** (e.g. **Postgres**) + **Auth.js–style session auth** (email magic link and/or OAuth). Swap later without rewriting the whole UI if the **contract** stays stable.

- **Are there required integrations? (APIs, third-party tools)**  
  **Founder:** **none required at launch.**  
  **Engineering posture:** build **integration-ready** — **env-driven config**, stable **API shapes**, hooks for future **webhooks** or **payments/donations** provider without redesigning core task APIs.

- **Any accessibility or compliance requirements?**  
  **Recommended default (no regulated domain stated):** treat **WCAG 2.1 Level AA** as the **design target** for core flows (list, board, task detail, auth if present): **keyboard** operation, visible **focus**, **labels** on controls, sensible **heading/landmark** structure. **Compliance:** no **HIPAA / PCI** scope implied for a generic task app unless you add billing or health data later — **none required for MVP** unless product direction changes. Use **Storybook a11y** checks where components are reviewed.

---

## 💰 Business Context

- **What is the monetization model?**  
  **Core product stays free.** **Optional donations** — e.g. a **popup reminder** to support the project; **must not block usage** — **no forced payment**; users **can dismiss and continue**; **gentle reminder**, **opt-in support**, **no paywall** on core features.

- **Who are the stakeholders involved in design decisions?**  
  **Founder only — Wildan** (sole decision-maker).

---

## Decisions & definitions (plain English)

These used to be “open questions” in `brief.md`. Short explanations + **recommended defaults** you can change anytime before build locks.

1. **“Backend / API contract and auth”**  
   - **Means:** Where tasks live on a server, and how a user **logs in** so assignees and data are private to your team.  
   - **Recommended default:** **Postgres** + **session-based auth** (e.g. Auth.js pattern) + **CRUD API** for tasks/workspaces; Next.js owns both UI and server routes in one deployable app **or** split later if the API contract stays the same.

2. **“Image storage (upload flow, limits)”**  
   - **Means:** Images shouldn’t live only in the browser — they need a **file store** and rules so costs and abuse stay bounded.  
   - **Recommended default:** **S3-compatible bucket** (e.g. **Cloudflare R2**); **client uploads via presigned URL**; **limits** e.g. **5 MB per file**, types **JPEG / PNG / WebP**, **N images per task** cap (e.g. **10**) until you have real usage data.

3. **“Exact default statuses / columns on the board”**  
   - **Means:** The **column titles** on the board and the **status** field on each task must match.  
   - **Recommended default (simple freelancer flow):** **To do** → **In progress** → **Done**. (Optional later: add **Blocked** or **Client review** if users ask — not required for MVP.)

---

*Contact: wildan*
