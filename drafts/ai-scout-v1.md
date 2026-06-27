# AI Scout v1 / 灵感巡逻系统

## 定义

AI Scout 是 P0 Living Personal OS 的“灵感巡逻系统”。

它不是自动生成内容工具，也不是自动发布工具。  
它的作用是定期提出灵感素材、观察方向和可转化 seed，帮助 P0 持续生长。

---

## 双输入系统

### Human Spark / 人类灵感

来源于 Tina 自己的想法，包括：

- 突然出现的脑洞
- 产品想法
- 内容选题
- 设计观察
- 情绪化表达
- what-if 设定
- 对未来生活或工作的想象

特点：

- 更个人
- 更跳跃
- 更有情绪和直觉
- 不需要一开始就结构化

---

### AI Scout / AI 灵感巡逻

来源于 AI 帮助整理和提出的灵感建议，包括：

- UX / 产品趋势
- AI 工具变化
- 交互模式
- 内容题材
- 小世界 / 游戏化 / 模拟器参考
- 可转化为 P0 的素材

特点：

- 更结构化
- 更适合归类
- 更适合作为候选 seed
- 需要 Tina 人工判断是否吸收

---

## Seed 字段规则

每条 seed 建议包含：

- title：标题
- source：human / ai_scout
- type：what_if / product / content / career / studio / system
- visibleSummary：公开页面可展示的一句话
- privateNotes：只保留在本地，不公开
- linkedLayer：career / simulation / inspiration / ai-lab / content / studio
- nextAction：下一步动作
- safetyNote：安全边界说明

---

## 关键规则

AI Scout 只能提出建议，不能自动发布。

禁止：

- 自动写入仓库
- 自动修改 data 层
- 自动 commit
- 自动 push
- 使用公司内部信息
- 使用敏感项目细节
- 把外部素材当成原创

必须：

- 人工确认
- 标注来源
- 只使用脱敏内容
- 明确区分 Human Spark 和 AI Scout

---

## 后续可能方向

当前阶段不实现自动化，只记录机制。

未来可以扩展为：

- 每周 AI Scout report
- 每周生成 8-12 条候选 seed
- Tina 选择 2-4 条进入 Inspiration Stream
- 部分 seed 转化为 What-if / AI Lab / Content / Studio
- 长期形成 Living Personal OS 的输入层
