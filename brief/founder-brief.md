## 🎯 Product & Vision

- What is the product and what problem does it solve?  
  aTodo is a simple task tracker focused on status/progress (list + board) for small freelance teams, positioned as an alternative to paying for broad feature sets they do not use.
- Who is the target user? (demographics, behavior, context of use)  
  Small-scale freelancers, typically 1-3 people (solo or tiny collaboration).
- What is the core value proposition — why would someone choose this over alternatives?  
  Simpler scope than broad paid tools: focused workflow (list, board, task detail), lighter feature set, and free core usage.

## 🏁 Competitors & Market

- Who are the direct competitors? (name them)  
  Linear.
- Who are the indirect competitors? (different product, same problem)  
  ClickUp and Plane.
- What do competitors do well that we should match or beat?  
  Linear is cited for speed and minimal UI; Plane is cited for project/issue-style task structure; ClickUp is cited for depth users may expect.
- What do competitors do poorly that we can exploit?  
  ClickUp and Plane are described as expensive for this audience and too broad for actual needs; for Linear, the exploitable angle is keeping tighter scope for small 1-3 person freelance teams.
- Is there a product the founder admires as a reference? (even outside the category)  
  Linear, Plane, and ClickUp are explicitly listed as references/inspiration.
- Scope note: identify which named products are `Reference only (not competitors)`.  
  Linear is treated as a direct competitor; ClickUp and Plane are treated as indirect competitors due to broader/different scope. All three are also valid references (especially Linear for speed/minimal UI).

## ⚙️ Product Scope

- What are the must-have features for launch (MVP)?  
  Web MVP with three surfaces: task list, board by status, and task detail (description/notes, image attachments, priority, assignee/user assignment, and core fields).
- What is explicitly out of scope for now?  
  No in-app AI agent in V1; responsive/mobile layouts deferred; heavy automation, enterprise features, deep customization, docs/wiki parity, and ClickUp-scale customization deferred.
- Are there any AI features planned? (copilot, agent, automation)  
  No in-app agent for V1; heavy automation deferred until after validation.
- What platforms? (web, iOS, Android, desktop)  
  Browser-based web app with desktop/fixed-layout MVP first; responsive and mobile layouts are deferred.

## 🎨 Design Direction

- Is there any existing brand identity? (logo, colors, fonts)  
  No locked logo or strict brand system yet; preferred direction is dark, compact, clean, and professional.
- What visual style feels right? (references, adjectives)  
  Linear-like speed/minimal UI is cited as aspirational; implementation is UI/frontend in code/components (not Figma-first).
- What should the product feel like to use? (fast, trustworthy, playful, professional)  
  Simple and workflow-close, with clear visibility of task status and ownership.
- Is there anything design-wise the founder dislikes or wants to avoid?  
  Bloated suite behavior, parity-chasing, and large-scope customization in V1.

## 🔧 Technical Constraints

- Are there required integrations? (APIs, third-party tools)  
  Frontend is expected to be ready to integrate with backend/API when wired; backend/API contract and auth are still open questions; image storage flow/limits are also open.
- Any accessibility or compliance requirements?  
  No specific legal/compliance requirement for MVP; baseline accessibility target is WCAG 2.1 AA for core flows.

## 💰 Business Context

- What is the monetization model?  
  Core product is free; monetization is optional donations (non-blocking popup reminder, no forced payment, no paywall on core features).

## Decisions & conflicts (from sources)

No conflicting statements captured in the sources read.

## Source index

- `brief/raw/brief.md`

## Client follow-up checklist (for unresolved items above)

- None for this pass.
