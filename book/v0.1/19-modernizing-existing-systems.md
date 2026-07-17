# Chapter 19 — Modernizing an Existing System

An established organization has the opposite problem from a startup. It does not lack artifacts. It has too many.

Multiple Figma libraries, duplicated components, local tokens, legacy frameworks, undocumented exceptions, and conflicting product patterns often coexist. The first task is not creation. It is interpretation.

A modernization effort begins with an audit:

- Inventory components, variants, tokens, and libraries
- Sample production screens rather than trusting documentation alone
- Map duplicate and near-duplicate patterns
- Interview experienced contributors about rationale and exceptions
- Review accessibility defects and support pain points
- Identify products with the greatest adoption leverage
- Distinguish legitimate domain differences from accidental drift

AI can help classify screenshots, cluster visual values, compare APIs, detect naming inconsistencies, and summarize repository history. These outputs are evidence, not final decisions.

The organization then chooses a migration strategy. A “big bang” replacement is rarely necessary. A strangler approach can introduce canonical tokens, adapters, and components while legacy products migrate incrementally.

Knowledge must migrate alongside code. Consolidating three alert components without resolving when each alert type is appropriate merely hides the inconsistency behind one API.

Prioritization should balance:

- Frequency of use
- Product risk
- Accessibility impact
- Maintenance burden
- Cross-product leverage
- Upcoming roadmap demand

Visible wins build credibility. Replacing a painful, inconsistent form workflow may matter more than completing an abstract foundation layer no product can yet use.

Legacy exceptions should be documented, not shamed. Some exist because of technical constraints, regulatory requirements, or product context. Others can be retired. The audit makes the distinction reviewable.

> **Modernization is not the replacement of old components. It is the recovery, reconciliation, and renewal of organizational decisions.**

## Key takeaways

- Existing systems require discovery before consolidation.
- Production reality is a more reliable audit source than libraries alone.
- AI can accelerate classification, but humans resolve meaning and legitimacy.
- Migrate knowledge and rationale together with code and design assets.
