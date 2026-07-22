# CODEX.md

# Codex Operating Policy

This document defines how Codex may operate locally when assisting with AGIT
repositories.

`ChatGPT.md` defines the general AGIT Collaboration Model. `CODEX.md` defines
local execution rules for Codex on the maintainer's machine.

The purpose of this file is to make local AI-assisted work transparent,
controlled and reproducible.

---

# Scope

This policy applies to local Codex sessions working on AGIT repositories.

It covers:

- local tool usage
- repository access
- Git usage
- local working directories
- package installation
- network access
- data disclosure
- delivery expectations

It does not replace the Collaboration Model in `ChatGPT.md`.

---

# Local-First Principle

Codex should prefer local analysis and local tooling.

Network access, external services and package downloads should be minimized and
used only for a clear purpose.

Project data should remain local by default.

---

# Repository Control

The repository maintainer controls Git state through GitHub Desktop unless a
project explicitly defines a different workflow.

Codex may prepare working tree changes, explain diffs, run checks and propose
commit metadata. Suggested metadata should follow the repository commit rules: Conventional Commit prefixes for regular working commits, and no prefix for milestone commits that include the completed version number.

Staging and unstaging are index operations and do not require a control word.
Codex may perform them only when the maintainer specifically requests the index
action or authorizes the corresponding commit. Codex must preserve existing
staged selections and unrelated changes.

Codex has no default permission to perform protected Git actions. File-edit,
tool or staging approval does not authorize committing, tagging, pushing or
another protected Git action. Each such action requires a maintainer instruction
for that specific action that
uses a recognized control word: `explicit` or `explicitly` in English, or the
German word family `explizit`, including `explizite`, `expliziten`, `expliziter`
and `explizites`.

---

# Allowed by Default

Codex may use local tools for analysis and project work when they operate inside
the active repository or read local context.

Allowed by default:

- read repository files
- create or edit files in the active repository when asked to implement a change
- use PowerShell for local commands
- use Git for read-only inspection
- use Python and project-local virtual environments when useful
- use Node.js tooling when already present or project-local
- use `rg` or equivalent local search tools
- run project-local checks, linters, renderers or validation scripts when present
- create local archives or generated files when explicitly relevant to the requested work
- use local PDF, document, spreadsheet or image tooling for local files supplied by the maintainer

Codex should report important command results that affect the conclusion of the
work.

---

# Git Inspection and Index Usage

Codex may use Git for read-only inspection by default. It may also perform a
specifically requested staging or unstaging action under the index rules above.
Protected Git actions require a recognized control word.

Allowed read-only Git commands include:

```text
git status
git diff
git diff --stat
git log
git show
git blame
git ls-files
git branch --show-current
git remote -v
git tag --list
git describe --tags
git rev-parse
```

Index commands allowed only under the specifically requested index rule are:

```text
git add -- <paths>
git restore --staged -- <paths>
```

Codex must not modify repository history, branches, tags or working tree
contents through Git without the required protected-action authorization.

Protected Git actions requiring a control word include:

```text
git commit
git push
git pull
git merge
git rebase
git reset
git revert
git checkout
git switch
git branch
git tag
git cherry-pick
git stash
git restore
git clean
```

Codex must not edit `.git/` directly.

If a Git command can change repository state, Codex should treat it as forbidden
even if the command is convenient.

This rule remains in force even when Codex is otherwise allowed to edit project
files. Changing repository history is a separate maintainer-controlled action.

---

# Allowed with Maintainer Approval

Codex should ask before performing actions that install software, use the
network, require elevated privileges or affect state outside the active
repository.

Approval is required for:

- package installation such as `pip install`, `npm install`, `pnpm install`, `winget` or external downloads
- global tool installation
- admin or UAC-level operations
- writing outside the active repository
- browser automation against external websites
- API calls that send project data to external services
- system-level Windows tools such as Registry changes, Scheduled Tasks, services, firewall rules, `bcdedit` or boot configuration changes
- destructive filesystem actions

When approval is requested, Codex should explain why the action is needed and
what data or system state may be affected.

---

# Internet and Data Disclosure

Codex should be cautious about sending data to the internet.

Default rules:

- Do not upload repository contents to external services without explicit maintainer approval.
- Do not send secrets, tokens, credentials, `.env` files, private keys or private project data to external services.
- Prefer official sources when external research is needed.
- Use web search only when current information is needed, when the maintainer requests it or when local context is insufficient.
- Treat package installation as network activity that may disclose package names, versions and environment metadata to package sources.
- Keep generated ZIP files, reports and other outputs local unless the maintainer explicitly requests external sharing.

Assistant access, Git versioning and publication or external sharing require
separate maintainer decisions. Approval for one does not authorize another.
Automated privacy, secret or content checks are warning systems and do not by
themselves establish that a file is safe.

If data disclosure is possible, Codex should state that before using the
external tool.

---

# Forbidden by Default

Codex must not perform the following actions unless the maintainer instructs
Codex to perform the specific action with a recognized control word:

- protected Git actions without the required control-word instruction
- staging or unstaging without a specific request or corresponding commit
  authorization
- destructive filesystem actions outside a clearly requested change
- hidden system changes
- global package or tool installation
- credential, token or security configuration changes
- upload of private repository data
- modification of unrelated repositories in a multi-repository workspace
- simulated completion of files or results that do not actually exist

Integrity has priority over appearing helpful.

---

# Local Tool Environments

Project-local tool environments are allowed when they are useful for validation
or project work.

Examples:

```text
.venv/
node_modules/
.codex-input/
.codex-cache/
.codex-tmp/
.codex-output/
generated/
deliverables/
```

These directories contain local working files and should normally be ignored by
Git.

Codex may create a project-local Python virtual environment when Python work is
required and the environment is ignored by Git.

Codex should prefer project-local environments over global tool changes.

---

# Multi-Repository Safety

When multiple repositories are present, Codex must identify the active
repository before making changes.

Reference repositories may be read for context when the maintainer requests it,
but Codex must not modify them unless explicitly asked.

Before editing files, Codex should make clear which repository will be changed.

---

# Delivery Format

When preparing a repository change, Codex should provide:

- a short change summary
- checks or validation performed
- known limitations or skipped checks
- a suggested commit summary
- a suggested commit description
- concise numbered maintainer decisions or next steps when practical

Suggested commit metadata must distinguish regular working commits from
milestone commits. Regular commits use an appropriate Conventional Commit
prefix and represent one logical step. Milestone commits use a human-readable
summary with the completed version number and should close already recorded,
reviewed work rather than bundle an entire milestone into one change.

The maintainer performs staging, commits, tags and pushes in GitHub Desktop
unless a project explicitly defines a different process.

Suggested commit metadata is advisory. It is not permission for Codex to create
the commit.

---

# Capability Transparency

Codex should state tool limitations directly.

Examples:

- Git is not available in `PATH`.
- A dependency is missing.
- A command could not run because of sandboxing.
- A check was not performed.
- A result is inferred from file analysis rather than validated execution.

Codex should not hide limitations behind confident wording.

---

# Relationship to Other Template Documents

Use the template documents as follows:

- `ChatGPT.md` defines the general collaboration model.
- `CODEX.md` defines local Codex operating rules.
- `PROJECT_SETUP.md` explains how to prepare a project created from the template.
- `PROJECT_CONTEXT.md` describes the current state of a derived project after setup.
- `REPOSITORY.md` defines repository-level conventions.
- `DOCUMENTATION.md` defines documentation standards.

These documents should remain aligned when the collaboration process changes.
