# Chapter 5 — Knowledge-Driven Design Systems

Most design systems are asset-driven.

They include:

- Components
- Colors
- Typography
- Icons
- Figma libraries
- Storybook examples

Those assets are valuable, but they are incomplete.

They often document what exists without documenting why it exists, when it should be used, or how decisions should be made when a new situation appears.

A knowledge-driven design system captures not only reusable assets, but also the design, engineering, accessibility, and governance knowledge required to create, evolve, and apply those assets consistently.

## Knowledge, Decisions, Artifacts

AINDS can be understood as three layers:

```txt
Knowledge
    ↓
Decisions
    ↓
Artifacts
```

Knowledge includes:

- Design principles
- Token philosophy
- Accessibility standards
- UX patterns
- Component standards
- Icon guidelines
- Governance rules
- Architecture decisions

Decisions include:

- Use this pattern
- Use this token
- Use this component
- Avoid this interaction
- Escalate this edge case
- Create a new component only when this threshold is met

Artifacts include:

- Components
- Code
- Icons
- Storybook stories
- Documentation
- Product screens
- Tests

Most AI workflows jump directly to artifacts.

AINDS insists on knowledge first.

## The Culinary School Analogy

A traditional design system can feel like a cookbook.

It gives you recipes.

A knowledge-driven design system is closer to culinary school.

It teaches principles, judgment, technique, and reasoning.

The cookbook tells you what to do.

The culinary school teaches you why.

AINDS aims to be the culinary school.

## Principles

- Assets are not enough.
- Decisions must be captured.
- Knowledge should be explicit, searchable, reviewable, and reusable.
- AI should apply knowledge, not invent it.

## Implementation Guidance

For every recurring artifact, ask:

- What does someone need to know before creating this?
- What decisions have already been made?
- What trade-offs were considered?
- What rules should AI follow?
- What should trigger human review?

## Knowledge Before Generation

A knowledge-driven system ensures that generation is grounded in documented organizational intent instead of model assumption.
