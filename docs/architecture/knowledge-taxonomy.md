# AINDS Knowledge Taxonomy

## Purpose

The AINDS Knowledge Taxonomy defines the kinds of knowledge a design system must capture so humans and AI can make consistent decisions from a shared source of truth.

> **Knowledge Before Generation.**

AINDS does not treat knowledge as supporting documentation added after components are built. Knowledge is an input to decisions, and decisions are inputs to artifacts.

```text
Knowledge
    ↓
Decisions
    ↓
Artifacts
```

Artifacts include components, tokens, prompts, Storybook documentation, tests, applications, icons, illustrations, copy, and governance records.

## Why a Taxonomy Is Necessary

Without a taxonomy, useful information becomes scattered across files, meetings, Figma comments, Storybook pages, pull requests, and individual memory.

A taxonomy gives contributors a shared answer to three questions:

1. What kind of knowledge is this?
2. Where should it live?
3. Which humans and AI specialists should consume it?

The taxonomy is not intended to produce a large documentation burden. A small team may begin with only a few short documents. The structure exists so knowledge can grow without becoming disorganized.

## Top-Level Knowledge Domains

### 1. Foundations

Defines the intent and boundaries of the system.

Includes:

- Mission and product vision
- Foundational principles
- User and business outcomes
- Design values
- Decision heuristics
- Scope and non-goals
- Definitions and shared vocabulary

Supports human decision-making by clarifying what the organization is trying to achieve.

Supports AI generation by providing the intent against which generated work should be evaluated.

### 2. Knowledge Sources

Records the trusted bodies of knowledge the organization has chosen to build upon.

Examples:

- Usability guidance such as *Don't Make Me Think*
- Accessibility standards such as WCAG and ARIA Authoring Practices
- An icon family such as Lucide
- A visual-design approach such as Refactoring UI
- A content style guide
- Framework and engineering guidance

AINDS does not ask every organization to invent best practices. It helps teams adopt trusted knowledge, document what they have adopted, and evolve it into their own organizational practice.

Knowledge-source records should distinguish:

- Source
- Adopted principles
- Local interpretation
- Known exceptions
- Licensing or attribution constraints

### 3. Users and Context

Captures who the system serves and under what conditions.

Includes:

- User groups and roles
- Needs, goals, and pain points
- Jobs to be done
- Journeys and workflows
- Devices and environments
- Assistive-technology considerations
- Domain constraints
- Research findings

This knowledge prevents components and flows from being generated in a vacuum.

### 4. Design Language

Defines how the organization expresses itself across products.

Includes:

- Visual language
- Interaction language
- Content language
- Icon language
- Illustration language
- Photography language
- Motion language
- Layout language
- Brand language

Design-language knowledge teaches humans and AI how a new artifact should belong to an existing family.

For example, an Icon Specialist should not merely generate a cowboy-hat icon. It should generate one that follows the selected family's grid, stroke, joins, simplification, optical balance, naming, and accessibility conventions.

### 5. Experience Principles and UX Patterns

Defines how recurring user problems should be solved.

Includes:

- Navigation
- Forms and validation
- Search
- Filtering and sorting
- Empty states
- Loading states
- Error recovery
- Success feedback
- Destructive actions
- Dialogs, drawers, and overlays
- Tables and data-dense interfaces
- Onboarding
- Permissions and access

A pattern should document:

- User problem
- Recommended behavior
- Rationale
- Accessibility implications
- Alternatives considered
- When to use it
- When not to use it
- Related components and tokens

This domain captures reusable decisions, not only reusable UI.

### 6. Accessibility

Defines accessibility as a system-wide responsibility rather than a final audit step.

Includes:

- Conformance targets
- Semantic HTML expectations
- Keyboard interaction
- Focus management
- Screen-reader behavior
- Color and contrast
- Touch targets
- Reduced motion
- Error identification
- International accessibility considerations
- Testing expectations

Accessibility knowledge should be linked to the components, patterns, tokens, and tests it governs.

### 7. Design Tokens

Defines the named decisions that express the design language across platforms.

Includes:

- Color
- Typography
- Spacing
- Sizing
- Borders
- Radius
- Elevation
- Motion
- Breakpoints
- Density
- Opacity
- Z-index

Token knowledge should include:

- Purpose
- Semantic meaning
- Allowed usage
- Theme behavior
- Accessibility constraints
- Source and transformation rules
- Deprecation guidance

Tokens should be described as decisions, not merely values.

### 8. Components

Defines reusable interface building blocks and the knowledge required to use and evolve them.

Each component should document:

- Purpose
- Anatomy
- Variants and states
- API
- Token dependencies
- Accessibility behavior
- UX rationale
- Content guidance
- Localization behavior
- Do and don't examples
- Governance rules
- AI-generation guidance
- Knowledge sources
- Tests
- Version and lifecycle status

Components capture UI. Their documentation must also capture the decisions around that UI.

### 9. Content and Language

Defines how the product communicates.

Includes:

- Voice and tone
- Terminology
- Text casing
- Labels and calls to action
- Validation messages
- Error messages
- Empty-state copy
- Confirmation language
- Reading level
- Inclusive language
- Content hierarchy

This knowledge allows AI to produce copy that sounds like the product rather than generic interface text.

### 10. Localization and Internationalization

Defines how the system works across languages, regions, and writing directions.

Includes:

- Translation strategy
- Locale formatting
- Date, time, number, and currency rules
- Text expansion
- Right-to-left behavior
- Pluralization
- Culturally sensitive content and imagery
- Component constraints
- Testing expectations

Localization must influence tokens, components, content, layouts, illustrations, and architecture.

### 11. Architecture and Engineering

Defines how design-system knowledge becomes reliable software.

Includes:

- Platform strategy
- Framework support
- Web Components and adapters
- Package structure
- State and event conventions
- Styling boundaries
- Rendering strategy
- Performance standards
- Security constraints
- Storybook architecture
- AI and MCP integrations
- Architecture Decision Records

This domain explains both the implementation and the reasons behind it.

### 12. Testing and Quality

Defines how the system proves that its decisions have been implemented correctly.

Includes:

- Unit testing
- Interaction testing
- Accessibility testing
- Visual regression
- End-to-end testing
- Cross-browser testing
- Localization testing
- Performance testing
- Content validation
- AI-output evaluation

Tests should be traceable to the knowledge and decisions they enforce.

### 13. Governance and Lifecycle

Defines how the system changes without losing coherence.

Includes:

- Contribution model
- Ownership
- Review requirements
- Decision authority
- Component admission criteria
- Variant creation rules
- Versioning
- Release process
- Deprecation
- Migration
- Exception handling
- Adoption measurement

Governance answers not only who may change the system, but what evidence is required before a change becomes canonical.

### 14. AI Specialists and Prompts

Defines how AI participates in the system.

Includes:

- Specialist purpose
- Required inputs
- Knowledge dependencies
- Allowed outputs
- Prompt templates
- Tool permissions
- Review gates
- Escalation rules
- Evaluation criteria
- Prohibited assumptions

Examples include:

- Knowledge Curator
- Design System Architect
- Component Engineer
- Accessibility Auditor
- Icon Specialist
- Content Specialist

AI specialists consume organizational knowledge. They should not silently invent organizational policy.

### 15. Evidence and Decisions

Preserves why the system has evolved.

Includes:

- Architecture Decision Records
- Design decisions
- Research evidence
- Usability findings
- Accessibility findings
- Analytics
- Experiments
- Rejected alternatives
- Exceptions and their expiration dates

This domain connects decisions to evidence and prevents old debates from being repeated without new information.

## Knowledge Classes

In addition to domains, every artifact should be understood as one of four classes.

### Source

External or internal knowledge selected as an input.

Example: WCAG 2.2 AA or Lucide's icon conventions.

### Principle

A durable belief or heuristic used to guide decisions.

Example: Primary actions should remain understandable and discoverable.

### Decision

A specific organizational choice made in context.

Example: Validate forms on progression attempt rather than disabling Continue.

### Artifact

A tangible implementation or expression of the decision.

Example: A Button component, Storybook story, validation helper, or test.

```text
Source
  ↓
Principle
  ↓
Decision
  ↓
Artifact
```

An artifact should be traceable upward. A contributor should be able to discover not only what exists, but why.

## Human and AI Consumption

Not all knowledge is consumed in the same way.

### Primarily human-facing

- Organizational purpose
- Governance authority
- Nuanced research findings
- Ethical trade-offs
- Unresolved questions
- Final approval criteria

### Primarily machine-actionable

- Token values and aliases
- Component APIs
- Interaction contracts
- Naming rules
- Test requirements
- Prompt input schemas

### Shared by humans and AI

Most AINDS knowledge belongs here:

- Principles
- Patterns
- Accessibility rules
- Content guidance
- Design-language rules
- Architecture decisions
- Governance constraints

AINDS should avoid creating separate, contradictory documentation for people and machines. The same knowledge should be structured so both can use it.

## Progressive Adoption

A startup does not need to complete every domain before building.

A minimum greenfield knowledge set may contain:

1. Product intent
2. Users and primary workflows
3. Selected knowledge sources
4. Accessibility target
5. Initial design-language seeds
6. Token baseline
7. First UX patterns
8. Component and governance conventions

A mature enterprise may begin by extracting tribal knowledge from existing products, interviews, design critiques, support data, code, and documentation.

Both paths converge on the same outcome: explicit, reviewable organizational knowledge.

## Promoting Session Notes into Permanent Knowledge

Session notes are capture artifacts, not automatically canonical knowledge.

A session discovery should be promoted when it:

- Defines or changes a principle
- Resolves a recurring decision
- Establishes a reusable pattern
- Changes architecture or governance
- Adds a trusted knowledge source
- Introduces a term required by the methodology
- Affects how humans or AI should generate work

Promotion process:

```text
Conversation
    ↓
Session Note
    ↓
Classification
    ↓
Draft Permanent Artifact
    ↓
Human Review
    ↓
Canonical Knowledge
```

A promoted artifact should identify its domain, class, status, owner, related knowledge, and evidence where appropriate.

## Suggested Metadata

Permanent knowledge documents should eventually support metadata such as:

```yaml
id: UX-FORM-VALIDATION
status: draft
knowledge_domain: experience-patterns
knowledge_class: decision
owners:
  - design-systems
consumers:
  - humans
  - component-engineer
  - accessibility-auditor
sources:
  - WCAG-2.2
related:
  - COMPONENT-BUTTON
  - COMPONENT-FIELD
last_reviewed: YYYY-MM-DD
```

The exact schema can evolve. The immediate goal is consistent classification and traceability.

## Litmus Test

Before a human or AI creates or changes an artifact, the system should help answer:

- What problem are we solving?
- Who is affected?
- What trusted knowledge applies?
- What principles govern the decision?
- Has the organization already made this decision?
- What accessibility requirements apply?
- What design language must be preserved?
- What evidence supports the choice?
- What requires human approval?

If these answers exist only in someone's memory, the system has identified knowledge that should be captured.

## Relationship to Knowledge Before Generation

The taxonomy operationalizes the principle of Knowledge Before Generation.

It ensures that generation begins with intent, evidence, standards, and shared decisions rather than isolated prompts or generic assumptions.

AINDS does not try to eliminate human judgment. It preserves and distributes that judgment so humans and AI can apply it consistently.
