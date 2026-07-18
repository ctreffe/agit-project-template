# PROJECT_CONTEXT.md

# Project Context Template

This document captures the current state of a project created from the AGIT Project Template.

It is the primary handoff document for resuming work after a pause, continuing on another computer or starting a new AI-assisted session.

Replace the placeholders during project setup.

---

# Template Lineage and Initialization

Repository role:

```text
<derived project>
```

Source template:

```text
AGIT Project Template
```

Initial template baseline:

```text
<template version and commit hash>
```

Initialization status:

```text
<not started | in progress | completed>
```

Initialization date:

```text
<YYYY-MM-DD | not yet completed>
```

Last template harmonization:

```text
<not yet performed | template version, commit hash and date>
```

Intentional template deviations and relevant Decision Records:

```text
<none | concise list>
```

Keep `PROJECT_SETUP.md` and `INITIAL_PROMPT.md` as initialization provenance.
They describe the project's methodological roots; this section records their
lifecycle status and the baselines used over time.

---

# Project

Project name:

```text
<project name>
```

Repository:

```text
<repository URL or local path>
```

Short description:

```text
<one or two sentences describing the project>
```

Project type:

```text
<general | research | documentation | process | planning | mixed | development-oriented>
```

Potential transition:

```text
<whether this project may later adopt the AGIT Dev Template>
```

---

# Maintainer Project Intent

Maintainer-owned initial context:

```text
<problem space, operating context, audience or environment>
```

Desired end state:

```text
<what the project should enable, produce or make easier when successful>
```

Boundaries and non-goals:

```text
<what the project should avoid, postpone or deliberately not cover>
```

Success criteria:

```text
<how the maintainer will know the project has succeeded>
```

---

# Current Status

Current project version or state:

```text
<version, date, milestone or named state>
```

Current phase or milestone:

```text
<current milestone name>
```

Current focus:

```text
<what the project is currently working on>
```

Status:

```text
<planned | in progress | review | waiting for input | validated | completed | paused | archived>
```

---

# Working Baseline

Current baseline:

```text
<local working tree | uploaded materials | public repository | accepted output artifact>
```

Baseline notes:

```text
<notes about which repository state, files or materials are authoritative>
```

---

# Roadmap

- `<next step>` - `<purpose or expected result>`
- `<later step>` - `<purpose or expected result>`

Roadmap entries should be small enough to review and validate.

---

# Inputs and References

Important input materials:

- `<input file or source>`

Important references:

- `<reference, source or link>`

Source handling notes:

```text
<privacy, licensing, verification or data-disclosure notes>
```

Source sensitivity and handling:

```text
<which raw inputs are private, confidential, licensed, unpublished or personal; what should be represented through reviewed derivatives>
```

Assistant-access approval:

```text
<exact sources or reviewed derivatives, permitted task and limitations>
```

Git-versioning approval:

```text
<exact reviewed artifacts approved for Git, or none>
```

Publication or sharing approval:

```text
<exact artifacts and audience, or none>
```

Reviewed derivatives:

- `<derived file or artifact>` - `<relationship to raw source and review status>`

---

# Outputs

Current or expected deliverables:

- `<deliverable>`

Output location:

```text
<output/ path, document path or external location>
```

Generated output status:

```text
<which outputs are generated, which source files produce them and whether they are versioned or regenerated locally>
```

---

# Open Questions

- `<open question>`

If there are no open questions, state that explicitly.

---

# Important Decisions

Important decisions already made:

- `<decision>`

Relevant decision records:

- `<decision record file, if any>`

---

# Relevant Documents

- `README.md` - project overview
- `PROJECT_SETUP.md` - retained initialization method and provenance
- `INITIAL_PROMPT.md` - retained first-session initialization prompt
- `CHANGELOG.md` - version or project-state history
- `ChatGPT.md` - collaboration model
- `CODEX.md` - local Codex operating policy, if Codex is used
- `CONTINUATION_PROMPT.md` - reproducible re-entry instruction for a new context window or assistant session
- `DECISIONS.md` - Decision Record guidance
- `decisions/` - Decision Record templates or project decisions, if used
- `PHILOSOPHY.md` - project philosophy
- `DOCUMENTATION.md` - documentation standards
- `REPOSITORY.md` - repository standards
- `input/` - input materials
- `references/` - references and sources
- `notes/` - working notes
- `output/` - deliverables

Remove or adapt entries that do not apply.

- `PROJECT_SETUP.md` and `INITIAL_PROMPT.md` remain as initialization provenance unless the maintainer documents a deliberate exception.
- Active roadmap milestones should progress through small regular commits when
  meaningful project steps can be reviewed separately.
- Maintainer decisions and clarification questions should be presented as
  concise numbered lists when practical.
- After milestone commits or tags, update this document to reflect the completed state rather than leaving pre-commit review instructions as the current focus.
- Git history actions require a maintainer instruction containing a recognized control word: `explicit` or `explicitly` in English, or `explizit` and inflected forms such as `explizite`, `expliziten`, `expliziter` and `explizites` in German. Commit, tag or push wording without a recognized control word only authorizes preparation and guidance.

---

# Notes for the Next Session

Use this section to make restarting work easy.

```text
<what to do next, what not to change yet, what needs review, what is blocked>
```
