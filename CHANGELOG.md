# Changelog

All notable changes to this project will be documented in this file.

This project follows Semantic Versioning.

## [Unreleased]

### Added

- Add `AGENTS.md` as the concise, automatically loaded entry point that routes
  AI agents to the complete repository rules and validation guidance.

### Changed

- Align the initialization and continuation prompts with `AGENTS.md`: setup is
  an explicit one-time workflow, while continuation only reconstructs state.
- Expand continuous-improvement guidance with the candidate-to-governance
  lifecycle and transparent, unlinked private Templateverse coordination.

## [0.3.0] - 2026-07-20

### Changed

- Clarify `INITIAL_PROMPT.md` as the sole maintainer entry point for agent-led
  initialization, separate language navigation from the collaboration note,
  move README authority guidance into documentation rules and link maintainer
  tools to their official sources.
- Standardize template README badges as status, version and license links and
  document how derived projects adapt badges without inheriting template state
  or advertising nonexistent automation.
- Upgrade the AGIT Generic Collaboration Model to v0.3.0 and classify staging
  and unstaging as specifically requested index operations outside the
  control-word rule while preserving staged and unrelated changes.

## [0.2.0] - 2026-07-19

### Added

- Add `RETROSPECTIVE_PROMPT.md` for evidence-based Maintainer-Agent
  collaboration review and controlled template-learning candidates.
- Add `HARMONIZATION_PROMPT.md` for source-template comparison, internal
  consistency review and roadmap alignment.
- Add `CONTINUATION_PROMPT.md` for reproducible project re-entry in a new
  context window or assistant session.
- Add `INITIAL_PROMPT.md` as a reproducible first-session prompt for derived project initialization.
- Add an AGIT Templateverse section to the English and German READMEs.
- Add `decisions/` as the shared Decision Record location with default PDR guidance and support for ADR, DDR and WDR prefixes when needed.

### Changed

- Retain initialization artifacts as project provenance, record template
  lineage and harmonization baselines in `PROJECT_CONTEXT.md`, and clarify that
  documentation and repository guidance remain active project rules.
- Separate assistant access, Git versioning and publication approval for
  sensitive sources, derivatives and generated outputs.
- Define automated sensitivity checks as warnings rather than safety approval.
- Add a standard checkpoint handoff for reviewable working steps.
- Limit the generic Decision Record vocabulary to PDR, ADR and DDR and remove
  domain-specific record guidance from the generic template.
- Formalize small working commits below roadmap milestones and reserve separate
  milestone commits for reviewed milestone closure.
- Require commit recommendations to contain consistent summaries and meaningful
  descriptions.
- Strengthen safeguards against adding sensitive raw sources to Git.
- Define completion criteria for structured project initialization.
- Prefer concise numbered maintainer decisions and next steps.
- Upgrade the AGIT Generic Collaboration Model to v0.2.0.
- Carry the working-commit rhythm and numbered collaboration convention into
  the derived-project context template.
- Require recognized Git history control words before an assistant may perform Git history actions.
- Clarify the AI Collaboration Note with an explicit AI-assisted collaboration sentence.
- Add setup guidance requiring derived projects to preserve and adapt a visible AI Collaboration Note linked to `ChatGPT.md`.
- Introduce the AGIT Generic Collaboration Model as v0.1.0.
- Add source-sensitivity, reviewed-derivative and generated-output guidance based on access-plan project retrospection.
- Add folder README, review artifact and post-milestone context-refresh guidance.
- Expand PDR candidate guidance for privacy, derivative versioning, output versioning and related-repository scope decisions.
- Clarify that template-only setup files may be removed or retained after initialization depending on project needs.
- Clarify that retained initialization files should keep their original names and may document setup status internally or in `PROJECT_CONTEXT.md`.
- Clarify that regular working commits must use Conventional Commit prefixes while milestone commits should omit prefixes and include the completed version number.

## [0.1.1] - 2026-07-02

### Added

- Add German README documentation.
- Add the AI Collaboration Note to the README files.
- Add explicit maintainer control over Git history actions to the collaboration
  and repository guidance.
- Add `CODEX.md` as the local Codex operating policy for generic AGIT projects.

## [0.1.0] - 2026-07-02

### Added

- Initialize the generic AGIT Project Template.
- Add collaboration, project context, setup, documentation, repository and philosophy guidance.
- Add `DECISIONS.md` as the generic Project Decision Record guidance.
- Add working folders for inputs, references, notes and outputs.
- Add changelog, version metadata and ignore rules.
