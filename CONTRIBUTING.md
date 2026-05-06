# Contributing to Expert Peer Mode

## What We Accept

### New persona instantiations
A fully filled-in expert peer mode for a well-known domain expert. Every placeholder replaced, worked example concrete and domain-specific, iron laws derived from the expert's own documented methodology.

### Improvements to the generalized template
Changes to `skills/expert-peer-mode/SKILL.md` that improve the backbone for all instantiations. The bar is high — changes must demonstrably improve output quality, not just reorganize structure.

### Bug fixes
Placeholders accidentally left in an instantiation, broken formatting, factual errors in a persona's credentials or iron laws.

## What We Do Not Accept

- Persona instantiations for fictional characters or composite personas
- Personas where the "iron laws" are invented rather than derived from the expert's documented work
- New sections added to the template without evidence they improve output
- Duplicate personas (check existing skills before submitting)
- Legal disclaimers weakened or removed from regulated-domain skills

## Skill File Requirements

Every `skills/<persona-name>/SKILL.md` must:

1. **Have valid YAML frontmatter** — `name` and `description` fields, description under 200 characters
2. **Zero placeholders** — no `[BRACKET_TOKENS]` remaining anywhere in the file
3. **Concrete worked example** — the ❌ bad and ✅ good examples must be real artifacts from the domain, not generic placeholders
4. **Sourced iron laws** — each iron law must cite or clearly derive from the expert's documented statements, writings, or interviews
5. **Legal disclaimer** — required for any regulated domain (finance, medicine, law, engineering, safety-critical software)
6. **Completed closing** — the poetic coda must be written, not left as a placeholder

## Structure

```
skills/
└── <persona-name>/
    └── SKILL.md
```

File naming: lowercase, hyphenated, matching the persona's name (e.g. `charlie-munger`, `linus-torvalds`, `richard-feynman`).

## Submission Process

1. Fork the repository
2. Create a branch: `git checkout -b skill/<persona-name>`
3. Add `skills/<persona-name>/SKILL.md`
4. Verify: zero placeholders, concrete example, sourced laws, legal disclaimer if applicable
5. Submit a PR with:
   - Who the persona is and why their methodology is worth encoding
   - Which of their documented works/interviews the iron laws derive from
   - A sample interaction showing the skill in action

## Quality Bar

Ask before submitting: *Would this persona instantiation embarrass the template if someone used it expecting rigor?*

If the answer is anything other than "no" — fix it first.
