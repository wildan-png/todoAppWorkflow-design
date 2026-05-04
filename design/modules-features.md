# Modules & Features Structure

This document translates the approved module and feature plan into implementation scope for aTodo.

## 1. Structure Tree (MVP-first)

```text
aTodo
├─ Task Inbox/List
│  ├─ Unified task list view
│  ├─ Quick add task
│  ├─ Inline status update from list
│  └─ Filter by status/assignee/priority
├─ Status Board
│  ├─ Three default status columns
│  ├─ Drag-and-drop status move
│  ├─ Board/list/detail parity sync
│  └─ Swimlane/group by assignee
├─ Task Detail
│  ├─ Core task fields (title, description)
│  ├─ Assignee and priority
│  ├─ Due date
│  ├─ Image attachment upload
│  └─ Task comments/activity trail (lightweight)
├─ Team & Access
│  ├─ Invite teammate by email/link
│  ├─ Simple member roles (owner/member)
│  └─ Join-state clarity (pending/accepted/expired invite)
├─ Activation & Onboarding
│  ├─ Create workspace + first task in <=2 steps
│  └─ First-use empty state guidance
└─ Light Settings & Trust
   ├─ Workspace basics (name, timezone)
   └─ Non-blocking donation reminder
```

## 2. Module Map

- **Task Inbox/List**
  - Purpose: Give one dense desktop surface for seeing all tasks with status + owner and acting quickly.
  - Primary persona: Founder/operator in a 1–3 person freelance team.

- **Status Board**
  - Purpose: Make progress and ownership visually obvious through fast status movement (`To do`, `In progress`, `Done`).
  - Primary persona: Delivery lead coordinating deadlines with collaborators.

- **Task Detail**
  - Purpose: Centralize complete task context (description, assignee, priority, due date, attachments, comments).
  - Primary persona: Task assignee doing execution work.

- **Team & Access**
  - Purpose: Keep micro-team collaboration frictionless via invite/join and simple role boundaries.
  - Primary persona: Founder inviting contractor/cofounder.

- **Activation & Onboarding**
  - Purpose: Reduce time-to-first-task and time-to-first-status-move with minimal setup.
  - Primary persona: New workspace owner on first day.

- **Light Settings & Trust**
  - Purpose: Handle essential preferences/guardrails (workspace basics, statuses, donation reminder behavior) without bloat.
  - Primary persona: Founder/owner.

## 3. Features per Module

### Task Inbox/List

| Name | Description | Label | JTBD it serves | Agent opportunity |
|---|---|---|---|---|
| Unified task list view | Single sortable/scannable list with status and assignee visible by default. | core | #2, #3 | yes |
| Quick add task | Fast create flow from list with required title and sensible defaults. | core | #2, #3 | yes |
| Inline status update from list | Change status directly without opening detail. | core | #5 | no |
| Filter by status/assignee/priority | Narrow task set to current execution context. | supporting | #2, #4 | yes |
| Sort by due date/priority/updated time | Re-order workload for execution clarity. | supporting | #2 | no |
| Keyboard command quick capture | Desktop shortcut to open create-task quickly. | nice-to-have | #2 | no |

### Status Board

| Name | Description | Label | JTBD it serves | Agent opportunity |
|---|---|---|---|---|
| Three default status columns | Fixed MVP columns (`To do`, `In progress`, `Done`) aligned to USP anti-bloat scope. | core | #3, #5 | no |
| Drag-and-drop status move | Move task cards across columns to update progress instantly. | core | #5 | no |
| Board/list/detail parity sync | Any status/owner update is reflected consistently across all views. | core | #5, #2 | no |
| Swimlane/group by assignee | Optional grouping for deadline coordination view. | supporting | #1, #5 | yes |
| WIP limit indicators | Lightweight visual warning when too many tasks are in progress. | nice-to-have | #2, #5 | yes |

### Task Detail

| Name | Description | Label | JTBD it serves | Agent opportunity |
|---|---|---|---|---|
| Core task fields (title, description) | Edit essential task identity and context. | core | #3, #4 | yes |
| Assignee and priority | Set ownership and urgency for execution clarity. | core | #1, #4 | yes |
| Due date | Add delivery target date for client/deadline planning. | supporting | #5 | yes |
| Image attachment upload | Attach visual context directly to a task. | supporting | #4 | no |
| Task comments/activity trail (lightweight) | Preserve async collaboration context per task. | supporting | #1, #5 | yes |
| Subtasks/checklist | Break a task into mini steps. | nice-to-have | #4 | yes |

### Team & Access

| Name | Description | Label | JTBD it serves | Agent opportunity |
|---|---|---|---|---|
| Invite teammate by email/link | Add collaborators quickly to same workspace. | core | #1 | no |
| Simple member roles (owner/member) | Minimal permission model suitable for micro-team. | supporting | #1 | no |
| Join-state clarity (pending/accepted/expired invite) | Remove ambiguity in invitation flow. | supporting | #1 | no |
| Guest/client read-only access | Let clients view status without full collaborator seat. | nice-to-have | #1, #5 | no |

### Activation & Onboarding

| Name | Description | Label | JTBD it serves | Agent opportunity |
|---|---|---|---|---|
| Create workspace + first task in <=2 steps | Compress setup to immediate value moment. | core | #2, #3 | yes |
| First-use empty state guidance | Clear prompts for first task, first status move, and first invite. | supporting | #2, #3 | yes |
| Sample project template | Optional starter tasks for common freelance workflow. | nice-to-have | #2, #4 | yes |

### Light Settings & Trust

| Name | Description | Label | JTBD it serves | Agent opportunity |
|---|---|---|---|---|
| Workspace basics (name, timezone) | Set minimum operational context for team coordination. | supporting | #1, #5 | no |
| Status configuration (locked in MVP, extensible later) | Keep 3 default statuses now; expose controlled editability later. | nice-to-have | #3, #5 | no |
| Non-blocking donation reminder | Optional support prompt with zero paywall impact. | supporting | #1, #3 | no |
| Personal notification controls | Reduce notification noise to preserve focus. | nice-to-have | #3 | yes |

## 4. MVP Cut

### Proposed MVP Scope (Core + Essential Supporting)

- **Task Inbox/List**
  - Unified task list view (`core`)
  - Quick add task (`core`)
  - Inline status update from list (`core`)
  - Filter by status/assignee/priority (`supporting`, essential)

- **Status Board**
  - Three default status columns (`core`)
  - Drag-and-drop status move (`core`)
  - Board/list/detail parity sync (`core`)
  - Swimlane/group by assignee (`supporting`, essential for 1–3 team clarity)

- **Task Detail**
  - Core task fields (`core`)
  - Assignee and priority (`core`)
  - Due date (`supporting`, essential)
  - Image attachment upload (`supporting`, essential)
  - Task comments/activity trail (`supporting`, essential for collaboration)

- **Team & Access**
  - Invite teammate by email/link (`core`)
  - Simple member roles owner/member (`supporting`, essential)
  - Join-state clarity (`supporting`, essential)

- **Activation & Onboarding**
  - Create workspace + first task <=2 steps (`core`)
  - First-use empty state guidance (`supporting`, essential)

- **Light Settings & Trust**
  - Workspace basics (`supporting`, essential)
  - Non-blocking donation reminder (`supporting`, essential)

### Post-MVP Backlog

- Keyboard command quick capture
- WIP limit indicators
- Subtasks/checklist
- Guest/client read-only access
- Sample project template
- Status configuration beyond default 3 statuses
- Personal notification controls

## 5. Feature Count Summary

| Module | Core | Supporting | Nice-to-have | Total |
|---|---:|---:|---:|---:|
| Task Inbox/List | 3 | 2 | 1 | 6 |
| Status Board | 3 | 1 | 1 | 5 |
| Task Detail | 2 | 3 | 1 | 6 |
| Team & Access | 1 | 2 | 1 | 4 |
| Activation & Onboarding | 1 | 1 | 1 | 3 |
| Light Settings & Trust | 0 | 2 | 2 | 4 |
| **Total** | **10** | **11** | **7** | **28** |

## Scope Guardrails

- No docs/wiki, automations, dashboards, roadmaps, cycles/sprints, or in-app AI agent in V1.
- Every feature must map to at least one JTBD statement.
- Desktop/fixed-layout first; mobile/responsive polish is out of this phase.
- Free-core collaboration with non-blocking donation prompt remains a positioning constraint.
