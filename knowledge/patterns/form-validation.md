# Pattern — Form Validation

**Status:** Draft

## Problem

Different teams may implement form validation differently even when using the same component library.

Example:

- One form disables the Continue button until all fields are valid.
- Another form keeps Continue enabled, validates on click, and blocks progression when errors exist.

Both approaches can be reasonable, but inconsistent use across a product creates a fragmented user experience.

## AINDS Perspective

The missing artifact is not another Button component.

The missing artifact is the organization's validation philosophy.

## Recommended Pattern

Primary action buttons should generally remain enabled.

Validation occurs on submit or progression attempt.

When invalid fields exist:

- Prevent progression.
- Display inline errors.
- Move focus to the first invalid field when appropriate.
- Provide clear, actionable error messages.
- Ensure errors are programmatically associated with fields.
- Do not rely on color alone.
- Preserve user input.

## Rationale

Keeping the action available allows users to discover what is missing and why they cannot proceed.

Disabled buttons can obscure the reason progression is unavailable, especially for keyboard and screen reader users.

## Accessibility Considerations

- Errors must be announced or discoverable by assistive technology.
- Invalid fields should expose appropriate ARIA state when needed.
- Focus behavior should support efficient correction.
- Error text should be specific and actionable.

## Knowledge Before Generation

Before generating a form, AI must know:

- Validation timing
- Button enablement rules
- Error placement
- Focus behavior
- Screen reader expectations
- Content guidelines
