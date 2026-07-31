# Chapter 17 — Governance Without a Governance Tax

Design-system governance often fails in one of two directions.

At one extreme, anyone can add anything. The system grows quickly and loses coherence. At the other, every change requires a ceremony so heavy that teams route around the system.

AINDS aims for lightweight, visible governance.

The central question is not “Who has permission?” It is “What evidence is required for this kind of change?”

A documentation correction may need only an owner review. A new component variant may require evidence of a recurring semantic need, accessibility review, token impact, tests, and cross-product relevance. A breaking pattern change may require research, migration guidance, and an ADR.

Governance should define:

- Ownership and decision rights
- Contribution paths
- Change classifications
- Evidence thresholds
- Lifecycle states
- Review gates
- Exceptions
- Versioning and release notes
- Deprecation and migration

The contribution experience should be builder-friendly. Templates can ask for the user problem, existing alternatives, evidence, accessibility impact, and proposed ownership. Automated checks can identify missing metadata or undocumented token use. AI specialists can help classify proposals and locate precedent.

Humans remain responsible for accepting new organizational decisions.

Exceptions are inevitable. A good system records their scope, rationale, owner, and review date. An exception without an expiration or reconsideration point often becomes an accidental pattern.

Adoption depends on trust. Teams use a system when it solves their problems, responds predictably, and evolves at a pace compatible with product delivery. Governance must protect coherence without treating the system as more important than the product.

> **The goal of governance is not to prevent change. It is to make change understandable, accountable, and reusable.**

## Key takeaways

- Governance should scale with the consequence of a change.
- Evidence thresholds are more useful than universal approval rituals.
- Contribution must be easy enough that teams do not bypass the system.
- Exceptions should be explicit, owned, scoped, and reviewed.
