# User Research — aTodo

Product context: `aTodo` targets solo freelancers and very small teams (1-3 people) who want simple task tracking (list + board + task detail) without bloated PM suites.

## Target User Profile

- Primary segment: solo freelancers and micro-teams (1-3 people) handling client delivery.
- Common roles: design, development, marketing, content, and other digital services.
- Environment: remote/distributed, browser-first work, moderate-to-high tool literacy.
- Usage pattern: many short daily check-ins (what is next, what is blocked, who owns what), not heavy planning rituals.
- Not primary for v1: large teams with deep process setup and enterprise reporting needs.

## Key Pain Points

1. Over-complex tools: setup/customization time is too high for very small teams.
2. Workflow mismatch: teams pay for broad suites while only using core task/status features.
3. Reliability friction: users lose trust when edits feel unsafe or unclear, especially on mobile ([Linear App Store reviews](https://apps.apple.com/us/app/linear-mobile/id1645587184?see-all=reviews)).
4. Cost/trust friction: pricing feels less predictable as collaboration grows.

## Unmet Needs

- Small-team-native defaults: status and owner clarity without setup overhead.
- Predictable pricing: no surprise jumps for small collaboration scenarios.
- Fast operation: low cognitive load and quick task updates.
- Focused scope: no forced modules, no enterprise ceremony.
- Reliable core interactions on desktop and mobile.

## Current Workarounds

- Docs/Notion databases: flexible but maintenance-heavy.
- Spreadsheets/Trello-like boards: quick start, weaker ownership visibility at team scale.
- Chat/email: fast updates, weak source of truth for status and accountability.

## Emotional Drivers

- Control and autonomy over daily work.
- Speed and low friction in execution.
- Trust and predictability in product behavior and pricing.
- Simplicity with enough structure to stay accountable.

## Shared Team Assumptions (Working)

- The first users are likely solo operators or 2-3 person teams, not larger structured organizations.
- Users open the product during active work to answer: "what should I do now?" and "who owns this?"
- Teams value fast clarity more than deep customization.
- If ownership or status is not obvious, users will move work tracking back to chat/spreadsheets.
- Pricing predictability affects trust, not only purchase decisions.
- These are working assumptions to guide collaboration; they should be validated with real users over time.

## How Users Are Expected to Use aTodo

- Core flows to optimize first:
  1. Create task
  2. Assign owner
  3. Move status (list/board)
  4. Mark blocked/unblocked
  5. Complete task
- Typical daily usage moments:
  - Quick capture during work ("do not forget this task")
  - Ownership handoff between teammates
  - Status check before client or team sync
  - End-of-day review of blocked and completed tasks

## Product Design Priorities

- Practical information architecture baseline:
  - `Task`: title, status, assignee, priority, due date (optional), note/description, attachment (optional)
  - `List`: fast scan by owner/status/priority
  - `Board`: quick status transitions with visible ownership
- Interaction direction:
  - Fast by default (few steps, clear actions)
  - Clear ownership and status at a glance
  - No hidden states or ambiguous success feedback
  - Minimal setup before first value
- Shared success signals (v1):
  - Time to first created task
  - Time to update status
  - Weekly active collaborators per workspace
  - Task completion rate
  - % tasks with explicit assignee

## Collaboration Notes for Design Team

- Treat this as a shared working model, not a fixed truth; refine with interview/test evidence.
- Use the core flows as the common language across design, PM, and engineering.
- Resolve debates by checking user goal fit first: capture, assign, update, unblock, complete.
- Keep output artifacts lightweight: user flow, key screens, and success signal impact.

## Open Questions to Validate

- Which pain is strongest in practice: complexity, pricing, or reliability?
- How often do users need mobile editing vs desktop-only updates?
- What is the minimum task metadata users accept before it feels "too heavy"?
- Which collaboration step breaks most often: assignment, status updates, or blocked handling?
- At what point does a 2-3 person team decide to switch away from their current tool?

## Source Notes

- Primary-weighted: MBO, Grand View, official product pages/App Store.
- Secondary/directional: Reddit and third-party review/roundup sources; useful for pattern discovery, not for hard quantitative decisions.
