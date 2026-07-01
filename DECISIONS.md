# DECISIONS.md

# Project Decision Records

Project Decision Records (PDRs) document important decisions that future collaborators should understand without relying on chat history.

PDRs are the generic AGIT equivalent of Architecture Decision Records. They are broader than software architecture and can apply to any project decision with durable consequences.

---

# When to Use a PDR

Use a PDR when a decision affects:

- project direction
- scope or non-goals
- collaboration structure
- documentation structure
- source or evidence handling
- privacy or data disclosure boundaries
- tool or repository choices
- review or approval process
- transition toward a development-oriented project

Do not create a PDR for every small choice. Use one when future collaborators would benefit from understanding why a decision was made.

---

# Recommended Location

When a project needs PDRs, create a `decisions/` folder.

Example:

```text
decisions/
  PDR-0001-project-direction.md
  PDR-0002-source-handling.md
```

The generic template explains the concept, but derived projects should create their own PDRs only when real decisions exist.

---

# Suggested Format

```text
# PDR-0001: Decision Title

## Status

Proposed | Accepted | Superseded

## Context

What situation, problem or uncertainty made the decision necessary?

## Decision

What was decided?

## Rationale

Why was this option chosen?

## Consequences

What follows from the decision?
```

---

# Relationship to Other Documents

- `PROJECT_CONTEXT.md` should summarize important decisions that affect current work.
- PDRs should preserve durable decision reasoning.
- `CHANGELOG.md` records completed changes, not decision rationale.
- `README.md` should link to relevant decisions only when users or contributors need them.
