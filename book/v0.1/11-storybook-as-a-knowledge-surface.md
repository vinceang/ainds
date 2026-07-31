# Chapter 11 — Storybook as a Knowledge Surface

Storybook is usually where teams demonstrate components. A story renders a state. Controls expose props. Docs show APIs and code examples.

AINDS asks Storybook to do more.

> **Storybook is where humans and AI learn how the system should be used.**

That means a component page should expose not only examples, but the knowledge contract around them:

- Purpose
- Appropriate and inappropriate use
- UX rationale
- Accessibility behavior
- Content guidance
- Token dependencies
- Governance status
- Knowledge sources
- Prompt contracts
- Tests and evidence

Storybook is well positioned for this role because it sits where design intent, implementation, documentation, and evaluation meet. A designer can inspect states. An engineer can inspect APIs. A product manager can understand workflow guidance. An AI tool can retrieve structured metadata and linked knowledge.

Storybook should be a knowledge surface, not the only source of knowledge. Canonical principles, patterns, ADRs, and token definitions should remain in governed repository artifacts. Storybook renders and connects them in context.

A Button page, for example, can show variants and states while linking to action hierarchy, form validation, accessible naming, content rules, tokens, and the rule for proposing a new variant. A workflow story can demonstrate how Button, Field, Alert, and focus management implement the form pattern together.

AINDS should begin with standard extension points:

1. MDX pages
2. Reusable documentation blocks
3. Structured component metadata
4. A dedicated addon only when repeated needs justify it

A fork is unnecessary unless public APIs fundamentally block the knowledge model.

The goal is practical adoption. Teams should be able to layer AINDS knowledge onto an existing Storybook rather than replace their tools.

## Key takeaways

- Storybook can teach intent, not merely display artifacts.
- Canonical knowledge should be linked rather than duplicated.
- Pattern and workflow stories are as important as isolated component states.
- Start with MDX and reusable blocks; add specialized tooling after proving the need.
