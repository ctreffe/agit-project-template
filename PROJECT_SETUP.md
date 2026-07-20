# PROJECT_SETUP.md

# Project Setup Guide

This document describes how to initialize a new project from the AGIT Project Template.

It is primarily used during project creation and should normally remain in a
derived repository as a record of its initialization method. Record lifecycle
status and template lineage in `PROJECT_CONTEXT.md` instead of rewriting this
guide after setup.

---

# 1. Establish Project Intent

Before filling the repository with structure, clarify the maintainer-owned project intent.

At minimum, define:

- problem space or operating context
- intended audience or users
- desired end state
- boundaries and non-goals
- success criteria
- whether the project may become development-oriented later

Record this in `PROJECT_CONTEXT.md`.

---

# 2. Establish the Baseline

Identify the starting point for the project:

- local repository working tree
- uploaded materials
- existing documents
- external references
- accepted output artifacts

The baseline should be explicit enough that a future session can continue from the repository. When using AI assistance, begin the first session with `INITIAL_PROMPT.md` when practical.

Before asking an assistant to inspect input files, classify potential sensitivity. For private, unpublished, confidential, licensed or personal material, start with a source inventory rather than raw content inspection. Decide whether the project needs anonymized or reviewed derivatives before raw inputs are read. Record assistant-access approval, Git-versioning approval and publication or sharing approval separately; none implies another. Treat automated checker results as warnings rather than proof that an artifact is safe.

Document source handling in `PROJECT_CONTEXT.md`, a folder README, `input/SOURCES.md` or another project-specific source registry when useful.

---

# 3. Review Core Documents

Review and adapt:

- `README.md`
- `PROJECT_CONTEXT.md`
- `AGENTS.md`
- `ChatGPT.md`
- `CODEX.md`
- `DECISIONS.md`
- `PHILOSOPHY.md`
- `DOCUMENTATION.md`
- `REPOSITORY.md`
- `CHANGELOG.md`
- `VERSION`
- `LICENSE`

## Required AI Collaboration Note

Every derived project README should include an AI Collaboration Note near the top of the file, directly below the title and badges or language link area.

The note is a visible disclosure and orientation artifact. It should preserve the purpose, position and level of visibility of the template note while adapting the wording to the derived project.

The derived note should state:

- that the project is developed or maintained through collaboration between the repository maintainer and an AI assistant
- what the collaboration model documents in that project, such as practices, workflows, handoff rules, decision records or repository conventions
- that the collaboration model is maintained in `ChatGPT.md`

If `README.de.md` is kept, it should contain a structurally aligned German note.

## README Badge Policy

Place the badge block directly below the README title and before the AI
Collaboration Note. Use this semantic order when the corresponding information
applies:

1. status
2. version
3. license
4. real build, test or documentation automation

Derived projects must adapt the template badges to their own documented state.
Do not retain the source-template version as the project version. A status
badge needs a defined project meaning, the license badge must match the actual
license and a release badge is appropriate only when the project maintains
tags or releases. Add automation badges only for workflows that actually exist
and avoid a last-commit badge by default because activity is not a quality or
readiness signal.

Keep English and German badge blocks identical when both READMEs are present.
Record source-template version and lineage in `PROJECT_CONTEXT.md`, not in the
derived project's badge block.

Keep only what is useful for the project.

---

# 4. Review Working Folders

The template provides:

- `input/`
- `references/`
- `notes/`
- `output/`

Use them when they help. Remove or adapt them when another structure is clearer.

Do not store private, confidential or unlicensed material in versioned folders unless the project intentionally tracks it.

Use `decisions/` when the project has real decision records to store. PDRs are the default for generic project decisions, while ADRs or DDRs may be added when the decision subject is technical or documentation-specific.

For data- or artifact-oriented projects, decide whether the project should distinguish raw inputs, reviewed derivatives and generated outputs. A project may remain based on the generic template while adopting selected development practices for scripts, validation and reproducible rebuild commands.

When a folder such as `input/`, `references/`, `notes/` or `output/` gets a project-specific role, add or update a short README in that folder.

---

# 5. Create the Initial Roadmap

Derive the roadmap from project intent and desired end state.

The initial roadmap should identify:

- the first useful milestone
- the next few planned steps
- what each step should produce
- what decisions or uncertainties each step addresses
- what remains intentionally out of scope

Record the roadmap in `PROJECT_CONTEXT.md` or a dedicated roadmap document.

---

# 6. Decide Whether Decision Records Are Needed

Use Decision Records for important decisions.

Good first PDR candidates include:

- project direction
- template structure
- documentation model
- source handling
- privacy boundaries
- transition toward the AGIT Dev Template

The Decision Record concept is documented in `DECISIONS.md`.

---

# 7. Review Repository Metadata

Update repository metadata:

- repository name
- repository description
- topics
- visibility
- license

Use precise language.

---

# 8. Initialize Versioning

Set the initial project version or state.

For template repositories, Semantic Versioning is recommended.

For derived non-software projects, another consistent scheme may be appropriate, such as:

- milestone names
- date-based versions
- document revisions
- named project states

The chosen scheme should be documented.

---

# 9. Record Initialization Provenance

Keep the two initialization artifacts under their original names:

- `PROJECT_SETUP.md`
- `INITIAL_PROMPT.md`

In `PROJECT_CONTEXT.md`, record their lifecycle status, initialization date,
source template version and commit, later harmonization baseline and intentional
template deviations. Remove an initialization artifact only as a deliberate,
documented maintainer exception.

Adapt `DOCUMENTATION.md` and `REPOSITORY.md` as ongoing project rules and keep
them current throughout the project lifecycle.

---

# 10. Prepare the First Commit

The first project-specific commit should describe the initialization.

Regular working commits must use Conventional Commit prefixes such as `feat:`, `fix:`, `docs:`, `refactor:`, `test:` or `chore:`. Milestone commits are the exception: they should be human-readable, omit the prefix and include the completed version number.

Example summary:

```text
chore: initialize project from AGIT template
```

Example description:

```text
Initialize the project from the AGIT Project Template.

Adapt the project context, README, repository metadata and working folders for
the new project. Establish the initial project intent and roadmap.
```

The initialization is complete only when repository identity, maintainer
intent, desired end state, boundaries, roadmap, source-sensitivity rules,
working folders, decision-record needs, versioning and retained template files
have been reviewed and the resulting repository state is internally
consistent. Do not begin substantive project work while required
maintainer-owned setup decisions remain hidden behind placeholders.

The initialization commit is normally a regular `chore:` commit. Use an
unprefixed milestone commit only when initialization also completes a genuinely
defined and reviewed versioned milestone.

---

# 11. Continue the Project

Continue according to `ChatGPT.md`. Begin work in a new context window or
assistant session with `CONTINUATION_PROMPT.md`.

Keep `PROJECT_CONTEXT.md` current when:

- a milestone completes, including after a commit or tag has been created
- the roadmap changes
- important decisions are made
- new inputs or references become important
- the project is paused
- a new session needs to resume work

`CONTINUATION_PROMPT.md` should remain in the derived repository for repeatable
re-entry after initialization.

`HARMONIZATION_PROMPT.md` should also remain for maintainer-initiated
source-template, internal-consistency and roadmap alignment.

`RETROSPECTIVE_PROMPT.md` should remain for maintainer-initiated, structured
reviews of Maintainer-Agent collaboration.
