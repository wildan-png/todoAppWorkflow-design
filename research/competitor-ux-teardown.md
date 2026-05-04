# Competitor UX teardown (screenshot-backed)

**Sources:** `assets/competitor-screens/` (Linear, Plane, ClickUp — **onboarding**, **view switching**, **invite/join**, core task flows), cross-checked with `research/competitor-analysis.md` and `brief/founder-brief.md`.  
**Lens:** **aTodo** — desktop-first MVP: **list + board + task detail**, **1–3 person** freelance teams, **no parity** with PM suites.

---

## 1. Feature inventory

Deduped features **visible or strongly implied** across the captured flows (not an exhaustive product spec).

### Cross-cutting (2+ products)

| Feature area | Linear | Plane | ClickUp |
|--------------|--------|-------|---------|
| Issue/task/work item with human-readable ID | ✓ | ✓ | ✓ (contextual) |
| Title + description (rich text) | ✓ | ✓ | ✓ |
| Status / workflow state | ✓ | ✓ | ✓ |
| Priority | ✓ | ✓ | ✓ |
| Assignee(s) | ✓ | ✓ | ✓ |
| Labels / tags | ✓ | ✓ | ✓ |
| Due dates (range / start–due) | ✓ | ✓ | ✓ |
| Attachments / files | ✓ | ✓ | ✓ |
| Comments + activity / audit trail | ✓ | ✓ | ✓ |
| Sub-work / sub-issues / checklists | ✓ | ✓ | ✓ |
| Links between items / relations | ✓ | ✓ | ✓ |
| List view grouped by status | ✓ | ✓ | ✓ |
| Multiple data views (board, table, calendar, Gantt, etc.) | ✓ (list + **board**; **Display** toggles) | ✓ (list, board, **spreadsheet/table**, calendar, Gantt icons) | ✓ (incl. **board** flow) |
| Filter + display controls | ✓ | ✓ | ✓ |
| Favorites / stars | ✓ | — (stars elsewhere in product) | ✓ |
| Global search (⌘K pattern) | ✓ | ✓ | ✓ |
| Workspace / project hierarchy | ✓ | ✓ | ✓ |
| Invite / join workspace | ✓ (**Invite co-workers**: comma-separated emails, **invite link**, **Continue** without sending) | ✓ (**Join a workspace**: invited email shown, workspace card + **role**, Accept / Go home) | ✓ (**Invite people** modal: **free seats** banner, **Invite as** role + workspace scope copy) |
| Onboarding / empty states / templates | ✓ (multi-step + **keyboard cues**) | ✓ (goals survey; **signup friction**) | ✓ (**module picker**, landing checklist) |
| AI surfacing (assistant, standup, inline on tasks) | — in captures | ✓ (Pi, inline AI) | ✓ (Brain, Ask AI, task AI) |
| Trial / upgrade indicators | ✓ | ✓ | ✓ |

### Linear-specific (from captures)

- **Teams** under workspace; **Issues** → Active / Backlog.
- **Cycles** (sprints) under team.
- **Projects** with health, lead, target dates, milestones, **Overview vs Issues** tabs, progress language.
- **Workspace Views** vs **team Views** (parallel IA); **All issues**-style cross-cutting list (from board captures).
- **GitHub** link, import, invite from sidebar.
- Issue creation modal: **Create more** toggle; metadata pills (status, priority, assignee, labels); expand/full-screen on modal.
- Issue detail: properties column; **Project** + **Cycle** + **Milestone** on issue; threaded discussion + reactions; mixed system + human activity.
- **List ↔ Board:** Toolbar **Display** menu — List/Board switch, **grouping** (e.g. status), **ordering**, completed/sub-issue visibility, **per-field column toggles** (priority, ID, labels, project, dates, assignee, etc.); column **+** add issue.
- **Onboarding:** Marketing landing (product preview); **email login code** step (monospace code field; “link” vs “code” wording); **Create workspace** (name → URL slug, **region locked forever** warning, company size + role); completion screen pushes **`c`** for new issue and **`?`** for shortcuts.
- **Invite:** Dedicated onboarding step **Invite co-workers** (step ~5/7): bulk email field, **Invite with link**, **Send invites**, **Continue** to skip — team-first positioning without hard-blocking.

### Plane-specific (from captures)

- **Dual rail:** global icon strip (Projects, Wiki, Pi) + contextual sidebar.
- **Home** dashboard: **Ask Pi**, quickstart checklist, quicklinks, widgets.
- Marketing preview surfaces **Initiatives**, **Teamspaces**, **Intake**, **Workflows and Approvals** as peer modules (alongside Projects / Wiki / Pi).
- Per-project: **Overview**, **Work items**, **Cycles**, **Modules**, **Views**, **Pages**.
- Overview: **progress bar** by state (Backlog / Unstarted / Started / Completed / Cancelled) with counts/%.
- Work item create: **Create more**; state, priority, assignees, labels, dates, **cycle**, **module**, **parent**; AI / “I’m feeling lucky” in description.
- Work item detail: parent hint, sub-items, relations, links, attach, **link pages**; properties panel; **Analytics** on work list.
- **View switching:** Same **Work items** context — **spreadsheet/table** layout with sortable column headers (state, priority, assignees, labels, modules); icon strip for list / board / calendar / Gantt.
- **Onboarding:** Sign up — Google/GitHub + email with **unique code** on the **same** screen as email (early exposure); goals step “What brings you to Plane?” — subhead mentions **team size** but **no team-size control** on that screen (copy/UX mismatch).
- **Join (invitee):** **Join a workspace** screen — copy that someone invited you; **single workspace card** with name + **Member** role; **Accept & Join** + **Go home** (capture shows primary CTA possibly disabled until selection — ambiguity if only one card).

### ClickUp-specific (from captures)

- **Far-left app rail:** Home, Planner, **Brain**, Dashboards, Teams, More.
- **Spaces → folders/lists** (deep tree); **Channels** + **DMs** in sidebar.
- **Home** dashboard: Recents, My Work (time buckets: Today, Overdue, Next, Unscheduled), Assigned comments, **AI StandUp**.
- **Create** menu: many object types (task, list, doc, etc.) + **keyboard hints**.
- **Space** creation: icon, description, **Make private**, share picker, templates.
- List context: **many view tabs** (List, Board, Team, Timeline, Activity, Workload, Mind Map, Table…); grouping by status; custom fields / statuses / automations prompts; **Agents**, **Automate**, **Ask AI** in header.
- **Board view:** Color-coded **status columns**, dense **cards** (avatars, relative dates, priority flags, tags, subtask progress, attachments); **Group / Subtasks / Sort / Filter** above board; **Add task** per column.
- Task create: list/context selectors; templates; rich metadata row.
- Task detail: **time estimate**, sprint points, **track time**; **Brain** prompts; related tasks; **ClickBot** / automation line in activity; comment bar mentions **@Brain**.
- **Onboarding:** Landing **“everything app”** + hero **workspace module checklist** (tasks, chat, AI, sprints, time tracking, docs, goals, dashboards, whiteboards, forms, automations…); **email OTP** (4 boxes), **Resend**, loading on submit; mid-flow **“Which features are you interested in?”** grid (~**18** toggles) with reassurance that **all features remain available** — still high choice load.
- **Invite:** **Invite people** modal from global **Invite** — email field; **“Invite members for FREE”** + **N seats available**; **Invite as** dropdown (e.g. **Member** + explainer: access to **public** workspace items).

---

## 2. Sitemap hypothesis (IA / navigation)

### Linear (inferred)

```
Workspace (switcher)
├── Inbox
├── My issues
├── Projects          [workspace-level]
├── Views             [workspace-level]
├── Teams
│   └── Team (e.g. SLMobbin)
│       ├── Issues → Active | Backlog
│       ├── Cycles → Upcoming | …
│       ├── Projects  [team-level]
│       └── Views     [team-level]
├── Import / Invite / Link GitHub
└── Issue detail      [Team > ISSUE-ID] + properties (project, cycle, milestone, …)
```

**Navigation tension:** duplicate **Projects** / **Views** at workspace vs team — power users learn it; new users can hesitate on “where work lives.”

### Plane (inferred)

```
Global rail: Projects | Wiki | Pi | Settings | Help
Workspace sidebar:
├── Home
├── Inbox
├── Your work
├── Projects → [Project]
│   ├── Overview
│   ├── Work items      [list | board | calendar | spreadsheet | gantt]
│   ├── Cycles
│   ├── Modules
│   ├── Views
│   └── Pages
└── …
Work item detail      [Project > Work items > ID]
```

**Navigation tension:** two sidebars + **Cycles vs Modules vs Views vs Pages** — clear for PM-savvy teams; heavy for “just tasks” users.

### ClickUp (inferred)

```
App rail: Home | Planner | Brain | Dashboards | Teams | …
Primary sidebar:
├── Inbox / Replies / Assigned comments
├── My Tasks ( Assigned to me | Today & Overdue | … )
├── Favorites
├── Spaces → [Space] → [Folder/List/Sections]
├── Channels
└── DMs
Context main:
├── Home dashboard (widgets)
├── Space/List: views List | Board | Calendar | Gantt | Table | …
├── Dashboards directory (templates, privacy, recents)
└── Task detail (full page) + breadcrumbs
```

**Navigation tension:** **Space/Folder/List** depth + **personal vs space** entry points + chat — maximum flexibility, maximum orientation cost.

---

## 3. UX weakness map

| Area | Linear | Plane | ClickUp |
|------|--------|-------|---------|
| **Auth / onboarding** | Login-code step: **no visible Resend** on captured screen; **region irreversible** pressure; **company size / role** feels like product analytics not user value | Sign-up shows **email + unique code together** (can confuse before mail arrives); goals screen **copy promises team size**, UI doesn’t collect it | **~18 feature tiles** + hero module checklist — breadth signaled early; OTP verify: **Change email** not obvious on capture |
| **Invite / join** | Team-first copy; **skippable**; **link invite** alternative | **Join** UI light on **who** invited you; **Accept** disabled state may confuse | **Seat math** + **public vs private** permission language early |
| **First-run / mental model** | Team/issue vocabulary and duplicate workspace/team nav | Many parallel concepts (Cycles, Modules, Views, Pages, Pi); marketing adds Initiatives / Intake / Workflows | “Space vs List vs Folder” and huge Create menu |
| **Density vs focus** | Toolbar/icons without labels; metadata easy to under-read in list rows | Double sidebar reduces canvas; icon-only row chrome needs tooltips | Stack of bars (tabs, filters, import/custom-field prompts); content starts far down |
| **View switching** | **Display** popover can **cover** board columns / right-side rows while adjusting toggles | Spreadsheet mode adds column chrome — powerful but more “database” than task board | Board cards **visually loud** (avatars, flags, tags, thumbs); same entity appears under **Spaces** and **Channels** |
| **Empty & gated states** | Empty project copy is strong; populated project still “PM-shaped” | Overview sparse; **properties panel gated** (“enable project grouping”) feels like paywall-adjacent friction | Empty groups OK; dashboard empty cards weakly actionable; favorites/recents duplication on dashboards |
| **Consistency / semantics** | Activity mixes bot + human; long threads get noisy | Due-date emphasis (e.g. red) vs meaning unclear without legend | Private/share dropdown overlaps actions; white modal on dark chrome |
| **Power-user vs casual** | Excellent for rapid issue entry; assumes issue-ID mental model | Strong parity with Linear-style create; AI buttons may distract | Everything available; analysis paralysis |
| **Collaboration scope** | Comments + reactions; integrations implied | Standard comments/activity | Chat + comments + AI @mentions — many channels |
| **Performance (from research, not screenshots)** | Mobile parity complaints | Heavier workspaces | Lag / sync themes at scale |

**Missing or weak states (inferred from captures):** explicit **errors** (failed save, conflict), **offline**, **permission denied** mid-flow, **billing limit** UX — not visible in these flows; assume enterprise tools bury them in settings.

---

## 4. Design patterns: adopt vs avoid

### Worth adopting (for aTodo’s scope)

1. **Focused create modal** — title first, metadata as compact chips/pills (Linear / Plane); optional **Create more** for fast backlog capture.
2. **Breadcrumbs** `Workspace / List or Board / Task` — cheap orientation without deep hierarchy.
3. **Right-rail or dedicated detail layout** — description + activity center, editable properties grouped (Linear / Plane task detail pattern).
4. **Clear group headers by status** in list (Plane / ClickUp list pattern) — aligns with board columns.
5. **Disciplined typography and spacing** — Linear-level calm for desktop MVP.
6. **Progress-by-status summary** (Plane overview bar) — *only if* we keep a single project/workspace summary; skip if it bloats MVP.
7. **Keyboard shortcut hints** on primary actions (ClickUp) — small win for desktop power users.
8. **View-level density control** (Linear **Display** chips: show/hide columns on list **and** board) — adopt *lightly* post-MVP if users ask for column noise control; default stays minimal for freelancers.

### Use sparingly or defer

- **Dual global sidebars** (Plane) — costs horizontal space; prefer one nav + content.
- **Parallel “workspace vs team” duplicates** (Linear) — aTodo: **one workspace** avoids this.
- **AI-first dashboard real estate** (Plane Home, ClickUp Brain strip) — conflicts with “no agent V1”; keep donations/onboarding minimal.
- **Omnibus Create** (ClickUp) — split “new task” from structural actions or hide structure entirely for MVP.
- **View proliferation** (ClickUp / Plane) — MVP: **list + board only**; don’t imply calendar/Gantt parity.
- **Pre-product module questionnaires** (ClickUp 18-tile step; Plane’s broad goals) — for aTodo, **≤2 steps** to first task: workspace name + optional invite, no feature shopping.

### Avoid for aTodo positioning

- **Space/Folder/List** taxonomies as required setup.
- **Chat + tasks** in the same nav tier for v1.
- **Automation/agent CTAs** on every task surface.

---

## 5. Our opportunity — UX moves that clearly beat these flows (for micro freelance teams)

Aligned with `research/competitor-analysis.md` **opportunity gaps** and screenshot friction:

1. **Zero hierarchy tax** — No Space/Folder/List/Team maze: land on **one task surface** (list + board toggle) with optional project label *inside* the task, not a navigation tree.
2. **Single creation path** — One **Add task** / shortcut; no 10-line Create menu; no “what object am I making?” moment.
3. **Default workflow only** — Three statuses (per brief); **no** custom-field / automation / import banner consuming vertical space on day one.
4. **Honest density** — Linear-like speed and clarity **without** issue IDs, cycles, milestones, or Git semantics unless you add them later deliberately.
5. **Properties that match freelancer reality** — Assignee, priority, due, images, notes — **no** time tracking, sprint points, modules, or wiki unless scoped later.
6. **Transparent free core** — No trial countdown framing as default anxiety; no gated “enable grouping” for basic metadata (Plane pain).
7. **Calm home** — Skip AI standup and widget dashboards for MVP; optional **“Your tasks”** slice is enough.
8. **Predictable detail** — One full detail view; avoid mixing four panes + omnibus headers (ClickUp task).
9. **Onboarding that doesn’t sell the universe** — No irreversible-region drama at freelancer scale (or hide behind advanced); teach **one** shortcut (e.g. **N** for new task) only if you ship keyboard UX; **Resend code** + **change email** always visible in auth.
10. **Invite without enterprise semantics** — Skip **seat inventory** and “public items in workspace” copy for 1–3 people; show **inviter name** + single role (member) + accept; optional **link invite** like Linear.

**Net:** Be **narrower than Plane**, **flatter than ClickUp**, **less ceremonious than Linear** — same core loop (capture → assign → status → discuss) with **fewer nouns** and **fewer rails**.

---

## Appendix: Screenshot coverage (what these flows do / don’t prove)

| Competitor | Captured flows | Gaps for future captures |
|------------|----------------|---------------------------|
| Linear | New issue, new project, issue detail, **onboarding**, **list + board + Display**, **inviting a team member** | Settings, cycles *execution*, mobile |
| Plane | Home, overview, work items, create work item, work item detail, **onboarding**, **list vs spreadsheet**, **joining a workspace** | Kanban **in motion**, Gantt, cycles/modules **setup**, wiki editing |
| ClickUp | Home, create space, list + chrome, create task, task detail, dashboards, **onboarding**, **board**, **inviting a member** | Timeline/workload/mind map, automation builder, mobile |

Folder reference: `linear/Linear Web Onboarding`, `linear/Linear Web Switching to board view`, `linear/Linear Web Inviting a team member`, `plane/Plane Web Onboarding`, `plane/Plane Web Switching view`, `plane/Plane Web Joining a workspace`, `klickup/ClickUp Web Onboarding`, `klickup/ClickUp Web Switching task views`, `klickup/ClickUp Web Inviting a member`, plus create/detail/dashboard flows.

---

*Screenshot analysis — April 30, 2026. Includes onboarding, view-switch, and invite/join captures.*
