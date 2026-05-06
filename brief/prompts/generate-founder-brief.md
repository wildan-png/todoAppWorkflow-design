# Prompt: Generate `founder-brief.md` in backup2 style

Use this prompt to synthesize all relevant context into a founder brief that matches the style and structure of `brief/founder-brief.backup2.md`.

---

## Instructions for the model

**Input scope:**

- Read all readable text files under `brief/raw/**` recursively (e.g. `.md`, `.txt`, `.csv`).
- Also read `brief/brief.md` if it exists.
- Exclude output and instruction files from source facts:
  - `brief/founder-brief.md`
  - `brief/prompts/**`
- Ignore binary-only files unless a text summary exists.

**Output:**

- Write exactly one file: `brief/founder-brief.md`.

**Style requirements (must match backup2 feel):**

1. Use this exact title line at top:
   `# Founder brief — synthesized from \`/brief/\``
2. Immediately below title, add a single-line `**Sources:** ...` summary.
3. Use `---` separators between major sections.
4. For each question, format as:
   `- **Question text?**`
   then answer on the next indented line.
5. Keep language practical and product-facing. Prefer concrete defaults over vague placeholders.
6. If information is missing, do **not** invent facts. Use one of:
   - `Founder: not specified yet.`
   - `Not specified in sources.`
7. You may include labeled defaults only when clearly marked, using:
   - `Recommended default (speculative — confirm): ...`
8. Competitor handling:
   - Only call products direct/indirect competitors when explicitly supported by sources.
   - If a product is inspirational only, label it as a reference.
9. No generic filler text. Every bullet must either cite source-backed fact or explicit labeled speculation.

---

## Required structure for `brief/founder-brief.md`

Use level-2 markdown headings (`##`) in this exact order:

1. `## 🎯 Product & Vision`
2. `## 🏁 Competitors & Market`
3. `## ⚙️ Product Scope`
4. `## 🎨 Design Direction`
5. `## 🔧 Technical Constraints`
6. `## 💰 Business Context`
7. `## Decisions & definitions (plain English)`

Under each section, keep the exact bullet questions below and answer each one.

### Under `## 🎯 Product & Vision`

- What is the product and what problem does it solve?
- Who is the target user? (demographics, behavior, context of use)
- What is the core value proposition — why would someone choose this over alternatives?
- What does success look like in 6 months? In 1 year?

### Under `## 🏁 Competitors & Market`

- Who are the direct competitors? (name them)
- Who are the indirect competitors? (different product, same problem)
- What do competitors do well that we should match or beat?
- What do competitors do poorly that we can exploit?
- Is there a product the founder admires as a reference? (even outside the category)

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

- Has a tech stack been decided?
- Are there required integrations? (APIs, third-party tools)
- Any accessibility or compliance requirements?

### Under `## 💰 Business Context`

- What is the monetization model?
- Who are the stakeholders involved in design decisions?

### Under `## Decisions & definitions (plain English)`

- Add numbered items for unresolved implementation decisions found in sources.
- For each item:
  - Explain what it means in plain English.
  - Add one `Recommended default (speculative — confirm): ...` if helpful.
- If there are no unresolved decisions, write:
  `No unresolved implementation decisions were captured in the sources read.`

---

*End of prompt.*
