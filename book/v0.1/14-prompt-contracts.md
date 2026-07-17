# Chapter 14 — Prompt Contracts

A prompt is often treated as disposable conversation. In an AI-native system, some prompts are operational interfaces and should be designed with the same care as component APIs.

AINDS calls these reusable, governed instructions **prompt contracts**.

A prompt contract defines:

- Task and intent
- Required context
- Applicable principles and patterns
- Components and tokens to use
- Accessibility, content, and localization constraints
- Expected output
- Evaluation criteria
- Escalation conditions

For example, “Build the post-intent screen” is not a sufficient contract. The phrase may be meaningful inside one team, but an agent needs the workflow definition, user state, approved pattern, required primitives, content rules, and human checkpoints.

A stronger contract might specify:

```text
Task: Compose the post-intent confirmation screen.
Context: The applicant has completed intent selection but has not entered underwriting details.
Use: Confirmation pattern, Progress pattern, Button, Alert.
Constraints: Sentence case, approved insurance terminology, WCAG AA, semantic tokens only.
Do not: Introduce new variants or skip the disclosure requirement.
Evaluate: hierarchy, keyboard flow, responsive behavior, content accuracy.
Escalate: policy ambiguity, new pattern, destructive or irreversible action.
```

Prompt contracts should be versioned. A change to validation behavior or terminology may require updating the prompts that depend on it. Their lifecycle may be experimental, recommended, deprecated, or retired.

They should also avoid pretending uncertainty does not exist. Good contracts tell AI when to ask, when to retrieve more knowledge, and when to stop.

> **A reliable prompt is not clever wording. It is a task bounded by organizational knowledge.**

## Key takeaways

- Reusable prompts are interfaces between organizational knowledge and AI execution.
- Contracts should include context, constraints, evaluation, and escalation.
- Prompt changes belong in version control and governance.
- Good prompts expose uncertainty rather than hiding it.
