# Awesome Animations

[English](README.md)

一个聚焦动画参考的资源仓库，并附带可安装的 Codex Skill。它既能解决 **“我脑海里有动画效果，但不知道该怎么准确形容”**，也能检查现有项目，基于真实组件给出动画建议。

## 仓库内容

- 精选 UI 动效、产品流程、CSS 动画和实验性网页动画网站。
- 可安装的 Codex [`animation-reference`](skills/animation-reference/SKILL.md) Skill。
- 实用的[动画术语表](skills/animation-reference/references/motion-vocabulary.md)，涵盖触发方式、动画名称、时间、物理感和无障碍要求。
- [项目感知审阅指南](skills/animation-reference/references/project-review.md)，用于生成有代码和组件依据的动画建议。

## 精选网站

| 网站 | 最适合 | 什么时候先看它 |
| --- | --- | --- |
| [60fps](https://60fps.design/) | UI 动效和微交互 | 脑中有 App 动效，但不知道它叫什么。 |
| [Motion Examples](https://motion.dev/examples) | 可运行的 React、JavaScript、Vue 动画 | 想知道准确技术名称，并准备进入代码实现。 |
| [Animista](https://animista.net/) | 可调参数的 CSS 动画预设 | 需要轻量的进入、退出或强调动画。 |
| [1human](https://reels.1human.tech/) | 带有制作方法、作者署名和逐项复用权限的动效参考 | 想在现有渲染流程中比较标题揭示或加载状态的节奏。 |
| [Mobbin](https://mobbin.com/) | 真实移动端和网页产品流程 | 想研究已经上线的产品如何处理某个交互。 |
| [Page Flows](https://pageflows.com/) | 真实用户流程录像 | 操作顺序和动画节奏比单张界面更重要。 |
| [Codrops](https://tympanus.net/codrops/) | 创意 Demo 和教程 | 想找文字、页面转场、鼠标、WebGL 或 Three.js 动效。 |
| [GSAP Showcase](https://gsap.com/showcase/) | 高完成度网页动画 | 想探索滚动叙事、固定滚动或多层时间线。 |
| [HOVERSTAT.ES](https://www.hoverstat.es/) | 另类互动网站 | 想找非常规导航、布局和编辑型动效。 |
| [Godly](https://godly.design/) | 综合现代设计灵感 | 还不确定动画类别，想先广泛浏览。 |

更详细的选择方式和标签说明见 Skill 内的[网站指南](skills/animation-reference/references/websites.md)。

## 安装 Skill

在仓库根目录运行：

```bash
mkdir -p ~/.codex/skills
cp -R skills/animation-reference ~/.codex/skills/
```

如果 Skill 没有立即出现，请重启 Codex。

## 使用 Skill

可以显式调用：

```text
$animation-reference 我想让商品卡片展开成全屏详情页，但不知道这种动画叫什么。
```

也可以直接提供截图、GIF、录屏、原型或参考链接。Skill 会帮你找到可能的准确名称和相似案例，并整理出包含以下信息的动画规格：触发方式、状态变化、持续时间、缓动或弹簧参数、中断和退出行为、弱化动画方案，以及适合当前技术栈的实现方法。

如果要审阅现有项目，但暂时不修改代码：

```text
$animation-reference 检查当前项目，基于现有组件提供动画建议。每项建议必须符合当前技术栈并指向具体源码，不要实现。
```

在项目感知模式中，Skill 会先检查框架、组件层级、交互状态、已有动画依赖、样式规范，并在条件允许时查看实际渲染效果；之后再输出与具体组件和文件绑定的优先级建议，同时给出全局动画 token、弱化动画方案，以及应该保持静态的设计。

## 仓库结构

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

## 参与贡献

欢迎补充资源。一个合适的新网站应该有稳定的直接链接、明确的动画用途，并简要说明它在哪类需求下比现有网站更有价值。

以上链接最后核对于 2026-08-26。网站功能、访问方式和价格可能会发生变化。

## 许可证

[MIT](LICENSE)
