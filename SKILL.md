---
name: Engineering Communication Translator
description: Convert engineering updates, debugging notes, incident postmortems, PR discussions, and technical threads into operationally clear communication for engineering leadership, PMs, TPMs, release managers, and technical stakeholders. Use this skill whenever the user shares engineering communication that needs to reach a non-engineering audience — paste a Slack thread, PR description, incident update, or debug notes and ask "translate for leadership" or "make this readable for PMs" or "convert to standup update." Preserves technical accuracy while adapting tone, structure, and detail level for ClickUp, JIRA, Slack, Discord, async standup, email, leadership summaries, escalations, and meeting talking points.
---

# Engineering Communication Translator

Translate implementation-heavy engineering communication into organization-level operational communication without losing technical truth.

This skill converts:
- debugging notes
- incident updates
- RCA summaries
- migration status
- PR discussions
- release coordination updates
- engineering investigation threads
- implementation progress updates

into communication optimized for:
- engineering leadership
- engineering managers
- PMs
- TPMs
- release managers
- tech leads
- architecture stakeholders
- technically-adjacent engineering executives

The goal is not simplification.

The goal is operational clarity.

---

# Core Principle

Do not remove technical meaning.

Remove implementation noise.

Preserve:
- operational truth
- delivery status
- ownership
- blockers
- risk level
- release implications
- customer/business impact
- dependency relationships
- coordination-critical identifiers

The rewrite should help stakeholders quickly understand:
- What happened?
- What changed?
- Who is affected?
- What is the current state?
- Who owns it?
- What happens next?
- Is there release risk?
- Is there customer impact?
- Is this blocked, mitigated, or resolved?

Do NOT:
- narrate debugging sessions
- replay investigation chronology
- expose implementation trivia
- explain code internals unnecessarily
- inflate urgency
- convert engineering updates into business theater

---

# Information Hierarchy

Prioritize information in this order:

1. customer/business impact
2. operational severity
3. current status
4. owner
5. next action
6. blockers/dependencies
7. release/timeline implications
8. technical explanation

Technical detail is supporting context, not the headline.

---

# Audience Boundary

This skill is for:
- engineering leadership
- engineering managers
- PMs
- TPMs
- release managers
- tech leads
- architecture stakeholders
- engineering-adjacent executives

The audience:
- understands systems and delivery
- coordinates releases and dependencies
- evaluates operational risk
- tracks milestones and rollout confidence
- understands engineering terminology

The audience does NOT:
- read code
- parse stack traces
- follow debugger sessions
- need implementation-level narration
- care about local reproduction mechanics

This skill is NOT for:
- customers
- marketing
- investor relations
- sales
- finance
- public relations
- non-technical executive communication
- true ELI5 explanations

If the requested audience is external or customer-facing, confirm before proceeding.

---

# Audience Technical Depth

Determine audience level first — it controls how much technical detail survives the rewrite.

| Audience | Allowed Technical Depth |
|----------|-------------------------|
| Engineer | Exact method/function detail acceptable |
| Tech Lead | Some implementation mechanics, architectural constraints |
| PM/Release/Leadership | Operational abstraction preferred — focus on impact, risk, rollout confidence |
| Executive Summary | Impact-first only — no implementation detail |

## Tech Lead / Architecture Stakeholders
May include:
- important implementation mechanics
- concurrency behavior
- migration sequencing
- architectural constraints

## PM / Release / Leadership
Prefer:
- operational behavior
- release implications
- rollout confidence
- dependency coordination
- risk and mitigation

Avoid:
- exact method names
- inheritance details
- internal lifecycle narration

## Executive Summary
Lead almost entirely with:
- impact
- delivery confidence
- release status
- operational risk

---

# Preserve Operational Specificity

Do not abstract concrete engineering issues into vague business language.

Bad:
> “A system issue affected stability.”

Good:
> “Users intermittently lost saved form progress after session expiry.”

Bad:
> “Infrastructure coordination is ongoing.”

Good:
> “Platform and mobile teams are coordinating rollout sequencing.”

Bad:
> “An integration issue caused instability.”

Good:
> “The API and mobile rollout became incompatible after the auth token format change.”

Operational clarity requires concrete system behavior and concrete impact.

---

# Translation Boundary

Keep low-level technical detail when it directly affects:
- rollout safety
- migration sequencing
- production stability
- distributed consistency
- scalability limits
- concurrency behavior
- recovery guarantees
- incident mitigation
- architectural constraints

Do not simplify away operationally significant engineering mechanics.

Good:
> “The migration must complete before enabling the new auth flow.”

Bad:
> “Some infrastructure dependencies still exist.”

---

# Communication Intent

Determine the operational purpose before rewriting.

Possible intents:
- status update
- blocker escalation
- release risk warning
- dependency coordination
- migration tracking
- incident communication
- implementation confirmation
- decision request
- rollout coordination
- validation update

Shape:
- urgency
- structure
- detail density
- tone
- prioritization

according to the communication intent.

A blocker escalation should not read like a routine status update.

---

# Rewrite Process

## 1. Extract

Identify:
- issue/change
- operational impact
- affected systems/users
- current state
- owner
- next action
- blockers
- dependencies
- timeline
- risk level
- release implications

---

## 2. Remove

Strip implementation-only detail unless operationally relevant:
- file paths
- line numbers
- stack traces
- debugger narration
- bisect history
- exploratory notes
- commit SHAs
- temporary local diagnostics
- exact conditionals
- low-level sequencing detail

Do NOT remove:
- ticket IDs
- PR numbers
- release versions
- workload identifiers
- migration names
- framework names
- service names
- environment labels

These are operational coordination anchors.

---

## 3. Translate

Convert implementation mechanics into operational cause-and-effect.

Bad:
> “The race occurs between stream registration and shared device synchronization.”

Good:
> “Two initialization paths executed in the wrong order under parallel workloads, causing intermittent failures.”

Bad:
> “The hydration layer reused conditional restoration logic from the existing mixin pattern.”

Good:
> “The new flow now reuses the same recovery behavior already proven in production.”

Focus on:
- system behavior
- operational implications
- delivery meaning
- customer impact
- coordination impact

not implementation narration.

---

## 4. Compress

When reducing detail:
- preserve outcomes
- preserve impact
- preserve ownership
- preserve blockers
- preserve identifiers

Compress:
- debugging chronology
- exploratory investigation steps
- repeated implementation detail
- code-level narration
- investigation dead ends

The shorter version must still allow stakeholders to:
- assess risk
- understand status
- coordinate dependencies
- evaluate delivery confidence

---

## 5. Reshape

Adapt:
- structure
- tone
- density
- pacing
- length

to the destination channel.

Examples:
- standup → compressed
- Slack → scan-friendly
- leadership summary → impact-first
- escalation → risk-first
- email → narrative
- meeting notes → speaking order

---

## 6. Validate

Before finalizing:
- no invented facts
- no fake certainty
- no hallucinated owners/timelines
- no missing operational identifiers
- no severity inflation
- no implementation trivia without operational value
- no customer-facing language unless requested
- no management consulting tone
- no unnecessary recommendations

---

# Decision Visibility

If the source contains:
- approval requests
- rollout decisions
- rollback discussions
- dependency conflicts
- unresolved tradeoffs
- release gates
- resource constraints

surface them explicitly.

Leadership communication should clearly expose:
- what decision exists
- who owns the decision
- what blocks the decision
- timeline implications

Do not bury operational decisions inside implementation detail.

---

# Severity Calibration

Match the emotional weight of the source material.

Do NOT escalate:
- bugs into incidents
- regressions into outages
- delays into blockers
- investigations into crises
- uncertainty into instability
- restoration failures into “data loss”

Prefer descriptive severity over dramatic labels:
- “localized regression”
- “intermittent issue”
- “validation still in progress”
- “users saw blank fields despite backend retaining the data”
- “draft restoration failure”

Over:
- “critical failure”
- “major instability”
- “catastrophic regression”
- “severe platform issue”
- “HIGH”
- “users lost their data” (unless truly lost)

Do not dramatize routine engineering work.

For leadership communication, prefer operational precision: describe what happened without escalation labels unless your org has formal severity taxonomy.

---

# Handling Unknowns

If information is genuinely unknown:
- state that directly
- preserve uncertainty accurately
- avoid filler language
- avoid artificial confidence
- avoid speculation

Good:
- “Root cause investigation is still in progress.”
- “Timeline depends on validation results.”
- “Ownership is still being coordinated.”
- “Impact scope is still under verification.”

Bad:
- “The team is continuing efforts to better understand the issue.”
- “There may potentially be additional contributing factors.”

Do not invent:
- owners
- timelines
- severity
- mitigation status
- rollout confidence
- impact scope
- root causes

---

# Avoid Corporate Rewrite Tone

Do not rewrite engineering updates into:
- executive marketing language
- management consulting phrasing
- performative professionalism
- artificial optimism
- vague business abstractions

Prefer:
> “Validation is still running.”

Over:
> “The team is continuing comprehensive validation efforts.”

Prefer:
> “Release confidence remains blocked pending migration validation.”

Over:
> “The organization is continuing cross-functional alignment activities.”

Use:
- active voice
- direct operational language
- short paragraphs
- concrete ownership
- calm confidence

---

# Multi-Item Updates

When summarizing multiple workstreams:
- group related work together
- lead with highest operational impact
- collapse repetitive implementation detail
- preserve important identifiers inline
- avoid repeated status phrasing

Prefer:
> “Three auth-related regressions were resolved across mobile and API flows.”

Over:
> Ticket-by-ticket narration with repeated technical detail.

---

# Keep vs Remove

## Keep

Preserve operational coordination anchors:
- ticket IDs
- PR numbers
- release versions
- migration names
- workload identifiers
- framework names
- service names
- environment labels

Examples:
- `PR #5751`
- `ClickUp-86d34jv42`
- `v7.2`
- `Flutter`
- `Next.js`
- `Golang`

---

## Remove

Remove implementation noise unless operationally necessary:
- stack traces
- file paths
- line numbers
- debugger chronology
- local reproduction steps
- exact conditionals
- temporary debug logs
- internal expressions
- exploratory diagnostics

Leadership cares about:
- impact
- ownership
- mitigation
- delivery risk
- release confidence

not low-level implementation narration.

---

# Channel Formats

## ClickUp / JIRA / Written Status Update

Use structured sections.

Preferred structure:
- Status
- Impact
- What changed
- Current state
- Owner
- Next steps
- Risk/blockers
- Mitigation/workaround

Example:

> **Status:** Fix in review.
>
> **Impact:** Users intermittently lose saved form progress after reconnecting following session expiry.
>
> **What changed:** A recent auth flow update interrupted draft restoration during reload.
>
> **Current state:** Root cause confirmed and validation passed locally.
>
> **Owner:** Somchai — PR #5751.
>
> **Next steps:** Review → merge → backport to v7.2.
>
> **Risk:** Low. The fix reuses an existing production-tested recovery pattern.

---

## Slack / Discord

Short and scan-friendly.

Structure:
- one bolded headline
- 2–4 concise bullets

Example:

> **Auth draft recovery regression identified; fix in review.**
>
> - Affects users resuming incomplete forms
> - Root cause confirmed in recent auth reload flow
> - Somchai’s fix: PR #5751
> - Backport to v7.2 planned after merge

Targets:
- top-level update: under ~80 words
- thread reply: under ~40 words

No greetings or sign-offs.

---

## Async Standup

Maximum:
- 1–3 lines
- status-first
- minimal wording

Pattern:

> `<state>. <owner>. <next>.`

Examples:

> Fixed auth registration regression (ClickUp-86d34jv42). PR #5751 in review. Backport after merge.
>
> Root cause narrowed to state synchronization during mount. Validation still running.

No bullets or labels.

---

## Leadership Summary

Optimize for:
- operational awareness
- delivery confidence
- release visibility
- dependency coordination
- major risk tracking

Lead with:
- impact
- delivery state
- release implications
- operational blockers

Avoid implementation narration.

---

## Escalation Update

Lead with:
- blocker
- affected systems
- release/timeline impact
- mitigation status
- owner

Keep concise and operational.

Avoid emotional language.

---

## Email

Use:
- strong subject line
- concise paragraphs
- minimal structure

Example subject:

> Auth registration regression: fix in review (PR #5751)

Structure:
- greeting
- status + impact
- current state
- next steps
- optional decision/request
- sign-off

Do not turn emails into ticket dumps.

---

## Meeting Talking Points

Optimize for spoken delivery.

Rules:
- bullet list only
- one idea per bullet
- chronological speaking order
- IDs inline
- short clauses

Example:

- Auth regression identified in v7.2
- Users lose draft state after reconnect
- Root cause confirmed in reload sequence
- Somchai’s fix in PR #5751
- Backport planned after validation

---

# Clarification Rule

If the destination format is unclear, ask exactly one concise clarifying question.

Example:

> “Which format do you want — ClickUp, Slack, standup, email, escalation, or meeting notes?”

Do not ask additional questions unless required to avoid inventing facts.

---

# Operational Abstraction Rule

When rewriting for leadership or cross-functional stakeholders:

Prefer:
- system behavior
- operational flow
- lifecycle stage
- recovery behavior
- initialization sequence
- rollout coordination

Over:
- exact method names
- hook names
- mixin names
- inheritance mechanics
- internal architecture narration
- code-level implementation detail

Bad:
> Added await loadSavedFormData() to onCacheLoaded()

Good:
> Added the missing draft restoration step during form initialization.

Bad:
> Auto-selection bypassed the mixin hydration path.

Good:
> One initialization path skipped the normal recovery flow.

Bad:
> The _backgroundRefresh() lifecycle hook was clearing savedFormData.

Good:
> The background refresh was clearing the draft state incorrectly.

---

# Behavioral Framing Rule

Prefer describing:
- system behavior
- operational outcome
- workflow impact
- release implications

Over:
- implementation terminology
- internal lifecycle labels
- validation category names
- architecture jargon

Bad:
> The cache-loaded phase missed the restoration call.

Good:
> The form initialization flow skipped draft recovery.

Bad:
> Static analysis passed.

Good:
> Automated validation passing (25/25 tests).

Bad:
> Users can re-enter their data.

Good:
> No backend recovery action required.

Bad:
> A latent architectural concern was identified.

Good:
> A related lifecycle dependency was identified during review and flagged for future monitoring. No immediate release risk identified.

Bad:
> May share the same dormant pattern.

Good:
> Additional forms will be reviewed to confirm consistent initialization.

Bad:
> Users lost their saved data.

Good:
> Users saw blank fields despite the backend retaining the data.

Bad:
> Added the missing restoration call during form load.

Good:
> Restored the missing draft recovery step during form initialization.

---

# Coordination Context Rule

When explaining why an issue escaped earlier fixes or audits:

Prefer:
- rollout scope
- audit coverage
- coordination sequencing
- release grouping

Over:
- internal bug taxonomy
- implementation classifications
- hook-level architecture narration
- debugging categorization

Good:
> “P602 was unintentionally excluded from the earlier draft restoration patch batch.”

Bad:
> “This belonged to a different bug class on the same initialization hook.”

Good:
> “Related to the May 14 form synchronization patch, but caused by a separate recovery-path gap that was not included in the earlier audit.”

Bad:
> “Same onCacheLoaded hook, different bug class.”

---

# Thai Language Support

When the user requests Thai output (e.g., "translate for leadership in Thai", "Thai standup", "ภาษาไทย"):

- Maintain all operational abstraction principles — the language changes, not the discipline
- Use natural Thai phrasing for technical concepts; do not transliterate English terms that have established Thai equivalents
- Keep stakeholder-facing tone: professional but not corporate
- Preserve operational identifiers (ticket IDs, PR numbers, service names, environment labels) in their original form — do not translate or transliterate them
- Severity calibration rules apply equally: avoid dramatic Thai labels (หายนะ, วิกฤตร้ายแรง) unless severity is genuinely confirmed; prefer descriptive terms (กรณีเฉพาะจุด, มีปัญหาเป็นช่วงๆ, ยังตรวจสอบอยู่)
- Channel format constraints (word limits, structure) remain the same

---

# Constraints

- Never invent owners, timelines, blockers, risks, or root causes.
- Never convert speculation into confirmed fact.
- Never remove operational identifiers.
- Never rewrite into customer-facing language unless requested.
- Never replace operational precision with vague business language.
- Never dramatize uncertainty.
- Never add recommendations unless explicitly requested.
- Never turn status updates into strategy memos.
- Never optimize for “executive polish” over operational clarity.

---

# Worked Examples

## Source (Engineering Comment)

> The `EntitySelectionMixin` draft hydration logic reused the same conditional restoration flow already implemented in P601/P606/P608.

---

## ClickUp Version

> **Status:** Draft recovery implementation confirmed.
>
> **What this means:** The new screen now restores previously saved form progress using the same recovery behavior already used in P601/P606/P608.
>
> **Implementation approach:** The work reused an existing production-tested pattern rather than introducing new recovery logic.
>
> **Risk:** Low. Behavior aligns with existing production flows.

---

## Slack / Discord Version

> **Draft recovery implemented using the same production-tested pattern as P601/P606/P608.**
>
> Users returning to incomplete forms will automatically recover saved progress. Low implementation risk since this reuses existing production behavior.

---

## Standup Version

> Reused the existing draft-recovery pattern from P601/P606/P608 for the new screen. Validation complete; low-risk rollout.

---

# Escalation Example

> **Release risk identified for v7.2 rollout.**
>
> Validation exposed intermittent failures during parallel workload initialization. Root cause is confirmed and mitigation is in progress.
>
> Current impact is limited to high-concurrency workloads, but release confidence remains blocked pending validation completion.
>
> **Owner:** Platform team.
>
> **Next update:** After validation completes.
