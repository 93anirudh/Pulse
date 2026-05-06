# CA AI Product — Project Context

> **Source of truth for the autonomous routine.** Read this first, every run. Update this last, every run.
> Version: v2 — 2026-05-06
> Repo location: `/_context.md` (root)
> Drive mirror: /CA AI Product/_context.md (auto-versioned by Drive)

---

## North Star

An AI **awareness layer** for Indian Chartered Accountants — solo and small-to-mid firms in Tier 2/3 cities — that proactively surfaces what's missing, stale, due, or inconsistent in their work.

Trust is built by being the firm's situational memory: deadlines, gaps, anomalies, follow-ups, missing client inputs, returns nearing cutoff. Smart data entry is downstream of awareness, not the other way around.

We are **not** building a chatbot the user queries. We **are** building a layer that flags *what they don't know to ask*.

---

## Current state

### The Pulse
- Single-file HTML AI readiness diagnostic, light/dark theming, Fraunces + Inter
- Five-pillar framework: Information, Workflow, Intake, Team, Safety
- Drag-and-drop Kanban, fullscreen modals, three-stage story visual, persona results
- **Question set is PLACEHOLDER.** Real set must route by (a) biggest pain workflow, (b) which inputs the user has standardized, (c) appetite for a 30-min plug-in solution
- Hosting: Netlify Drop primary

### DigiMon (deprioritized, not deleted)
- Local Electron + LangChain + Gemini agent
- Critique: feels like an API wrapper + chatbot, not a complete product
- On hold; revisit only if the awareness-layer thesis points back to local-first

### Plug-in product (in design)
- Constrained-environment, plug-and-play tool
- Constraint = input format (file types, naming, source-software output), NOT storage layer
- Live improvement metric on landing page from production DB
- Fallback for unfit users: consultation → eventual onboarding once data is shaped right

---

## Active priorities

| # | Priority | Status | Last progress |
|---|---|---|---|
| 1 | Finalize Pulse question set (route by readiness × workflow) | Drafting | 2026-05-06 (init) |
| 2 | Lock the wedge workflow for plug-in product | Hypothesis: GSTR-2B reconciliation | 2026-05-06 (init) |
| 3 | Set up 2 distribution channels for 30-day test (LinkedIn + ICAI) | Not started | — |
| 4 | Build plug-in product MVP for chosen workflow | Blocked by #2 | — |
| 5 | Live-impact-metric infrastructure on landing page | Blocked by #4 | — |

---

## Decisions locked

- Drive is an *example* of constrained environment, not the platform decision
- Local-first not abandoned in principle — platform follows workflow choice
- Cowork scheduled tasks abandoned in favor of **Claude Code Routines** (cloud, autonomous, no machine dependency)
- Versioning = GitHub commits on `_context.md` + Drive revision history on outputs
- Workflow first, platform falls out of it
- Ani is reactive on direction; brainstorming/scanning/drafting/coding runs autonomously

---

## Open questions

> Any question marked **[answerable]** can be worked on by the routine without Ani.
> Any question marked **[needs Ani]** stays open until Ani replies via email.

- **[answerable]** What does a tight Pulse question set look like? Draft v1 of 12–15 questions covering 5 pillars × workflow-routing logic.
- **[answerable]** Which CA workflow has highest pain × clearest inputs × monthly recurrence? Score GSTR-2B, TDS, Form 3CD, ITR, MCA on these axes from public sources.
- **[answerable]** What is the actual landscape of Indian CA tools (Tally, ClearTax, KDK, Winman, others)? Build a competitive matrix.
- **[needs Ani]** What's the price floor for solo CAs in Tier 2/3? (Hypothesis ₹500–2,000/month)
- **[needs Ani]** Does the awareness layer ship as a separate free tier, or is the Pulse the front door indefinitely?
- **[needs Ani]** Confirm GSTR-2B as the v1 wedge after the workflow scoring is done.

---

## Signal (from market scans — append-only, do not delete)

> Whatever the routine finds in scans that hasn't been acted on yet. Each entry: date, source, claim, implied action.

*(empty on init — first scan will populate)*

---

## Operating principles

- Iterative and fast — evaluate options quickly, commit ("B, go")
- Honest technical assessment before coding
- Self-contained deployable artifacts (single HTML, portable .exe)
- UI/UX reference-driven (kubrick.life/pathsofglory2, hellomonday.com, ESPN E-Ticket)
- Tone: surface specifics from the user; don't project narrow scenarios onto them
- Token efficiency matters in every output

---

## File / artifact locations

| Type | Where |
|---|---|
| This doc | GitHub repo root: `_context.md` |
| Drive mirror | /CA AI Product/_context.md |
| Pulse codebase | GitHub (private) |
| Pulse question drafts | /CA AI Product/Pulse/Questions/ |
| Architecture / design docs | /CA AI Product/Architecture/ |
| Working brainstorm docs | /CA AI Product/Working/ |
| Daily/weekly review docs | /CA AI Product/Reviews/ |
| Market scan outputs | /CA AI Product/Scans/ |
| DigiMon (paused) | github.com/93anirudh/DigiMon, branch `feat/google-oauth` |

---

## Reactivity contract

- **Routine (autonomous)**: brainstorming, scanning, drafting, coding, doc maintenance, surfacing options, answering [answerable] questions
- **Ani (reactive)**: direction calls, validation, customer conversations, "B, go", anything tagged [needs Ani]

If a routine run surfaces a [needs Ani] question and Ani hasn't replied within 48 hours, the next run flags it as outstanding in the email and continues with [answerable] work.

---

## Decision Log (append-only)

> Every routine run appends one entry. Format: timestamp UTC, action, artifact link, what unblocks next.
> The routine MUST read the last 5 entries before choosing its next action, and MUST NOT repeat any of them.

| Timestamp (UTC) | Action | Artifact | Unblocks |
|---|---|---|---|
| 2026-05-06 init | Project context v2 written, autonomous loop designed | this doc | Routine setup |

---

*End of context. Routine: read `routine_prompt.md` next.*
