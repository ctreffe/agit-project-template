# AGIT Project Template

AGIT project template for structured collaboration, project context and documentation.

## Overview

The AGIT Project Template is a generic starting point for projects that benefit from structured collaboration, clear context, documented decisions and reliable handoff between work sessions.

It is intentionally not limited to software development. It can be used for research, planning, documentation, process design, concept work, operational projects and other structured project work.

For development-oriented projects with code, scripts, automation, tests, releases and technical architecture, use or migrate toward the AGIT Dev Template.

## What the Template Provides

This template provides:

- a collaboration model for human-AI project work
- a project context document for session handoff
- project setup guidance
- documentation standards
- repository standards
- a shared project philosophy
- Project Decision Record guidance for important decisions
- working folders for inputs, references, notes and outputs
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

## Project Decision Records

Important decisions are documented as Project Decision Records (PDRs).

Use PDRs for durable decisions such as project direction, scope, collaboration structure, documentation model, tool choices, review process, privacy boundaries or transition to a development-oriented project.

When a project needs PDRs, create:

```text
decisions/
```

The PDR concept is documented in [DECISIONS.md](DECISIONS.md).

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
- [ChatGPT.md](ChatGPT.md) - AGIT Collaboration Model
- [PHILOSOPHY.md](PHILOSOPHY.md) - project philosophy
- [DOCUMENTATION.md](DOCUMENTATION.md) - documentation standards
- [REPOSITORY.md](REPOSITORY.md) - repository standards
- [DECISIONS.md](DECISIONS.md) - Project Decision Record guidance
- [CHANGELOG.md](CHANGELOG.md) - version history
- [VERSION](VERSION) - current template version metadata
- [LICENSE](LICENSE) - MIT License

## License

This project is licensed under the MIT License.
