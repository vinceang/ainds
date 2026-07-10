# AINDS Storybook Knowledge Model

## Purpose

The AINDS Storybook Knowledge Model defines how Storybook becomes more than a component catalog.

> **Storybook is where humans and AI learn how the system should be used.**

Traditional Storybook documentation answers questions such as:

- What does this component look like?
- What props or attributes does it accept?
- What states and variants exist?
- How do I implement it?

AINDS extends that model to answer:

- Why does this component exist?
- What user problem does it solve?
- When should it be used?
- When should it not be used?
- What organizational decisions govern it?
- What knowledge must AI consult before generating with it?
- When may it be extended, and who approves that change?

Storybook becomes a **knowledge surface**: a human-readable and machine-consumable projection of the design system's canonical knowledge.

## Storybook Is a Surface, Not the Source

Storybook should expose knowledge, but it should not become the only place that knowledge exists.

The canonical sources remain the repository's knowledge articles, ADRs, pattern documents, token definitions, content standards, and governance records.

```text
Canonical Knowledge
        ↓
Storybook Knowledge Model
        ↓
Interactive Documentation
        ↓
Humans and AI
```

This distinction prevents component documentation from drifting away from the decisions it represents.

## Information Architecture

AINDS Storybook should organize knowledge at four levels.

### 1. Foundation Level

System-wide guidance that applies across components.

Suggested sections:

- Start Here
- Foundations
- Design Language
- Accessibility
- Content and Language
- Tokens
- UX Patterns
- Governance
- AI Guidance
- Changelog and Migration

Examples:

- Accessibility target
- Validation philosophy
- Voice and tone
- Icon-family rules
- Dark-mode strategy
- Localization expectations
- Contribution and deprecation rules

### 2. Pattern Level

Reusable decisions that coordinate multiple components.

Examples:

- Form validation
- Search and filtering
- Empty states
- Destructive actions
- Loading and progress
- Dialogs and drawers
- Data-table behavior
- Notifications

Pattern pages should link to the components that implement them. Component pages should link back to the patterns that govern them.

### 3. Component Level

The complete contract for an individual component.

Each component page should include the standard knowledge sections defined below.

### 4. Example and Workflow Level

Composed experiences showing how multiple patterns and components work together.

Examples:

- Account registration
- Checkout
- CRUD editing flow
- Search-results page
- Settings form
- Accessible confirmation flow

These examples reveal gaps that isolated component stories cannot.

## Component Documentation Model

Every component page should use a consistent structure. Sections may be collapsed or omitted only when they genuinely do not apply.

### 1. Summary

A concise explanation of what the component is and the user problem it solves.

Include:

- One-sentence definition
- Lifecycle status
- Package and version
- Owner
- Related patterns

### 2. Interactive Examples

Show the component in meaningful states rather than only visual permutations.

Include:

- Default
- Variants
- States
- Responsive behavior
- Light and dark themes
- High-contrast or forced-colors behavior where relevant
- Localized and right-to-left examples
- Reduced-motion behavior

### 3. When to Use

Explain the situations in which the component is the preferred solution.

This should describe user and product context, not merely implementation convenience.

### 4. When Not to Use

Document common misuses and the preferred alternatives.

This section is essential for both human contributors and AI generation because it constrains plausible but incorrect choices.

### 5. Anatomy

Identify the named parts of the component and their responsibilities.

Anatomy should connect visual regions to APIs, slots, tokens, content rules, and accessibility semantics.

### 6. Behavior

Describe the interaction contract.

Include:

- Pointer behavior
- Keyboard behavior
- Focus behavior
- State transitions
- Validation behavior
- Loading behavior
- Error recovery
- Disabled versus unavailable behavior

### 7. Accessibility

Describe the required accessible experience.

Include:

- Native semantic element or role
- Accessible name requirements
- Keyboard interaction
- Focus management
- Screen-reader expectations
- Contrast and non-color cues
- Touch-target requirements
- Motion considerations
- Testing instructions

Accessibility guidance should link to the source standards and relevant system decisions.

### 8. Content Guidance

Define the language that belongs inside the component.

Include:

- Text casing
- Recommended length
- Terminology
- Voice and tone
- Error-message guidance
- Localization constraints
- Truncation and wrapping behavior

### 9. Tokens and Theming

List the semantic tokens the component consumes.

Include:

- Token names
- Purpose
- Theme behavior
- Allowed overrides
- Accessibility constraints
- Deprecated tokens

Avoid documenting raw values as the primary contract. The semantic decision is more durable than the value.

### 10. API and Code

Provide implementation details appropriate to each supported platform.

Include:

- Props, inputs, attributes, events, slots, and parts
- Framework-specific examples
- Minimal code example
- Composition example
- Import and package information
- Stability and deprecation notes

### 11. Do and Don't

Show concrete, visually comparable examples.

Each example should explain the reason, not merely mark one image as correct and another as incorrect.

### 12. UX Rationale

Explain the decisions behind the component.

Examples:

- Why submit remains enabled before validation
- Why a dialog traps focus
- Why a destructive action requires confirmation
- Why a link is preferred over a button for navigation

This is where the component stops being only an artifact and becomes organizational knowledge.

### 13. Governance

Document how the component may change.

Include:

- Owner and reviewers
- Admission criteria
- Variant-creation rules
- Allowed customization
- Extension points
- Breaking-change policy
- Deprecation process
- Exception process

### 14. AI Guidance

Provide structured guidance for AI-assisted work.

Include:

- Required knowledge sources
- Required patterns
- Required tokens
- Prohibited assumptions
- Generation prompts
- Evaluation checklist
- Human-review triggers

### 15. Knowledge Sources and Traceability

Link the component to its canonical knowledge.

Examples:

- UX pattern
- Accessibility standard
- ADR
- Research finding
- Content standard
- Token definition
- External adopted source

A contributor should be able to move from artifact to decision, principle, and source.

### 16. Tests and Quality Evidence

Expose the tests that prove the component contract.

Include:

- Interaction tests
- Accessibility tests
- Visual-regression coverage
- Localization coverage
- Browser support
- Known limitations

### 17. Changelog and Migration

Document meaningful changes and the action required from consumers.

## Sample: Button Knowledge Page

The following is an abbreviated example of how the model applies to a Button.

### Summary

A Button initiates an action in the current context.

### Use

Use a Button to submit data, confirm a choice, trigger a process, or change application state.

### Do Not Use

Do not use a Button for navigation when a semantic link is available.

### Behavior

Primary actions generally remain enabled so users may attempt progression and receive clear validation feedback. Disable an action only when the action is truly unavailable and the reason is understandable.

### Accessibility

- Use the native `button` element when possible.
- Ensure every button has an accessible name.
- Preserve visible focus.
- Do not communicate state by color alone.
- Announce loading state without changing the accessible name unexpectedly.

### Content

- Use sentence case.
- Begin with a clear verb.
- Prefer specific labels such as `Save changes` over generic labels such as `Submit`.

### Governance

A new visual variant requires evidence of a recurring semantic need that cannot be expressed by existing variants. Product-specific decoration is not sufficient.

### AI Guidance

Before generating a Button implementation or usage example, consult:

- Button component contract
- Form-validation pattern
- Action hierarchy guidance
- Content standards
- Accessibility requirements
- Relevant semantic tokens

Prompt example:

```text
Create a form action area using the AINDS Button component.

Consult the form-validation and action-hierarchy patterns before generating.
Use semantic tokens only.
Keep the primary action enabled unless the action is genuinely unavailable.
Include loading, validation-error, keyboard, and screen-reader behavior.
Explain any deviation from the documented pattern.
```

Evaluation checklist:

- Is a Button semantically correct for this action?
- Is the hierarchy clear?
- Does the label describe the outcome?
- Are keyboard and focus states covered?
- Does validation follow the system pattern?
- Are only documented variants and tokens used?

## Prompt Model

Prompts in Storybook should not be presented as magic phrases that bypass judgment. They should be reusable task contracts grounded in system knowledge.

Each prompt should contain:

1. **Task** — what should be created or evaluated
2. **Context** — user, product, and workflow
3. **Required knowledge** — patterns, components, tokens, and standards to consult
4. **Constraints** — accessibility, content, architecture, localization, and governance requirements
5. **Expected output** — code, explanation, tests, or documentation
6. **Evaluation** — criteria used to judge the result
7. **Escalation** — conditions requiring human review

### Prompt Categories

- Generate an implementation
- Compose a workflow
- Review an implementation
- Audit accessibility
- Produce tests
- Write or localize content
- Extend an icon or illustration family
- Propose a new variant
- Migrate deprecated usage

### Prompt Status

Prompts should carry lifecycle status:

- Experimental
- Recommended
- Deprecated

Prompts should be versioned because they are part of the design system's interface with AI.

## Governance Model

Storybook should make governance visible at the point of use.

### Component Status

Each component should display a status such as:

- Proposed
- Experimental
- Stable
- Deprecated
- Removed

### Ownership

Each knowledge page should identify the responsible team or role.

### Decision Boundaries

Storybook should clearly state:

- What consumers may configure
- What consumers may compose
- What requires a contribution
- What requires an ADR
- What is prohibited

### New Variant Threshold

A new variant should require:

- A recurring semantic need
- Evidence that composition or existing variants are insufficient
- Accessibility review
- Token impact review
- Cross-product relevance or an explicit exception
- Documentation and test updates
- Design-system approval

### Exception Records

Exceptions should be documented with:

- Context
- Owner
- Rationale
- Scope
- Expiration or review date

## Knowledge Links

Every Storybook page should link to stable identifiers rather than only relative prose references.

Suggested relationships:

```text
Component
  ├── governed_by → UX Pattern
  ├── consumes → Tokens
  ├── conforms_to → Accessibility Standard
  ├── uses_language → Content Standard
  ├── decided_by → ADR
  ├── supported_by → Research or Evidence
  └── generated_with → Prompt Contract
```

Over time, these relationships can support a machine-readable manifest or knowledge graph.

## Machine-Readable Companion

Human-readable MDX should be paired with structured metadata where practical.

Example:

```yaml
id: COMPONENT-BUTTON
status: stable
owner: design-systems
knowledge_domain: components
patterns:
  - UX-ACTION-HIERARCHY
  - UX-FORM-VALIDATION
tokens:
  - color.action.primary.background
  - color.action.primary.foreground
  - space.control.inline
accessibility:
  - A11Y-KEYBOARD-ACTIVATION
  - A11Y-FOCUS-VISIBLE
content:
  - CONTENT-ACTION-LABELS
ai:
  prompt_contracts:
    - PROMPT-BUTTON-COMPOSE
  human_review_when:
    - new_variant
    - destructive_action
```

The metadata should not duplicate full guidance. It should provide identity, relationships, status, and discovery.

## Implementation Strategy

### Phase 1: MDX and Existing Storybook Capabilities

Start without a fork.

Use:

- Component Story Format for examples and states
- MDX for structured documentation
- Storybook Doc Blocks for stories, controls, source, and API information
- Custom React documentation components for AINDS sections such as Governance, AI Guidance, Knowledge Sources, Do/Don't, and Status
- Unattached MDX pages for foundations, patterns, governance, and AI guidance

Storybook's current MDX implementation supports Markdown, linked stories, Doc Blocks, arbitrary JSX components, custom documentation pages, and documentation attached to or independent from stories. This is sufficient for the first reference implementation.

### Phase 2: Reusable AINDS Doc Blocks

Create an internal package of reusable documentation components, for example:

```text
<AindsStatus />
<AindsUseWhen />
<AindsAvoidWhen />
<AindsAccessibility />
<AindsGovernance />
<AindsPrompt />
<AindsKnowledgeLinks />
<AindsDecision />
<AindsDoDont />
```

These blocks should normalize structure and consume component metadata where possible.

### Phase 3: AINDS Storybook Addon

Build an addon when dedicated user-interface behavior becomes valuable.

Potential addon capabilities:

- Knowledge panel beside Canvas and Docs
- Governance and lifecycle badges
- Knowledge-source graph
- Prompt copying with resolved context
- AI-readiness checks
- Missing-knowledge warnings
- Traceability from stories to decisions and tests
- Export of machine-readable manifests

An addon is preferable to a fork because it remains compatible with Storybook releases and can be adopted by existing design systems.

### Phase 4: External Knowledge Integration

Connect Storybook to the canonical knowledge repository or service.

Potential integrations:

- Static manifests generated at build time
- Repository Markdown and YAML
- Search index
- MCP server
- Knowledge graph
- ADR and issue links

### Phase 5: Fork Only if Fundamentally Blocked

Do not fork Storybook merely to customize documentation layout or add panels. MDX, custom Doc Blocks, and addons are intended extension points.

A fork should be considered only if AINDS requires core behavior that cannot reasonably be implemented through public APIs, such as a fundamentally different data model or navigation/runtime architecture.

A fork would create significant maintenance cost, delay compatibility with Storybook improvements, and make adoption harder for teams with existing Storybooks.

## Decision

The initial AINDS reference implementation will use **Storybook with custom MDX pages and reusable AINDS Doc Blocks**.

An **AINDS Storybook addon** is the preferred next extension when the knowledge model requires dedicated panels, automated validation, or machine-readable exports.

AINDS will **not fork Storybook** unless a documented architectural limitation makes the addon path insufficient.

## Reference Implementation Outline

A future implementation may use a structure such as:

```text
.storybook/
  main.ts
  preview.ts
  manager.ts
  ainds-theme.ts

src/
  components/
    button/
      button.ts
      button.stories.ts
      button.docs.mdx
      button.ainds.yaml
  patterns/
    form-validation.mdx
  foundations/
    accessibility.mdx
    content-language.mdx
    design-language.mdx
  governance/
    contribution.mdx
    component-lifecycle.mdx
  ainds-doc-blocks/
    Governance.tsx
    Prompt.tsx
    KnowledgeLinks.tsx
    Status.tsx
```

The exact framework can change. The knowledge contract should remain portable.

## Success Criteria

The Storybook knowledge model succeeds when a contributor—or AI assistant—can answer:

- What is this component?
- Why does it exist?
- When should it be used or avoided?
- How must it behave?
- What accessible experience is required?
- What content and localization rules apply?
- Which tokens and patterns govern it?
- What may be customized?
- When is a new variant justified?
- Which knowledge sources and decisions support it?
- Which prompt contracts can safely generate or evaluate it?
- What requires human review?

At that point, Storybook no longer documents only a component library.

It teaches humans and AI how the design system should be applied and extended.

## Official Storybook References

- MDX: https://storybook.js.org/docs/writing-docs/mdx
- Doc Blocks: https://storybook.js.org/docs/writing-docs/doc-blocks
- Writing Addons: https://storybook.js.org/docs/addons/writing-addons
