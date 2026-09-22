# Responsive Adaptation

Use when layout or interaction must adapt across viewport, container, input or content constraints.

## Principles
Adapt hierarchy and behavior, not only dimensions.

Verify:
- content priority;
- navigation transformation;
- wrapping and stacking;
- overflow;
- minimum interactive targets;
- readable line length;
- dense data behavior;
- modal/sheet behavior;
- keyboard and focus behavior after adaptation;
- zoom and reflow.

Prefer existing project breakpoints, container rules and responsive component behavior. Do not invent breakpoints when official values exist.

When a component cannot preserve its behavior at a smaller size, define an explicit adaptation instead of compressing it until it fails.
