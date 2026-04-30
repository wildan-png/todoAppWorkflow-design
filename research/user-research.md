# User research — aTodo target audience

**Product context (from [founder-brief.md](../brief/founder-brief.md)):** aTodo is a **simple** web task tracker for **small freelance teams (typically 1–3 people)** — list + board by status + task detail — positioned against **Linear**, **Plane**, and **ClickUp** on **cost** and **feature breadth mismatch** (paying for tools larger than the job).

**Research method:** **Perplexity Deep Research was not available** in this Cursor workspace (no Perplexity MCP/API). Findings below synthesize **open-web research** (industry press releases, analyst summaries, G2-derived editorial, Reddit threads, and product-strategy literature). Treat percentages and “X mentions” on G2 as **aggregated vendor/third-party summaries**, not raw review exports.

---

## Target User Profile

**Who they are**

- **Role:** Solo freelancers and **micro-teams** (designers, developers, marketers, writers, video, consultants) often wearing sales, delivery, and ops hats; sometimes a **founder + 1–2 contractors** or a **tiny studio** with shared client work.
- **Team size:** Matches the brief: **1–3 active collaborators**; occasionally a few more seats for visibility (guests/clients) without wanting enterprise licensing math.
- **Industry:** Skilled independent work clusters in **professional services** (legal, accounting, marketing, bookkeeping, consulting), **technical services** (IT, design, engineering), and **creative services** — Fiverr’s 2025 Freelance Economic Impact Report (Census-based) segments the U.S. independent workforce roughly **51% / 26% / 22%** across those three buckets respectively ([Fiverr investor news](https://investors.fiverr.com/news-releases/news-release-details/freelance-economy-grows-amid-workforce-and-economic-volatility/)).
- **Location:** **Remote-first / distributed** is common; U.S. data shows independent professionals spread across major metros with strong growth in Sunbelt and smaller “rising tech hub” cities (same Fiverr release).
- **Age / career stage:** **Speculation (flagged):** aggregate freelance statistics often skew **Millennial / Gen X** in Western markets, with rising **Gen Z** participation on platforms; exact fit for *tiny-team PM* is not isolated in public datasets — validate in interviews.
- **Tech-savviness:** **High for core tools** (browser SaaS, Slack/Discord, Figma, GitHub, Google Workspace). They can adopt Linear-class UX **if** onboarding and scope stay small; they **resent** admin-heavy configuration and per-seat math for part-time collaborators.

**Behavior & context of use**

- **When:** **Continuous light usage** — daily stand-up style glances (“what’s in progress, who owns it”), spikes before **client deadlines** and **invoicing milestones**.
- **Where:** **Desktop browser** during deep work (aligned with aTodo’s desktop-first MVP); mobile may be secondary for this segment in V1.
- **How:** They need **one shared picture of status** (list *or* board), **assignee clarity**, and **minimal fields** — closer to **workflow tracking** than portfolio governance.

---

## Key Pain Points

1. **Price scales with seats** — Small teams and contractors chafe at **per-user** pricing when clients, PMs, or part-timers need visibility; discussion threads explicitly frame **Linear alternatives** and **“overpaying for PM tools”** for small teams ([Reddit — micro SaaS / Linear alternative](https://www.reddit.com/r/micro_saas/comments/1psyula/built_a_linear_alternative_for_small_teams_no/), [Reddit — small business PM pricing](https://www.reddit.com/r/smallbusiness/comments/1rcbrva/are_small_teams_overpaying_for_project_management/)).
2. **“Too much product” for the job** — **All-in-one** PM suites add hierarchy, views, notifications, and customization that **increase cognitive load**; industry writing ties **feature bloat** to slower decisions, buried core value, and UX clutter ([HubSpot Product — feature bloat](https://product.hubspot.com/blog/the-5-whys-of-feature-bloat); practitioner summary: [KodeKX on Medium](https://kodekx-solutions.medium.com/feature-bloat-how-it-happens-and-how-to-avoid-a-products-downfall-32279981027c)).
3. **ClickUp-specific signals (aggregated reviews / G2 editorial):** Users and G2-sourced writeups cite **initial overwhelm**, **noisy notifications**, and **sluggishness as workspaces grow** ([G2 Learn — ClickUp review](https://learn.g2.com/clickup-review)). G2’s own pros/cons pages are the canonical **quantified complaint themes** (learning curve, intuitiveness, performance) for buyers doing diligence ([G2 — ClickUp reviews](https://www.g2.com/products/clickup/reviews)).
4. **Linear-specific mismatch (community):** Praised for **speed and minimal UI**, but criticized as **very engineering-centric** for “general” small teams seeking a lighter PM layer ([Reddit — Linear alternatives](https://www.reddit.com/r/Linear/comments/1o5tveb/best_linear_alternative_for_general_use/)); PM-forum threads also note **cost / tier** friction when comparing ecosystems ([Reddit — Linear vs Jira](https://www.reddit.com/r/ProductManagement/comments/1neyq6j/been_using_linear_for_6_months_vs_jira_heres_my/)).
5. **Plane (inferred for this ICP):** Attractive to **technical** users who want **issue-style** work tracking; **self-hosting** and setup overhead skew toward **more technical** micro-teams — partial overlap with aTodo’s “keep it in the browser, no ops” positioning (**speculation**).

---

## Unmet Needs

- **A “right-sized” PM layer:** List + board + ownership + status **without** roadmap parity, automation marketplaces, or wiki-scale surface area (explicitly aTodo’s wedge per founder brief).
- **Predictable collaboration cost:** Ways to share **status** with occasional collaborators **without** treating every eyeball as a paid enterprise seat (recurring theme in small-team threads cited above).
- **Fast, calm UI:** **Linear-like** responsiveness and density, but **scope** closer to **Trello-kanban + task detail** than dev backlog tooling (**aspirational** — validate with prototypes).
- **Low ceremony onboarding:** Start tracking in **minutes**, not a multi-day “workspace architecture” project (contrast with deep hierarchy tools; G2 editorial describes **mapping Spaces/Folders/Lists** before creating work to avoid mess — [G2 Learn — ClickUp review](https://learn.g2.com/clickup-review)).

---

## Current Workarounds

- **Spreadsheets** (Google Sheets / Excel) for client + task lists — zero marginal SaaS cost, poor assignee semantics and history.
- **Notion databases** for tasks + docs — flexible but **manual** to keep status/assignments disciplined; agencies debate **Notion vs Trello** for ops vs creative workflows ([Reddit — agency tooling](https://www.reddit.com/r/projectmanagement/comments/1kiptfh/trello_or_notion_for_a_marketing_and_solutions/)).
- **Trello / Asana / Monday** (often free or low tiers) for **kanban**; may later **graduate** or **splinter** into dev tools (Linear/Jira) + docs — see comparisons in vendor blogs (e.g. [monday.com — Notion vs Trello](https://monday.com/blog/project-management/notion-vs-trello-vs-monday-work-management/)).
- **Slack / email + threads** as the “source of truth” — high **search friction** and weak **structured status**.
- **Roll-your-own micro-SaaS / internal board** to dodge seat pricing ([Reddit — micro SaaS Linear alternative](https://www.reddit.com/r/micro_saas/comments/1psyula/built_a_linear_alternative_for_small_teams_no/)) — proves demand, not a mass-market workaround.

---

## Emotional Drivers

| Driver | Why it matters for this ICP |
|--------|------------------------------|
| **Control** | Micro-teams need to **own workflow** without being forced into a vendor’s full methodology. |
| **Simplicity / clarity** | Reduces anxiety: “Are we shipping?” beats “Did we configure the portal correctly?” |
| **Speed** | Time is billable; slow loads and noisy notifications feel like **direct revenue leak** ([G2 Learn — ClickUp review](https://learn.g2.com/clickup-review)). |
| **Trust / professionalism** | Clients infer competence from **crisp** delivery rituals; the founder brief explicitly rejects a **generic blank-template** aesthetic. |
| **Cost fairness** | Strong **moral-economic** reaction to paying for unused **breadth**; aligns with donation / free-core positioning. |
| **Status (light)** | Less “enterprise procurement” prestige, more **peer respect** for being organized without enterprise baggage. |

---

## Market Signals

**Freelance / independent economy (demand side)**

- Fiverr’s **2025** economic impact release (Census / tax-based methodology) estimates **~6.9 million** U.S. independent professionals, **~$319B** revenue (~**1.1% of U.S. GDP**), with **~4M** in the top 30 metros ([Fiverr investor news](https://investors.fiverr.com/news-releases/news-release-details/freelance-economy-grows-amid-workforce-and-economic-volatility/)).
- Freelance **platform** market forecasts appear in syndicated summaries (e.g. industry articles citing **single-digit to low tens of billions USD** platform TAM by early 2030s) — useful for **labor-market tailwinds**, not direct aTodo SAM ([Yahoo Finance — freelance platforms market article](https://finance.yahoo.com/news/freelance-platforms-market-report-2025-161300920.html)).

**Project / work management software (supply side TAM)**

- Grand View Research (press materials) sizes the global **project management software** market at **USD 20.47B by 2030**, **~15.7% CAGR** (2023–2030 framing in their press copy), driven by **real-time tracking**, **remote collaboration**, and **digitization** across industries ([Grand View Research press release](https://www.grandviewresearch.com/press-release/global-project-management-software-market)).
- Same source highlights **SME** segment expected to grow at **~17.3% CAGR** (2023–2030 in that document) — directionally supportive for **small-team** buyers.
- **Interpretation for aTodo:** TAM is **large and growing**, but **highly contested**. aTodo’s realistic slice is **SAM/SOM**: teams that refuse **seat-tax** + **bloat** and want **status-first** tracking — size **unknown** without bottom-up pricing and channel tests.

---

## Source index (quick links)

| Source type | URL |
|-------------|-----|
| Founder product definition | [../brief/founder-brief.md](../brief/founder-brief.md) |
| U.S. freelance economy (Census-based) | https://investors.fiverr.com/news-releases/news-release-details/freelance-economy-grows-amid-workforce-and-economic-volatility/ |
| PM software market size / CAGR | https://www.grandviewresearch.com/press-release/global-project-management-software-market |
| ClickUp UX / G2-backed review | https://learn.g2.com/clickup-review |
| ClickUp raw review themes | https://www.g2.com/products/clickup/reviews |
| Feature bloat (product strategy) | https://product.hubspot.com/blog/the-5-whys-of-feature-bloat |
| Reddit — Linear cost / alternatives | https://www.reddit.com/r/micro_saas/comments/1psyula/built_a_linear_alternative_for_small_teams_no/ |
| Reddit — small team PM pricing | https://www.reddit.com/r/smallbusiness/comments/1rcbrva/are_small_teams_overpaying_for_project_management/ |
| Reddit — Linear general-use fit | https://www.reddit.com/r/Linear/comments/1o5tveb/best_linear_alternative_for_general_use/ |
| Reddit — agency Notion vs Trello | https://www.reddit.com/r/projectmanagement/comments/1kiptfh/trello_or_notion_for_a_marketing_and_solutions/ |

---

## Jobs To Be Done

These will be used as a design decision filter throughout the project.  
Any feature that doesn't serve at least one JTBD should be questioned.

**1.** When a **client, part-time contractor, or short-term collaborator** needs visibility into what’s in flight and our **1–3 person studio** would otherwise have to **add another paid seat** (or juggle logins) on Linear-class pricing,  
I want to **keep everyone on the same list, board, and assignees** we already use for delivery—without buying breadth we don’t run the business on,  
So I can **protect margin on small engagements** and still answer “who’s on what?” in one honest place.

**2.** When I sit down **between client calls or at the start of a billable day** with **multiple client threads** and no PMO to reconcile them,  
I want to **open one desktop view that shows every task with status and owner**—not reconstruct state from Slack subjects, email chains, or a shared spreadsheet,  
So I can **spend the first minutes on throughput, not archaeology**, and pick what actually moves today.

**3.** When our **all-in-one PM** has turned into **Spaces/Folders/Lists, noisy notifications, and slow loads** while we only need **“what’s next / who owns it / done?”** for client work,  
I want to **run list + board + task detail** without roadmap parity, doc/wiki depth, or automation marketplaces in the same product surface,  
So I can **lower cognitive load and admin** and get back to **billable delivery** instead of maintaining a workspace architecture.

**4.** When we’re a **tiny creative or professional-services micro-team** that bounced off **engineering-centric backlog tools** (or their pricing) but still envy **fast, dense UI**,  
I want **clear task identity, status columns, assignee, priority, and attachments** in a workflow that matches **freelance delivery**, not sprint rituals,  
So I can **signal competence to clients** and keep internal coordination **as light as Trello felt**, without adopting dev-team ceremony.

**5.** When we’re **24–48 hours from a client deadline or invoice milestone** and syncing with a **cofounder or subcontractor** who isn’t in every channel,  
I want to **drag or update status in one shared board** that stays in sync with the list and detail view—**same tasks, same statuses, same owners**,  
So I can **close the loop on what’s done vs blocked vs in review** with zero ambiguity before money or reputation is on the line.
