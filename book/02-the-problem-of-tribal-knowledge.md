# Chapter 2 — The Problem of Tribal Knowledge

Tribal knowledge is the undocumented understanding that allows experienced people to make consistent decisions inside an organization.

It includes things like:

- We validate forms on submit.
- We do not disable primary actions unless the user cannot take the action for a known reason.
- We use inline validation instead of summary-only validation.
- We avoid modals for complex multi-step workflows.
- We use this icon style, not that one.
- We never use red for warnings.
- We move focus to the first invalid field.
- We always provide a visible focus indicator.

Tribal knowledge is powerful, but fragile.

It is not searchable.  
It is not scalable.  
It is not reviewable.  
It is not easily inherited by new team members.  
It is invisible to AI.

## The Form Validation Example

Two forms use the same component library.

In one form, the Continue button is disabled until all fields are valid.

In another form, the Continue button remains enabled and triggers validation when clicked, preventing the user from proceeding until errors are corrected.

Neither implementation is inherently irrational.

Both teams made reasonable local decisions.

The inconsistency exists because the design system documented the button but not the validation philosophy.

The missing artifact was not another component.

The missing artifact was organizational knowledge.

## Components Capture UI. Knowledge Captures Decisions.

A button component answers:

> What does a button look like?

A validation pattern answers:

> How should users discover, understand, and recover from invalid input?

AINDS treats the second question as a first-class design system concern.

## Principles

- Inconsistency is often caused by missing shared knowledge, not poor execution.
- Senior judgment should be captured, not merely consulted.
- AI cannot follow organizational rules that have never been written down.

## Implementation Guidance

Create pattern documents for recurring product decisions.

Start with known inconsistencies:

- Form validation
- Dialog behavior
- Empty states
- Error handling
- Success feedback
- Data table interactions
- Loading states
- Destructive actions

## Knowledge Before Generation

Before generating a form, AI must know the organization's validation philosophy, accessibility expectations, error-message guidance, focus behavior, and submit behavior.
