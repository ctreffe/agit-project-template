# Retrospective Prompt

Use this prompt when the maintainer requests a deliberate review of
Maintainer-Agent collaboration over a selected milestone, project phase or
other defined period.

A retrospective evaluates collaboration. It does not harmonize project content
or revise the roadmap directly.

When the assistant can access the repository, invoke it with
`Read and execute RETROSPECTIVE_PROMPT.md.`

## Prompt

```text
Perform a structured retrospective of Maintainer-Agent collaboration in this
AGIT project.

The retrospective evaluates how we worked, not whether the project content is
correct or what the roadmap should contain. Project-content implications must
be handed to a later harmonization.

Establish the retrospective scope and evidence:

1. Read CODEX.md and ChatGPT.md for current authority, collaboration and Git
   rules.
2. Read PROJECT_CONTEXT.md, the relevant roadmap or milestone record, current
   CHANGELOG.md sections and Decision Records that govern collaboration.
3. Read CONTINUATION_PROMPT.md and HARMONIZATION_PROMPT.md to preserve the
   boundary between re-entry, content alignment and collaboration review.
4. Inspect relevant commit history, checkpoint handoffs, review files and
   documented decisions with read-only commands and subject to documented
   access boundaries. Preserve uncommitted work.
5. Use current-session evidence and maintainer observations where available.
   Do not claim access to earlier private chats that are not present.

Label the evidence source for material findings: repository evidence,
current-session observation, maintainer report or inference. Do not turn commit
counts, message counts or isolated mistakes into conclusions without context.
The retrospective normally needs process evidence, not raw project inputs. Do
not open sensitive materials merely to evaluate collaboration.

Evaluate collaboration across:

- clarity of maintainer intent, questions and decision ownership
- usefulness of numbered decisions and checkpoint handoffs
- division of responsibility between maintainer and agent
- repository-first continuity across sessions and prompts
- work-step, validation, review and commit rhythm
- quality of summaries, descriptions, limitations and completion claims
- handling of sensitive, private, licensed or unpublished materials
- tool, capability and authority boundaries
- rules that worked well and should remain unchanged
- recurring friction, ambiguity, repetition, delay or avoidable rework

Separate outcomes into:

- retain: collaboration practices that demonstrably work
- adjust in project: project-specific collaboration-rule improvements
- hand to harmonization: content, roadmap or repository-state implications
- template candidate: transferable collaboration learning that may help future
  projects using the recorded source template
- no action: observations that do not justify a change

Template candidates must be abstracted from project-specific detail, stripped
of sensitive information, supported by more than a single unexplained incident
and checked against overfitting. A candidate is not an instruction to change a
template.

Do not create, modify or delete files in the source-template repository unless
I instruct you to perform that specific template change and use a recognized
control word: `explicit` or `explicitly` in English, or the German word family
`explizit`. Permission to run this retrospective, edit the concrete project or
apply project findings does not authorize template changes.

If the current repository is itself a template, treat every proposed change to
its collaboration model or reusable template guidance as a template change and
apply the same control-word requirement.

Template-edit permission does not authorize Git index or protected Git actions.
Staging and unstaging require a specific maintainer instruction but no control
word. Committing, amending, tagging, pushing, pulling, merging, rebasing,
resetting, switching branches and manipulating stashes require a maintainer
instruction for that specific action containing a recognized control word.

Before any retrospective-driven edits, provide a concise numbered report:

1. retrospective scope, period or milestone and available evidence
2. collaboration practices to retain, with evidence
3. friction points and likely causes, with confidence and evidence source
4. proposed collaboration changes in the concrete project
5. project-content or roadmap implications for a later harmonization
6. abstracted source-template candidates, including transfer rationale and
   overfitting risk
7. no-action observations
8. maintainer decisions required

If my instruction also clearly authorizes project-level collaboration edits,
apply only agreed project changes after the report. Do not implement content or
roadmap changes; hand them to harmonization. Do not implement template
candidates without the separate template-change control-word permission.

After approved project edits, update all affected collaboration documents
consistently and validate links and internal references. Record durable
collaboration decisions in the appropriate project Decision Record when useful.
Update the last collaboration retrospective in PROJECT_CONTEXT.md only when the
reviewed scope and outcome are accurately recorded.
Do not claim the retrospective is complete while material maintainer decisions
remain unresolved.
```
