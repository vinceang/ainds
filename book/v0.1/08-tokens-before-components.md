# Chapter 8 — Tokens Before Components

A color value such as `#2563eb` is not a design decision. It is a value.

A token such as `color.action.primary.background` begins to express a decision: this color represents the default background of a primary action. The semantic name explains why the value exists and where it belongs.

Tokens are often introduced as a synchronization mechanism between Figma and code. That is important, but incomplete. In AINDS, tokens are named organizational decisions that can be transformed across platforms.

A useful token architecture separates:

- **Reference tokens:** raw palette, type scale, spacing scale
- **Semantic tokens:** roles such as foreground, surface, border, action, feedback
- **Component tokens:** narrowly scoped decisions used when semantic tokens are insufficient

This layering allows a theme to change values without changing meaning.

The order matters. Teams that build components first often discover their tokens by extracting repeated values from finished UI. The result may describe what happened, but not necessarily what should happen.

Starting with token intent forces useful questions:

- Which concepts need stable names?
- Which values must respond to theme or mode?
- What contrast relationships must remain valid?
- Which tokens are public contracts?
- Which values are implementation details?

AI makes semantic naming even more valuable. An agent can reason about `color.feedback.danger.foreground` more reliably than `red.600`. The first communicates intent; the second requires guesswork.

Tokens should include documentation for purpose, allowed use, theme behavior, accessibility constraints, ownership, and deprecation. They should also move through a reliable pipeline so Figma variables, source token files, platform outputs, and Storybook remain aligned.

The ideal pipeline is not “Figma always wins” or “code always wins.” It is a governed source of truth with clear ownership and generated projections.

> **Tokens are not a prettier way to store values. They are a durable vocabulary for design decisions.**

## Key takeaways

- Semantic tokens communicate intent to humans and AI.
- Token architecture should precede uncontrolled component styling.
- Figma and code should consume governed projections of one canonical model.
- Token documentation must cover meaning, constraints, and lifecycle.
