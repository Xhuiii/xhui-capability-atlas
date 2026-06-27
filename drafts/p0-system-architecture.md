# P0 System Architecture / P0 系统架构

本文档基于 `README.md` 整理 P0 的当前信息架构。`README.md` 仍然是唯一系统定义源 / single source of truth；本文只是实验层里的架构草稿，用于统一网页表达和后续原型方向。

---

## 1. 默认视觉模型 / Default Visual Model

P0 的默认视觉模型是：

`Living Pixel Atlas / 小世界地图`

它不是工程 dashboard，不是普通目录页，也不是纯 RPG 打卡页。默认首页应该像一个可以浏览的个人成长世界展：

- `Pixel`：结构、网格、节点、地图、入口、能力场。
- `Felt`：柔软、毛毡、温度、脑洞、灵感、漂浮感。
- `Glow`：状态、活跃区域、已启动能力、可点击路径。

XP / Level / Stats 只属于 `Progress View / 成长数据视图`，是可切换的补充数据，不是 P0 的默认表达。

---

## 2. P0 总定义 / Overall Definition

P0 = `Personal Skill Simulator Atlas / 个人技能模拟器地图`。

P0 是一个长期生长的小世界系统，用于收纳：

- 真实项目和能力证据 / proven capability evidence
- what-if 脑洞和想象表达 / what-if expression
- AI 产品实验 / AI product experiments
- 内容表达和个人品牌 / content and personal brand
- 生活成长和状态变化 / life growth and state changes
- 审美实验、设计师工坊和未来商业可能 / studio and future productization

任何单一层都不能替代 P0 全部。

---

## 3. 当前系统层 / Current Layers

| Layer | 首页区域名 | 状态 | 作用 | 对应 |
| --- | --- | --- | --- | --- |
| Career Layer | Career District / 现实能力场 | Active | 真实项目、能力证据、项目痕迹和迁移方向 | #7 |
| Simulation Expression Mode | Simulation Field / 表达场 | Building | 把现实能力、what-if 脑洞、灵感和成长状态转译成可玩的世界视角 | #14 |
| What-if Layer | What-if Islands / 脑洞奇想岛 | Planned | 收纳 if 设定、隐喻、另类用户和潜在能力模拟 | README What-if Cards |
| AI Product Lab Layer | AI Lab / 实验室 | Planned | AI-native 工作流、产品原型、Agent 和灵感整理工具 | P2 / #12 |
| Content Layer | Content Tower / 表达塔 | Planned | 内容选题、个人叙事、审美身份和公众可见度 | P3 / #13 |
| Studio Layer | Studio Market / 设计师工坊 | Backlog | 审美实验、数字产品、商业想象和未来个人 IP 资产 | P4 |

---

## 4. #7 与 #14 的关系 / #7 and #14

### #7 = Career District / Career Capability Evidence System

#7 是 P0 的 `Career District / 现实能力场`，也可以称为 `Career Capability Evidence System / 职业能力证据系统`。

它负责把 2022-2026 的真实项目经历整理成可浏览的能力证据：

- 年度成长路径
- 能力节点
- 项目证据
- 设计痕迹
- 迁移方向

#7 不是简历页，也不是 P0 全部。它是小世界里最先形成的现实能力区域。

### #14 = Simulation Expression Mode / What-if Simulation Field

#14 不定义为“生活世界”，也不只是 RPG 打卡面板。

#14 是 `Simulation Expression Mode / What-if Simulation Field`。它既可以作为 P0 的一个 layer，也可以作为 P0 的另一种表达方式：把 P0 里的当前技能、what-if 脑洞、灵感素材、成长状态和未来自我，转译成一种可玩的世界视角。

#14 可以包含：

- 当前技能的另一种表达 / current skill avatar
- what-if 脑洞可视化 / floating idea cards
- 灵感素材聚类 / inspiration clustering
- 未来自我或未来世界模拟 / future self and world simulation
- 项目、能力、脑洞之间的转译关系 / translation map

---

## 5. Inspiration Stream / 灵感流

`Inspiration Stream / 灵感流` 是 P0 的输入机制之一，服务于：

- What-if Layer
- Simulation Expression Mode
- AI Product Lab Layer
- Content Layer
- Studio Layer

它包含两种来源：

1. `Human Spark / 我自己迸发的脑洞`
   - 突然出现的想法、隐喻、观察、设定和创意冲动。

2. `AI Scout / AI 灵感侦察员`
   - 未来由 AI 主动收集、整理和提示的灵感素材。
   - 这是未来能力，不是当前默认自动行为。
   - 所有外部来源必须标注 `source`。
   - 所有材料必须经过安全检查、脱敏判断和人工确认。
   - 未确认的 AI Scout 素材不能直接进入公开页面或核心数据。

---

## 6. Living Personal OS / 活的个人操作系统

`Living Personal OS / 活的个人操作系统` 是 P0 的动态生长机制，不替代 P0，而是让 P0 持续更新。

它的 v0 机制是：

```text
Human Spark / 我的灵感
  + AI Scout / AI 主动收集与整理的素材
  + Reality Evidence / 现实项目与能力证据
  + Reflection / 复盘与状态
  + Simulation / what-if 转译
  = Living Personal OS / 活的个人操作系统
```

当前 v0 文件边界：

- `drafts/living-personal-os-v0.md`：机制定义、数据形态、安全规则和更新节奏。
- `data/p0-living-seeds-v0.js`：v0 静态 seed 数据，不通过 fetch 读取，不连接外部 API。
- `docs/inspiration/index.html`：Inspiration Stream 的公开展示层。
- `docs/index.html`：Living Pixel Atlas 首页中的灵感流 preview 和入口。

seed 数据里可以保留 `privateNotes`，但网页公开展示层不展示 `privateNotes`。网页只展示 `title`、`source`、`type`、`visibleSummary`、`linkedLayer` 和 `nextAction`。

AI Scout 是未来能力。它可以主动收集灵感素材，但所有外部来源必须标注 `source`，所有转化必须经过人工确认，未确认素材不能直接进入 P0 世界或公开页面。

---

## 7. 三层信息策略 / Three-layer Information Strategy

网页面向人阅读，不是给工程系统解析。因此采用三层信息策略：

### Layer 1: Visible

首屏和默认视图只展示 10% 重点信息：

- 这是什么
- 这个人是谁
- 哪些世界区域已经启动
- 可以点哪里继续看
- 当前最重要的成长、能力或脑洞是什么

### Layer 2: Expandable

通过 hover、click 或切换视图展示：

- 项目证据
- 年份
- 关键词
- 能力来源
- 未来迁移方向

### Layer 3: Local Only

完整架构、系统关系、字段定义和长期规则留在本地 drafts，不全部塞进网页。

---

## 8. 文件边界 / File Boundaries

- `README.md`：唯一系统定义源。
- `docs/`：UI 层，只放可浏览页面和交互原型。
- `drafts/`：实验层，放架构、草稿、卡片和数据结构。
- `issues`：执行层，用于任务拆解和推进，不作为系统定义源。

当前网页目标：

- `docs/index.html`：Living Pixel Atlas 首页。
- `docs/inspiration/index.html`：Inspiration Stream / 灵感流公开展示层。
- `docs/p0-career-capability-map-v0.html`：Career District 的早期可视化原型。
- `data/p0-living-seeds-v0.js`：Living Personal OS v0 的静态 seed 数据。
- 未来若创建 `docs/career/index.html`：应表达为 `Career District / Pixel Capability Field`。
- 未来若创建 `docs/life-rpg/index.html`：应表达为 `Simulation Expression Mode / What-if Simulation Field`。

---

## 9. UX 验收方向 / UX Acceptance Direction

首页应像一个“个人成长世界展”，而不是：

- 工程 dashboard
- 密集系统说明
- 纯 RPG 打卡页
- 简历页
- 文件目录页

Career 页面应像 `Pixel Capability Field / 像素能力场`，重点是能力节点、成长路径、证据 chips 和迁移桥。

#14 页面应像 `Simulation Expression Mode / What-if Simulation Field`，重点是当前技能表达形态、floating idea cards、translation map 和未来世界预览。
