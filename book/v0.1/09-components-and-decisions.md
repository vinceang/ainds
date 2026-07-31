# Chapter 9 — Components Capture UI; Knowledge Captures Decisions

A button component can encode markup, styling, states, events, and accessibility behavior. It cannot, by itself, explain when a product should use a primary button, whether a destructive action requires confirmation, or why navigation should use a link.

That distinction matters.

> **Components capture UI. Knowledge captures decisions.**

A production component needs more than an API. Its knowledge contract should include:

- Purpose and user problem
- When to use it
- When not to use it
- Anatomy
- Variants and states
- Interaction behavior
- Accessibility contract
- Content guidance
- Token dependencies
- Localization behavior
- Governance and ownership
- Tests and quality evidence
- AI-specific guidance

Without this context, component reuse can still produce design-system misuse. A team may technically use the shared Button while giving every action primary emphasis. An agent may select a Dialog because it resembles a screenshot even though the workflow requires a page. Shared code does not guarantee shared judgment.

Component APIs should also express semantic intent. A variant named `danger` is more meaningful than `red`. An event named `dismiss` communicates more than a generic click handler. Clear states, slots, and constraints make components legible to designers, engineers, and agents.

The component lifecycle belongs in the system too. A component can be proposed, experimental, stable, deprecated, or removed. Consumers need migration guidance. Contributors need to know when a new variant is justified. Owners need evidence that the component solves a repeated need.

A practical admission test asks:

1. Is the need recurring?
2. Is it cross-product or intentionally domain-specific?
3. Can composition solve it?
4. Does it introduce a new semantic concept?
5. Are accessibility and content requirements understood?
6. Who will own it?

This keeps the library from becoming a museum of one-off solutions.

## Key takeaways

- Reusing code does not guarantee correct product decisions.
- Every component needs a knowledge contract, not only an API.
- Semantic names make components easier for humans and AI to apply.
- Lifecycle and contribution rules are part of component quality.
