# REPOSITORY.md

# Repository Standards

This document describes repository-level standards for projects created from the AGIT Project Template.

---

# Repository as Project Memory

The repository should contain enough context to continue the project without relying on private chat history.

Important project state, decisions, references and outputs should be captured in repository documents when practical.

---

# Suggested Structure

```text
README.md
ChatGPT.md
CODEX.md
PROJECT_CONTEXT.md
PROJECT_SETUP.md
INITIAL_PROMPT.md
DOCUMENTATION.md
REPOSITORY.md
PHILOSOPHY.md
CHANGELOG.md
VERSION
LICENSE
.gitignore
DECISIONS.md
input/
references/
notes/
output/
```

Projects may adapt this structure. When a folder gains project-specific meaning, add a short README that explains its role, expected contents and privacy or artifact handling rules.

---

# Working Folders

`input/` stores project input materials.

`references/` stores references, sources or source notes.

`notes/` stores working notes, open questions or draft thinking.

`output/` stores deliverables.

`DECISIONS.md` explains Decision Records.

Use `decisions/` when the project has real decision records to store.

Do not store private, confidential or unlicensed material in versioned folders unless that is an intentional project decision.

---

# Raw Inputs, Reviewed Derivatives and Generated Outputs

Projects should distinguish raw inputs, reviewed derivatives and generated outputs when that distinction matters.

Raw inputs are maintainer-provided or external materials in their original form. They may be private, confidential, licensed, unpublished or personal. Assistants should not inspect such raw materials by default. First document a source inventory and decide whether inspection is appropriate.

Reviewed derivatives are project-specific representations that have been checked for the intended use, such as anonymized tables, extracted observations, redacted excerpts, normalized CSV files, summaries or review workbooks. They are often safer and more useful to version than raw inputs.

Generated outputs are produced from sources, derivatives or scripts. The repository should make clear whether generated outputs are versioned review artifacts or regenerated locally.

`.gitignore` rules and source documentation should be updated together when private local inputs are required.

---

# Git Workflow

GitHub Desktop is a suitable Git client for the repository maintainer.

The repository maintainer controls Git history.

AI assistants may inspect Git status, diffs and logs when useful. They may
prepare changes, propose commit boundaries and suggest commit summaries and
descriptions.

AI assistants must not stage files, create commits, amend commits, rebase,
reset, revert, create or delete branches, create or delete tags, push, pull,
merge or otherwise change Git history unless the maintainer instructs the
assistant to perform that specific action and uses a recognized control word:
`explicit` or `explicitly` in English, or the German word family `explizit`,
including `explizite`, `expliziten`, `expliziter` and `explizites`.

Approval for file edits is not approval for Git history actions. Approval for
one history action is not approval for another. Requests such as "commit this",
"create the commit", "tag this" or "push this" do not authorize the assistant to
run Git history commands unless they contain a recognized control word.

Commits should be small enough to review and should represent one logical project step.

Regular working commits must use Conventional Commit prefixes such as:

```text
feat:
fix:
docs:
refactor:
test:
chore:
```

Milestone commits are the exception. A milestone commit should not use a Conventional Commit prefix. It should use a human-readable summary that includes the completed version number.

Each commit should include:

- a concise summary
- a meaningful description when useful

Commit descriptions should describe the actual change and should not claim future work as completed.

---

# Review and Harmonization Commits

Harmonization commits are appropriate when a project-wide rule, roadmap, decision or documentation model changes.

A harmonization commit should update affected documents together so the repository reads as one coherent state.

---

# Versioning

Templates should use Semantic Versioning.

Derived projects may use the versioning scheme that fits the work:

- Semantic Versioning
- date-based versions
- milestone names
- document revisions
- named project states

Whatever scheme is chosen should be documented and used consistently.

---

# Transition to AGIT Dev Template

If a project becomes development-oriented, consider adopting or migrating toward the AGIT Dev Template.

This is useful when the project becomes centered on:

- code
- scripts
- automation
- tests
- releases
- technical architecture
- implementation lifecycle

The transition should be documented with a PDR.
