# Motion Vocabulary

Use this reference to translate visual descriptions into searchable names and implementation parameters.

## Triggers

- **Enter / exit:** an element appears or leaves because it mounts, unmounts, or changes state.
- **Hover / focus / press:** motion responds to a pointer or keyboard interaction.
- **Drag / swipe / scrub:** progress follows a gesture rather than a fixed timeline.
- **Scroll-triggered:** scrolling starts an animation that then plays independently.
- **Scroll-linked:** animation progress maps continuously to scroll progress.
- **Layout transition:** elements animate between measured layouts after content or state changes.
- **Idle / ambient:** motion loops without direct input.

## Common Pattern Names

| Visual idea | Useful name or search term |
| --- | --- |
| One card becomes the next screen | shared-element transition, shared-layout animation |
| Content appears through a moving window | clip-path reveal, masked reveal, wipe |
| Page stays fixed while scenes change | scroll pinning, scrollytelling, sticky sequence |
| Layers move at different speeds | parallax, depth scroll |
| Items enter one after another | staggered entrance, cascading reveal |
| Shape changes into another shape | morph, SVG path morphing, icon morph |
| Element slightly passes the target and returns | overshoot, spring animation |
| Object follows the pointer with delay | spring follow, cursor follower, magnetic cursor |
| Text breaks into animated letters or lines | split text, character stagger, line reveal |
| Letters rapidly change before resolving | text scramble, decoding text |
| Content moves endlessly across an edge | marquee, ticker, infinite loop |
| Old page is covered and replaced | page wipe, curtain transition, blinds, iris transition |
| Image grows from a thumbnail into a modal | shared image transition, lightbox zoom |
| List rearranges without jumping | layout animation, FLIP animation, reorder transition |
| Surface tilts toward the pointer | tilt card, perspective hover, pointer parallax |
| Content blurs and scales while changing | blur transition, depth transition |

## Motion Properties

Describe the effect as a combination of:

- **Geometry:** translate, scale, rotate, skew, perspective, transform origin.
- **Visibility:** opacity, blur, brightness, color, shadow.
- **Shape:** border radius, clip path, mask, SVG path.
- **Layout:** size, position, grid order, shared bounds.
- **Time:** duration, delay, stagger, iteration, direction.
- **Feel:** linear, ease-in, ease-out, ease-in-out, cubic Bézier, spring, inertia.
- **Spring parameters:** stiffness, damping, mass, bounce, initial velocity.
- **Input mapping:** pointer coordinates, drag distance, scroll progress, velocity.

## Implementation-Ready Specification

Record observable values before choosing a library:

```text
Pattern: shared-element card expansion
Trigger: click or keyboard activation on a result card
Initial state: card at its grid bounds; details hidden
Transition: card bounds interpolate to the viewport; radius 20px -> 0;
            image preserves continuity; background fades to 40% black
Timing: 420ms; spring-like deceleration; details stagger in after 160ms
Exit: reverse on close; return focus to the originating card
Interruption: a second activation finishes or cancels the active transition
Reduced motion: instant layout change with a 120ms opacity crossfade
```

Avoid vague phrases such as “make it smooth” when the behavior can be stated as a trigger, property change, timing curve, and continuity rule.
