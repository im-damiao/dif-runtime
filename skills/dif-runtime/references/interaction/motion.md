# Interaction and Motion

Use when an interface contains transitions, gestures, direct manipulation or animated state changes.

## Response
Feedback should begin as close as possible to the initiating user action. Avoid artificial latency.

## Direct manipulation
Dragged or manipulated content should track input continuously and preserve the user's grab relationship when technically applicable.

## Interruptibility
Gesture-driven motion should remain interruptible. Do not lock input solely because a transition is running.

## Spatial consistency
Entry, exit and transformation should preserve understandable spatial relationships. Reversible transitions should return through a coherent path.

## Momentum
When velocity is part of the interaction, preserve continuity between gesture release and resulting motion. Do not add momentum or bounce when the interaction does not justify it.

## Functional motion
Motion must communicate change, causality, hierarchy or feedback. Avoid repeated decorative animation.

## Accessibility
Respect reduced-motion preferences. Critical state changes must remain understandable without motion.

## Review checks
Verify:
- response latency;
- continuity;
- interruptibility;
- spatial origin;
- state communication;
- reduced-motion behavior.
