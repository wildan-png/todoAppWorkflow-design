# User journeys — aTodo

## Part A — App-level journeys (persona × lifecycle)

### Journey: Jordan Reyes — Keep client deliverables visible with owner + status without seat-tax overhead

| Stage | Touchpoint | Action | Thought / Emotion | Pain to avoid | Opportunity |
|---|---|---|---|---|---|
| Awareness | Pricing comparison moment while evaluating Linear/ClickUp alternatives | Scans positioning, pricing logic, and product scope claims | "I need clarity fast, not another expensive system." Cautious but hopeful | Seat-based pricing shock for short-term contractors; vague value proposition | Lead with free-core collaboration and anti-bloat promise in the first screen/message |
| Onboarding | Workspace creation + first-task setup flow | Creates workspace, adds first task, sets assignee/status in <=2 steps | "If this takes more than a few minutes, I am out." Time-pressure mindset | Long setup, forced hierarchy design, too many required fields | One-path onboarding: workspace name -> first task -> visible list/board parity immediately |
| First value | Unified list with status + assignee visible | Adds several active client tasks via quick add and inline status update | Relief: "Now I can see everything in one place." | Reconstructing work from Slack/email/spreadsheets; hidden ownership | Dense default list sorted for triage (status/owner/priority visible by default) |
| Core loop | Board/list/detail workflow during daily triage and handoffs | Moves tasks across statuses, assigns contractor, adds context in task detail/comments | "Good, I can answer who owns what in seconds." Confident, in control | View mismatch across list/board/detail; ambiguous invite/join state | Keep board/list/detail fully synced and frictionless invite flow for rotating collaborators |
| Power use | Pre-milestone coordination window (24–48h before deadline/invoice) | Filters by assignee + priority, checks due dates, uploads proof attachments, resolves blockers | Focused urgency: "No surprises before client review." | Last-minute chaos, stale task states, lost context in chat threads | Deadline mode cues (e.g., smart sorting/highlight) that accelerate closure without adding complexity |
| Advocacy | Post-delivery reflection and peer/tool recommendation moments | Keeps using product for next engagement; recommends to other independents | "This protects my margin and looks professional." Pride + trust | Feeling "cheap tool" stigma or design that looks generic/unpolished | Reinforce professional aesthetic and simple reliability as a differentiator for solo+contractor teams |

### Journey: Priya Nair — Run a calm, professional delivery flow without all-in-one PM bloat

| Stage | Touchpoint | Action | Thought / Emotion | Pain to avoid | Opportunity |
|---|---|---|---|---|---|
| Awareness | Frustration point in bloated PM workspace (noise/slow loads) | Searches for simpler list+board alternative for a 2-person studio | "We need less software, more shipping." Frustrated by admin overhead | Notification overload, performance lag, enterprise-style terminology | Message around "list + board + detail only" and "no workspace architecture project" |
| Onboarding | First-day setup for studio workspace | Creates workspace, invites cofounder/freelancer, seeds active client tasks | "Please don’t make me configure Spaces/Folders/Lists again." | Forced structural setup and unclear role/invite states | Immediate invite/join clarity and pre-opinionated defaults (To do/In progress/Done) |
| First value | Board by status with clear ownership | Uses board to visualize pipeline; checks that list/detail reflect same updates | "This is the exact level of structure we need." Calm confidence | Inconsistent data between views; unclear responsibility per card | Make ownership and status chips prominent in every view to reduce coordination chatter |
| Core loop | Daily stand-up glance + review-week crunch | Moves cards, updates assignees/priority/due dates, adds image references in task detail | "Now deadline conversations are objective, not memory-based." | Slack as source of truth; missing visual context for creative work | Attachment-first detail experience for creative assets and fast async comments trail |
| Power use | 48h pre-client review and invoice checkpoint | Runs assignee-focused board/list scans, closes in-progress drift, confirms done criteria | Controlled urgency: "We can walk into client review prepared." | Last-minute rework from hidden blockers; too many in-progress items | Lightweight WIP/risk signaling to prevent overload while preserving a simple UI |
| Advocacy | Client-facing professionalism and peer studio recommendations | Continues workflow, shares tool with other tiny agencies/studios | "This makes us look organized without enterprise baggage." | Tool that feels amateur or too rigid for creative teams | Differentiate with polished, dense visual design that signals competence to clients |

### Journey: Miguel Santos — Get issue-like clarity for tiny team execution without dev-tool ceremony

| Stage | Touchpoint | Action | Thought / Emotion | Pain to avoid | Opportunity |
|---|---|---|---|---|---|
| Awareness | Comparison between dev-centric tools and lightweight alternatives | Evaluates whether product keeps Linear-like speed but strips ceremony | "I want speed and clarity, not backlog religion." Skeptical, technical | Engineering-heavy workflows, pricing friction for half-time collaborators | Position as "fast task tracking for micro teams" with explicit no-sprint/no-roadmap surface |
| Onboarding | Minimal desktop setup and first collaborative invite | Creates workspace, enters patch/client tasks, invites one collaborator | "If setup is instant, this can replace my spreadsheet." | Slow onboarding, mandatory process config, unclear permissions | Fast path to first status move and clear owner/member model without extra governance |
| First value | List triage at start of deep-work block | Sorts by priority/due date, verifies assignee/status, picks next execution thread | "Great, I can start work now." Focused momentum | Morning archaeology across Discord/Slack/email; weak status semantics in spreadsheets | High-density list defaults optimized for quick prioritization and immediate action |
| Core loop | Handoff and execution cycle across list/board/detail | Updates status via drag/drop, adds screenshots in detail, leaves async comments for partner | "We stay aligned without meetings." Efficient, low-friction collaboration | Sync drift between screens; context split between tools | Guarantee parity sync and make status transitions feel instant for context preservation |
| Power use | Pre-deploy/pre-invoice quality pass | Uses filters/grouping by assignee to validate done vs blocked vs in review | "No ambiguity before we ship or bill." High-alert but controlled | Hidden blockers, stale ownership, missing evidence of completion | Add crisp blocker visibility patterns without introducing enterprise dashboards |
| Advocacy | Community conversations with other dev-founders/freelancers | Recommends tool as practical middle ground between Trello simplicity and dev PM overhead | "This is the right-sized stack for tiny teams." | Perception that product is either too basic or too process-heavy | Own the "micro-team execution OS" narrative: fast, calm, and cost-fair collaboration |

## Part B — Feature-level journeys (every feature)

### Feature: Unified task list view — Task Inbox/List

- **Label:** core
- **Primary persona:** Jordan Reyes — morning triage across clients; list is the default throughput surface.
- **JTBD refs:** #2 (one desktop view, status+owner, not Slack/spreadsheet archaeology); #3 (focused scope vs bloated PM)

| Stage | Touchpoint | Action | Thought / Emotion | Pain to avoid | Opportunity |
|---|---|---|---|---|---|
| Trigger | Lands on main workspace after onboarding or bookmark | Scrolls to see all open work in one columnar list | "Show me the honest queue." | Empty chrome with no tasks; having to hunt multiple projects | Default land on dense list with status + assignee visible without configuration |
| Orient | List header, sort indicators, row chips | Scans columns for title, status, assignee, priority | "I can parse this in one pass." | Hidden ownership; cryptic status icons | Opinionated column visibility matching founder brief (dense, dark, professional) |
| Act | List row hover / row menu | Opens detail when needed; otherwise stays in list for triage | "Stay shallow until I must go deep." | Forced navigation to edit trivial fields | Inline affordances for status (see inline status feature) and clear row click target for detail |
| Confirm | Same list after teammate moves a card on board | Sees status/assignee update without refresh | "We share one truth." | Stale row after board update (parity failure) | Real-time or instant revalidation; same task ids across views |
| Recover / Next | Mis-sorted or overwhelming list | Changes sort (see sort feature) or applies filters | "Let me narrow without losing context." | Dead end after filter (zero results with no guidance) | Clear empty filter state + one-click reset |

### Feature: Quick add task — Task Inbox/List

- **Label:** core
- **Primary persona:** Priya Nair — captures client asks mid-review without breaking flow.
- **JTBD refs:** #2 (fast capture at start of day); #3 (low ceremony vs enterprise create dialogs)

| Stage | Touchpoint | Action | Thought / Emotion | Pain to avoid | Opportunity |
|---|---|---|---|---|---|
| Trigger | List top bar or persistent "+" | Decides to log new deliverable while on a call | "If I don’t capture this now, it lives in Slack." | Buried create button; modal with 12 fields | Single obvious quick-add anchored to list |
| Orient | Quick-add popover / inline row | Sees title required; defaults for status/assignee | "Defaults should match how we work." | Forcing project/folder picks (out of scope guardrail) | Default To do + self assign when solo; minimal required fields |
| Act | Quick-add surface | Types title, optional assignee/status, commits | "One breath, one task." | Network lag with no optimistic row | Optimistic insert row; validate title non-empty |
| Confirm | List body | New row appears in unified list with chips | "It’s real, not a draft somewhere." | Task created in a hidden view | Scroll/focus to new row subtly; parity so board shows same card |
| Recover / Next | Mistyped title | Opens detail from new row or undo if offered | "Let me fix without shame." | Hard delete only; no path to edit | Soft focus title in detail; archive vs delete per brief |

### Feature: Inline status update from list — Task Inbox/List

- **Label:** core
- **Primary persona:** Miguel Santos — updates status without leaving keyboard flow.
- **JTBD refs:** #5 (fast status move before deadline; stays in sync with board/detail)

| Stage | Touchpoint | Action | Thought / Emotion | Pain to avoid | Opportunity |
|---|---|---|---|---|---|
| Trigger | Row shows in-progress client patch still in To do | Opens status control from list | "Don’t make me open a panel." | Only editable in detail | Status chip/dropdown always visible on desktop row |
| Orient | Inline status menu on row | Sees exactly three statuses (MVP) | "Matches the board mental model." | Surprise custom statuses in MVP | Locked labels To do / In progress / Done |
| Act | Dropdown or cycle control | Selects In progress | "Done." | Two-step confirm for non-destructive change | Single select applies; no save button |
| Confirm | Row + board (if open elsewhere) | Chip updates; board column reflects | "Parity holds." | Board lags list | Same mutation updates all subscribers |
| Recover / Next | Wrong column intent | Picks correct status again | Mild annoyance | No audit of who changed what when debugging handoffs | Lightweight updated-at + optional activity in detail |

### Feature: Filter by status/assignee/priority — Task Inbox/List

- **Label:** supporting
- **Primary persona:** Jordan Reyes — pre-milestone slice: "what does this contractor owe?"
- **JTBD refs:** #2 (narrow to execution context); #4 (clarity for micro-team without dashboards)

| Stage | Touchpoint | Action | Thought / Emotion | Pain to avoid | Opportunity |
|---|---|---|---|---|---|
| Trigger | List grows past ~15 mixed-client tasks | Opens filter control in list toolbar | "I only care about In progress + Alex today." | Export to spreadsheet workaround | Filter chips persistent but dismissible |
| Orient | Filter popover | Sees triad: status, assignee, priority | "Obvious AND logic." | Advanced query language | Simple multi-select with live result count |
| Act | Applies assignee + status | List re-renders subset | "This is my stand-up subset." | Full-page reload flash | Client-side or snappy server filter; preserve sort |
| Confirm | Row set + optional board sidecar | Only matching tasks visible; counts make sense | Trust | Board shows superset while list filtered — feels broken | Optional "filter applies to board" toggle or clear messaging |
| Recover / Next | Over-filtered to zero | Clears one chip at a time | "Where did everything go?" | Blank screen with no CTA | Zero-state copy + "clear all filters" |

### Feature: Sort by due date/priority/updated time — Task Inbox/List

- **Label:** supporting
- **Primary persona:** Miguel Santos — starts deep-work block with highest leverage thread.
- **JTBD refs:** #2 (re-order workload for execution clarity)

| Stage | Touchpoint | Action | Thought / Emotion | Pain to avoid | Opportunity |
|---|---|---|---|---|---|
| Trigger | Deadline morning | Opens sort menu on list | "What’s due soonest?" | Fixed arbitrary ordering | Expose due date / priority / updated sort |
| Orient | Sort dropdown | Reads current selection + options | "Predictable semantics." | Unclear ascending vs descending | Label arrows + persistent indicator in header |
| Act | Chooses due date ascending | List reorders | "Top is next fire." | Tasks without dates vanish or sort randomly | Explicit handling: nulls last + inline hint to add dates |
| Confirm | Rows animate or stable reorder | Scans top of list | Confidence | Sort appears changed but field wrong (timezone) | Respect workspace timezone from settings |
| Recover / Next | Wrong sort choice | Switches to updated time | Quick correction | No way back to prior sort | Remember last sort per user locally |

### Feature: Keyboard command quick capture — Task Inbox/List

- **Label:** nice-to-have
- **Primary persona:** Miguel Santos — expects desktop shortcuts; minimal mouse.
- **JTBD refs:** #2 (capture without leaving flow)

| Stage | Touchpoint | Action | Thought / Emotion | Pain to avoid | Opportunity |
|---|---|---|---|---|---|
| Trigger | Mid-typing in IDE or email | Hits global shortcut (when implemented) | "Open capture now." | Shortcut conflicts with OS/browser | **Post-MVP** per modules-features §4; document conflict-free default when shipped |
| Orient | Quick-add focused | Cursor in title field | "I’m already typing." | Focus trap stealing keys from wrong app | Only registers when app focused unless extension later |
| Act | Types title, Enter to save | Task created | Flow | Silent failure on Enter | Toast or row insert confirmation |
| Confirm | List updates | Sees task | Satisfaction | Parity miss | Same as quick add parity rules |
| Recover / Next | Shortcut not wired yet | Uses mouse quick add | "Fine for now." | Dead shortcut advertised in empty state | Gate hint in settings/help until feature ships |

### Feature: Three default status columns — Status Board

- **Label:** core
- **Primary persona:** Priya Nair — board is pipeline ritual for studio.
- **JTBD refs:** #3 (To do / In progress / Done without hierarchy theater); #5 (deadline alignment)

| Stage | Touchpoint | Action | Thought / Emotion | Pain to avoid | Opportunity |
|---|---|---|---|---|---|
| Trigger | Switches nav to Board | Views columns | "This is our motion." | Custom column setup before first card | Pre-built three columns matching statuses |
| Orient | Column headers + WIP visual density | Maps cards to stages | Calm | Mislabeled columns vs list statuses | Strict naming parity with task model |
| Act | Reads cards per column | Plans moves (pairs with drag feature) | "In progress isn’t a junk drawer." | Unlimited columns causing scatter | Fixed three in MVP per guardrail |
| Confirm | Card counts per column | Validates load balance | "We see overload." | No counts | Optional column counts (lightweight) |
| Recover / Next | Needs future custom status | Notes limitation | Pragmatic | Selling enterprise configurability in MVP | **Opportunity:** status configuration is nice-to-have/post roadmap — link to feedback not settings maze |

### Feature: Drag-and-drop status move — Status Board

- **Label:** core
- **Primary persona:** Priya Nair — moves creative tasks visually before client review.
- **JTBD refs:** #5 (drag board that syncs with list/detail)

| Stage | Touchpoint | Action | Thought / Emotion | Pain to avoid | Opportunity |
|---|---|---|---|---|---|
| Trigger | Stand-up or async review on board | Grabs card | "Move means progress." | Drag disabled on desktop | Hit targets meet WCAG AA intent per brief |
| Orient | Column drop zones highlight | Sees ghost card | "I know where it lands." | Ambiguous drop between columns | Strong column affordance; keyboard alternative path if drag fails |
| Act | Drops in In progress | Releases pointer | "State changed." | Long request; card snaps back mysteriously | Optimistic UI + rollback toast on error |
| Confirm | Board + list + detail | Status chip everywhere updates | Trust | Any view stale | Single source of truth write |
| Recover / Next | Dropped wrong column | Drags back or uses inline list | Low cost | Accidental archive | Prefer status change over destructive gestures |

### Feature: Board/list/detail parity sync — Status Board

- **Label:** core
- **Primary persona:** Jordan Reyes — contractor on board, Jordan on list.
- **JTBD refs:** #5 (same tasks/statuses/owners); #2 (single picture)

| Stage | Touchpoint | Action | Thought / Emotion | Pain to avoid | Opportunity |
|---|---|---|---|---|---|
| Trigger | Two surfaces open in tabs | Expects mirrored truth | "No debates about which screen lies." | Split-brain tools | Document parity as invariant in UI tests |
| Orient | Any view after mutation | Checks other tab | Vigilance | Needing manual refresh | Websocket/poll/revalidate on focus |
| Act | Updates assignee in detail | Watches list/board | "Propagates." | Partial field sync (status yes, assignee no) | Uniform mutation pipeline for task fields |
| Confirm | All surfaces show same assignee/status | — | Relief | Race: last-write wins without surfacing conflict | Timestamp conflict rare; show toast if rejected |
| Recover / Next | Stale cache edge | Refreshes page | Annoyance if frequent | No hard refresh story | Soft refetch button in toolbar |

### Feature: Swimlane/group by assignee — Status Board

- **Label:** supporting
- **Primary persona:** Jordan Reyes — sees per-person load inside each status.
- **JTBD refs:** #1 (who owes what without seat overhead); #5 (deadline coordination)

| Stage | Touchpoint | Action | Thought / Emotion | Pain to avoid | Opportunity |
|---|---|---|---|---|---|
| Trigger | Multiple contractors active | Toggles group-by assignee on board | "Whose In progress is bloated?" | Only manual scanning | MVP-essential per modules-features §4 |
| Orient | Lanes labeled by member + unassigned | Reads matrix | "Spatial clarity." | Lanes reorder randomly | Stable member sort (owner first, alphabetical) |
| Act | Drags card across lane boundary if supported, or reassigns | Updates ownership | "Rebalance work." | Drag breaks assignee semantics | Explicit assignee change action if cross-lane drag ambiguous |
| Confirm | List/detail assignee matches lane | — | Control | Lane shows old owner | Same parity pipeline |
| Recover / Next | Too many lanes | Turns grouping off | "Back to simple board." | Toggle buried | Prominent view option next to board/list switch |

### Feature: WIP limit indicators — Status Board

- **Label:** nice-to-have
- **Primary persona:** Miguel Santos — wants gentle overload signal without enterprise WIP config.
- **JTBD refs:** #2 (execution clarity); #5 (pre-deadline triage)

| Stage | Touchpoint | Action | Thought / Emotion | Pain to avoid | Opportunity |
|---|---|---|---|---|---|
| Trigger | In progress column feels heavy | Notices soft threshold styling (when shipped) | "We should finish before starting." | **Post-MVP** per §4 backlog — avoid blocking MVP board | Ship as visual-only hint first: column tint when count > N |
| Orient | Column header badge | Reads count vs limit | "Numerate overload." | Arbitrary limits with no tuning | Sensible default N with tooltip |
| Act | Team throttles new pulls | Moves cards to Done | Discipline | Hard enforcement (out of scope) | Advisory-only to match anti-bloat |
| Confirm | Indicator clears when under limit | — | Calm | Indicator wrong vs actual count | Derive from live query |
| Recover / Next | Limit feels wrong for team | Ignores indicator | Pragmatic | No dismiss | Optional hide per workspace (later) |

### Feature: Core task fields (title, description) — Task Detail

- **Label:** core
- **Primary persona:** Priya Nair — writes creative brief fragments on the task.
- **JTBD refs:** #3 (task identity without wiki); #4 (client-ready clarity)

| Stage | Touchpoint | Action | Thought / Emotion | Pain to avoid | Opportunity |
|---|---|---|---|---|---|
| Trigger | Clicks row from list/board | Detail panel/page opens | "Context lives here." | Full navigation away losing list position | Split pane or overlay preserving list scroll |
| Orient | Title + description editor | Sees current content | "Plain is fine." | Rich-text bugs in MVP | Plain text MVP per founder brief |
| Act | Edits title/description; autosave or save | Types deliverable notes | "Autosave or obvious save?" | Data loss on blur | Debounced autosave + last-saved indicator |
| Confirm | Toast or inline "Saved" | — | Trust | Silent fail | Error banner with retry |
| Recover / Next | Wrong task opened | Uses breadcrumb/back to list | Low friction | No back gesture | Esc to close detail overlay |

### Feature: Assignee and priority — Task Detail

- **Label:** core
- **Primary persona:** Jordan Reyes — assigns rotating contractor.
- **JTBD refs:** #1 (shared assignees without seat drama); #4 (urgency + ownership visible)

| Stage | Touchpoint | Action | Thought / Emotion | Pain to avoid | Opportunity |
|---|---|---|---|---|---|
| Trigger | Task needs owner before stand-up | Opens detail | "Who’s on the hook?" | Assignee picker empty | Seed workspace members in picker |
| Orient | Assignee dropdown + priority control | Sees self + teammates | "Simple enum." | Role jargon | Owner/member both assignable per micro-team model |
| Act | Picks assignee + High priority | Saves | "They’ll see it." | Requires re-invite to assign | Guest assignee rules deferred — only members MVP |
| Confirm | List/board chips update | — | Confidence | Priority invisible on board/list | Show priority chip consistently where spec demands |
| Recover / Next | Picked wrong person | Reassigns | Quick fix | Audit trail missing | Comment ping optional later |

### Feature: Due date — Task Detail

- **Label:** supporting
- **Primary persona:** Priya Nair — ties tasks to client review dates.
- **JTBD refs:** #5 (deadline / invoice window planning)

| Stage | Touchpoint | Action | Thought / Emotion | Pain to avoid | Opportunity |
|---|---|---|---|---|---|
| Trigger | Client sends date | Opens detail date field | "This drives sort." | Date buried | Datepicker near title block |
| Orient | Calendar popover | Sees timezone-aware day | "No UTC surprises." | Wrong timezone | Workspace timezone from settings |
| Act | Picks date; clears optional | Saves | "Nullable is OK." | Forced date on every task | Allow clear date |
| Confirm | List sort by due works | Row shows compact date | Visibility | Date not shown on list | Compact due label on row per MVP essential |
| Recover / Next | Date moved by client | Edits inline or detail | Adaptation | Versioning dates | Comment "date changed" optional |

### Feature: Image attachment upload — Task Detail

- **Label:** supporting
- **Primary persona:** Priya Nair — attaches mockups for campaign tasks.
- **JTBD refs:** #4 (visual proof for creative delivery)

| Stage | Touchpoint | Action | Thought / Emotion | Pain to avoid | Opportunity |
|---|---|---|---|---|---|
| Trigger | Needs reference on task | Scrolls to attachments | "Boards aren’t Figma." | Out-of-scope video | Images only per brief |
| Orient | Upload dropzone + file picker | Sees size/type limits (5MB etc.) | "Fair guardrails." | Opaque failure | Presigned upload progress |
| Act | Selects PNG | Uploads | "Did it stick?" | Long hang no progress | Progress bar + cancel |
| Confirm | Thumbnail grid | Opens lightbox | "Client-facing proof." | Broken thumbnail | Retry upload affordance |
| Recover / Next | Wrong file | Deletes attachment | Clean slate | Accidental delete no confirm | Soft confirm delete |

### Feature: Task comments/activity trail (lightweight) — Task Detail

- **Label:** supporting
- **Primary persona:** Miguel Santos — async handoff with partner without Slack.
- **JTBD refs:** #1 (collaboration context); #5 (closure before deadline)

| Stage | Touchpoint | Action | Thought / Emotion | Pain to avoid | Opportunity |
|---|---|---|---|---|---|
| Trigger | Blocker note after deploy | Opens detail comments | "Keep it near the task." | Thread in Slack only | Comment stream anchored to task |
| Orient | Chronological list | Sees author + timestamp | "Lightweight, not Jira." | Full activity graph | Text comments MVP; system events minimal |
| Act | Types comment; submit | Adds @mention if supported later | "They’ll read this here." | **MVP:** plain comments without complex mentions | Start simple; mentions post roadmap |
| Confirm | Comment appears top/bottom consistent | — | Trust | Ordering bugs | Stable sort (oldest/newest toggle optional) |
| Recover / Next | Typo | Edit window or delete | Low shame | No edit | Allow short edit window |

### Feature: Subtasks/checklist — Task Detail

- **Label:** nice-to-have
- **Primary persona:** Priya Nair — breaks campaign task into asset checklist.
- **JTBD refs:** #4 (mini steps without full project hierarchy)

| Stage | Touchpoint | Action | Thought / Emotion | Pain to avoid | Opportunity |
|---|---|---|---|---|---|
| Trigger | Large deliverable in one card | Expands subtasks (when shipped) | "Checklist beats new cards." | **Post-MVP** per §4 | Keep description headings as MVP workaround in copy |
| Orient | Checklist UI | Sees progress % | Motivation | Nested sub-subtasks | One level only |
| Act | Adds items; checks done | Updates progress | "Micro wins." | Checklist doesn’t affect status | Optional "all done suggests move to Done" later |
| Confirm | Parent row shows progress chip | Teammate sees | Alignment | Parity: optional mirror on list row | Collapsed count on list |
| Recover / Next | Checklist too long | Collapses section | Focus | Performance drag | Virtualize long lists later |

### Feature: Invite teammate by email/link — Team & Access

- **Label:** core
- **Primary persona:** Jordan Reyes — invites 2-week contractor.
- **JTBD refs:** #1 (same list/board without extra paid seat elsewhere)

| Stage | Touchpoint | Action | Thought / Emotion | Pain to avoid | Opportunity |
|---|---|---|---|---|---|
| Trigger | New engagement starts | Opens invite from workspace menu | "Fast invite, no procurement." | Hidden invite | Always-visible team entry |
| Orient | Invite modal | Chooses email vs link | "They’ll know what they’re joining." | Opaque workspace name | Show workspace name + inviter |
| Act | Sends invite | Copies link or emails | "They’re in." | CAPTCHA hell on collaborator | Smooth magic-link pattern per brief posture |
| Confirm | Pending member appears | — | Expectation | No pending state | Join-state clarity feature complements |
| Recover / Next | Wrong email | Revokes/resends | Fix | Cannot revoke invite | Expire + resend |

### Feature: Simple member roles (owner/member) — Team & Access

- **Label:** supporting
- **Primary persona:** Miguel Santos — one owner, partner as member.
- **JTBD refs:** #1 (minimal governance)

| Stage | Touchpoint | Action | Thought / Emotion | Pain to avoid | Opportunity |
|---|---|---|---|---|---|
| Trigger | First collaborator accepts | Owner checks permissions | "Who can break things?" | RBAC matrix | Binary owner vs member |
| Orient | Team settings table | Sees role column | "Obvious." | Enterprise roles (admin/editor/viewer stack) | Only two labels |
| Act | Promotes/demotes if ever needed | Changes role | Rare action | Accidental demote locks billing — N/A for donation model | Confirm modal on owner demote |
| Confirm | Role badge updates | Member sees allowed actions | Clarity | Member cannot perform needed task actions | Member full task edit; owner-only billing/settings later |
| Recover / Next | Wrong role | Owner adjusts | Recovery | No owner | Always ≥1 owner invariant |

### Feature: Join-state clarity (pending/accepted/expired invite) — Team & Access

- **Label:** supporting
- **Primary persona:** Jordan Reyes — tracks whether contractor actually joined.
- **JTBD refs:** #1 (visibility without login juggling)

| Stage | Touchpoint | Action | Thought / Emotion | Pain to avoid | Opportunity |
|---|---|---|---|---|---|
| Trigger | Sent invite yesterday | Opens team panel | "Did they click?" | Black hole | Explicit pending/expired chips |
| Orient | Invites list | Reads timestamps | "When to nudge." | No expiry story | Show expiry countdown per invite policy |
| Act | Resends or copies fresh link | Follows up | Pragmatic | Spammy resend | Rate-limit with friendly copy |
| Confirm | State flips to accepted | Avatar appears | Relief | Stuck pending after accept | Webhook-style poll on team panel focus |
| Recover / Next | Expired | One-click regenerate | Fix | Manual support | Self-serve renew invite |

### Feature: Guest/client read-only access — Team & Access

- **Label:** nice-to-have
- **Primary persona:** Priya Nair — wants client to see status without collaborator seat.
- **JTBD refs:** #1 (visibility without seat-tax); #5 (client confidence)

| Stage | Touchpoint | Action | Thought / Emotion | Pain to avoid | Opportunity |
|---|---|---|---|---|---|
| Trigger | Client asks "where are we?" | Considers share link (future) | "Read-only is enough." | **Post-MVP** per §4 | Position in roadmap comms; MVP: export screenshot workaround |
| Orient | Share dialog (future) | Sees read-only badge | Trust | Client edits tasks by accident | Hard server enforced read-only role |
| Act | Copies client link | Sends | "Professional." | Token leak | Expiring tokens |
| Confirm | Client view loads board/list read-only | — | Pride | Parity breaks | Read replica of same views |
| Recover / Next | Client shouldn’t see anymore | Revokes token | Safety | No revoke | Revocation list |

### Feature: Create workspace + first task in <=2 steps — Activation & Onboarding

- **Label:** core
- **Primary persona:** Miguel Santos — evaluates tool in <5 minutes.
- **JTBD refs:** #2 (time-to-truth); #3 (no architecture project)

| Stage | Touchpoint | Action | Thought / Emotion | Pain to avoid | Opportunity |
|---|---|---|---|---|---|
| Trigger | Landing from marketing | Starts signup | "Don’t waste my night." | Long forms | Workspace name + user in one flow |
| Orient | Step indicator (max 2) | Sees next is first task | Predictable | Surprise email verify wall | If email verify needed, still ≤2 product steps after auth |
| Act | Names workspace; creates first task title | Submits | "Already useful." | Forced invite before value | Invite deferred to empty state guidance |
| Confirm | Unified list shows task | — | Momentum | Empty state persists incorrectly | Immediate transition to list/board |
| Recover / Next | Typo in workspace name | Renames in settings later | Low regret | Locked forever | Workspace rename in basics settings |

### Feature: First-use empty state guidance — Activation & Onboarding

- **Label:** supporting
- **Primary persona:** Priya Nair — orients studio without admin manual.
- **JTBD refs:** #2 (first minutes on throughput); #3 (low cognitive load)

| Stage | Touchpoint | Action | Thought / Emotion | Pain to avoid | Opportunity |
|---|---|---|---|---|---|
| Trigger | Lands on empty workspace | Sees empty list/board | "What now?" | Blank generic template per founder fear | Tailored dark compact empty illustration + 3 CTAs |
| Orient | Checklist: first task, first status move, first invite | Reads short copy | "I can skim." | Essay | Max 3 bullets |
| Act | Clicks suggested actions sequentially | Completes seed actions | "Guided, not babysat." | Forced sample data | Optional template ties to sample project feature |
| Confirm | List/board non-empty | Empty state dismisses | Achievement | Dismiss too aggressive if user deletes all | Re-show gentle hint if zero tasks |
| Recover / Next | Skipped invite | Returns via team menu | OK path | Guilt copy | Positive tone |

### Feature: Sample project template — Activation & Onboarding

- **Label:** nice-to-have
- **Primary persona:** Jordan Reyes — wants freelance-shaped starter tasks.
- **JTBD refs:** #2 (faster orientation); #4 (credible structure)

| Stage | Touchpoint | Action | Thought / Emotion | Pain to avoid | Opportunity |
|---|---|---|---|---|---|
| Trigger | Empty state "use template" | Clicks | "Show me conventions." | **Post-MVP** per §4 | Until shipped, link to manual first task only |
| Orient | Template picker | Sees 1–2 simple presets | Not overwhelming | 20 templates | One freelance default |
| Act | Applies template | Board fills | "I’ll rename, not rebuild." | Pollutes production with fake clients | Clear "demo tasks" banner with bulk delete |
| Confirm | Tasks editable/deletable | — | Control | Locked demo | All real tasks post-insert |
| Recover / Next | Chose wrong template | Deletes batch | Cleanup | No multi-select | Multi-select delete later |

### Feature: Workspace basics (name, timezone) — Light Settings & Trust

- **Label:** supporting
- **Primary persona:** Jordan Reyes — EU clients + US work; timezone correctness for due dates.
- **JTBD refs:** #1 (coordination); #5 (deadline truth)

| Stage | Touchpoint | Action | Thought / Emotion | Pain to avoid | Opportunity |
|---|---|---|---|---|---|
| Trigger | Due dates look off | Opens settings | "Fix the basics." | Settings maze | Small settings surface |
| Orient | Name + timezone fields | Sees current values | "Only what matters." | 50 toggles | Single page section |
| Act | Updates timezone; saves | Confirms | "Dates should align." | Silent apply | Explicit save or autosave with feedback |
| Confirm | Due labels re-render | — | Relief | Old cached dates | Invalidate client cache on TZ change |
| Recover / Next | Broke name | Reverts edit | Low stakes | No undo | Inline validation |

### Feature: Status configuration (locked in MVP, extensible later) — Light Settings & Trust

- **Label:** nice-to-have
- **Primary persona:** Priya Nair — may want Client review later; not MVP.
- **JTBD refs:** #3 (future flexibility); #5 (workflow fit)

| Stage | Touchpoint | Action | Thought / Emotion | Pain to avoid | Opportunity |
|---|---|---|---|---|---|
| Trigger | Wants fourth column someday | Visits settings (future) | "Later." | **MVP locked** per modules-features + founder brief defaults | Show read-only explanation of three statuses |
| Orient | Disabled or absent editor | Reads "locked for MVP" | Acceptance | Teasing nonfunctional toggle | Honest copy + feedback link |
| Act | Sends feedback | Submits short request | "I’ll wait for a real migration path." | False hope that toggles work today | Capture request; don’t pretend config exists |
| Confirm | Read-only status explainer remains accurate | Closes settings | "At least they’re honest." | Drift between copy and product (e.g. hidden fourth column) | Keep copy versioned with releases |
| Recover / Next | Needs Client review now | Uses task title prefix or comment convention | Pragmatic | Forcing custom status in MVP | Document lightweight naming patterns internally |

### Feature: Non-blocking donation reminder — Light Settings & Trust

- **Label:** supporting
- **Primary persona:** Priya Nair — tolerant if dismissible and tasteful.
- **JTBD refs:** #1 (free core collaboration); #3 (trust without paywall)

| Stage | Touchpoint | Action | Thought / Emotion | Pain to avoid | Opportunity |
|---|---|---|---|---|---|
| Trigger | Session milestone or time-based | Modal/banner surfaces | "Here it comes." | Blocking modal | Dismiss continues work per brief |
| Orient | Copy explains optional support | Reads once | "Fair." | Guilt manipulation | Neutral tone; no dark patterns |
| Act | Dismisses or donates | Chooses | Autonomy | Paywall on features | Never gate task actions |
| Confirm | Banner stays dismissed per policy | — | Respect | Reappears every minute | Sensible cooldown |
| Recover / Next | Wants to donate later | Opens from settings/about | Positive | Hidden donate | Persistent low-key entry in menu |

### Feature: Personal notification controls — Light Settings & Trust

- **Label:** nice-to-have
- **Primary persona:** Priya Nair — escaped noisy PM once; fears repeat.
- **JTBD refs:** #3 (reduce noise vs all-in-one)

| Stage | Touchpoint | Action | Thought / Emotion | Pain to avoid | Opportunity |
|---|---|---|---|---|---|
| Trigger | Email pings too often (future channel) | Opens notification settings | "Let me throttle." | **Post-MVP** per §4 | MVP may ship with email defaults only — set expectations |
| Orient | Simple toggles: mentions, assignments, digest | Reads labels | "Understandable." | Per-task overrides | Global workspace-level first |
| Act | Turns off noisy class | Saves | "Sanity." | Hidden dependencies | Don’t break invite emails |
| Confirm | Fewer emails arrive | — | Calm | No confirmation | Send test email optional later |
| Recover / Next | Missed important ping | Re-enables category | Learning | No audit | Activity trail in task as backstop |
