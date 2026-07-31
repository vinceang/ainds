# Chapter 7 — Patterns Preserve Decisions

Components are nouns. Patterns are sentences.

A Field, Button, Alert, and Dialog can each be well designed, yet a team can combine them into an incoherent experience. Components define reusable parts. Patterns define how parts work together to solve recurring user problems.

Consider form validation. A component library can document field states and error text. It may still leave unanswered questions:

- When should validation occur?
- Should progression actions remain available?
- Where should focus move after a failed submission?
- Is there an error summary?
- When should errors clear?
- How are server and client errors distinguished?

These are pattern decisions.

A useful pattern article should capture:

1. The user problem
2. Recommended behavior
3. Rationale
4. Accessibility requirements
5. Content guidance
6. Components and tokens involved
7. Alternatives considered
8. When the pattern does not apply
9. Tests and evidence

Patterns prevent a common design-system failure: locally correct components producing globally inconsistent workflows.

They are also essential AI context. An agent asked to build a registration flow should not choose validation, progress, error recovery, and action hierarchy independently. It should retrieve the organization’s established patterns and compose from them.

Patterns need not eliminate exceptions. Insurance underwriting, for example, may require a different disclosure or progression model than a low-risk profile form. The exception should be explicit, scoped, and tied to its rationale.

A mature system therefore distinguishes between:

- Stable cross-product patterns
- Domain-specific patterns
- Experimental patterns
- Approved exceptions

This makes the system useful without pretending one answer fits every context.

> **Reusable components reduce duplicated code. Reusable patterns reduce duplicated decisions.**

## Key takeaways

- Components alone cannot coordinate complete experiences.
- Patterns preserve recurring behavioral decisions.
- Pattern guidance should include rationale, accessibility, and boundaries.
- AI should compose workflows from approved patterns rather than invent them per prompt.
