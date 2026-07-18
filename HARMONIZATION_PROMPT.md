# Harmonization Prompt

Use this prompt for a deliberate project-content harmonization. It compares a
derived project with its recorded source template, checks internal repository
consistency and reviews whether the roadmap still fits project intent and the
current state.

Harmonization concerns the project. It does not evaluate Maintainer-Agent
collaboration and does not derive improvements for the source template.

When the assistant can access the repository, invoke it with
`Read and execute HARMONIZATION_PROMPT.md.`

## Prompt

```text
Perform a structured content harmonization of this AGIT project.

Harmonization aligns the concrete project. The project, its maintainer-owned
intent, its Decision Records and its documented intentional deviations remain
authoritative. Never copy template changes blindly.

Begin with repository safety and state:

1. Read CODEX.md and ChatGPT.md for authority, sensitivity and Git rules.
2. Read PROJECT_CONTEXT.md, including repository role, source template,
   initial baseline, last harmonization and intentional deviations.
3. Read README.md, VERSION, the current CHANGELOG.md sections, the roadmap,
   relevant Decision Records, DOCUMENTATION.md, REPOSITORY.md and the active
   project files referenced by PROJECT_CONTEXT.md.
4. Inspect branch, working tree, recent commits, relevant tags and staged or
   unstaged changes with read-only Git commands. Preserve all uncommitted work.
5. Apply documented access, privacy, licensing and publication boundaries
   before opening inputs, references, feedback or generated artifacts.

If the repository role is a derived project, locate the exact recorded source
template and establish both the last compared baseline and the latest
verifiable template baseline. Do not assume that a local template clone is
current; use authoritative read-only remote evidence when it is available and
permitted. If freshness, template or baseline cannot be verified, stop the
external comparison at metadata level and ask for the missing path, version or
commit. Do not substitute another Templateverse repository and do not compare
against unrelated or proprietary templates.

Compare relevant source-template changes since the recorded baseline when that
history is available. For every material template change, classify the project
response as:

- adopt: use the template change without a project-specific alteration
- adapt: integrate the intent in a project-specific form
- reject: keep the current project behavior for a documented reason
- defer: postpone the decision because evidence, timing or authority is missing

Identify conflicts with project intent, existing rules, Decision Records,
privacy boundaries or intentional deviations. Present every conflict to me as
a numbered maintainer decision before editing. Never modify the source-template
repository during project harmonization.

If the repository role is template, do not infer a parent template. Skip the
external comparison and perform the internal and roadmap passes only.

Then check internal content consistency. At minimum, reconcile:

- project identity, scope, status, version and changelog
- PROJECT_CONTEXT.md, roadmap, completed milestones and next-session guidance
- Decision Records, documented deviations and current project rules
- README, documentation, source files, generated outputs and validation state
- sensitivity, assistant-access, Git-versioning and publication boundaries
- commit-ready state versus actual working-tree evidence

Review the roadmap as project content. Check whether its milestones, ordering,
validation expectations and non-goals still fit maintainer intent, the current
state, known decisions and remaining work. Propose additions, removals,
reordering or clarification when needed. Do not invent a new project direction
or resolve maintainer-owned choices without asking.

Harmonization is not a retrospective. Do not evaluate collaboration quality,
derive lessons for the source template or modify collaboration rules merely
because a different workflow might be preferable. Record an observed
collaboration issue only as a candidate for a future retrospective. Likewise,
do not implement template feedback.

Before substantive harmonization edits, provide a concise numbered report:

1. repository role, project baseline and source-template baseline
2. template comparison matrix with change, adopt/adapt/reject/defer status,
   rationale, affected project files and maintainer decision needed
3. internal consistency findings ordered by impact
4. roadmap coherence findings and proposed project-content changes
5. validation, sensitivity and disclosure checks required
6. proposed edit sequence with reviewable boundaries
7. collaboration observations to defer to a retrospective, if any
8. blocking maintainer decisions

If my instruction also clearly authorizes applying the harmonization findings,
apply only unambiguous agreed changes after the report. Stop before any
maintainer-owned conflict. Otherwise wait for my decisions.

After approved edits, validate affected files and outputs. Update the last
template harmonization baseline and intentional deviations in
PROJECT_CONTEXT.md only when the corresponding comparison and integration were
actually completed. Do not claim harmonization is complete while material
conflicts, validation failures or deferred baseline questions remain.

Staging and unstaging do not require a control word, but perform them only when
I specifically request the index action or authorize the corresponding commit.
Preserve existing staged selections and unrelated changes.

Do not commit, amend, tag, push, pull, merge, reset, rebase, switch branches,
manipulate stashes or perform another protected Git action unless I instruct
you to perform that specific Git
action and use a recognized control word: `explicit` or `explicitly` in
English, or the German word family `explizit`.
```
