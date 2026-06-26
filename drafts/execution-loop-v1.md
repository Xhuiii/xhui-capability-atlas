# Execution Loop v1 / 执行闭环 v1

本文档是 `xhui-capability-atlas` 的执行流程草稿，用来说明这个仓库未来如何把一个松散想法，逐步变成可追踪、可执行、可检查、可沉淀的个人资产。

这个闭环服务于 P0 `Personal Skill Simulator Atlas / 个人技能模拟器地图`，同时允许 P1-P5 持续向 P0 输入内容。

---

## 1. Idea Capture / 想法捕获

入口可以很轻：一句话、一个灵感、一个观察、一个产品念头、一个内容选题、一次复盘、一个 What-if 设定，或一个待整理的真实项目经验。

这一层不急着判断价值，重点是先接住。

最小记录内容：

- 原始想法 / Raw idea
- 来源 / Source
- 时间 / Date
- 直觉标签 / Initial tags
- 是否含敏感信息 / Safety check

安全原则：

- 不记录公司资料
- 不记录内部项目细节
- 不记录真实同事姓名
- 不记录 token、API key、auth file、`.env` 或任何凭据
- 不记录未脱敏材料

---

## 2. P0-P5 Classification / P0-P5 分类

被捕获的想法需要先判断属于哪个项目域，或会向哪个项目域输入。

- P0 / Personal Skill Simulator Atlas：能力地图、技能模拟、What-if 表达卡、能力卡、项目卡、证据链、时间线
- P1 / Agent Workbench：想法分流、任务管理、复盘流程、自动化辅助、项目经理 Agent 工作流
- P2 / AI Product Lab：AI 产品、小工具、游戏概念、互动叙事、沙盒系统、产品实验
- P3 / Content and Personal Brand：内容选题、表达风格、个人品牌、视觉叙事、公开表达
- P4 / Designer Shop Lab：审美实验、商业想象、数字产品、设计师的店
- P5 / Exercise, Health, and Self-Growth：运动、能量、习惯、状态、自我成长记录

分类不是为了限制想法，而是为了判断它如何进入 P0。

一个想法可以同时关联多个域。例如，一个“情绪天气站”既可能属于 P0 的 What-if 表达卡，也可能连接 P2 的产品实验、P3 的内容表达和 P5 的状态记录。

---

## 3. GitHub Issue / GitHub 任务

当一个想法进入可执行状态，就可以变成 GitHub Issue。

Issue 的作用是任务追踪，不是保存秘密信息，也不是替代 README 的项目定义。

适合进入 Issue 的内容：

- 明确的小任务
- 可检查的产物
- 草稿文件
- 数据结构设计
- 原型实验
- 安全规则
- 路线图或优先级整理

Issue 最好包含：

- 背景 / Context
- 目标 / Goal
- 范围 / Scope
- 产物 / Output
- 不做什么 / Non-goals
- 安全边界 / Safety
- 检查方式 / Review method

---

## 4. Codex Execution / Codex 执行

Codex 负责把 Issue 或用户明确给出的任务变成小而可检查的变更。

执行原则：

- 先读相关上下文
- 修改前说明计划
- 优先小改动
- 只改任务要求范围内的文件
- 不碰 README 和 AGENTS，除非用户明确要求
- 不读取或写入仓库外文件，除非用户明确批准
- 不打印、不保存、不提交任何秘密信息

Codex 的理想产物不是一次性做完全部系统，而是每次推进一个清晰的小块。

---

## 5. User Diff Review / 用户检查 diff

Codex 完成变更后，用户需要检查 diff。

检查重点：

- 是否只修改了预期文件
- 是否没有误改 README 或 AGENTS
- 是否没有写入敏感信息
- 是否符合 P0-P5 的项目定义
- 是否足够小，方便 review
- 是否需要补充、删减或改名

常用查看方式：

```bash
git diff
```

如果只想看某个文件：

```bash
git diff -- drafts/execution-loop-v1.md
```

---

## 6. Commit and Push / 提交与推送

只有在用户确认 diff 后，才进入 commit。

提交前需要：

- 用户确认变更可以提交
- Codex 展示或总结 diff
- 确认没有敏感信息
- 确认 commit message

推送需要额外明确确认。默认不 push。

推荐节奏：

- 小任务，小 commit
- 每个 commit 对应一个明确目的
- 不把无关文件混入同一个 commit

---

## 7. Update Log When Needed / 必要时追加更新记录

不是每次执行都需要更新 README。

只有当变更影响项目定义、定位、命名、路线图、核心规则或阶段性理解时，才需要考虑追加到 `Update Log / 更新记录`。

README 更新原则：

- 不删除现有解释
- 不直接覆盖重大定位变化
- 新理解优先追加到 `Update Log / 更新记录`
- 旧理解若不再准确，标记为 `Deprecated / 已废弃` 或 `Refined / 已修正`
- 敏感信息永远不能写入 README 或 Update Log

---

## 8. Full Loop / 完整闭环

完整流程：

```text
Idea Capture / 想法捕获
  -> P0-P5 Classification / P0-P5 分类
  -> GitHub Issue / GitHub 任务
  -> Codex Execution / Codex 执行
  -> User Diff Review / 用户检查 diff
  -> Commit and Push / 提交与推送
  -> Update Log When Needed / 必要时追加更新记录
```

这个闭环的目标不是制造更多任务，而是让想法可以被接住、被筛选、被执行、被检查，并最终沉淀进 P0 的个人技能模拟器地图。
