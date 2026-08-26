---
name: animation-reference
description: Find, identify, and specify web or UI animation from a vague visual idea or a reference. Use when the user can picture an effect but cannot name it, wants motion inspiration, needs precise animation vocabulary, or wants a reference translated into an implementation-ready motion spec.
---

# Animation Reference

Turn an imprecise motion idea into named patterns, useful references, and a buildable specification.

## Workflow

1. Establish the context from what the user already supplied: web or native UI, the element involved, and whether motion begins on load, hover, click, drag, state change, or scroll. Ask only for missing details that would materially change the result.
2. If the user provides a screenshot, clip, prototype, or URL, inspect it before naming the effect. Distinguish what is directly visible from assumptions about its implementation.
3. Choose the smallest relevant set of sources from [references/websites.md](references/websites.md). Prefer real interaction recordings when behavior and timing matter; prefer runnable examples when the user needs terminology or code.
4. Search using the visible mechanism and trigger, not only an aesthetic adjective. Read [references/motion-vocabulary.md](references/motion-vocabulary.md) when the name is unclear or a precise specification is needed.
5. Return up to six close references. For each, state the likely pattern name and the one or two traits that make it relevant. Do not claim that a showcased site uses a particular library unless that implementation is verified.
6. Convert the selected direction into a motion spec. Include:
   - trigger and affected elements;
   - initial, intermediate, and final states;
   - position, scale, rotation, opacity, blur, mask, or layout changes;
   - duration, delay, stagger, easing, or spring behavior;
   - scroll mapping or gesture response when applicable;
   - entry, interruption, reversal, and exit behavior;
   - reduced-motion fallback;
   - suitable implementation approach for the user's existing stack.

## Response Shape

For discovery requests, lead with the closest likely name and reference, then give alternatives only when they are meaningfully different.

For implementation requests, use this compact structure:

```text
Pattern:
Trigger:
Elements:
Motion:
Timing:
Continuity:
Reduced motion:
Implementation fit:
Reference:
```

If the user's description remains ambiguous, offer two or three visibly distinct interpretations instead of forcing a single label. Preserve the user's chosen reference and visual intent when implementation constraints require simplification.

## Quality Boundaries

- Treat inspiration galleries as visual evidence, not proof of usability, performance, conversion, or technical architecture.
- Prefer transforms and opacity for ordinary interface motion; justify expensive blur, filter, large-area paint, WebGL, or continuous pointer effects.
- Keep keyboard behavior, focus, content order, and the `prefers-reduced-motion` experience functional.
- Separate exact observations, likely pattern names, and implementation recommendations.
- When the user only wants identification or research, do not modify their project.
