# Chapter 20 — Platform Architecture

AINDS is a methodology before it is a platform. Still, the methodology implies an architecture.

The architecture should keep knowledge canonical while allowing many tools to consume it.

```text
Repository knowledge
   ├── Markdown guidance
   ├── Structured metadata
   ├── Tokens
   ├── ADRs
   ├── Prompt contracts
   └── Tests
          ↓
Build and validation layer
          ↓
Figma projections, code packages, Storybook, search, MCP, and AI context
```

The repository is not required to be the only storage technology, but every artifact needs a stable source of truth, ownership, and version history.

Key architectural concerns include:

- Stable knowledge identifiers
- Token transformation and distribution
- Component packages and framework adapters
- Storybook generation
- Search and retrieval
- Context bundling for AI tools
- Validation of required relationships
- Versioning and migration
- Access control for sensitive knowledge

Platform Over Framework is an important principle. The knowledge model should not depend on React, Angular, Vue, or Web Components, even when the reference implementation chooses one. Components may have platform-specific implementations while sharing semantic contracts, tokens, accessibility expectations, and pattern guidance.

An MCP server is one possible interface for exposing knowledge to tools such as Cursor or Claude Code. It is not the methodology itself. A static generated bundle, repository search, or API may be sufficient for early implementations.

Architecture should grow through demonstrated needs. Begin with files, schemas, build scripts, and Storybook. Add services when scale, permissions, freshness, or retrieval quality require them.

The most dangerous architecture is one that creates a new inaccessible knowledge silo while claiming to solve fragmentation.

> **The repository is memory. Tools are projections of that memory.**

## Key takeaways

- AINDS separates canonical knowledge from the interfaces that display or consume it.
- The knowledge model should remain portable across frameworks.
- MCP is a useful interface, not a prerequisite.
- Add platform complexity only when proven needs justify it.
