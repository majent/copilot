# Code Review Instructions

This file defines specific instructions that GitHub Copilot should consider when conducting code reviews.

## Coding guideline

Apply the [general coding guidelines](./general-coding.instructions.md) to all code.
Apply the [typescript coding guidelines](./typescript.instructions.md) to all code.
Apply the [react coding guidelines](./react.instructions.md) to all code.

## Definition of Code Quality

In reviews, we maintain high-quality code by considering the following aspects:

### Readability

- Easy to understand at a glance
- Use clear names
- Simple structure with minimal nesting

### Maintainability

- Easy to change without breaking other parts
- Reuses common logic instead of duplicating
- Dependencies are clear and controlled
- Can be tested easily

### Efficiency

- Avoid unnecessary loops, recalculations, and rerenders
- Appropriately utilize data fetching, caching strategies, and memoization
- Balance performance and readability

### Heigh cohesion (Module Internal Consistency)

- Single-responsibility principle
- Related logic stays together.

### Low coupling (Module Interdependencies)

- Modules work independently
- Modules don't depend on unrelated things
- Modules connect only through simple, clear interfaces
