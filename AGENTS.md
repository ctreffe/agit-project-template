# AGENTS.md

This is the resident contract. Load routed context only when needed.

## Safety

- Inspect repository, branch, working tree and staged state. Preserve existing
  changes, selections and unrelated work.
- Maintainers own intent, scope and consequential decisions.
- Read-only checks and authorized in-scope edits are allowed. Commits,
  tags, pushes, pulls, merges, rebases, resets, reverts, branch or stash
  actions, destructive restores and direct `.git/` changes require a specific
  instruction using `explicit`, `explicitly` or the German word family
  `explizit`. Authorize every action separately.
- Ask before installation, privilege, external-system operations, outside
  writes or data transmission. Access, versioning and publication are separate.
- `input/intake/` never grants access; keep `input/` unchanged. Registered
  `materials/` and unrestricted `temp/` are readable; temporary content is
  never versionable. Never inspect `temp/restricted/`. Synchronization grants
  no access.

## Routing

- For bounded work use `start-task`, `TASK_HANDOFF.md`, requested targets and
  applicable checks. Load `PROJECT_CONTEXT.md` only for project-wide state or
  unresolved scope.
- Read `COLLABORATION.md` for initialization, full review, authority
  conflicts or collaboration-model changes. Load `REPOSITORY.md`,
  `DOCUMENTATION.md`, `PHILOSOPHY.md`, `SYNCHRONIZED_STORAGE.md` and domain
  guidance only when applicable.
- Read `DECISIONS.md` and applicable records before durable changes.
- Task entry, handoff, ordinary commits and Decision Records route
  automatically. Invoke initialization, comprehensive review, template sync,
  consistency checks, retrospectives, local creation and `commit-milestone`
  explicitly.
- Keep the template generic. Resolve material guidance conflicts before
  consequential work.

## Validation

Review diffs and run `git diff --check`. Add relevant tests, renders, link and
bilingual checks. Report outcomes, limitations and skipped checks; do not call
unvalidated work complete.
