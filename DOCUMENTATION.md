# DOCUMENTATION.md

# Documentation Standards

Documentation is part of the project.

It should make the project understandable without relying on private chat history.

---

# Document Roles

## README.md

The public entry point. It explains what the project is, who it is for and where to find more information.

## PROJECT_CONTEXT.md

The current-state handoff document. It describes where the project stands now.

## CHANGELOG.md

The history of completed project states or template versions.

## ChatGPT.md

The collaboration model.

## CODEX.md

Local Codex operating policy for repository access, tool use, Git usage and
data-disclosure boundaries.

## PHILOSOPHY.md

The project values and reasoning style.

## REPOSITORY.md

Repository organization and version-control guidance.

## DECISIONS.md

Project Decision Record guidance.

It explains when to create PDRs, where to store them and which structure to use.

## input/

Maintainer-provided or project input materials.

## references/

Sources, background material and reference notes.

## notes/

Working notes and open questions.

## output/

Deliverables and final outputs.

---

# Current State vs. History

Keep current state and history separate.

- Current state belongs in `PROJECT_CONTEXT.md`.
- History belongs in `CHANGELOG.md`.
- Durable decisions belong in PDRs when the project creates them.
- Working notes belong in `notes/`.
- Deliverables belong in `output/`.

---

# Source and Evidence Notes

When a project uses external sources, document enough context to understand how they were used.

Where relevant, distinguish:

- direct source material
- summaries
- assumptions
- maintainer-provided context
- AI interpretation
- information that still needs verification

---

# Harmonization

When a change affects multiple documents, update them together.

Avoid adding isolated notes when existing sections should be revised.

Harmonization is especially important after:

- roadmap changes
- important decisions
- scope changes
- completion of a milestone
- retrospectives
- transition toward a development-oriented project

---

# Language and Tone

Use precise, plain language.

Avoid promotional wording.

Prefer clarity over persuasion.

State limitations, uncertainty and open questions directly.
