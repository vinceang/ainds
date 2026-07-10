# AINDS Storybook Knowledge Model

## Purpose

The AINDS Storybook Knowledge Model defines how Storybook becomes more than a component showcase.

Traditional Storybook documentation explains what a component is, how it renders, and how to call its API.

AINDS extends that model so Storybook also explains:

- Why the component exists
- When it should be used
- When it should not be used
- Which organizational decisions govern it
- Which knowledge sources informed it
- Which accessibility requirements apply
- Which tokens and patterns it depends on
- How humans and AI may extend it safely

> **Storybook is where humans and AI learn how the system should be used.**

## Storybook as a Knowledge Surface

A knowledge surface is any interface through which organizational knowledge becomes discoverable and actionable.

Storybook is especially valuable because it sits at the point where design intent, component behavior, code, testing, and documentation meet.

In an AINDS implementation, Storybook should serve four audiences at once:

### Product designers

They need to understand intended use, interaction patterns, variants, states, accessibility, and the boundaries of the component.

### Engineers

They need APIs, examples, event behavior, token dependencies, implementation constraints, and tests.

### Product and content practitioners

They need terminology, content rules, workflow guidance, localization behavior, and examples of appropriate use.

### AI specialists and coding assistants

They need explicit, structured knowledge that prevents them from treating a component as a generic visual primitive.

The same canonical knowledge should support all four audiences rather than creating separate and potentially contradictory documentation.

## Information Architecture

AINDS Storybook should organize information into five layers.

```text
System Knowledge
    ↓
Pattern Knowledge
    ↓
Component Knowledge
    ↓
Stories and Examples
    ↓
Implementation and Evaluation
```

### Layer 1: System Knowledge

System-level documentation applies across the entire design system.

Recommended pages:

- Start Here
- Foundational Principles
- Knowledge Before Generation
- Design Language
- Accessibility Baseline
- Token Philosophy
- Content and Language
- Localization and Internationalization
- Governance and Contribution
- AI Usage and Review Policy
- Knowledge Sources

These pages answer the broad questions that should not be repeated on every component page.

### Layer 2: Pattern Knowledge

Patterns explain how recurring user problems are solved across components.

Recommended pattern groups:

- Forms and validation
- Navigation
- Feedback and status
- Empty and loading states
- Errors and recovery
- Search, filtering, and sorting
- Destructive actions
- Dialogs, drawers, and overlays
- Tables and data-dense interfaces
- Onboarding and progressive disclosure

A component page should link to relevant pattern pages instead of restating the full pattern.

### Layer 3: Component Knowledge

Each component page contains the complete knowledge contract for using and extending that component.

### Layer 4: Stories and Examples

Stories show the component in meaningful states and realistic product contexts.

Examples should demonstrate decisions, not just visual permutations.

### Layer 5: Implementation and Evaluation

This layer includes source examples, API references, tests, accessibility checks, visual-regression coverage, and AI-generation guidance.

## Standard Component Documentation Model

Every production component should use a consistent documentation model.

Not every section must be equally long, but missing sections should be intentional.

### 1. Summary

A plain-language description of the component and the user problem it solves.

Example:

> A Button triggers an immediate action. It should communicate what will happen next and remain understandable across default, hover, focus, loading, disabled, and error-related states.

### 2. Purpose

Explain why the component exists in the system.

Questions to answer:

- What recurring problem does it solve?
- Why is it a shared component rather than local application UI?
- What inconsistency does it prevent?

### 3. When to Use

List appropriate contexts in product language.

### 4. When Not to Use

Identify common misuse and point to better alternatives.

This is particularly important for AI, which often selects components by visual resemblance rather than product intent.

### 5. Anatomy

Document the component's visible and semantic parts.

For a Button, anatomy may include:

- Container
- Label
- Leading icon
- Trailing icon
- Loading indicator
- Accessible name

### 6. Variants, States, and Behaviors

Document supported variants and meaningful states.

Examples:

- Primary, secondary, tertiary, and destructive intent
- Default, hover, active, focus-visible, disabled, and loading
- Icon-only and text-plus-icon forms
- Responsive and high-contrast behavior

Variants should not be treated as a visual catalog alone. Each variant must explain the decision it represents.

### 7. UX Rationale

Explain the reasoning behind the component's behavior.

For example:

- Why primary actions remain enabled during form completion
- Why loading preserves button width
- Why destructive styling is reserved for irreversible or high-risk actions
- Why icon-only buttons require accessible names and often visible tooltips

This section captures the judgment that would otherwise become tribal knowledge.

### 8. Accessibility Contract

Document the behavior that must remain true in every implementation.

Include:

- Required semantics
- Keyboard behavior
- Focus management
- Screen-reader expectations
- Contrast and non-color requirements
- Touch-target requirements
- Reduced-motion behavior
- High-contrast or forced-colors considerations
- Known limitations
- Required automated and manual tests

The accessibility contract should be testable.

### 9. Content Guidance

Define how words work inside or around the component.

Include:

- Label grammar
- Text casing
- Terminology
- Recommended length
- Voice and tone
- Localization considerations
- Error or confirmation language

Example:

> Use concise verb-led labels such as “Save changes.” Avoid vague labels such as “Continue” when a more specific outcome is available.

### 10. Token Contract

List the semantic tokens consumed by the component and why.

Avoid presenting only raw values.

Example:

```text
color.action.primary.background.default
color.action.primary.background.hover
color.action.primary.foreground
border.focus.visible
motion.feedback.short
```

Document:

- Semantic purpose
- Theme behavior
- Accessibility constraints
- Which tokens may be overridden
- Which values are implementation details and must not be consumed directly

### 11. Localization and Internationalization

Document:

- Text expansion behavior
- Right-to-left mirroring
- Locale-sensitive content
- Truncation rules
- Icon-direction considerations
- Minimum and maximum content assumptions

### 12. API and Code Examples

Provide framework-appropriate examples while keeping the knowledge model platform-neutral.

Examples may include:

- Native Web Component usage
- Angular adapter usage
- React adapter usage
- Event handling
- Loading state
- Icon usage
- Accessible naming

Code snippets should demonstrate recommended product behavior, not merely valid syntax.

### 13. Do and Don't

Use paired examples to make intent memorable.

Each example should include a short rationale.

Weak:

> Don't use too many primary buttons.

Better:

> Do use one clear primary action per decision area. Don't style every available action as primary, because equal emphasis forces the user to determine hierarchy without guidance.

### 14. Governance

Document how the component may change.

Include:

- Owner
- Lifecycle status
- Admission criteria for new variants
- Required evidence for behavior changes
- Reviewers
- Backward-compatibility expectations
- Deprecation policy
- Exception process

Example rule:

> A new Button variant requires a recurring product need that cannot be represented by an existing semantic intent. A one-product visual preference is not sufficient.

### 15. AI Guidance

Provide explicit instructions for AI assistants and specialists.

This is not a collection of generic prompts. It is a component-specific generation contract.

Include:

- Required knowledge to consult
- Allowed uses
- Prohibited assumptions
- Questions that require human input
- Expected output format
- Validation requirements

### 16. Knowledge Sources and Related Decisions

Link back to the canonical knowledge that governs the component.

Examples:

- UX pattern documents
- Accessibility standards
- Design-language rules
- ADRs
- Research findings
- Content guidance
- Token decisions
- Knowledge sources

### 17. Evaluation and Tests

Show how the system proves the component meets its contract.

Include:

- Interaction tests
- Accessibility tests
- Visual-regression coverage
- Keyboard test cases
- Localization examples
- Dark-mode and high-contrast examples
- AI-output evaluation where applicable

## Sample Component Knowledge Page: Button

The following condensed model illustrates how a Button page should read.

### Summary

A Button triggers an immediate action.

### Use it for

- Submitting a form
- Confirming a decision
- Starting a task
- Triggering a reversible or irreversible action with clear intent

### Do not use it for

- Navigation to another destination; use a link
- Toggling a persistent state; use an appropriate switch or toggle control
- Selecting one item from a set; use a selection control

### UX rationale

The visual hierarchy of buttons should reflect decision hierarchy. A screen may contain several actions, but usually only one should receive primary emphasis within a decision area.

For form validation, keep the submit or progression action available unless a known prerequisite makes the action impossible. Let the action reveal validation feedback rather than leaving users to infer why a disabled button cannot be used.

### Accessibility contract

- Use native button semantics when possible
- Preserve keyboard activation with Enter and Space
- Provide a visible focus indicator
- Do not use color alone to express destructive intent
- Icon-only buttons require an accessible name
- Loading must communicate progress without unexpectedly moving focus
- Disabled behavior must remain understandable to assistive-technology users

### Content guidance

Prefer specific verb-led labels:

- Save changes
- Add member
- Delete account

Avoid vague language when the result can be named:

- Submit
- Okay
- Continue

### Governance

Create a new variant only when an existing semantic intent cannot represent a repeated cross-product need.

### AI generation contract

Before generating a Button implementation:

1. Identify the user action and its consequence.
2. Confirm whether the control performs an action or navigation.
3. Consult the form-validation pattern when used in forms.
4. Select an existing semantic intent.
5. Use approved tokens only.
6. Include loading, focus, disabled, and error-adjacent behavior where relevant.
7. Validate keyboard and accessible-name behavior.
8. Escalate requests for a new variant to human review.

## Prompt Model

AINDS prompts in Storybook should be practical, scoped, and traceable to knowledge.

### Prompt anatomy

A prompt should contain:

```text
Intent
+ Relevant knowledge
+ Constraints
+ Required components
+ Required states
+ Evaluation criteria
+ Escalation conditions
```

### Example: Generate a form action area

```text
Create a responsive form action area using the AINDS Button component.

Intent:
Allow a user to save profile changes or cancel and return without saving.

Required knowledge:
- Forms and Validation pattern
- Button component guidance
- Content and Language guidance
- Accessibility baseline

Constraints:
- Use one primary action: “Save changes”
- Use a secondary or tertiary action for “Cancel”
- Do not disable Save solely because the current form is invalid
- On activation, expose validation errors and move focus according to the form pattern
- Include loading behavior that prevents duplicate submission
- Use semantic tokens only

Evaluation:
- Correct action hierarchy
- Keyboard operability
- Clear accessible names
- Understandable validation behavior
- Responsive layout

Escalate when:
- The workflow requires a new Button variant
- Product policy conflicts with the validation pattern
```

### Prompt presentation in Storybook

Prompts should appear as copyable, versioned examples near the knowledge they depend on.

Each prompt should display:

- Purpose
- Intended AI specialist or tool
- Required knowledge links
- Inputs to replace
- Expected output
- Evaluation checklist
- Version or last-reviewed date

Prompts should not be presented as magical one-line commands. They should demonstrate how organizational knowledge constrains generation.

## Governance Model per Component

Governance should be visible in Storybook rather than hidden in a contribution repository.

Each component should display a compact governance panel containing:

- Status: proposed, experimental, stable, deprecated
- Owner
- Last reviewed
- Supported platforms
- Related ADRs
- Approved variants
- Known exceptions
- Contribution path
- Deprecation or replacement guidance

### Change classification

#### Documentation-only change

Clarifies usage without changing behavior.

Typical review:

- Component owner
- Content or accessibility reviewer when relevant

#### Additive change

Adds a supported state, capability, or adapter without breaking existing usage.

Typical evidence:

- Repeated product need
- Accessibility review
- Token and API review
- Tests

#### Behavioral change

Changes interaction, semantics, content expectations, or state behavior.

Typical evidence:

- UX rationale
- Research or product evidence
- Accessibility impact
- Migration guidance
- ADR when system-wide

#### Breaking or deprecating change

Removes or replaces existing behavior.

Typical evidence:

- Replacement path
- Adoption analysis
- Migration plan
- Versioning decision
- Communication plan

## Knowledge Links and Traceability

Every component page should make its knowledge dependencies visible.

Recommended relationship model:

```text
Knowledge Source
    ↓
Principle
    ↓
Pattern or Decision
    ↓
Component
    ↓
Story
    ↓
Test
```

A Button story demonstrating form submission should link to:

- Button component guidance
- Forms and Validation pattern
- Accessibility contract
- Relevant tokens
- Content guidance
- Interaction tests

Traceability gives humans and AI a way to move from implementation back to intent.

## Story Design

Stories should represent meaningful states and decisions.

### Required story categories

#### Foundations

- Default
- Variants
- Sizes
- Themes

#### Interaction states

- Focus-visible
- Loading
- Disabled
- Error-adjacent use
- Keyboard interaction

#### Content stress tests

- Long labels
- Localized labels
- Right-to-left content
- Icon-plus-text
- Icon-only where allowed

#### Accessibility contexts

- High contrast or forced colors
- Reduced motion
- Zoom or text scaling
- Screen-reader-oriented examples where behavior is not visually obvious

#### Product-context examples

- Form actions
- Confirmation dialog actions
- Toolbar actions
- Destructive workflow

Product-context stories are essential because isolated component stories cannot teach interaction hierarchy by themselves.

## Recommended Storybook Navigation

```text
Introduction
  ├── Start Here
  ├── AINDS Principles
  ├── Knowledge Before Generation
  └── How to Use This Storybook

Foundations
  ├── Design Language
  ├── Accessibility
  ├── Tokens
  ├── Content
  ├── Localization
  └── Motion

Patterns
  ├── Forms and Validation
  ├── Feedback
  ├── Navigation
  ├── Empty States
  └── Destructive Actions

Components
  ├── Actions
  ├── Forms
  ├── Navigation
  ├── Feedback
  ├── Data Display
  └── Overlays

Governance
  ├── Contribution
  ├── Component Lifecycle
  ├── Decision Records
  └── Release and Deprecation

AI
  ├── Using AI with the System
  ├── Prompt Library
  ├── AI Specialists
  └── Evaluation and Review
```

## Implementation Strategy

AINDS should not fork Storybook at this stage.

Forking would create a significant maintenance obligation and would separate AINDS from improvements in the upstream Storybook ecosystem.

Use a progressive implementation strategy.

### Phase 1: MDX and standard Docs

Use existing Storybook capabilities to prove the information architecture.

Implement:

- Standalone MDX pages
- Custom component Docs pages
- Existing Docs blocks
- Links to repository knowledge
- Copyable prompts
- Governance and knowledge-source sections

Goal:

Validate the content model before building specialized tooling.

### Phase 2: Reusable AINDS Docs blocks

Create reusable React/MDX documentation blocks such as:

- `<KnowledgeSources />`
- `<Governance />`
- `<AIGuidance />`
- `<TokenContract />`
- `<AccessibilityContract />`
- `<DoDont />`
- `<RelatedKnowledge />`

Goal:

Reduce documentation drift and establish consistent presentation.

### Phase 3: AINDS Storybook addon

Build an addon only after repeated needs are proven.

Potential capabilities:

- Knowledge panel
- Governance status
- Prompt library
- Traceability graph
- Machine-readable export
- Review status and freshness warnings
- Links to ADRs and knowledge sources
- AI-specialist context bundles

Goal:

Make the knowledge layer easier to maintain and consume without changing Storybook's core.

### Phase 4: External knowledge integration

Connect Storybook to the canonical knowledge repository or knowledge service.

Potential capabilities:

- Resolve stable knowledge IDs
- Detect stale or broken links
- Generate context bundles for AI tools
- Show ownership and review dates
- Validate required documentation sections

### Fork threshold

Consider a Storybook fork only when all of the following are true:

- A core AINDS capability cannot be implemented through MDX, Docs customization, addons, presets, or external services
- The capability is central to the methodology rather than a convenience
- The maintenance cost is understood and funded
- Upstream contribution has been attempted or evaluated
- The fork has a clear compatibility and upgrade strategy

Current decision:

> **Do not fork Storybook. Begin with MDX, reusable Docs blocks, and an addon path.**

## Machine-Readable Knowledge

Storybook is a human-facing knowledge surface, but AINDS should avoid trapping knowledge only in rendered prose.

Where practical, component documentation should reference structured metadata.

Example:

```yaml
id: COMPONENT-BUTTON
status: stable
knowledge_domain: components
owners:
  - design-systems
patterns:
  - UX-FORM-VALIDATION
  - UX-ACTION-HIERARCHY
knowledge_sources:
  - WCAG-2.2
  - CONTENT-STYLE-GUIDE
ai_consumers:
  - component-engineer
  - accessibility-auditor
required_sections:
  - accessibility-contract
  - token-contract
  - governance
last_reviewed: YYYY-MM-DD
```

Storybook can render this metadata while AI tooling consumes the same source.

## Definition of Done for an AINDS Component Page

A component page is complete when:

- Its purpose and boundaries are clear
- Appropriate and inappropriate uses are documented
- UX rationale is explicit
- Accessibility behavior is testable
- Token dependencies are visible
- Content and localization guidance are present where relevant
- Governance and ownership are visible
- AI-generation guidance is constrained by canonical knowledge
- Knowledge sources and related decisions are linked
- Stories cover meaningful states and realistic contexts
- Tests are traceable to the documented contract

## Relationship to Knowledge Before Generation

Traditional component documentation often begins after implementation.

AINDS reverses that order.

The knowledge model defines intent, constraints, rationale, and evaluation before humans or AI generate or change a component.

Storybook then becomes the place where that knowledge and its implementation are experienced together.

> **The component is not the whole product of the design system. The shared understanding around the component is part of the product too.**
