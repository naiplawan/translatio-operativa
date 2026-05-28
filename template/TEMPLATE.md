# Engineering Communication Translator
## Template for Operational Communication

---

## What This Does

Transforms engineering debug notes, incident updates, PR discussions, and technical threads into operationally clear communication for engineering leadership, PMs, TPMs, and stakeholders — without losing technical accuracy.

---

## When to Use

Use whenever you need to communicate engineering work to non-engineering audiences:
- "translate for leadership"
- "make this readable for PMs"
- "convert to standup update"
- "Slack update"
- Leadership summary
- Incident postmortem

---

## Transformation Rules

### 1. Operational Abstraction

Prefer system behavior over method/hook names.

| Instead of... | Use... |
|---------------|--------|
| `onCacheLoaded` didn't call `loadSavedFormData()` | Form initialization skipped draft restoration |
| Auto-selection bypassed the mixin path | One initialization path skipped normal recovery |
| The `_backgroundRefresh()` hook was clearing | Background refresh was clearing incorrectly |

### 2. Behavioral Framing

Describe system outcomes, not implementation.

| Instead of... | Use... |
|---------------|--------|
| Static analysis passed | Automated validation passing |
| Added the restoration call | Restored missing draft recovery |
| Cache null-clobber | Data was inadvertently cleared |
| Latent architectural concern | Flagged for future monitoring |

### 3. Severity Calibration

Descriptive severity over dramatic labels.

| Avoid | Preferred |
|-------|-----------|
| HIGH | localized regression |
| critical failure | intermittent issue |
| users lost data | users saw blank fields (backend retained data) |
| catastrophic | Low-risk fix |

### 4. Coordination Context

Explain audit gaps with scope, not internal taxonomy.

| Instead of... | Use... |
|---------------|--------|
| Same hook, different bug class | Separate recovery-path gap not included in earlier audit |
| Belonged to bug class #2 | Unintentionally excluded from patch batch |

### 5. Audience Technical Depth

| Audience | Allowed Detail |
|----------|----------------|
| Engineer | Exact method names OK |
| Tech Lead | Some implementation mechanics |
| PM/Leadership | Operational abstraction only |
| Executive | Impact-first only |

---

## Output Formats

### Slack / Discord

- Under 80 words
- Bold headline
- 2-4 scan-friendly bullets
- No greetings/sign-offs

Example:
> **Safari iOS cart data regression identified; fix in progress.**
> - Impacts users with Safari private mode enabled
> - Root cause: Storage layer rejects writes silently
> - Implementation path being finalized

---

### ClickUp / JIRA

- Structured sections
- Status, Impact, What changed, Current state, Owner, Next steps, Risk

Example:
> **Status:** Fix in review.
>
> **Impact:** Users losing cart data on Safari iOS when navigating.
>
> **What changed:** Storage error handling added during initialization.
>
> **Risk:** Low — localized regression, uses existing pattern.

---

### Standup

- 1-3 lines
- Status-first
- No bullets/labels

Example:
> Fixed Safari cart regression. Error handling for private browsing mode. Validation passes locally.

---

### Leadership Summary

- Impact-first
- Delivery state
- Risk assessment
- Release implications
- No implementation detail

Example:
> **Impact:** Users on Safari (iOS) private browsing lose cart contents when navigating.
>
> **Root cause:** Browser storage rejects writes silently in private mode. App doesn't handle this gracefully.
>
> **Risk:** Low — localized, reuses existing pattern.

---

### Email

- Strong subject line
- Concise paragraphs
- Minimal structure

Subject: `[Feature] Cart regression: fix in review`

---

### Meeting Talking Points

- Bullets only
- Chronological order
- One idea per bullet
- Short clauses

---

## Language Support

Both Thai and English supported.

For Thai output:
- Maintain operational abstraction principles
- Use natural Thai phrasing for technical concepts
- Keep stakeholder-facing tone

---

## Quick Reference Card

```
INPUT: Engineering notes/debugging thread/incident
↓
APPLY:
□ Operational abstraction (no method names)
□ Behavioral framing (no implementation labels)
□ Severity calibration (no drama)
□ Coordination context (scope, not taxonomy)
□ Audience-appropriate detail depth
↓
OUTPUT: Channel-optimized format
```

---

## Skill Source

Location: `~/Desktop/Workhub/skill-tree/translatio-operrativa/SKILL.md`

Last Updated: 2026-05-28