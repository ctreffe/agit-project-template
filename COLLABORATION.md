# AGIT Project Collaboration Contract

## Purpose and Roles

This repository is durable shared memory for collaboration between the project
maintainer and AI assistants. The maintainer owns project intent, desired end
state, scope, priorities, domain responsibility and consequential decisions.
Agents may structure evidence, propose options, create authorized artifacts and
validate work without inventing project direction or approval.

The generic template supports mixed project types. Specialize it only when a
concrete project need justifies additional development, documentation, analysis
or writing rules.

## Authority and Decisions

Maintainer intent controls the roadmap and definition of success. Record durable
project choices through the local Decision Record workflow when they affect
direction, scope, structure, evidence handling, privacy, tools or review. Do not
turn unresolved options or routine implementation choices into accepted policy.

Assistant access, Git versioning, publication and external sharing are separate
decisions. A file's presence, synchronization or successful automated check does
not grant another form of approval.

## Repository and Evidence

Use current repository files and Git evidence rather than private chat history.
Separate verified facts, source-based summaries, maintainer context,
assumptions, open questions and AI interpretation. Never simulate completed
artifacts, validation or results.

`PROJECT_CONTEXT.md` contains current project-wide state, not a diary.
`TASK_HANDOFF.md` contains only the active bounded checkpoint. Decision Records
hold durable choices, `CHANGELOG.md` and Git hold history, and the roadmap links
maintainer intent to reviewable next steps.

## Sensitive Sources and Deliverables

Inventory plausibly private, confidential, licensed, unpublished or personal
sources at metadata level before content access. Prefer reviewed, redacted,
anonymized or normalized derivatives when they are sufficient. Sensitive raw
material stays outside Git by default, and generated outputs remain subject to
disclosure review. Automated privacy, secret or content checks are warnings,
not approval.

Deliverables may be documents, plans, records, reports, data products or
repository changes. Report one as complete only when it exists in the agreed
form and has received the applicable validation.

## Work and Evolution

Work in small coherent steps that reduce uncertainty or produce a reviewable
result. Keep affected context, documentation, decisions and validation aligned.
Use explicit skills for comprehensive review, template synchronization,
internal consistency, retrospective, initialization and milestone closure;
ordinary tasks use lean entry and a compact handoff.

A concrete project remains authoritative when synchronizing from its source
template. Retrospective findings are candidates, not permission to modify the
template. A transition toward a development-oriented template is a deliberate
project decision.

Retry a tool or environment failure once only when plausibly transient. On
recurrence or a setup, policy or permission failure, pause the task and use the
implicitly discoverable `troubleshoot-environment` workflow. Load portable and
host-local known issues only after activation, require a verified signature and
applicability match before reuse, and resume only after the original operation
succeeds. Troubleshooting grants no input, material, privilege, installation,
Git, external-operation or publication authority.

## Definition of Success

A successful project has clear intent, reproducible evidence, useful current
context, documented durable decisions, reviewable outputs, transparent
limitations, proportionate validation and a clear next step or completion
state—without depending on private conversation history.
