# ADR-0002 — Platform-Agnostic Web Components Core

**Status:** Proposed  
**Date:** 2026-06-29

## Context

AINDS should demonstrate platform thinking rather than framework lock-in. The reference implementation should support Angular applications while remaining useful to React, Vue, vanilla JavaScript, and future frameworks.

## Decision

The core design system implementation should use platform-native Web Components for foundational UI primitives, supported by framework-specific adapters where needed.

## Recommended Architecture

```txt
packages/
  tokens/
  icons/
  elements/       Native Web Components
  angular/        Angular adapters and wrappers
  storybook/
  agents/
  knowledge/
```

## Web Components Are Best For

- Buttons
- Badges
- Cards
- Alerts
- Icons
- Tabs
- Accordions
- Empty states
- Theme providers
- Simple layout primitives

## Framework Adapters Are Best For

- Angular forms integration
- Typed APIs
- Router integration
- Signal-friendly APIs
- Complex workflows
- Enterprise CRUD screens
- Product-specific orchestration

## Consequences

This approach improves portability but requires additional attention to developer experience, especially for Angular and React users.

## How This Reinforces Knowledge Before Generation

The component implementation becomes one consumer of shared knowledge rather than the source of truth itself. Frameworks may change, but the knowledge remains.
