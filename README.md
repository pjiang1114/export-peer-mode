# Expert Peer Mode

A library of AI skills that configure your agent as a rigorous, flattery-free peer to named domain experts. Each skill suppresses sycophancy, enforces structured three-layer thinking, and applies the expert's own iron laws to every response.

## How It Works

Instead of a generic AI assistant, you get a thinking peer who operates under a specific expert's methodology — their discipline, their quality standards, their way of finding the root cause, their poetic philosophy. The agent checks itself against the expert's iron laws before every reply and delivers evidence, not confidence.

The backbone is a generalized 12-section template (`expert-peer-mode`) that can be instantiated for any domain expert. Each instantiation is a ready-to-use system prompt or Claude Code skill.

## Skills Library

### Foundation

| Skill | Persona | Domain |
|-------|---------|--------|
| [expert-peer-mode](skills/expert-peer-mode/SKILL.md) | Generalized template | Any domain |

### Instantiations

*No instantiations yet — see [Contributing](CONTRIBUTING.md) to add a persona.*

## The Backbone: 12-Section Template

Every expert peer mode skill follows the same structure:

1. **Identity block** — establishes peer authority, not VIP treatment
2. **Addressing ceremony** — minimal, specific, non-negotiable
3. **Core discipline** — verify before speaking; the anti-pattern-matching contract
4. **Three-layer shuttle** — Phenomenon → Essence → Philosophy → Delivery
5. **Iron laws** — 2–4 domain-specific quality rules, each with a concrete trigger
6. **Worked example** — bad vs good, with ❌/✅, showing elimination not handling
7. **Output protocol** — fixed shape for every reply + 3-question self-check
8. **Deletion list** — anti-patterns that get cut on sight
9. **Retention list** — what earns a place in the response
10. **Disagreement protocol** — evidence beats opinion; no groveling either way
11. **Hard metrics** — quantitative hygiene ceilings
12. **Legal disclaimer** — domain-appropriate disclaimers for regulated fields

## Quickstart

### Claude Code

**Official marketplace:**
```bash
/plugin install expert-peer-mode@claude-plugins-official
```

**Manual installation:**
```bash
# Clone the repo
git clone https://github.com/pjiang1114/export-peer-mode.git

# Copy skill to Claude global commands
cp -r export-peer-mode/skills/expert-peer-mode ~/.claude/commands/

# Or symlink for auto-updates
ln -s $(pwd)/export-peer-mode/skills/expert-peer-mode ~/.claude/commands/expert-peer-mode
```

Then in Claude Code:
```
/expert-peer-mode
```

### Use as a system prompt

Copy the contents of any `SKILL.md` directly into your agent's system prompt field. Works with Claude, GPT-4, Gemini, and any instruction-following model.

## Usage

### Invoke the generalized template

```
/expert-peer-mode
```

The skill asks for: persona name, domain, credentials, addressing formula, and 2–4 iron laws. It instantiates the full framework for the session.

### Generate a new persona prompt

```
Use /expert-peer-mode to generate a prompt for [PERSONA_NAME]
```

The skill produces a fully instantiated, zero-placeholder system prompt you can save as a new skill file.

## The Three-Layer Shuttle

The core thinking method used by every persona:

```
┌──────────────────────────────────────────────────────────────┐
│  Phenomenon layer  — what the user sees                       │  ← receive + deliver
│  Essence layer     — what's really wrong/missing/broken       │  ← diagnose
│  Philosophy layer  — the underlying law/principle/pattern     │  ← generalize
└──────────────────────────────────────────────────────────────┘
```

**Phenomenon (doctor):** collect the symptom. Do not theorize.
**Essence (detective):** find the structural cause. This is where the real work happens.
**Philosophy (poet):** name the timeless law this violated — the statement that prevents the next occurrence.
**Return:** fix + essence + law, in that order.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for how to submit new expert persona instantiations.

**To add a new persona:**
1. Copy `skills/expert-peer-mode/SKILL.md` as your starting template
2. Replace all `[PLACEHOLDER]` tokens with persona-specific content
3. Ensure zero placeholders remain in the final file
4. Add a worked example with ❌/✅ that is concrete and domain-specific
5. Include the legal disclaimer section if the domain is regulated
6. Submit a PR with the new `skills/<persona-name>/SKILL.md`

## Philosophy

The problem with AI "expert mode" prompts is they produce flattery dressed as expertise. The persona says smart-sounding things without the discipline that made the expert credible in the first place.

This template enforces the discipline: read the primary source before speaking, invert before advocating, eliminate before handling, name the underlying law not just the fix. The persona is rigorous because the scaffold forces it to be.

> Code is written for humans to read; machines just happen to run it.
> Analysis is judgment; overconfidence is the shattering of the circle.
> The template is the constraint; the constraint is what produces the clarity.

## License

MIT License — see [LICENSE](LICENSE) for details.
