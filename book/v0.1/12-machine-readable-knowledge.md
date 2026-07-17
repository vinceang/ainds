# Chapter 12 — Machine-Readable Knowledge

Human-readable documentation is essential, but prose alone is difficult for tools to query reliably.

AINDS pairs narrative guidance with structured identity and relationships. A component article may explain rationale in Markdown while a small metadata file declares its status, owner, patterns, tokens, accessibility rules, prompt contracts, and related decisions.

```yaml
id: COMPONENT-BUTTON
status: stable
owner: design-systems
patterns:
  - UX-ACTION-HIERARCHY
  - UX-FORM-VALIDATION
tokens:
  - color.action.primary.background
accessibility:
  - A11Y-FOCUS-VISIBLE
human_review_when:
  - new_variant
  - destructive_action
```

The structured layer should not duplicate the full prose. It should make knowledge discoverable and composable.

Stable identifiers allow tools to build context bundles. An agent generating a form can retrieve the form pattern, Field and Button contracts, content guidance, accessibility requirements, and relevant tokens. A linter can detect a missing owner or stale review date. Storybook can display governance status. A future MCP server can expose the same knowledge to multiple tools.

Machine readability also creates traceability:

```text
Source → Principle → Decision → Pattern → Component → Story → Test
```

This chain helps a contributor answer not only “What should I use?” but “Why does this rule exist?”

The schema should begin small. Prematurely modeling every relationship creates maintenance burden. Useful first fields include identity, status, owner, consumers, sources, related artifacts, review date, and human-review triggers.

The test is practical: does the structure help humans or tools find, apply, validate, or maintain knowledge? If not, it is metadata for its own sake.

> **Write knowledge once, structure its relationships, and project it wherever people and agents need it.**

## Key takeaways

- Prose explains nuance; metadata supports retrieval and automation.
- Stable identifiers create traceability across the system.
- Structured knowledge should reference, not duplicate, canonical guidance.
- Start with a minimal schema and expand only through proven needs.
