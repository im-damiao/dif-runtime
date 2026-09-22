# Component Composition

Use during component creation, extension and implementation mapping.

## Resolution order
1. Inspect project context.
2. Search existing component.
3. Search existing variant/property.
4. Search existing composition/pattern.
5. Inspect official component documentation when available.
6. Verify semantic and behavioral fit.
7. Only then propose extension or creation.

## Composition
Prefer existing primitives and composition over duplicating functionality. Keep public APIs minimal and predictable.

## States
Define applicable default, hover, focus, pressed, selected, disabled, loading, error, success and read-only states.

## Accessibility
Define semantic role, accessible name, keyboard behavior, focus behavior and announcements where applicable.

## Implementation evidence
Do not recommend a component API from memory when the project's actual component implementation or documentation can be inspected.
