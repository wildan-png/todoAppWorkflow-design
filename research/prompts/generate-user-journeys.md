# Prompt: generate `/research/user-journeys.md` (Part A + Part B)

Run this against the repo (human or agent). Output is the **full file body** for `research/user-journeys.md` only.

## Read (in order)

1. `/brief/founder-brief.md` — constraints and positioning
2. `/research/user-research.md` — pains, JTBD
3. `/research/personas.md` — Jordan, Priya, Miguel
4. `/design/modules-features.md` — modules, feature names, descriptions, labels (core/supporting/nice-to-have), MVP cut §4, guardrails §Scope

## File structure (Option B — one file, two parts)

```markdown
# User journeys — aTodo

## Part A — App-level journeys (persona × lifecycle)

### Journey: [Full persona name] — [Primary goal in one line]
| Stage | Touchpoint | Action | Thought / Emotion | Pain to avoid | Opportunity |
...

## Part B — Feature-level journeys (every feature)

### Feature: [Feature name] — [Module name]
- **Label:** …
- **Primary persona:** …
- **JTBD refs:** …

| Stage | Touchpoint | Action | Thought / Emotion | Pain to avoid | Opportunity |
...
```

## Part A — App-level journey (per persona)

For **each** persona in `personas.md`, one end-to-end **product** journey (discovery → advocacy).

**Stages (exactly six rows):** Awareness → Onboarding → First value → Core loop → Power use → Advocacy

**Columns:** Stage | Touchpoint | Action | Thought / Emotion | Pain to avoid | Opportunity

Ground pains in `user-research.md` / personas; opportunities may align with `modules-features.md` without dumping specs.

## Part B — Feature-level journeys (all features)

**Source:** Every feature row in **§3 Features per Module** of `modules-features.md` (core + supporting + nice-to-have). Preserve **module order** and **row order** within each module.

**Per-feature heading:** `### Feature: [Feature name] — [Module name]`

**Metadata block (bullets, 3–4 lines):**

- **Label:** core | supporting | nice-to-have
- **Primary persona:** one of Jordan / Priya / Miguel + one-sentence justification
- **JTBD refs:** `#n` from the feature row, briefly spelled out

**Table — same columns as Part A; five stages:**

| Stage |
|-------|
| Trigger |
| Orient |
| Act |
| Confirm |
| Recover / Next |

**Rules:**

- Touchpoints name plausible aTodo surfaces (list, board, detail, settings, invite, empty state).
- If feature is **post-MVP** per `modules-features.md` §4 **Post-MVP Backlog**, add a short caveat in *Pain to avoid* or *Opportunity*.
- Reflect **board/list/detail parity** in Confirm/Recover where the feature touches workflow state.
- No empty cells; English; GitHub-flavored markdown tables.

## Quality bar

- No features omitted from Part B.
- Terminology: default statuses To do / In progress / Done; 1–3 person teams; desktop-first; free-core + non-blocking donation per brief.

Deliver **only** the complete `research/user-journeys.md` content (no preamble or postscript).
