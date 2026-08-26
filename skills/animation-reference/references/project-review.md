# Project-Aware Animation Review

Use this reference only when recommending animation for an existing project, page, or component.

## Evidence Pass

Inspect enough of the current project to make recommendations specific rather than generic:

1. Repository instructions and the user's review-versus-implementation boundary.
2. Framework and rendering model from manifests and configuration.
3. Existing animation libraries, CSS transitions, duration or easing tokens, and reduced-motion rules.
4. Component hierarchy, design-system primitives, responsive behavior, and styling conventions.
5. Meaningful states: loading, empty, success, error, expanded, selected, reordered, mounted, unmounted, and route changes.
6. Rendered behavior through an existing preview, local run, screenshots, or recordings when visual hierarchy affects the recommendation.

Record whether each conclusion comes from source, rendered behavior, or inference. If the project is too large, start with the requested page and the components it directly uses.

## Selection Criteria

Recommend motion when it has at least one clear job:

- **Feedback:** confirms input, progress, completion, rejection, or changed state.
- **Continuity:** shows where an element came from or where it went.
- **Orientation:** helps users understand navigation, hierarchy, or spatial relationships.
- **Attention:** directs focus to a new or important change without competing with content.
- **Character:** reinforces the project's visual identity after usability needs are satisfied.

Prefer no animation when motion would delay a frequent task, repeat unnecessarily, obscure content, amplify layout instability, or compete with several effects already on screen.

## Component Opportunities

Use these as hypotheses to test against the actual project, not as a checklist.

| Component or state | Candidate pattern | Evidence that justifies it |
| --- | --- | --- |
| Button or control | press scale, color transition, progress morph | an action needs immediate confirmation |
| Card to detail | shared-element or image transition | source and destination visibly share content |
| Modal, drawer, sheet | overlay fade plus scale or directional slide | spatial origin and focus transfer are clear |
| Tabs or segmented control | shared indicator plus short content crossfade | selection changes content in place |
| Accordion or disclosure | measured expansion with content fade | hidden content must retain spatial continuity |
| List insert, delete, reorder | FLIP or layout animation | items otherwise jump between positions |
| Loading to content | skeleton crossfade or staged reveal | data arrival creates a visible state change |
| Form validation | local message reveal and subtle field feedback | error or success needs attribution to a field |
| Toast or notification | short slide/fade with stable stacking | transient feedback needs a clear arrival and exit |
| Route or view change | restrained crossfade, shared layout, or directional transition | navigation hierarchy supports the direction |
| Hero or editorial section | staged entrance, mask reveal, or scroll-linked sequence | storytelling is important and content remains readable |
| Data value or chart | number interpolation or path transition | the change itself carries meaning |

## Technique Fit

- Use CSS transitions or keyframes for local, deterministic state changes.
- Use the project's existing motion library for presence, layout, gesture, or shared-element behavior.
- Consider Motion when a compatible React, JavaScript, or Vue project needs layout, presence, gesture, or scroll primitives.
- Consider GSAP for deliberately authored timelines, advanced SVG, or complex scroll choreography.
- Consider Canvas, WebGL, or Three.js only when the visual result genuinely requires a rendered scene.
- Do not add a dependency for a simple opacity or transform transition.

Prefer transform and opacity for frequent UI motion. Evaluate layout properties, blur, filters, shadows, masks, large painted regions, and continuous pointer or scroll handlers against the actual performance budget.

## Recommendation Format

Lead with three to five high-value opportunities. Add lower-priority polish only when it supports a coherent motion system.

For each recommendation include:

- **Priority:** P0 for required feedback or orientation, P1 for meaningful usability improvement, P2 for optional character or polish.
- **Component / file:** the exact component and source path when available.
- **Current evidence:** the state, code, or rendered behavior that supports the idea.
- **Suggested motion:** a named pattern and concise behavioral description.
- **Trigger and states:** the input and the initial, intermediate, and final states.
- **Timing:** duration, easing or spring feel, delay, and stagger if relevant.
- **Implementation fit:** existing primitive or the smallest suitable technique.
- **Why:** the user-facing purpose, not merely that it looks polished.

Conclude with reusable global motion tokens, a reduced-motion strategy, and ideas intentionally rejected. If implementation was not requested, stop at recommendations.
