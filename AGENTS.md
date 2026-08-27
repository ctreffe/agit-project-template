# AGENTS.md

Resident contract.

## Safety

- Inspect repository, branch, worktree and staging; preserve changes,
  selections and unrelated work.
- Maintainers own intent, scope and consequential decisions.
- Authorized reads and edits are allowed. Commits, tags, pushes, pulls, merges,
  rebases, resets, reverts, branches, stashes, destructive restores and direct
  `.git/` changes each require an instruction containing `explicit`,
  `explicitly` or German `explizit`.
- Ask before installation, privilege, external operations, outside writes or
  transmission; access, versioning and publication are separate.
- Retry once only if plausibly transient. On recurrence or setup/policy error,
  pause; use `troubleshoot-environment`; diagnose, obtain authority, repair,
  verify and resume.
- `input/intake/` grants no access; keep `input/` unchanged. Registered
  `materials/` and unrestricted `temp/` are readable; never version temporary
  content or inspect `temp/restricted/`. Synchronization grants no access.

## Routing

- Bounded work uses `start-task`, `TASK_HANDOFF.md`, targets and checks. Load
  `PROJECT_CONTEXT.md` only for project-wide state or
  unresolved scope.
- Read `COLLABORATION.md` for initialization, full review, authority
  conflicts or collaboration-model changes. Load `REPOSITORY.md`,
  `DOCUMENTATION.md`, `PHILOSOPHY.md`, `SYNCHRONIZED_STORAGE.md` and domain
  guidance only when applicable.
- Read `DECISIONS.md` and applicable records before durable changes.
- Task entry, handoff, ordinary commits and Decision Records route
  automatically. Invoke initialization, review, template sync,
  consistency checks, retrospectives, local creation and `commit-milestone`
  explicitly.
- Keep the template generic. Resolve material guidance conflicts before
  consequential work.

## Validation

Review diffs and run `git diff --check`. Add relevant tests, renders, links and
bilingual checks. Report outcomes, limits and skipped checks; do not call
unvalidated work complete.
