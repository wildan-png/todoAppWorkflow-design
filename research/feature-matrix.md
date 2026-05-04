# Feature matrix — aTodo vs competitors

Source basis: `research/competitor-analysis.md` + `research/competitor-ux-teardown.md` (plus MVP constraints from founder brief).  
Legend: ✅ = has it, ❌ = does not have it, 🟡 = partial/limited.

## 1) Feature comparison table

| Feature | aTodo (our product) | Linear | Plane | ClickUp |
|---|---:|---:|---:|---:|
| Task list view | ✅ | ✅ | ✅ | ✅ |
| Board by status | ✅ | ✅ | ✅ | ✅ |
| Task detail page/panel | ✅ | ✅ | ✅ | ✅ |
| Task title + description | ✅ | ✅ | ✅ | ✅ |
| Assignee | ✅ | ✅ | ✅ | ✅ |
| Priority | ✅ | ✅ | ✅ | ✅ |
| Labels/tags | 🟡 | ✅ | ✅ | ✅ |
| Due date | ✅ | ✅ | ✅ | ✅ |
| Image/file attachment | ✅ | ✅ | ✅ | ✅ |
| Comments/activity trail | 🟡 | ✅ | ✅ | ✅ |
| Invite team members | ✅ | ✅ | ✅ | ✅ |
| Role/permission selection | ❌ | 🟡 | 🟡 | ✅ |
| Global search / command search | ❌ | ✅ | ✅ | ✅ |
| Multiple views beyond list+board (calendar/table/gantt/timeline) | ❌ | 🟡 | ✅ | ✅ |
| Cycles / sprint planning | ❌ | ✅ | ✅ | 🟡 |
| Project roadmap / milestones | ❌ | ✅ | ✅ | 🟡 |
| Docs / wiki | ❌ | ❌ | ✅ | ✅ |
| Chat / channels / DMs | ❌ | ❌ | ❌ | ✅ |
| Dashboards / analytics | ❌ | 🟡 | 🟡 | ✅ |
| Time tracking / estimates | ❌ | ❌ | ❌ | ✅ |
| Automation rules | ❌ | 🟡 | 🟡 | ✅ |
| In-app AI assistant/agent | ❌ | 🟡 | ✅ | ✅ |
| Pricing clarity / no upsell friction | ✅ | 🟡 | 🟡 | ❌ |
| Low setup complexity for 1–3 users | ✅ | 🟡 | ❌ | ❌ |

Notes:
- `aTodo` values are target-state from current MVP scope (list + board + detail + core task fields + invite-only small team).
- `🟡` means feature exists but with constraints, weaker UX, or narrower scope in available evidence.

## 2) Feature frequency score (competitor prevalence)

Frequency counts are across **competitors only** (Linear, Plane, ClickUp), not including aTodo.

| Feature | Competitors with feature (0-3) | Frequency | Read |
|---|---:|---:|---|
| Task list view | 3 | 100% | **Table stakes** |
| Board by status | 3 | 100% | **Table stakes** |
| Task detail page/panel | 3 | 100% | **Table stakes** |
| Title + description | 3 | 100% | **Table stakes** |
| Assignee | 3 | 100% | **Table stakes** |
| Priority | 3 | 100% | **Table stakes** |
| Due date | 3 | 100% | **Table stakes** |
| Attachments | 3 | 100% | **Table stakes** |
| Comments/activity | 3 | 100% | **Table stakes** |
| Invite members | 3 | 100% | **Table stakes** |
| Global search | 3 | 100% | **Table stakes** |
| Extra views (calendar/table/gantt/etc.) | 3 | 100% | Common in mature suites (not MVP-required) |
| Cycles/sprints | 3 | 100% | Common in PM suites; optional for our niche |
| Role/permissions | 3 | 100% | Mature-suite baseline |
| Dashboards/analytics | 3 | 100% | Mature-suite baseline |
| Automation | 3 | 100% | Mature-suite baseline |
| AI assistant/agent | 3 | 100% | Category trend, not user-universal need |
| Roadmaps/milestones | 3 | 100% | Product-team oriented |
| Docs/wiki | 2 | 67% | Strong secondary feature |
| Chat/channels/DMs | 1 | 33% | Potential differentiator to **exclude** |
| Time tracking | 1 | 33% | Potential differentiator to **exclude** |

Interpretation:
- **Must-have at launch for our market:** only high-frequency features that also map to freelancer core loop (capture → assign → prioritize → progress → discuss).
- **Do not auto-include** just because frequency is high (e.g., AI, automations, roadmaps): frequency here reflects competitor breadth, not small-team fit.

## 3) Feature gap list (user demand where no competitor does well)

| Gap feature / need | Why users want it | Why competitors fail (from research) | Opportunity for aTodo |
|---|---|---|---|
| Fast core workflow with low cognitive load | Small teams want to manage work, not configure systems | ClickUp overload; Plane concept-heavy; Linear can feel dev-centric | One workspace, 3 statuses, single create path, minimal chrome |
| Predictable free-core pricing/trust | Users dislike seat traps, AI upsells, billing surprises | ClickUp billing pain; Plane cloud/self-host confusion; AI often monetized add-on | Donation model + plain pricing language + no gating on core loop |
| Reliable perceived performance + sync confidence | Users need trust that task state is current | Lag/sync complaints (esp. ClickUp, larger Plane setups); parity concerns on mobile | Lightweight scope + clear save states + fewer moving modules |
| Invite/join clarity for tiny teams | Freelancers need frictionless collaborator onboarding | Role/permission wording can be enterprise-heavy; join/invite ambiguity in flows | Invite by email/link, clear inviter context, simple role model |
| Calm onboarding that gets to first task fast | Users want value before setup fatigue | Feature shopping questionnaires and multi-step profiling add setup tax | <=2 setup steps before first task; optional invite later |

## 4) MVP candidates (high-value + launch-feasible)

| MVP candidate | User value | Build complexity (launch) | Why now |
|---|---|---|---|
| List + Board parity on same dataset | Core daily workflow visibility | Low | Foundation of product promise |
| Task detail with title, notes, assignee, priority, due date, images | Covers 90% of freelancer execution needs | Low-Med | Directly replaces ad-hoc trackers |
| Quick add + keyboard shortcut for new task | Faster capture loop | Low | Desktop-first leverage |
| Status move via board drag (or inline status menu) | Progress becomes obvious and tactile | Med | Makes board materially useful, not decorative |
| Lightweight comments/activity on task | Collaboration context for 1–3 people | Med | Needed once inviting teammates |
| Invite teammate (email + share link) | Enables real team usage, not solo-only | Med | Critical for target segment |
| Clear empty states + first-task guidance | Reduces setup confusion | Low | Immediate activation lift |
| Non-blocking donation reminder | Aligns business model without paywall friction | Low | Strategic differentiation from seat-gating |
| Basic search/filter (status + assignee) | Findability without heavy views | Low-Med | Keeps interface simple while scaling task count |

Not MVP (defer): automations, roadmap/milestones, cycles, docs/wiki, chat, dashboards, time tracking, in-app AI.
