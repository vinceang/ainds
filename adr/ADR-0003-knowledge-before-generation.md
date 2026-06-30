# ADR-0003 — Knowledge Before Generation

**Status:** Proposed  
**Date:** 2026-06-29

## Context

Many AI-assisted workflows begin with prompts and generation. This can produce fast results but often lacks consistency, traceability, accessibility, and design-system alignment.

AINDS reverses the order.

## Decision

AINDS will require documented knowledge before AI generation.

AI specialists must consult relevant knowledge sources before producing artifacts.

## Examples

An Icon Specialist should consult:

- Icon grid rules
- Stroke weight
- Corner radius
- Existing icon library
- Visual weight guidance
- Export requirements

A Component Engineer should consult:

- Component standards
- Token rules
- Accessibility standards
- Storybook requirements
- Testing expectations
- Framework adapter guidelines

## Consequences

This may make early setup slower, but it improves consistency, explainability, and long-term scalability.

## How This Reinforces Knowledge Before Generation

This ADR names the central principle of AINDS and makes it enforceable as an architectural rule.
