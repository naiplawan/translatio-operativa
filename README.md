# Engineering Communication Translator

Transform engineering updates, debugging notes, incident summaries, and technical threads into operationally clear communication for engineering leadership, PMs, TPMs, and stakeholders — without losing technical truth.

---

## What This Does

Converts:
- Debugging notes → operational updates
- Incident RCAs → leadership summaries
- PR discussions → project coordination updates
- Engineering threads → Slack/standup/email formats

Into channel-optimized communication for:
- Engineering leadership
- PMs / TPMs
- Release managers
- Technical stakeholders

---

## When to Use

Use this skill whenever the user:

- Pastes debugging notes and asks to "translate for leadership"
- Shares incident summary and asks to "make this readable for PMs"
- Provides engineering thread and asks for "standup update"
- Needs engineering communication adapted for non-engineering audience

---

## Key Principles

1. **Operational Abstraction** — Describe system behavior, not code mechanics
2. **Behavioral Framing** — Focus on outcomes, not implementation labels
3. **Severity Calibration** — Descriptive over dramatic
4. **Coordination Context** — Explain gaps with scope, not internal taxonomy
5. **Audience Depth** — Adjust technical detail by audience level

---

## Output Formats

| Format | Target | Length |
|--------|--------|--------|
| Slack/Discord | Quick updates | ~80 words |
| ClickUp/JIRA | Task tracking | Structured |
| Standup | Daily sync | 1-3 lines |
| Leadership | Exec visibility | Impact-first |
| Email | Formal comms | Narrative |
| Meeting points | Discussion prep | Bullets |

---

## Language Support

- English ✅
- Thai ✅

---

## Install

```bash
npx skill install ./translatio-operrativa
```

Or manually copy `SKILL.md` to your skills directory.

---

## Files

- `SKILL.md` — Full skill specification
- `TEMPLATE.md` — Quick reference template

---

## Credit

Built with [skill-creator](https://github.com/anthropics/claude-code)

---

## Version

2026-05-28