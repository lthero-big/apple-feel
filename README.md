# apple-feel

一个 Agent Skill：把 Apple 式的克制配色与设计感，变成做 UI 时可以直接套用的规则。

做网页 UI、主题、卡片或组件复刻时，想要 Apple 式的克制配色与设计感（灰阶层次 + 单点强调色、留白、字重对比、克制动效）时使用；也用于评审一个界面「够不够 Apple」。它借的是 Apple 的**做法**——内容优先、层次靠灰阶和字重、颜色只用来表达含义——而不是照抄它的界面或系统色。规则全文见 [SKILL.md](./SKILL.md)。

## 内容概览

1. **配色：灰阶打底，单点强调** — 先定 4–5 级中性灰分层；只选一个强调色、只给它一个含义，面积控制在一屏 5% 以内；深浅两套按语义角色映射，正文对比度至少 4.5:1，状态不能只靠颜色区分。
2. **版式与字体** — 字号字重拉开反差，数字一律等宽（tabular-nums），间距按 4/8 网格，圆角同心，分隔优先用留白。
3. **材质与层次** — 浮层用白或近白实色配大而淡的阴影，毛玻璃只给真正浮在内容之上的工具条；一屏最多三层。
4. **动效** — 弹簧曲线，200–400ms、小回弹；动效必须表达状态变化，并遵守 `prefers-reduced-motion`。
5. **评审清单** — 六条可勾选的检查项，交付前逐项过。

## 安装

把本仓库克隆到你的 Agent 的 skills 目录即可。以 Claude Code 为例：

```bash
git clone https://github.com/lthero-big/apple-feel.git ~/.claude/skills/apple-feel
```

其他兼容 Agent Skills 规范的工具同理：把 `apple-feel` 文件夹（含 `SKILL.md`）放进它读取 skills 的目录。

## 使用

装好后无需配置：在做网页 UI、主题、卡片或组件复刻时，Agent 会按 skill 描述自动触发；也可以在对话里直接点名，例如「用 apple-feel 评审一下这个界面够不够 Apple」。

## 博客文章

发布说明与全文：[《apple-feel：一个讲 Apple 式配色与设计感的 skill》](https://blog.lthero.com/posts/apple-feel-skill)

## 参考

- Apple 人机界面指南（官方）：https://developer.apple.com/design/human-interface-guidelines/
- 更细的规范版 skill：https://github.com/justinwetch/HIGAgentSkills（全量）、apple-hig-color（只讲配色）

## License

MIT，见 [LICENSE](./LICENSE)。
