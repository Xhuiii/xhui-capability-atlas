# Living Personal OS v0 / 活的个人操作系统 v0

Living Personal OS 是让 P0 持续生长的动态机制。它不是新的作品集页面，也不替代 P0；它负责把灵感、证据、复盘和模拟输入持续整理成 P0 可以吸收的种子。

一句话定义：

`Human Spark / 我的灵感` + `AI Scout / AI 主动收集与整理的素材` + `Reality Evidence / 现实项目与能力证据` + `Simulation / what-if 转译` = `Living Personal OS / 活的个人操作系统`

---

## 1. 系统定位 / System Positioning

P0 是 `Personal Skill Simulator Atlas / 个人技能模拟器地图`。

Living Personal OS 是 P0 的生长机制 / growth mechanism。它让 P0 不只是静态页面，而是可以持续接收新想法、新证据、新复盘、新状态和新实验。

Living Personal OS 不替代：

- P0 总系统
- Career District / 职业能力区
- Simulation Field / 表达场
- What-if Islands / 脑洞奇想岛
- AI Lab / AI 实验室
- Content Tower / 内容表达塔
- Studio Market / 设计师工坊

它只负责把输入变成可以被筛选、转译和更新的 seeds / 种子。

---

## 2. 数据来源 / Data Sources

### Human Spark / 我的灵感

我自己突然想到的脑洞、观察、产品想法、内容想法、比喻、场景和问题意识。

### AI Scout / AI 灵感侦察员

AI 主动帮我收集或整理的灵感素材，例如：

- 设计趋势 / design trends
- 产品模式 / product patterns
- AI 工具 / AI tools
- 交互案例 / interaction cases
- 内容题材 / content topics

v0 不接真实外部 API，不做自动爬虫，只先建立静态机制。

### Reality Evidence / 现实项目与能力证据

来自真实项目、能力卡、项目卡、成果证据、指标变化、奖项激励和可迁移方向。

### Reflection / 复盘与状态

每周复盘、健康状态、创作状态、职业状态、能量变化、执行节奏和长期成长观察。

---

## 3. 数据形态 / Seed Shape

每条 seed 包含：

```js
{
  id: "seed-001",
  title: "情绪天气站",
  source: "human",
  type: "what_if",
  status: "raw",
  visibleSummary: "把情绪状态可视化成天气系统。",
  privateNotes: "placeholder only, do not expose on page",
  linkedLayer: "simulation",
  nextAction: "转成 what-if card",
  safetyNote: "脱敏，无外部来源"
}
```

字段说明：

- `id`：唯一编号
- `title`：标题
- `source`：`human` / `ai_scout` / `reality` / `reflection`
- `type`：`what_if` / `product` / `content` / `career` / `studio` / `system`
- `status`：`raw` / `selected` / `developed` / `archived`
- `visibleSummary`：给网页展示的一句话
- `privateNotes`：只给本地和 AI 看的细节
- `linkedLayer`：`career` / `simulation` / `what-if` / `ai-lab` / `content` / `studio`
- `nextAction`：下一步最小动作
- `safetyNote`：安全说明

---

## 4. 页面展示原则 / Page Display Rule

网页只展示：

- `title`
- `source`
- `type`
- `visibleSummary`
- `linkedLayer`
- `nextAction`

网页不展示：

- `privateNotes`

`privateNotes` 可以留在本地数据中，用于后续整理、AI 辅助分类或人工复盘，但不应该出现在公开页面。

---

## 5. AI Scout 安全规则 / AI Scout Safety Rules

- AI Scout 只能提出素材与链接，不自动发布。
- 重要内容必须人工确认。
- 所有外部素材必须保留 `source`。
- 不收集公司内部信息。
- 不写敏感项目细节。
- 不写真实同事姓名。
- 不把健康数据变成羞耻感或焦虑源。
- 未确认、未脱敏、来源不清的素材不能进入公开页面。

---

## 6. 更新节奏 / Update Rhythm

### daily capture / 每天临时捕捉

快速记录新 seed，不急着判断价值。

### weekly distill / 每周筛选

把 raw seeds 分成 selected、developed 或 archived。

### monthly world update / 每月更新 P0 世界状态

把已经成熟的 seeds 转化为：

- What-if card
- Product experiment
- Content topic
- Career evidence
- Studio idea
- System improvement

---

## 7. 未来自动化 / Future Automation

未来可以接入：

- GitHub Issues
- flomo
- 手动输入表单
- AI trend search
- 本地 seed 管理器

但 v0 只做静态种子和页面展示：

- `data/p0-living-seeds-v0.js`：本地静态 seed 数据
- `docs/inspiration/index.html`：Inspiration Stream 展示页
- `docs/index.html`：首页入口与轻量 preview

---

## 8. v0 边界 / v0 Boundaries

- 不接真实外部 API
- 不自动爬取外部内容
- 不使用 fetch 远程数据
- 不使用 localStorage
- 不使用 cookies
- 不自动发布内容
- 不写公司敏感内容
- 不写内部项目细节
- 不把 privateNotes 展示到网页
