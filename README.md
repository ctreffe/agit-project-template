# AGIT Project Template

AGIT project template for structured collaboration, project context and documentation.

[Deutsche Dokumentation](README.de.md)

> [!NOTE]
> **AI Collaboration**
>
> This repository maintains the generic AGIT Project Template.
>
> The template documents AI-assisted collaboration practices, context handoff, decision records and repository conventions for structured project work.
>
> The collaboration model is maintained in [ChatGPT.md](ChatGPT.md).

## Overview

The AGIT Project Template is a generic starting point for projects that benefit from structured collaboration, clear context, documented decisions and reliable handoff between work sessions.

It is intentionally not limited to software development. It can be used for research, planning, documentation, process design, concept work, operational projects and other structured project work.

For development-oriented projects with code, scripts, automation, tests, releases and technical architecture, use or migrate toward the AGIT Dev Template.

## AGIT Templateverse

The public AGIT templates form a small templateverse: a family of related templates that share a repository-first, maintainer-led Human-AI collaboration model while specializing it for different project types.

- [AGIT Project Template](https://github.com/ctreffe/agit-project-template) is the generic starting point for structured project work, research, planning, concept work, process design and mixed projects.
- [AGIT Dev Template](https://github.com/ctreffe/agit-dev-template) is for development-oriented projects where code, scripts, automation, validation, architecture or release workflows are central.
- [AGIT Documentation Template](https://github.com/ctreffe/agit-docs-template) is for technical documentation projects such as user guides, admin guides, operating procedures, tutorials, migration guides and documentation sites.

Use the generic project template when the project shape is still open. Use a specialized template when development or documentation practice is already the center of the work.

## What the Template Provides

This template provides:

- a collaboration model for human-AI project work
- local Codex operating rules
- a project context document for session handoff
- project setup guidance and a reproducible initial prompt
- documentation standards
- repository standards
- a shared project philosophy
- Decision Record guidance for important decisions
- working folders for inputs, references, notes and outputs
- source-sensitivity guidance for raw inputs, reviewed derivatives and generated outputs
- changelog and version metadata

## Project Flow

AGIT projects should start with maintainer-owned intent:

1. Define the project purpose and context.
2. Describe the desired end state.
3. Identify boundaries and non-goals.
4. Derive a practical roadmap.
5. Work in small reviewable steps.
6. Document important decisions.
7. Keep `PROJECT_CONTEXT.md` current.
8. Harmonize affected documents before important milestones.
9. Run retrospectives when reusable lessons emerge.

## Git History Control Words

AI assistants must not perform Git history actions such as staging, committing, tagging, pushing, pulling, merging, rebasing, resetting or switching branches unless the maintainer instruction for that specific action contains a recognized control word.

Recognized control words are `explicit` and `explicitly` in English-language instructions, and the German word family `explizit`, including inflected forms such as `explizite`, `expliziten`, `expliziter` and `explizites`, in German-language instructions. Requests without one of these control words authorize preparation and guidance only.

## Decision Records

Important decisions are documented as Decision Records.

Use PDRs for durable project decisions such as project direction, scope, collaboration structure, documentation model, tool choices, review process, privacy boundaries or transition to a development-oriented project. Use ADRs or DDRs when a derived project also needs technical or documentation-specific decisions.

When a project needs decision records, use:

```text
decisions/
```

The decision record concept is documented in [DECISIONS.md](DECISIONS.md), and the default location is [decisions/](decisions/).

## Working Folders

The template includes optional working folders:

- `input/` for maintainer-provided materials
- `references/` for sources and reference material
- `notes/` for working notes and open questions
- `output/` for project deliverables

Projects may adapt or remove these folders when they are not useful.

## Transition to Dev Projects

Some projects start as general projects and later become development-oriented.

When code, scripts, automation, tests, releases, technical architecture or implementation lifecycle become central, the project may adopt guidance from the AGIT Dev Template or migrate to it.

The transition should be documented deliberately, preferably with a Project Decision Record.

## Core Documents

- [PROJECT_CONTEXT.md](PROJECT_CONTEXT.md) - current project state and handoff point
- [PROJECT_SETUP.md](PROJECT_SETUP.md) - setup guide for derived projects
- [INITIAL_PROMPT.md](INITIAL_PROMPT.md) - reproducible first prompt for project initialization
- [ChatGPT.md](ChatGPT.md) - AGIT Collaboration Model
- [CODEX.md](CODEX.md) - local Codex operating policy
- [PHILOSOPHY.md](PHILOSOPHY.md) - project philosophy
- [DOCUMENTATION.md](DOCUMENTATION.md) - documentation standards
- [REPOSITORY.md](REPOSITORY.md) - repository standards
- [DECISIONS.md](DECISIONS.md) - Decision Record guidance
- [decisions/](decisions/) - Decision Record templates
- [CHANGELOG.md](CHANGELOG.md) - version history
- [VERSION](VERSION) - current template version metadata
- [README.de.md](README.de.md) - German documentation
- [LICENSE](LICENSE) - MIT License


## Template-Only Initialization Documents

The following documents primarily support project initialization:

- `PROJECT_SETUP.md`
- `INITIAL_PROMPT.md`
- `DOCUMENTATION.md`
- `REPOSITORY.md`

After the initial setup is complete, these documents may be removed from the derived project unless they remain useful there. They may also be retained for onboarding, traceability or future re-initialization. If retained, keep their original names and optionally document their setup status inside the file or in `PROJECT_CONTEXT.md`.

## License

This project is licensed under the MIT License.
