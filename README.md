# Awesome Animations

[简体中文](README.zh-CN.md)

A focused collection of animation reference websites plus a Codex skill for turning “I can picture it, but I cannot describe it” into precise motion vocabulary—or inspecting an existing project and recommending animations for its actual components.

## What is included

- A curated list of UI, product-flow, CSS, and experimental web-animation references.
- The [`animation-reference`](skills/animation-reference/SKILL.md) Codex skill.
- A practical [motion vocabulary](skills/animation-reference/references/motion-vocabulary.md) covering triggers, pattern names, timing, physics, and accessibility.
- A [project-aware review guide](skills/animation-reference/references/project-review.md) for evidence-based, component-level animation recommendations.

## Curated websites

| Website | Best for | Start here when... |
| --- | --- | --- |
| [60fps](https://60fps.design/) | UI motion and micro-interactions | You can picture an app effect but do not know its name. |
| [Motion Examples](https://motion.dev/examples) | Runnable React, JavaScript, and Vue patterns | You want a technically named example and a path to code. |
| [Animista](https://animista.net/) | Customizable CSS animation presets | The effect is a lightweight entrance, exit, or attention animation. |
| [1human](https://reels.1human.tech/) | Motion references with recipes, credits, and item-specific reuse rights | You want to compare a title reveal or loading-state rhythm in your existing renderer. |
| [Mobbin](https://mobbin.com/) | Real mobile and web product flows | You need to see how shipped products handle an interaction. |
| [Page Flows](https://pageflows.com/) | Recorded user journeys | Sequence and timing matter more than a single screen. |
| [Codrops](https://tympanus.net/codrops/) | Creative demos and tutorials | You want typography, page transition, pointer, WebGL, or Three.js ideas. |
| [GSAP Showcase](https://gsap.com/showcase/) | High-end production web motion | You are exploring scroll storytelling or layered timelines. |
| [HOVERSTAT.ES](https://www.hoverstat.es/) | Alternative interactive websites | You want unconventional navigation, layouts, and editorial motion. |
| [Godly](https://godly.design/) | Broad modern design inspiration | You want to browse before narrowing the animation category. |

See the skill's [website guide](skills/animation-reference/references/websites.md) for routing notes and useful filters.

## Install the skill

From this repository's root:

```bash
mkdir -p ~/.codex/skills
cp -R skills/animation-reference ~/.codex/skills/
```

Restart Codex if the skill does not appear immediately.

## Use the skill

Invoke it explicitly:

```text
$animation-reference I want a product card to expand into a full-screen detail page, but I do not know what that animation is called.
```

You can also attach a screenshot, GIF, screen recording, prototype, or direct reference URL. The skill will identify likely names, find close references, and produce a motion spec containing trigger, state changes, timing, easing or spring behavior, interruption, exit, reduced-motion fallback, and implementation fit.

To review an existing project without changing it:

```text
$animation-reference Inspect this project and recommend animations for its current components. Base every suggestion on the existing stack and source files. Do not implement.
```

In project-aware mode, the skill first inspects the framework, component hierarchy, interactive states, animation dependencies, styling conventions, and rendered behavior when available. It then returns prioritized recommendations tied to specific components and files, plus shared motion tokens, reduced-motion behavior, and ideas that should remain static.

## Repository structure

```text
awesome-animations/
├── README.md
├── README.zh-CN.md
├── LICENSE
└── skills/
    └── animation-reference/
        ├── SKILL.md
        ├── agents/openai.yaml
        └── references/
            ├── motion-vocabulary.md
            ├── project-review.md
            └── websites.md
```

## Contributing

Suggestions are welcome. A useful addition should have a stable direct URL, a clear motion-related purpose, and a short explanation of when it is more useful than the existing sources.

Links were last reviewed on 2026-08-26. Features, availability, and pricing may change.

## License

[MIT](LICENSE)
