# AGENTS.md

This file is the automatically loaded entry point for AI agents working in an
AGIT Project Template repository. Keep it concise: it routes agents to the
repository's authoritative guidance and does not replace that guidance.

## Before Substantive Work

1. Read `CODEX.md` in full before using tools or changing files. It defines the
   local operating policy, access boundaries and protected Git actions.
2. Read `ChatGPT.md` for the Maintainer-Agent collaboration model.
3. Read `README.md`, `PROJECT_CONTEXT.md`, `REPOSITORY.md`, `DOCUMENTATION.md`
   and `PHILOSOPHY.md` as relevant to the task.
4. Read `DECISIONS.md` and applicable records before changing established
   project direction or durable structure.
5. For initialization, continuation, harmonization or retrospective work,
   follow the corresponding prompt file instead of reconstructing its workflow.

If repository guidance appears inconsistent, report the conflict and ask for a
maintainer decision when it could materially affect the result.

## Working Agreement

- Confirm the active repository and inspect its current Git state before edits.
- Preserve existing staged selections, working-tree changes and unrelated work.
- Treat maintainer intent, scope, priorities and consequential decisions as
  human-owned.
- Keep this generic template suitable for mixed project types. Do not impose
  software, documentation, analysis or writing specialization without a
  concrete project need.
- Work in small, reviewable changes and keep affected context, documentation,
  decisions and changelog entries coherent.
- Treat assistant access, Git versioning and publication or external sharing as
  separate maintainer decisions.
- Classify new external files through `input/`; presence in `input/intake/`
  never authorizes assistant access.
- Follow the authorization rules in `CODEX.md`; an edit request does not by
  itself authorize protected Git actions.

## Validation and Handoff

Run checks proportionate to the task. At minimum, review the diff and run
`git diff --check` for repository changes. Validate local Markdown links and
English/German structural alignment when documentation is affected, plus any
project-specific tests, renders or scripts relevant to the change.

Report the outcome, changed files, checks performed, limitations or skipped
checks and suitable commit metadata. Do not present unvalidated work as
complete.
