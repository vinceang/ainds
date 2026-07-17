# AINDS Version 0.1 Manuscript Plan

## Working Method

The first priority is a complete book, not a perfect opening chapter.

AINDS will use breadth-first drafting:

1. Draft the entire argument.
2. Give every chapter a practical example.
3. Identify missing evidence and weak transitions.
4. Revise in deliberate passes.

> **A rough complete manuscript is more useful than a polished fragment.**

## Working Title

# AINDS

**Knowledge Before Generation**

*A methodology for building knowledge-driven design systems for humans and AI.*

## Intended Reader

The book is for people responsible for how digital products are designed and built:

- Design-system practitioners
- UX and product-design leaders
- Front-end and platform engineers
- Accessibility and content specialists
- Product and engineering leaders
- Startups building their first system
- Enterprises modernizing an existing system

The book should remain understandable to all of them. Technical depth may increase in later chapters, but the central argument must never depend on jargon.

## Narrative Arc

### Part I — The Coordination Problem

#### Foreword: The Fastest Team Does Not Always Win

**Core idea:** AI increases individual velocity, but organizations succeed through aligned velocity.

**Door handle:** Fifty capable people using fifty AI assistants, each moving rapidly according to different assumptions.

**Gold:** Organizations are entering an era where individual velocity is no longer the limiting factor. Alignment is.

#### Chapter 1: The Invisible Design System

**Core idea:** The visible assets of a design system sit on top of an invisible system of decisions, judgment, habits, and shared understanding.

**Door handles:**

- Two Continue buttons in the same product behaving differently
- A recipe that lists ingredients but omits the chef's judgment
- The new hire whose questions all begin with “Which one do we usually use?”

#### Chapter 2: Tribal Knowledge Is Organizational Debt

**Core idea:** Knowledge held only by experienced individuals is valuable, fragile, and expensive.

**Door handle:** The expert leaves; the code remains; consistency slowly disappears.

#### Chapter 3: Why Traditional Design Systems Stop Too Soon

**Core idea:** Components and tokens preserve outputs, but rarely preserve enough context to reproduce good decisions.

**Door handle:** A fully documented Button API that cannot answer whether the product should disable Continue or validate after activation.

#### Chapter 4: Why AI Changes the Stakes

**Core idea:** AI did not create the knowledge problem; it amplified the consequences of missing shared context.

**Door handle:** Four teammates ask four assistants to create the same modal and receive four plausible but incompatible solutions.

### Part II — The Knowledge Layer

#### Chapter 5: Knowledge Before Generation

**Core idea:** Generation should begin from explicit intent, knowledge, and constraints rather than isolated prompts.

**Door handle:** A GPS can calculate a route quickly, but speed is useless until the destination is known.

#### Chapter 6: Knowledge Sources — You Do Not Have to Invent Expertise

**Core idea:** Teams can deliberately adopt trusted standards, books, systems, and practices as inputs.

**Door handle:** A startup says, “We do not know usability yet; begin with the principles in *Don't Make Me Think*.”

#### Chapter 7: Seeds — Starting With Taste Instead of a Questionnaire

**Core idea:** Teams often begin with examples, screenshots, a preferred icon family, a trusted framework, or an admired product.

**Door handle:** “Use Lucide, follow Refactoring UI, and make the product feel as calm as Linear.”

#### Chapter 8: From Decisions to Design Language

**Core idea:** Repeated decisions become patterns; patterns become a recognizable design language.

**Door handle:** Every product has an accent—its casing, motion, terminology, spacing, validation, and imagery form a recognizable voice.

#### Chapter 9: The Knowledge Taxonomy

**Core idea:** Knowledge needs a shared structure so people and AI can discover what governs an artifact.

**Door handle:** A library without a catalog may contain the right book, but nobody can reliably find it.

### Part III — Making Knowledge Executable

#### Chapter 10: Tokens Before Components

**Core idea:** Tokens encode named design decisions and make system behavior portable across themes, products, and platforms.

**Door handle:** A value such as `#0057B8` says what a color is; `color.action.primary.background` says what it means.

#### Chapter 11: Components Capture UI; Knowledge Captures Decisions

**Core idea:** A component is incomplete without its purpose, constraints, rationale, and governance.

**Door handle:** The toolbox contains a hammer, but experience determines when the problem is not a nail.

#### Chapter 12: Accessibility by Default

**Core idea:** Accessibility must exist in principles, tokens, patterns, component contracts, stories, and tests—not as a final audit.

**Door handle:** A ramp added after a building is finished is usually more awkward and expensive than an entrance designed for everyone.

#### Chapter 13: Content Is Part of the System

**Core idea:** Terminology, casing, labels, errors, confirmations, and tone are reusable design decisions.

**Door handle:** One workflow says “Member,” another says “Customer,” and a third says “User”; all refer to the same person but make the product feel fragmented.

#### Chapter 14: Localization, Themes, and Adaptation

**Core idea:** A design system is not truly systematic if it works only in one language, one color scheme, one density, or one cultural context.

**Door handle:** A perfectly designed English button breaks when its German label is twice as long.

#### Chapter 15: Storybook as a Knowledge Surface

**Core idea:** Storybook should teach humans and AI why, when, and how to use the system—not merely display examples and APIs.

**Door handle:** A showroom can display every tool while still failing to teach anyone how to build a house.

### Part IV — Humans and AI Working as a System

#### Chapter 16: AI Specialists

**Core idea:** Specialized agents should have bounded roles, required knowledge, tool permissions, and escalation rules.

**Door handle:** A hospital does not ask one generalist to perform every specialty; it coordinates experts around a shared patient record.

#### Chapter 17: Prompts Are Interfaces

**Core idea:** Prompts that repeatedly create or evaluate system artifacts should be versioned, governed contracts.

**Door handle:** A verbal instruction repeated differently on every factory shift is not a process.

#### Chapter 18: Governance in an Age of Abundant Generation

**Core idea:** When creation becomes cheap, deciding what becomes canonical becomes more important.

**Door handle:** A photocopier makes duplication easy; it does not decide which version is official.

#### Chapter 19: Organizational Alignment

**Core idea:** AINDS coordinates people with different AI skill, velocity, roles, and interests around shared intent.

**Door handle:** A rowing team does not win because one athlete rows ten times faster in a different direction.

**Gold:** AI increases individual velocity. AINDS aligns organizational velocity.

### Part V — Architecture and Adoption

#### Chapter 20: Platform Over Framework

**Core idea:** Knowledge, tokens, patterns, and contracts should outlive any individual UI framework.

**Door handle:** A city's traffic laws should not need to be rewritten every time residents buy a different brand of car.

#### Chapter 21: Greenfield — Building Intentionally From Day One

**Core idea:** A startup can begin with a small knowledge foundation, trusted sources, and seeds rather than a large bureaucracy.

**Door handle:** A two-person startup chooses Lucide, WCAG 2.2 AA, sentence case, a validation pattern, and a token baseline before producing its first reusable components.

#### Chapter 22: Enterprise — Recovering the Invisible System

**Core idea:** Established organizations must extract knowledge from products, people, research, code, support data, and existing documentation.

**Door handle:** An archaeological dig does not invent the city; it uncovers and interprets what is already there.

#### Chapter 23: The Reference Implementation

**Core idea:** Demonstrate how repository knowledge, tokens, framework-neutral component contracts, Storybook, adapters, AI specialists, and tests connect.

**Door handle:** Follow one Button decision from adopted source to principle, pattern, token, component, story, prompt, and test.

#### Chapter 24: Building Products With AINDS

**Core idea:** Prove the methodology through multiple distinct products powered by one system.

Potential case studies:

- Restaurant ordering
- Small-business quoting
- Digital-download commerce
- SaaS administration

The applications should differ in domain and visual expression while sharing accessibility, tokens, components, content standards, localization, governance, and Storybook knowledge.

### Conclusion — Preserve the Thinking

**Core idea:** Organizations deserve to preserve not only what they built, but how they learned to build it well.

**Gold:** The greatest value of a design system is not the components it contains. It is the decisions you no longer have to make.

## Version 0.1 Chapter Contract

Each chapter must contain, at minimum:

- One clear central claim
- One relatable door-handle example
- One practical consequence
- One connection to the larger methodology
- One transition to the next chapter
- A short end section:
  - Principle
  - Practice
  - Knowledge Before Generation

## Revision Passes

### Pass 1 — Completeness

Every chapter exists and makes its core argument.

### Pass 2 — Structure

Remove repetition, repair sequencing, and strengthen transitions.

### Pass 3 — Door Handles

Ensure each chapter contains a memorable real-world example.

### Pass 4 — Evidence

Add research, standards, historical context, citations, and industry examples.

### Pass 5 — Practical Application

Add templates, checklists, diagrams, implementation guidance, and case studies.

### Pass 6 — Voice

Make the writing consistently direct, relatable, and quotable.

### Pass 7 — Technical and Editorial Review

Validate accuracy, accessibility language, architecture, licensing, terminology, and copy editing.

## Anti-Perfection Rule

During Pass 1, unfinished material should be marked instead of blocking progress:

```text
[NEEDS EXAMPLE]
[NEEDS EVIDENCE]
[VERIFY TECHNICAL CLAIM]
[REVISIT STRUCTURE]
```

A visible gap can be fixed. An unwritten chapter cannot.
