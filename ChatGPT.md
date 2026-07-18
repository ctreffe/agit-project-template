# ChatGPT.md

# AGIT Generic Collaboration Model v0.2.0

**Status:** Stable generic model
**Applies to:** AGIT projects  
**Repository Maintainer:** ctreffe

---

# Purpose

This document describes the collaboration model used for AGIT projects.

It is intentionally written for both human contributors and AI assistants. It contains no hidden prompts. It openly documents how AGIT projects are planned, executed, reviewed, documented and improved.

The model exists to make collaboration reproducible across conversations, work sessions and projects. A new session should be able to reconstruct the project state from repository documents, not from private memory or chat history.

---

# Core Principles

AGIT projects follow these principles:

- Clarify intent before defining the roadmap.
- Work from the repository as the source of truth.
- Prefer small reviewable steps over large opaque changes.
- Document important decisions.
- Keep current state separate from history.
- Preserve useful context for future sessions.
- Use precise language.
- Validate results before declaring completion.
- Prefer integrity over apparent helpfulness.
- Never simulate completed work or invented artifacts.

---

# Maintainer Intent and Desired End State

At the start of a project, the maintainer should describe the project intent from their own point of view.

This should normally include:

- the problem space or operating context
- intended users, maintainers or audience
- desired end state
- important boundaries and non-goals
- risks, constraints or sensitivities
- what would make the project successful

The assistant may help structure this input, but should not invent the project direction from technical possibilities alone.

---

# PROJECT_CONTEXT.md as Handoff Point

Every AGIT project should maintain `PROJECT_CONTEXT.md`.

`PROJECT_CONTEXT.md` is the primary entry point for resuming work. It should describe the current state, not the full project history.

It should capture:

- project intent and desired end state
- current status
- current roadmap
- working baseline
- completed milestones or project states
- open questions
- important decisions already made
- relevant documents and materials
- notes for the next session

When a session becomes long, when a substantial change is in progress or when work may continue on another computer or in another conversation, the project context should be updated before lower-priority work continues.

Begin a new context window or assistant session with
`CONTINUATION_PROMPT.md`. It defines the ordered re-entry check and requires the
assistant to reconcile `PROJECT_CONTEXT.md` with current read-only Git evidence
before substantive work continues.

---

# Roadmap-First Work

The roadmap is the guide for deciding what to do next.

A roadmap should be derived from maintainer intent, desired end state, boundaries and current project status.

Roadmap entries should be small enough to review and validate. They should explain what uncertainty they reduce, what result they produce or what decision they enable.

The roadmap may evolve deliberately as learning accumulates.

---

# Work Rhythm

AGIT projects should progress through small loops:

```text
Plan -> Produce -> Review -> Harmonize -> Record -> Continue
```

For repository-based work, these loops should normally map to regular working
commits. For non-code projects, they may map to reviewed document states,
decision records or deliverable versions.

A work step should represent one logical change or result. A roadmap milestone
should normally contain several small, reviewable working steps when the work
can be separated meaningfully. The project should not accumulate an entire
milestone as one undifferentiated change merely to create a single milestone
commit at the end.

The preferred repository rhythm is:

```text
Plan -> Produce -> Review or validate -> Adjust -> Prepare working commit -> Continue
```

When the milestone objective is satisfied, perform a separate freshness and
consistency pass, then prepare the milestone commit. Invoke the formal
harmonization prompt only when the maintainer requests it. The milestone commit
closes the milestone; it is not a container for work that should already have
been recorded in regular commits.

At a meaningful checkpoint, the assistant should provide a concise numbered
handoff that identifies the result ready for review, validation performed,
known limitations or disclosure risks, decisions required from the maintainer,
the proposed next step and, when ready, a commit summary and description.

---

# Git History Authority

The assistant has no default permission to perform Git history actions.

Git history actions include, but are not limited to:

- staging files
- creating commits
- amending commits
- rebasing
- resetting
- reverting
- creating, deleting or switching branches
- creating or deleting tags
- pushing or force-pushing
- pulling or merging
- changing `.git/` contents directly

The assistant may inspect Git status, diffs and logs when useful. The assistant
may prepare file changes, propose commit boundaries and suggest commit summaries
and descriptions.

The assistant must not perform Git history actions unless the maintainer
instructs the assistant to perform that specific action and uses a recognized
control word.

Recognized control words are `explicit` and `explicitly` in English-language
instructions, and the German word family `explizit`, including inflected forms
such as `explizite`, `expliziten`, `expliziter` and `explizites`, in
German-language instructions.

For Git history actions, general intent is not enough. Requests such as "commit
this", "create the commit", "set the tag" or "push this" remain requests to
prepare the repository-ready state and commit metadata unless the instruction
contains a recognized control word.

Maintainer approval for file edits does not imply approval for Git history
actions. A request to prepare, build, organize or document a change does not
imply permission to commit it. Approval for one class of Git history action does
not imply approval for another; local commits, tags and pushes each require
their own maintainer instruction with a recognized control word.

Repository history is maintainer-controlled project memory.

Regular working commits must use Conventional Commit prefixes such as `feat:`,
`fix:`, `docs:`, `refactor:`, `test:` or `chore:`. Milestone commits are the
exception: they should not use a Conventional Commit prefix and should include
the completed version number.

Every recommended commit must include both a concise summary and a meaningful
description. The description should state what the commit actually changes and,
when useful, why; it must not repeat unrelated history or present future work as
completed.

When decisions, review questions or maintainer actions need a response, the
assistant should use a concise numbered list whenever practical. Each item
should be independently answerable and distinguish decisions, checks, review
points and Git actions.

---

# Sensitive Sources and Derivatives

Before inspecting private, unpublished, confidential, licensed or personal raw material, the assistant should first help inventory the material at the metadata level: file names, file types, maintainer descriptions, expected use and sensitivity. The assistant should ask before reading raw contents when sensitivity is plausible.

When possible, prefer reviewed derivatives that expose only the information needed for the project, such as anonymized tables, redacted excerpts, normalized data, extracted observations or review artifacts.

The maintainer remains responsible for approving access to sensitive source
material and for deciding what may be versioned or shared. Approval for an
assistant to inspect a specific source or reviewed derivative, approval to
version it in Git and approval to publish or otherwise share it are separate
decisions. None implies another.

Sensitive raw material should not be added to Git by default. Before placing
source files in a repository, define what is allowed to be versioned, establish
the necessary `.gitignore` rules and prefer reviewed, redacted or anonymized
derivatives when they are sufficient. If sensitive material has entered the
working tree or staging area, stop and review its handling before preparing a
commit.

Generated outputs may remain sensitive even when they do not contain the raw
source. Review tables, figures, screenshots, excerpts, archives, interactive
content, embedded resources and file metadata for disclosure risk before Git
versioning or sharing them.

Automated privacy, secret or content checks are warning systems, not approval.
A clean result does not prove that an artifact is anonymous, non-confidential,
licensed for use or safe to version or publish.

---

# Decisions and Decision Records

Important decisions should be documented as Decision Records.

The Decision Record concept is described in `DECISIONS.md`.

Use a PDR when a decision affects:

- project direction
- scope or non-goals
- collaboration structure
- documentation structure
- source or evidence handling
- privacy or data disclosure boundaries
- tool or repository choices
- review or approval process
- transition toward a development-oriented project

Decision records should explain context, decision, rationale and consequences.

Not every small choice needs a PDR.

---

# Evidence and Source Handling

When a project relies on external material, distinguish clearly between:

- verified facts
- source-based summaries
- assumptions
- open questions
- maintainer-provided context
- AI-generated interpretation

Sensitive or private material should not be sent to external services without explicit approval.

---

# Deliverables

Deliverables depend on the project.

Examples include:

- project plans
- research notes
- decision records
- documentation
- reports
- checklists
- process descriptions
- presentations
- spreadsheets
- repository changes
- implementation plans

The assistant must not report a deliverable as complete unless it actually exists and is available in the agreed form.

---

# Documentation and Harmonization

Documentation is part of the project.

When a change affects multiple documents, update them together so the repository reads as one coherent state.

Do not append isolated notes when an existing section should be updated.

Use `HARMONIZATION_PROMPT.md` for a deliberate content harmonization. A
harmonization compares a derived project with its recorded source template,
reconciles internal project files and checks whether the roadmap still fits
maintainer intent and the current state. The concrete project and its Decision
Records remain authoritative; template changes are never copied blindly.

Harmonization concerns project content. It does not evaluate Maintainer-Agent
collaboration or derive changes for the source template. Collaboration
observations are deferred to a retrospective.

---

# Retrospectives and Template Evolution

Retrospectives evaluate Maintainer-Agent collaboration and the rules, feedback,
decision, handoff and work rhythms that shape it. The maintainer decides when
to invoke a retrospective and which period it should cover.

Use `RETROSPECTIVE_PROMPT.md` for the structured collaboration review. Separate
practices to retain, project-level collaboration changes, content implications
for later harmonization, abstracted template candidates and no-action findings.

When a derived project reveals a collaboration pattern that would help future projects, propose it for the template.

Template changes should be made deliberately and should avoid overfitting the template to one project.

A retrospective finding is only a template candidate. The assistant must not
modify the source-template repository unless the maintainer authorizes that
specific template change with a recognized control word. Template-edit
permission does not authorize staging, committing, pushing or any other Git
history action; each Git action requires its own specific control-word
instruction.

---

# Transition to Development-Oriented Projects

Some AGIT projects start as general projects and later become development-oriented.

When code, scripts, automation, tests, releases, technical architecture or implementation lifecycle become central, the project may adopt or migrate toward the AGIT Dev Template.

This transition should be intentional and documented, preferably with a PDR.

---

# Definition of Success

A successful AGIT project has:

- clear intent
- understandable current context
- useful documentation
- documented important decisions
- reviewable outputs
- transparent open questions
- a clear next step or completion state
- enough repository context for future continuation
