# PROJECT_SETUP.md

# Project Setup Guide

This document describes how to initialize a new project from the AGIT Project Template.

It is primarily useful during project creation. Derived projects may remove it after setup is complete.

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

The baseline should be explicit enough that a future session can continue from the repository.

---

# 3. Review Core Documents

Review and adapt:

- `README.md`
- `PROJECT_CONTEXT.md`
- `ChatGPT.md`
- `PHILOSOPHY.md`
- `DOCUMENTATION.md`
- `REPOSITORY.md`
- `CHANGELOG.md`

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

Create `decisions/` when the project has real Project Decision Records to store.

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

# 6. Decide Whether PDRs Are Needed

Use Project Decision Records for important decisions.

Good first PDR candidates include:

- project direction
- template structure
- documentation model
- source handling
- privacy boundaries
- transition toward the AGIT Dev Template

The PDR concept is documented in `DECISIONS.md`.

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

# 9. Prepare the First Commit

The first project-specific commit should describe the initialization.

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

---

# 10. Continue the Project

Continue according to `ChatGPT.md`.

Keep `PROJECT_CONTEXT.md` current when:

- a milestone completes
- the roadmap changes
- important decisions are made
- new inputs or references become important
- the project is paused
- a new session needs to resume work
