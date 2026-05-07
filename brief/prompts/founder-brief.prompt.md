Instructions for the model

Goal:
Create a new `brief/founder-brief.md` from source files under `brief/raw/**`, following the required structure and rules in this prompt.

Input scope:
- Read all readable text files under `brief/raw/**` recursively (`.md`, `.txt`, `.csv`, and other text-like files).


- Ignore binary-only files unless a text summary exists under `brief/raw/`.

Output:
- Write exactly one file: `brief/founder-brief.md`.
- Do not write any other files.
- **Replace entire file contents** each run. Never append to an existing `brief/founder-brief.md`. If the file exists, overwrite it completely in one write.
- **Integrity check before finishing:** each required `##` heading (listed below) must appear **exactly once**. If any heading would appear twice, rewrite until the document is a single copy only.
- **Document boundaries:** first line must be the required title; last line must be exactly `<!-- end founder-brief -->`.

Output style contract (must match existing founder brief style):
- Use markdown.
- Keep section separators as `---` lines between major sections.
- For each question bullet, answer using one or more lines prefixed with evidence labels:
  - `[[<repo-relative-path>#Lx-Ly](<repo-relative-path>#Lx-Ly)]` for explicit source facts, with exact file + line range.
  - `[Founder statement, unvalidated]` for source statements that are subjective/opinion/intent and not externally validated.
- Every source-backed claim must include exact citation anchor(s) as clickable Markdown links. Bare source labels without link are invalid.
- Citation format examples:
  - `[[brief/raw/brief.md#L11-L13](brief/raw/brief.md#L11-L13)] <claim>`
  - `[[brief/raw/brief.md#L11-L13](brief/raw/brief.md#L11-L13); [brief/raw/other.md#L4-L9](brief/raw/other.md#L4-L9)] <claim from multiple sources>`
- Keep tone concise and implementation-facing.
- Prefer source-backed wording whenever possible.
- Do not invent or assume. Only include claims explicitly stated in sources.
- If a field is unclear or absent, write exactly:
  `⚠️ Not mentioned — needs follow-up`
- Keep synthesis conservative. Combine facts only when the link is explicit and unavoidable from source wording.
- Competitor labeling must be explicit. Do not call a tool a direct competitor unless sources explicitly frame it as competitor/alternative/replacement.
- Role-based classification for named products:
  - Direct competitor: explicitly framed as competitor/alternative/replacement with meaningful overlap.
  - Indirect competitor: explicitly solves similar core problem but via different category/scope.
  - Reference only (not competitor): cited for workflow/UX pattern/adaptation, not market replacement.
  - If role is unclear, write exactly: `⚠️ Role unclear — needs follow-up`
- Tie-break rule (strict): if a product shares workflow but is not explicitly framed as competitor, keep it out of direct competitors and place it under founder reference products with note: `Workflow reference only (not a competitor)`.
- Conflicts: if sources disagree, capture both statements under existing section `## Decisions & definitions (plain English)` and end that section with:
  `⚠️ Needs follow-up with client`
- Provenance must stay in the top `**Sources:** ...` line only. Do not add new sections for source index. List **only** repo-relative paths under `brief/raw/**` that were actually read as evidence.

Required top header:
1) First line (exact):
`# Founder brief — synthesized from /brief/raw`
2) Then:
`**Sources:** <N> source file(s) read from \`brief/raw/**\` (<comma-separated repo-relative paths only under \`brief/raw/\`>); optional note if expected inputs were missing.`
3) Then blank line, then `---`.

Required section order and exact headings:
1. `## 🎯 Product & Vision`
2. `## 🧭 Business Objectives & Success Definition`
3. `## ⚙️ Redesign Scope & Priorities`
4. `## 👥 User Segments & Personas`
5. `## 😖 Pain Points & User Needs`
6. `## 🏁 Competitive Landscape`
7. `## 🎨 Design Preferences & Brand Identity`
8. `## 🧱 Technical Aspects`
9. `## 🔧 Technical Constraints`
10. `## ✅ Functional Requirements`
11. `## 🤝 Stakeholders & Decision Process`
12. `## Decisions & definitions (plain English)`
13. `## Top follow-up interview questions`

Under each section, include the exact question bullets below and answer each one.

## 🎯 Product & Vision
- **What is the name of the Project?**
- **What are the primary goals you're aiming to achieve with this SaaS application?**
- **Please describe your products and/or service!**
- **What is your overall vision for the output of this project in terms of visual design and user experience? How do you envision the UI enhancing the user journey and achieving your project goals?**

## 🧭 Business Objectives & Success Definition
- **What are the top business objectives for this project? (ranked)**
- **How does the client define success for this redesign/project?**
- **What are the key success metrics for this project?**
- **For each objective, provide: Metric, Baseline, Target, Timeframe, Owner.**
- **What trade-offs is the client willing to make to hit timeline/scope goals?**

## ⚙️ Redesign Scope & Priorities
- **What is the device/platform of your project? Desktop/mobile**
- **To what extent are you looking to redesign the application? Are we focusing on aesthetics, user flow, or a complete overhaul?**
- **What prompted the decision for a redesign at this time?**
- **Classify scope as one: Visual refresh / UX flow improvement / Full overhaul / Hybrid.**
- **What is explicitly in scope for this phase?**
- **What is explicitly out of scope for this phase?**
- **What are the top priorities for this phase? (mark each P0/P1/P2)**

## 👥 User Segments & Personas
- **Can you describe the different user segments that use your app?**
- **What common behaviors or usage patterns do you observe within each user segment?**
- **What are the primary goals or outcomes that each user segment seeks to achieve by using your app?**
- **How do their needs or use cases differ across segments?**
- **Which segments are highest priority for this redesign? (P0/P1/P2)**
- **What do you use to measure success for each user segment?**

## 😖 Pain Points & User Needs
- **What specific challenges or pain points do different segments experience while using your app?**
- **What are the most significant challenges or frustrations users currently face with the app?**
- **Are there specific features or areas where users encounter difficulties more frequently?**
- **Could you share insights or data on user feedback regarding the current version of the app?**
- **What are the top needs and expectations your users have expressed?**
- **For each major pain point, include: affected segment, impact if unsolved, and priority (P0/P1/P2).**

## 🏁 Competitive Landscape
- **Who are your primary competitors?**
- **How do you position your app in the market relative to your competitors?**
- **What unique strengths or features do you believe your app has over the competition?**
- **What do competitors do well that we should match or beat?**
- **Where are competitors weak, and where can we differentiate?**
- **How do your user segments perceive your app compared to competitors? What features do they value most?**
- **Please list some product that you like (Separate with @comma)**
- **Separate `Competitors` vs `Reference products` explicitly.**

## 🎨 Design Preferences & Brand Identity
- **How do you envision the redesign aligning with your current brand identity?**
- **Are there any design elements or themes you’re particularly interested in exploring?**
- **Please list and describe some product that you like !**
- **Are there visual patterns or design choices you want to avoid?**
- **What emotional tone should the product convey? (e.g., professional, friendly, premium, playful)**

## 🧱 Technical Aspects
- **What platforms, devices, and operating systems must the redesign be optimized for?**
- **Are there new technologies or integrations you're considering incorporating in the redesign?**
- **What current stack, architecture, and integration points are already decided?**
- **What technical non-functional requirements matter most? (performance, accessibility, security, reliability)**

## 🔧 Technical Constraints
- **Are there any existing technical constraints or legacy systems that the redesign needs to accommodate?**
- **For each constraint, include: design implication, workaround option, owner, and decision deadline.**
- **Which constraints are hard blockers vs acceptable trade-offs?**

## ✅ Functional Requirements
- **Can you list the specific functionalities that are crucial for the app post-redesign?**
- **Are there new features or improvements you’re prioritizing in this redesign?**
- **For each functional requirement, include:**
  `Requirement | user story | acceptance criteria | priority (P0/P1/P2) | dependencies | phase (MVP or Post-MVP)`

## 🤝 Stakeholders & Decision Process
- **Who are the key stakeholders in this project?**
- **Who decides, who approves, and who must be consulted?**
- **Who signs off scope, UX, and visual direction?**
- **What is the review cadence and communication rhythm?**
- **What unresolved stakeholder concerns should be tracked?**

## Decisions & definitions (plain English)
- Provide numbered items for each unresolved/high-impact decision captured in sources.
- For each item use this exact shape:
  1. `[[<repo-relative-path>#Lx-Ly](<repo-relative-path>#Lx-Ly)] <decision statement>`
     - `[[<repo-relative-path>#Lx-Ly](<repo-relative-path>#Lx-Ly)] Plain English: <simple explanation>`
     - `[[<repo-relative-path>#Lx-Ly](<repo-relative-path>#Lx-Ly)] Risk level: <High|Medium|Low>`
     - `[Founder statement, unvalidated] Decision owner: <owner or not specified>`
     - `[Founder statement, unvalidated] Decision deadline: <date or Not specified in sources.>`
     - `⚠️ Not mentioned — needs follow-up` (use this line when no explicit decision owner/deadline/default is stated)

## Top follow-up interview questions
- Provide 8-12 numbered questions.
- Prefix each source-tied question with clickable citation link(s), otherwise `[Founder statement, unvalidated]`.
- Do not include speculative assumptions as facts in questions.

Consistency rules:
- Preserve product names and entities exactly as sources write them.
- Do not claim integrations, compliance, metrics, dates, owners, or technical architecture unless present in sources; if absent, mark appropriately.
- Keep competitor/reference distinctions explicit, but do not force market claims beyond source wording.
- Avoid long prose paragraphs; use short factual lines per bullet.
- Use only source line ranges that actually contain the cited claim text. Do not cite broad ranges that do not support the claim.

End of prompt.
