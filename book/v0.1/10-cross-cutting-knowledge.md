# Chapter 10 — Accessibility, Content, Localization, and Motion

Some design-system concerns do not belong to a single component. They cut across the entire product.

Accessibility is the clearest example. A button can have correct semantics, but an inaccessible workflow can still emerge from poor focus order, unclear errors, insufficient contrast, motion that cannot be reduced, or content that assumes too much.

Content works the same way. A component may support a label, but the system must define terminology, casing, tone, reading level, and how messages behave under stress. Localization affects layout, truncation, dates, names, plurals, and right-to-left behavior. Motion affects hierarchy, feedback, attention, and comfort.

These concerns must be treated as first-class knowledge domains rather than final review checklists.

A cross-cutting knowledge article should define:

- Baseline principles
- Non-negotiable requirements
- Component implications
- Pattern implications
- Testing expectations
- Exceptions and ownership

For accessibility, this may include WCAG target, keyboard interaction, focus visibility, error identification, touch targets, semantics, reduced motion, and manual assistive-technology testing.

For content, it may include voice, terminology, casing, verb-led action labels, error structure, and inclusive language.

For localization, it may include text expansion, locale formatting, bidirectional layouts, cultural review, and assumptions that must never be encoded into fixed dimensions.

For motion, it may include duration ranges, easing, meaningful versus decorative movement, interruption behavior, and reduced-motion alternatives.

AI needs this cross-cutting context because it often optimizes for the visible artifact in front of it. A generated screen can look polished while violating product language, keyboard flow, translation needs, or motion preferences.

The system therefore evaluates artifacts from multiple perspectives before they become canonical.

> **Accessibility by default means accessibility knowledge is present before generation, not discovered after implementation.**

## Key takeaways

- Accessibility, content, localization, and motion span components and workflows.
- They belong in system knowledge, not only QA checklists.
- AI-generated output should be evaluated against every applicable cross-cutting contract.
- Defaults should make the accessible, localizable, coherent path the easiest path.
