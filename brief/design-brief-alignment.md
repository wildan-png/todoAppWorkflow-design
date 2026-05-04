## Part 1 — Design Brief Alignment

| Area | Alignment draft for sign-off | Needs human input |
|---|---|---|
| Scope: pages + platform | In scope pages: `Task List`, `Board by Status`, `Task Detail`, plus minimum supporting flows for task CRUD and teammate invite. Platform in scope: web app, desktop/fixed-layout first. Out of scope for this phase: responsive/mobile-specific layouts. | Confirm exact page inventory (e.g., auth screens, settings, donation prompt, onboarding flow) and whether any additional admin/utility pages are required. |
| Deliverables | Agency deliverable is frontend implementation-ready UI in code (backend/API integration-ready), explicitly not a Figma-first handoff. | Confirm whether any supporting design artifact is still needed (`none`, lightweight wireframe, or selective Figma references only). |
| Design depth | Design depth should be reflected directly in coded UI for MVP surfaces (`list`, `board`, `detail`) with production-level interaction and visual polish for desktop/fixed layout. | Confirm whether secondary/supporting flows require production-level polish in this phase or can remain functional baseline. |
| States in scope | Must include state coverage for core UX: empty, loading, error, success/confirmation, validation errors, and key edge cases (long titles, no assignee, attachment upload failure, permission/invite mismatch, sync conflict messaging). | Confirm exact state checklist and whether skeleton/loading motion specs and offline/retry behavior are required in design scope. |
| Approval process | Current decision-maker is founder (`Wildan`) as single approver. | Confirm sign-off workflow: number of revision rounds included, feedback SLA per round, and final acceptance criteria. |
| Timeline | Milestones and dates are not defined in source docs. | Fill milestone dates: kickoff, coded UI review #1, coded UI review #2 (if needed), integration-ready handoff, and final delivery date. |
| Agent/AI scope | Explicitly out of scope for V1: no in-app copilot/agent, no advanced automation layer. Product remains focused on task list + board + detail workflow. | Confirm whether any AI-assisted micro-feature (e.g., smart defaults/copy assist) is allowed in design exploration or fully excluded from this phase. |

## Part 2 — JTBD-Driven Metrics

JTBD: When a client/contractor needs visibility and our 1–3 person studio would otherwise add paid seats, I want to keep everyone on the same list, board, and assignees, so I can protect margin and answer “who’s on what?” quickly.  
→ Design metric: A new collaborator can open the shared workspace and correctly identify owner + status for target tasks in <=60 seconds without onboarding help.

JTBD: When starting a billable day with scattered client threads, I want one desktop view showing all tasks with status and owner, so I can spend first minutes on throughput, not archaeology.  
→ Design metric: A user can identify top 3 tasks to execute next from the default desktop view in <=90 seconds with no context-switch to external tools.

JTBD: When all-in-one PM bloat creates setup/admin overhead, I want list + board + task detail only, so I can lower cognitive load and return to billable delivery.  
→ Design metric: Core task lifecycle (create -> assign -> prioritize -> move status -> close) is completable in <=6 interactions per task without visiting non-core configuration surfaces.

JTBD: When a tiny non-enterprise team needs fast, dense UX without engineering ceremony, I want clear task identity/status/assignee/priority/attachments in a freelance-native flow, so I can signal competence to clients.  
→ Design metric: In usability review, users can complete a client-facing status update (including attachment + priority + owner) with zero ambiguity errors and no sprint-specific terminology prompts.

JTBD: When we are 24–48 hours from deadline/invoice and syncing with a cofounder/subcontractor, I want board updates to stay in sync with list/detail, so I can close the loop on done vs blocked vs in review without ambiguity.  
→ Design metric: After status changes from any entry point (board/list/detail), reflected status and owner consistency across all three surfaces is immediate and always visible in the same session flow.
