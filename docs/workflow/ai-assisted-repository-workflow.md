# AI-Assisted Repository Workflow

## Purpose

Define how humans and AI collaborate on AINDS now that the GitHub repository is the single source of truth.

## Core Principle

> Knowledge Before Generation.

The repository is the canonical knowledge base. Conversations are discovery spaces.

## Workflow

```txt
Idea
  ↓
Conversation
  ↓
Discovery
  ↓
Classification
  ├── Issue
  ├── ADR
  ├── Handbook Chapter
  ├── Knowledge Article
  ├── Agent Definition
  ├── Positioning Message
  └── Roadmap Item
  ↓
Repository Update
  ↓
Review
  ↓
Canonical Knowledge
```

## Roles

### Human

Humans own intent.

The human decides:

- what matters
- what belongs in AINDS
- what should become canonical
- when an idea is ready to be promoted
- whether the generated artifact reflects the intended meaning

### AI

AI accelerates execution.

The AI may:

- summarize conversations
- identify reusable insights
- create issues
- draft Markdown files
- update repository documentation
- propose ADRs
- create positioning language
- suggest next actions

## Operating Rules

### Nothing important lives only in chat

Any reusable insight should be promoted into the repository as an issue, ADR, handbook chapter, knowledge article, glossary entry, positioning note, or roadmap item.

### The repository is memory

The AI should treat the repository as the source of truth, not prior conversation memory.

### Conversations are discovery

Side explorations are welcome. They are useful because they reveal ideas, language, patterns, and decisions. If a discovery matters, it is captured.

### Humans approve meaning

AI can draft and commit, but humans remain responsible for intent, direction, and canonical meaning.

## When To Create An Issue

Create an issue when an idea is important but not yet ready to become final documentation.

Examples:

- Define the knowledge taxonomy
- Define the Storybook knowledge model
- Explore AINDS governance
- Draft a new AI Specialist
- Evaluate a technical direction

## When To Commit A File

Commit a file when the idea is stable enough to become part of the knowledge base.

Examples:

- Positioning language
- Workflow documentation
- Session notes
- Draft handbook chapters
- Knowledge articles
- Agent definitions

## Capture Checklist

At the end of a meaningful session, ask:

- What did we discover?
- Did we make a decision?
- Did we find language worth preserving?
- Does this require an issue?
- Does this require an ADR?
- Does this belong in the handbook?
- Does this belong in the knowledge base?
- What should happen next?

## AINDS Fit

This workflow practices the methodology itself.

AINDS exists to transform tribal knowledge into organizational knowledge. Therefore, AINDS conversations must not become tribal knowledge.
