# Chapter 16 — The Prompt-to-Production Pipeline

The promise of AI-assisted product development is not that a prompt instantly becomes production software. The promise is that a well-governed pipeline can reduce the distance between intent and a reviewed, tested implementation.

A practical AINDS pipeline may look like this:

```text
Intent or Figma frame
        ↓
Knowledge retrieval
        ↓
Pattern and primitive selection
        ↓
AI-assisted generation
        ↓
Storybook composition
        ↓
Automated checks
        ↓
Human review gates
        ↓
Application integration
        ↓
Production evidence
```

Each stage has a purpose.

Knowledge retrieval gathers the applicable principles, patterns, components, tokens, content rules, accessibility contracts, and domain decisions. Selection determines whether the requested experience can be composed from existing primitives. Generation creates code, stories, tests, or documentation within those constraints.

Storybook provides a controlled place to inspect states and workflows before application integration. Automated checks evaluate type safety, tests, accessibility, token usage, visual regression, and documented requirements. Human reviewers resolve novelty, policy, language, visual quality, and tradeoffs.

The pipeline should preserve traceability. A generated component or screen should be able to declare which knowledge it consulted and which checks it passed.

A PM’s prompt should not bypass design and engineering. It should enter the same system of knowledge and evaluation. A designer’s Figma frame should not become unreviewed code. It should be interpreted against existing patterns and implementation contracts.

The goal is not zero friction. It is useful friction placed where it protects quality.

Teams should begin with a narrow workflow, such as generating a Storybook composition from an approved Figma frame using existing components. Prove retrieval, generation, validation, and review before attempting autonomous feature delivery.

> **Prompt-to-production is a pipeline of accountable transformations, not a single act of generation.**

## Key takeaways

- Production quality comes from the pipeline, not the prompt alone.
- Storybook is a useful checkpoint between generation and application integration.
- Traceability should connect outputs to knowledge and evaluation.
- Start with narrow, repeatable workflows and expand after proving reliability.
