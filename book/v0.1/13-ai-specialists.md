# Chapter 13 — AI Specialists

A general AI assistant can help with almost any task. That flexibility is useful, but it also encourages vague responsibility.

AINDS introduces AI specialists: constrained roles that operate from defined knowledge, permissions, outputs, and review gates.

Examples include:

- Knowledge Curator
- Design System Architect
- Token Specialist
- Component Engineer
- Accessibility Auditor
- Content Specialist
- Icon Specialist
- Documentation Maintainer

An Icon Specialist, for example, should know which family governs the product, which geometric rules apply, which source assets may be used, how names are formed, and what evaluation is required before a generated icon is accepted.

A specialist definition should include:

1. Purpose
2. Required knowledge
3. Allowed tools
4. Inputs
5. Expected outputs
6. Prohibited assumptions
7. Evaluation criteria
8. Human-review conditions

This does not require a separate model for every role. Specialists may be prompt and context configurations applied to the same underlying model. The specialization is organizational, not necessarily technical.

Clear roles make AI behavior more inspectable. If an Accessibility Auditor proposes a visual redesign rather than reporting violations and options, it has crossed its boundary. If a Component Engineer invents a token, the system can require escalation instead of silently accepting the change.

Specialists also support division of labor. One agent may draft an implementation while another evaluates accessibility, token use, and conformity to patterns. Humans remain responsible for accepting decisions and resolving conflicts.

> **AI should consume organizational knowledge, not invent organizational policy.**

## Key takeaways

- Specialist roles reduce ambiguity in AI-assisted workflows.
- Each specialist needs explicit knowledge, outputs, limits, and review gates.
- Specialization can be implemented through context and permissions, not separate models.
- Humans remain accountable for policy and unresolved tradeoffs.
