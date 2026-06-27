# P0 System Architecture / P0 系统架构

本文档是基于 `README.md` 的 P0 System Architecture 草稿，用于统一当前信息架构，避免 `Career Layer`、`Life RPG Layer`、`What-if Layer`、`AI Product Lab Layer`、`Content Layer`、`Studio Layer` 之间出现重复或冲突定义。

重要边界：

- `README.md` 是唯一系统定义源 / Single source of truth。
- `docs/` 是 UI 层 / UI layer，用于放置可打开、可体验的页面与原型。
- `drafts/` 是实验层 / Experiment layer，用于承载结构草稿、卡片草稿和架构草稿。
- `issues` 是执行层 / Execution layer，用于任务拆解、状态追踪和推进。
- 本文档不替代 README，只把 README 中已有定义整理成当前可执行的信息架构。

---

## 1. P0 总定义 / Overall Definition

P0 = `Personal Skill Simulator Atlas / 个人技能模拟器地图`。

P0 不是普通作品集，也不是单一职业总结。它是一个可持续生长、可交互、可视化的个人技能模拟器系统，用于收纳真实项目、能力证据、方法论、复盘、what-if 设定、创意实验、产品想象、内容表达、审美实验和未来方向。

P0 的核心问题不是“我有哪些文档”，而是：

- 我已经通过真实项目证明了哪些能力？
- 哪些能力可以从证据、项目、指标和产出中被看见？
- 哪些潜在能力可以通过 what-if、产品实验、内容表达和生活模拟显影？
- 这些能力如何持续更新、互相连接，并最终成为一张动态地图？

---

## 2. 唯一真相结构 / Single Architecture

当前 P0 被统一为 6 个系统层：

| Layer | 中文名称 | 状态 | 作用 | 主要对应 |
| --- | --- | --- | --- | --- |
| Career Layer | 职业能力证据层 | Active | 整理真实项目、能力证据、项目产出、指标变化、奖项激励和迁移方向 | #7 |
| Life RPG Layer | 生活模拟层 | Building | 把自我成长、状态、习惯、生活行动和长期角色成长转化为模拟系统 | #14 |
| What-if Layer | 想象表达层 | Building | 收纳 what-if 设定、思辨设计、魔法版脑洞和潜在能力模拟 | README What-if Cards |
| AI Product Lab Layer | AI 产品实验层 | Planned | 承载 AI-native 产品、小工具、互动系统、Agent 工作流和原型实验 | P2 / #12 |
| Content Layer | 内容与个人品牌层 | Planned | 承载内容选题、表达风格、个人叙事、审美身份和公众可见度 | P3 / #13 |
| Studio Layer | 设计师的店与审美实验层 | Planned | 承载设计师的店、审美实验、数字产品、商业想象和未来产品化 | P4 |

这 6 层共同组成 P0。任何一个单层都不能被写成 P0 的全部。

---

## 3. #7 与 #14 的关系 / Issue Relationship

### #7 = Career Capability Evidence System

#7 的定位是 `Career Capability Evidence System / 职业能力证据系统`。

它负责把 2022-2026 的真实职业经历整理为可视化首页概念，包括：

- 年度成长线 / Timeline
- 项目簇 / Project clusters
- 能力节点 / Capability nodes
- 证据类型 / Evidence types
- 可见产出 / Visible outputs
- 影响级别 / Impact level
- 迁移方向 / Transfer directions

#7 不等于 P0 全部，只是 P0 中最适合优先可视化的 `Career Layer`。

### #14 = Life Simulation System

#14 的定位是 `Life Simulation System / 生活模拟系统`。

它从 README 中的 What-if Expression Cards 延展出来，但不应该只被理解成“灵感卡片”。它更接近 P0 中关于生活、状态、角色成长、行动节奏和自我模拟的系统入口。

#14 可以包含：

- What-if 表达卡 / What-if expression cards
- 情绪、能量、习惯和行动状态 / State variables
- 生活角色成长 / Life role progression
- 技能模拟场景 / Skill simulation scenarios
- 自我成长和长期执行条件 / Self-growth conditions

#14 不替代 Career Layer，也不和 #7 竞争。它负责让 P0 不只是职业证据系统，而是更完整的个人技能模拟器。

### P0 = Overall System

P0 是 overall system / 总系统。

#7 和 #14 都是 P0 的子系统：

```text
P0 Personal Skill Simulator Atlas
  -> #7 Career Capability Evidence System
  -> #14 Life Simulation System
  -> What-if Layer
  -> AI Product Lab Layer
  -> Content Layer
  -> Studio Layer
```

---

## 4. 文件与层级边界 / File Boundaries

### README.md

系统定义源。只通过 `Update Log / 更新记录` 追加重大理解变化。

### docs/

UI 层。用于放可打开的可视化页面和交互原型。

当前建议：

- `docs/index.html`：P0 System Game Hub / P0 系统游戏化入口首页。
- `docs/p0-career-capability-map-v0.html`：Career Layer 的 v0 可视化原型。

### drafts/

实验层。用于放结构草稿、数据草稿和探索性卡片。

当前建议：

- `drafts/project-cards-v0.md`：Career Layer 年度项目成长卡片。
- `drafts/capability-cards-v0.md`：Career Layer 职业能力成长索引。
- `drafts/what-if-expression-cards-v0.md`：What-if / Life Simulation 方向的表达卡草稿。
- `drafts/p0-system-architecture.md`：本架构整理草稿。
- `drafts/execution-loop-v1.md`、`drafts/p0-execution-filter.md`：P1 / 执行辅助，不是 P0 内容主体。

### issues

执行层。用于记录任务，不存放秘密信息，不作为系统定义源。

---

## 5. 冲突修复规则 / Conflict Rules

为避免后续冲突，统一采用以下规则：

1. 不把 `Career Layer` 写成 P0 全部。
2. 不把 `Life RPG Layer` 写成 What-if 的全部，也不把 What-if 写成随机幻想。
3. 不把 `docs/` 写成草稿仓库；docs 只放 UI / prototype / visual pages。
4. 不把 `drafts/` 写成最终系统定义；drafts 只放实验材料。
5. 不通过新文档覆盖 README；README 永远是系统定义源。
6. 不重复建 issue；已有 #7 和 #14 分别承载 Career Layer 和 Life Simulation System。

---

## 6. 首页 UX 目标 / Home UX Goal

`docs/index.html` 应该是 `P0 System Game Hub / P0 系统游戏化入口`，而不是文件目录页。

它需要帮助用户快速理解：

- P0 是一个总系统。
- 当前 Active 的是 Career Layer。
- Life RPG / What-if 正在 Building。
- AI Product Lab / Content / Studio 是 Planned。
- 每一层都是一个可进入、可成长、可解锁的系统模块。

首页的交互应该像“进入系统地图”，而不是“点击文档列表”。

---

## 7. 当前状态 / Current State

| Layer | Status | 当前产物 |
| --- | --- | --- |
| Career Layer | Active | `docs/p0-career-capability-map-v0.html`、`drafts/project-cards-v0.md`、`drafts/capability-cards-v0.md` |
| Life RPG Layer | Building | `drafts/what-if-expression-cards-v0.md` 可作为早期输入 |
| What-if Layer | Building | `drafts/what-if-expression-cards-v0.md` |
| AI Product Lab Layer | Planned | 等待 P2 实验启动 |
| Content Layer | Planned | 等待 P3 启动 |
| Studio Layer | Planned | 暂存于 P4 |

---

## 8. 下一步 / Next Step

优先顺序：

1. 完成 `docs/index.html` 的 P0 System Game Hub 首页。
2. 保持 `docs/p0-career-capability-map-v0.html` 作为 Career Layer 入口。
3. 后续再为 #14 设计 Life Simulation System 的 v0 原型。
4. 暂不扩写 P2/P3/P4，避免系统过早膨胀。
