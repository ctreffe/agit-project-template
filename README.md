# AGIT Project Template

[![Status](https://img.shields.io/badge/status-stable-green)](VERSION)
[![Version](https://img.shields.io/github/v/tag/ctreffe/agit-project-template?label=version)](CHANGELOG.md)
[![License](https://img.shields.io/github/license/ctreffe/agit-project-template)](LICENSE)

> [!NOTE]
> **AI Collaboration**
>
> This repository maintains the generic AGIT Project Template.
>
> The template documents AI-assisted collaboration practices, context handoff, decision records and repository conventions for structured project work.
>
> The collaboration model is maintained in [ChatGPT.md](ChatGPT.md).

[Deutsche Dokumentation](README.de.md) · The English README is authoritative; the German README is maintained as a close translation.

## Contents

- [Overview](#overview)
- [Core Principle](#core-principle)
- [AGIT Templateverse](#agit-templateverse)
- [When to Use This Template](#when-to-use-this-template)
- [Project Initialization](#project-initialization)
- [Recommended Workflow](#recommended-workflow)
- [Git Index and Protected Git Actions](#git-index-and-protected-git-actions)
- [Decision Records](#decision-records)
- [Repository Structure](#repository-structure)
- [Template and Derived Project Files](#template-and-derived-project-files)
- [How to Use This Template](#how-to-use-this-template)
- [Maintainer Tool Setup](#maintainer-tool-setup)
- [Continuous Improvement](#continuous-improvement)
- [License](#license)

## Overview

The AGIT Project Template is a generic starting point for projects that benefit from structured collaboration, explicit context, documented decisions and reliable handoff between work sessions. It is intentionally not limited to software development: it supports research, planning, concept work, process design, operational projects and mixed project types.

The template provides a repository-first collaboration model, local Codex rules, reproducible setup and continuation prompts, a current-state project context, documentation and repository standards, decision-record guidance and optional working folders. It is a project method and repository foundation, not a domain-specific framework.

## Core Principle

The maintainer owns the project intent and direction. The assistant may help structure information, identify gaps, prepare artifacts, check consistency and preserve project memory, but it must not invent the desired end state, silently resolve consequential decisions or report work as complete when it does not exist.

The repository is the durable project memory. A future maintainer, contributor or assistant should be able to understand the current state and continue the work without relying on private chat history.

## AGIT Templateverse

The public AGIT templates form a small templateverse: a family of related templates that share a repository-first, maintainer-led Human-AI collaboration model while specializing it for different project types.

- [AGIT Project Template](https://github.com/ctreffe/agit-project-template) is the generic starting point for structured project work, research, planning, concept work, process design and mixed projects.
- [AGIT Dev Template](https://github.com/ctreffe/agit-dev-template) is for development-oriented projects where code, scripts, automation, validation, architecture or release workflows are central.
- [AGIT Documentation Template](https://github.com/ctreffe/agit-docs-template) is for technical documentation projects such as user guides, admin guides, operating procedures, tutorials, migration guides and documentation sites.

## When to Use This Template

Use the Project Template when the project shape is still open or when several kinds of work need one coherent project memory. It is well suited to discovery, planning, research, coordination, process design and projects that may later become more specialized.

Start from a specialized template when the primary work is already clear:

- choose the Dev Template for implementation, tests, automation and releases;
- choose the Documentation Template for audience-oriented technical documentation and publication;
If a generic project later becomes development-oriented, document the transition and adopt or migrate toward the Dev Template deliberately.

## Project Initialization

Initialization turns the reusable template into a concrete project and preserves how that project began.

1. Create a repository from this template and establish the authoritative local baseline.
2. Start the first assistant session with [INITIAL_PROMPT.md](INITIAL_PROMPT.md).
3. Follow [PROJECT_SETUP.md](PROJECT_SETUP.md).
4. Provide the maintainer-owned purpose, desired end state, intended users or audience, boundaries, risks and non-goals.
5. Decide which working folders, source-handling rules, review expectations and Decision Record types the project needs.
6. Adapt the README files, repository metadata and ongoing project rules.
7. Complete [PROJECT_CONTEXT.md](PROJECT_CONTEXT.md) with the initial roadmap, repository baseline and template provenance.
8. Prepare the first small, reviewable project state and validate its internal consistency before committing it.

Initialization is incomplete while required project choices remain hidden behind placeholders. `PROJECT_SETUP.md` and `INITIAL_PROMPT.md` normally remain in the derived repository as initialization provenance.

## Recommended Workflow

AGIT projects proceed from maintainer intent through small, reviewable project loops:

```text
Intent -> Roadmap -> Produce -> Review -> Harmonize -> Record -> Continue
```

1. Establish or confirm the repository baseline.
2. Review the maintainer intent, desired end state and current roadmap.
3. Select the smallest useful step that reduces uncertainty or produces a reviewable result.
4. Create or revise the project artifact.
5. Review or validate the result and make limitations visible.
6. Update affected context, documentation and decision records.
7. Prepare a regular working commit with an appropriate Conventional Commit prefix.
8. Continue until the milestone objective is satisfied.
9. Close the milestone separately by reconciling current state, versioning and history.

Use [CONTINUATION_PROMPT.md](CONTINUATION_PROMPT.md) to reconstruct the project in a new session. Use [HARMONIZATION_PROMPT.md](HARMONIZATION_PROMPT.md) for deliberate project-content alignment and [RETROSPECTIVE_PROMPT.md](RETROSPECTIVE_PROMPT.md) for a separate review of Maintainer-Agent collaboration.

## Git Index and Protected Git Actions

The maintainer controls Git history. Assistants may inspect status, diffs and logs and may prepare working-tree changes and commit metadata.

Staging and unstaging are index operations. They do not require a control word, but they may be performed only after a specific maintainer request or authorization of the corresponding commit. Existing staged selections and unrelated changes must be preserved.

Protected actions include commits, amendments, tags, pushes, pulls, merges, rebases, resets, branch changes, stash manipulation and other Git history operations. An assistant may perform a specific protected action only when the instruction for that action contains `explicit` or `explicitly` in English, or the German word family `explizit`. File-edit approval does not authorize Git history changes, and approval for one protected action does not authorize another.

Regular working commits use Conventional Commit prefixes such as `feat:`, `fix:`, `docs:` or `chore:`. Milestone commits omit the prefix, use a human-readable summary containing the completed version and close already reviewed work.

## Decision Records

Decision Records preserve why consequential choices were made. Choose the prefix by decision subject, not merely by repository type:

- **PDR — Project Decision Record:** project direction, scope, roadmap, collaboration, governance, privacy boundaries, review models or repository relationships.
- **ADR — Architecture Decision Record:** technical architecture, tooling, formats, automation or another durable technical structure in a derived project.
- **DDR — Documentation Decision Record:** documentation structure, terminology, audience-facing material, publication rules or documentation QA.

The generic template defaults to PDRs and explains the model in [DECISIONS.md](DECISIONS.md). Use [decisions/](decisions/) only for decisions whose rationale will matter to future collaborators; small routine choices do not need a record.

## Repository Structure

### Entry Points and Project Memory

- **`README.md` and `README.de.md`** introduce the project, explain how to start and link to the deeper rules. English is authoritative, while German is maintained as a close structural and semantic translation.
- **`PROJECT_CONTEXT.md`** is the primary re-entry point. It records current intent, status, roadmap, baseline, validation state, open decisions and the next useful step rather than duplicating the full project history.
- **`CHANGELOG.md` and `VERSION`** describe completed states and version history. They are updated when a versioned milestone is completed, not merely when work begins.

### Collaboration and Operating Rules

- **`ChatGPT.md`** defines the general Maintainer-Agent collaboration model, authority boundaries and work rhythm. It is transparent project documentation, not a hidden prompt.
- **`CODEX.md`** defines local execution, network, disclosure and Git rules for Codex. Keep it when Codex performs local repository work and adapt it only for deliberate project-specific needs.
- **`PHILOSOPHY.md`** records the values behind the project method, including intent before structure, traceability, lightweight process and integrity over appearance.

### Setup, Continuation and Review

- **`PROJECT_SETUP.md` and `INITIAL_PROMPT.md`** guide the first initialization and preserve its methodological provenance. Derived projects normally retain both files and record their lifecycle status in `PROJECT_CONTEXT.md`.
- **`CONTINUATION_PROMPT.md`** defines the ordered re-entry check for a later context window or assistant session. It reconciles project context with read-only Git evidence before substantive work resumes.
- **`HARMONIZATION_PROMPT.md`** aligns project content, internal documentation and roadmap with the recorded template baseline. It does not evaluate collaboration quality or copy template changes blindly.
- **`RETROSPECTIVE_PROMPT.md`** evaluates Maintainer-Agent collaboration over a selected period. Project-content implications are handed to later harmonization, while transferable process findings remain controlled template candidates.

### Repository Guidance and Decisions

- **`DOCUMENTATION.md`** defines documentation roles, current-state versus history boundaries and quality expectations. It remains an ongoing project rule after initialization.
- **`REPOSITORY.md`** defines repository organization, Git conventions, source and output handling, versioning and repository-ready delivery. Derived projects adapt it to their actual workflow rather than treating it as disposable setup material.
- **`DECISIONS.md` and `decisions/`** explain Decision Records and store durable decision rationale. The template provides reusable PDR guidance and subject-specific record templates.

### Optional Working Folders

- **`input/`** holds maintainer-provided material when the project needs local inputs. Raw private, confidential, licensed or personal material requires an access and versioning decision before inspection or Git inclusion.
- **`references/`** holds sources, references or reviewed source notes. Projects should document provenance, licensing and sensitivity when these affect use.
- **`notes/`** holds working notes and open questions that are useful to the project but are not yet durable decisions or deliverables.
- **`output/`** holds project deliverables or generated results. Projects define whether outputs are versioned milestones, review artifacts or reproducible local products and review them before sharing.

## Template and Derived Project Files

The template contains reusable rules and placeholders. In a derived project:

- fill and maintain `PROJECT_CONTEXT.md` as the current project state;
- adapt both README files, `DOCUMENTATION.md` and `REPOSITORY.md` to the concrete project;
- keep `ChatGPT.md`, `CODEX.md` and `PHILOSOPHY.md` unless a documented project need requires a change;
- retain `PROJECT_SETUP.md` and `INITIAL_PROMPT.md` as initialization provenance;
- retain the continuation, harmonization and retrospective prompts for repeatable later use;
- adapt or remove optional working folders only when their role is understood;
- replace template Decision Records with real records only when consequential decisions exist.

Record the source-template version and commit, initialization status, last harmonization baseline and intentional deviations in `PROJECT_CONTEXT.md`. A derived project is authoritative for its own intent and accepted decisions; template updates are reviewed and adapted rather than copied blindly.

## How to Use This Template

1. Initialize the repository through `INITIAL_PROMPT.md` and `PROJECT_SETUP.md`.
2. Keep `PROJECT_CONTEXT.md` current as the concise project handoff.
3. Derive the roadmap from maintainer-owned intent, boundaries and success criteria.
4. Work in small artifacts or changes that can be reviewed independently.
5. Distinguish raw inputs, reviewed derivatives and generated outputs before granting access, versioning or publication.
6. Record consequential decisions in `decisions/` using the appropriate subject prefix.
7. Validate results before presenting them as complete.
8. Begin later sessions with `CONTINUATION_PROMPT.md` instead of repeating initialization.
9. Invoke harmonization when project content or template alignment needs a deliberate review.
10. Invoke a retrospective separately when the collaboration process should be evaluated.
11. Close milestones with coherent context, documentation, changelog and version metadata.

## Maintainer Tool Setup

The generic template has no mandatory domain toolchain. A practical local baseline is:

- Git and a maintainer-controlled Git client such as GitHub Desktop;
- a text or Markdown editor;
- PowerShell on Windows or an equivalent local shell;
- `rg` or another fast search tool;
- project-specific tools installed only when the concrete work requires them.

Prefer project-local environments such as `.venv/` or `node_modules/` over global changes. Package installation, external services and network use should have a clear project purpose, and private repository material should remain local by default.

## Continuous Improvement

Use harmonization to keep a concrete project internally consistent and aligned with relevant template developments. Use retrospectives to evaluate collaboration practices and identify reusable lessons without overfitting the template to a single project.

Template changes are deliberate, cross-document changes. A retrospective finding is only a candidate until the maintainer approves the specific template update; derived projects and their Decision Records remain authoritative for project-specific choices.

## License

This project is licensed under the [MIT License](LICENSE).
