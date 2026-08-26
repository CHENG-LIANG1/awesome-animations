---
name: animation-reference
description: Find, identify, and specify web or UI animation, or inspect an existing project and recommend suitable component motion. Use when the user cannot name an effect, wants motion inspiration, needs an implementation-ready animation spec, or asks which animations would improve the current interface.
---

# Animation Reference

Turn an imprecise motion idea into named patterns and a buildable specification, or turn an existing interface into evidence-based component animation recommendations.

## Choose the Mode

- **Reference discovery:** use when the user describes, shows, or links an effect and wants its name, close examples, or an implementation spec.
- **Project-aware recommendations:** use when a project, page, or component is available and the user wants animation ideas that fit what already exists.

## Reference Discovery

1. Establish the context from what the user supplied: web or native UI, the element involved, and whether motion begins on load, hover, click, drag, state change, or scroll. Ask only for missing details that would materially change the result.
2. Inspect any screenshot, clip, prototype, or URL before naming the effect. Distinguish what is directly visible from assumptions about its implementation.
3. Choose the smallest relevant set of sources from [references/websites.md](references/websites.md). Prefer real interaction recordings when behavior and timing matter; prefer runnable examples when the user needs terminology or code.
4. Search using the visible mechanism and trigger, not only an aesthetic adjective. Read [references/motion-vocabulary.md](references/motion-vocabulary.md) when the name is unclear or a precise specification is needed.
5. Return up to six close references. For each, state the likely pattern name and the traits that make it relevant. Do not claim that a showcased site uses a particular library unless that implementation is verified.
6. Convert the selected direction into a motion spec containing:
   - trigger and affected elements;
   - initial, intermediate, and final states;
   - position, scale, rotation, opacity, blur, mask, or layout changes;
   - duration, delay, stagger, easing, or spring behavior;
   - scroll mapping or gesture response when applicable;
   - entry, interruption, reversal, and exit behavior;
   - reduced-motion fallback;
   - suitable implementation approach for the user's existing stack.

## Project-Aware Recommendations

Read [references/project-review.md](references/project-review.md), then inspect the project before proposing motion.

1. Follow repository instructions and preserve the user's requested boundary between review and implementation.
2. Identify the framework, component system, styling approach, animation dependencies, tokens, routes, and state model. Inspect the relevant component sources and their interactive states; do not infer behavior from filenames alone.
3. When rendered hierarchy or timing matters, use an existing preview or run the project if a read-only preview is in scope. Label recommendations as source-only when the interface cannot be rendered.
4. Find places where motion improves feedback, state clarity, spatial continuity, hierarchy, or orientation. Do not assign animation to every component.
5. Base each recommendation on a concrete component, file, visible state, or interaction. Reuse current libraries and motion conventions unless a new dependency has a clear benefit.
6. Rank the smallest useful set of recommendations and provide an implementable spec for each. State when no animation is the better choice.

For a project review, report:

```text
Motion direction:

Priority | Component / file | Current evidence | Suggested motion
Trigger and states | Timing | Implementation fit | Why it helps

Global motion tokens:
Reduced-motion strategy:
Ideas intentionally rejected:
```

## Motion Spec Shape

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
- When the user only wants identification, research, review, or recommendations, do not modify their project.
