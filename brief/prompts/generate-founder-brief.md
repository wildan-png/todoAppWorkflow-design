# Prompt: Generate `founder-brief.md` from `brief/raw/`

Use this prompt to synthesize all client context in `brief/raw/` into one structured founder brief for product design work.

---

## Instructions for the model

**Input scope (strict):**

- Read all readable text files under `brief/raw/**` recursively (e.g. `.md`, `.txt`, `.csv`).
- Exclude output and instruction files from source facts:
  - `brief/founder-brief.md`
  - `brief/prompts/**`
- Ignore binary-only files unless a text summary exists in `brief/raw/`.

**Output:**

- Write exactly one file: `brief/founder-brief.md`.

**Rules:**

1. **Do not invent or assume.** Only include claims explicitly stated in sources. If a field is unclear or absent, write exactly:
   `⚠️ Not mentioned — needs follow-up`
2. **Keep synthesis conservative.** Combine facts only when the link is explicit and unavoidable from source wording.
3. **Competitor labeling must be explicit.** Do not call a tool a direct competitor unless sources explicitly frame it as competitor/alternative/replacement.
4. **Role-based classification for named products.** For each named product, classify using explicit source wording:
   - **Direct competitor**: explicitly framed as competitor/alternative/replacement with meaningful overlap.
   - **Indirect competitor**: explicitly solves similar core problem but via different product category/scope.
   - **Reference only (not competitor)**: cited for workflow/UX pattern/adaptation, not market replacement.
   - If role is unclear, write: `⚠️ Role unclear — needs follow-up`
5. **Tie-break rule (strict).** If a product shares a workflow but is not explicitly framed as competitor, keep it out of direct competitors and place it under founder reference products with note: `Workflow reference only (not a competitor)`.
6. **Conflicts.** If sources disagree, add both statements under `## Decisions & conflicts (from sources)` and end with:
   `⚠️ Needs follow-up with client`
7. **Provenance.** Add a `## Source index` section listing all source file paths used (repo-relative).
8. **Sections constraint.** Output only the sections listed below, in exact order. One exception is allowed: `## Client follow-up checklist (for unresolved items above)` may be appended after `## Source index`.

---

## Required structure for `brief/founder-brief.md`

Use level-2 markdown headings (`##`) in this exact order:

1. `## 🎯 Product & Vision`
2. `## 🏁 Competitors & Market`
3. `## ⚙️ Product Scope`
4. `## 🎨 Design Direction`
5. `## 🔧 Technical Constraints`
6. `## 💰 Business Context`
7. `## Decisions & conflicts (from sources)`
8. `## Source index`
9. `## Client follow-up checklist (for unresolved items above)` *(optional; only when unresolved items exist)*

Under each section, keep the exact bullet questions below and answer each one.

### Under `## 🎯 Product & Vision`

- What is the product and what problem does it solve?
- Who is the target user? (demographics, behavior, context of use)
- What is the core value proposition — why would someone choose this over alternatives?

### Under `## 🏁 Competitors & Market`

- Who are the direct competitors? (name them)
- Who are the indirect competitors? (different product, same problem)
- What do competitors do well that we should match or beat?
- What do competitors do poorly that we can exploit?
- Is there a product the founder admires as a reference? (even outside the category)
- Scope note: identify which named products are `Reference only (not competitors)`.

### Under `## ⚙️ Product Scope`

- What are the must-have features for launch (MVP)?
- What is explicitly out of scope for now?
- Are there any AI features planned? (copilot, agent, automation)
- What platforms? (web, iOS, Android, desktop)

### Under `## 🎨 Design Direction`

- Is there any existing brand identity? (logo, colors, fonts)
- What visual style feels right? (references, adjectives)
- What should the product feel like to use? (fast, trustworthy, playful, professional)
- Is there anything design-wise the founder dislikes or wants to avoid?

### Under `## 🔧 Technical Constraints`

- Are there required integrations? (APIs, third-party tools)
- Any accessibility or compliance requirements?

### Under `## 💰 Business Context`

- What is the monetization model?

### Under `## Decisions & conflicts (from sources)`

- Add conflict bullets if present.
- If none, write exactly:
  `No conflicting statements captured in the sources read.`

### Under `## Source index`

- List every file path used as evidence from `brief/raw/**`.

### Under `## Client follow-up checklist (for unresolved items above)` *(optional)*

- Include only unresolved items already present in the brief.
- If there are no unresolved items, write exactly:
  `- None for this pass.`

---

*End of prompt.*
