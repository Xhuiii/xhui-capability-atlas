# Entry Map v1 / 统一入口说明 v1

本文档是 Tina 以后打开 `xhui-capability-atlas` 仓库时的统一入口说明，用来判断不同工具分别适合做什么、什么内容应该发给谁，以及每次使用 Codex App 后如何检查变更。

这个仓库的默认原则是：Codex App 负责理解和生成，Terminal 负责机械命令，GitHub 负责远程事实核对，Hermes 和 Google AI Studio 作为未来入口暂时不承担当前主线执行。

---

## 一、四个主要入口 / Main Entry Points

### 1. Codex App / 自然语言任务入口

Codex App 是自然语言任务入口。

适合用来：

- 创建 drafts / docs 文件
- 修改草稿
- 总结 README
- 整理 workflow
- 基于已有 drafts 生成新草稿
- 检查仓库结构
- 解释当前项目定义
- 协助拆分 GitHub Issue

使用 Codex App 时，可以直接用中文描述目标和边界，例如：

- 不要修改 README.md
- 不要修改 AGENTS.md
- 不要 commit
- 不要 push
- 只创建或修改某个指定文件

### 2. Terminal / 机械命令入口

Terminal 是机械命令入口。

适合执行明确、短小、确定的命令，例如：

- 查看 git 状态
- 查看 diff
- 添加文件
- 提交 commit
- 推送 push
- 打开目录
- 打开应用

Terminal 不适合接收自然语言写作任务，也不适合接收大段中文需求。

### 3. GitHub / 远程事实源

GitHub 是远程事实源。

适合用来看：

- README
- AGENTS
- drafts
- docs
- Issues
- commit history / 提交历史
- 已经 push 到远程的真实版本

GitHub 用于核对远程状态，不替代本地执行，也不保存秘密信息。

### 4. Hermes / 未来消息入口

Hermes 是未来消息入口。

后续可以用于：

- Discord 消息接入
- 想法捕获 / Idea capture
- P0-P5 初步分类
- GitHub Issue 分流
- 每日行动建议

当前阶段，Hermes 暂不直接操作仓库。

### 5. Google AI Studio / 未来 AI 原型实验入口

Google AI Studio 是未来 AI 原型实验入口。

它主要服务于 P2 `AI Product Lab / AI 产品实验池`，适合未来做：

- AI 产品原型
- Prompt 实验
- 多模态 Demo
- 小工具验证
- P2 产品想法测试

它不是当前主线执行入口。当前仓库主线仍以 P0 / P1 和 Codex App 协作为主。

---

## 二、什么内容应该发给 Codex App / Send to Codex App

适合发给 Codex App 的内容，是需要理解、判断、整理、写作或修改文件的任务。

例如：

- 请创建某个文件。
- 请总结 README。
- 请整理 workflow。
- 请基于 drafts 生成草稿。
- 请检查仓库结构。
- 请根据 README 和 AGENTS 总结当前规则。
- 请把某个想法整理成 What-if 表达卡。
- 请只修改指定文件。
- 请不要修改 README。
- 请不要修改 AGENTS。
- 请不要 commit。
- 请不要 push。

推荐写法：

```text
请创建 drafts/example.md。

要求：
1. 不要修改 README.md；
2. 不要修改 AGENTS.md；
3. 不要 commit；
4. 不要 push；
5. 只创建或修改这个文件；
6. 用中文为主，中英文关键词并列。
```

---

## 三、什么内容应该发给 Terminal / Send to Terminal

Terminal 只适合执行明确命令。

常用命令：

```bash
cd ~/AIProjects/xhui-capability-atlas
git status
git diff
git add
git commit
git push
open .
open /Applications/Codex.app
```

更具体的常用检查命令：

```bash
git status --short
git diff -- README.md AGENTS.md
git diff -- docs/entry-map-v1.md
```

Terminal 的角色是执行命令，不负责理解大段任务说明。

---

## 四、什么内容不能发给 Terminal / Do Not Send to Terminal

不要把这些内容发给 Terminal：

- 自然语言任务
- 大段中文需求
- 给 Codex 的写作指令
- 项目构思长文
- README 改写要求
- What-if 表达卡生成要求
- workflow 整理要求
- token
- API key
- `auth.json` 内容
- `.env` 内容
- 任何凭据或秘密信息

尤其不要在 Terminal 里粘贴：

```text
~/.codex/auth.json
~/.hermes/.env
token
API key
private key
password
```

Terminal 可以执行命令，但不应该成为秘密信息或自然语言任务的输入框。

---

## 五、每次使用 Codex 后的标准检查流程 / Standard Review Flow

每次 Codex App 修改文件后，回到 Terminal 做标准检查。

推荐流程：

```bash
cd ~/AIProjects/xhui-capability-atlas
git status
git diff
```

检查确认：

- 只改了预期文件
- 没有修改 README.md
- 没有修改 AGENTS.md
- 没有写入 token、API key、auth file、`.env` 或秘密信息
- 没有混入无关文件
- 草稿内容符合当前 P0-P5 项目定义

确认无误后，再执行：

```bash
git add
git commit
git push
```

更安全的提交方式是只添加预期文件，例如：

```bash
git add docs/entry-map-v1.md
git commit -m "Add entry map draft"
git push
```

注意：commit 和 push 都需要用户自己确认后再做。Codex 默认不 commit、不 push。

---

## 六、安全边界 / Safety Boundaries

这个仓库只能保存手动整理、脱敏后的个人项目材料。

禁止写入：

- 公司资料
- 内部项目细节
- 真实同事姓名
- 内部组织信息
- token
- API key
- `~/.codex/auth.json`
- `~/.hermes/.env`
- `.env`
- auth file
- 私人凭据
- 敏感个人文件
- 敏感健康信息
- 未脱敏材料

使用 Codex 时还要遵守：

- 不让 Codex 访问公司目录
- 不让 Codex 读取公司文件
- 不让 Codex 处理 confidential work materials
- 不让 Codex 随意修改 README
- 不让 Codex 随意修改 AGENTS
- 不把 secrets 粘贴到聊天里
- 不把 secrets 写进 drafts、docs、README、Issues 或 commit

README 规则：

- README 是当前项目定义的 baseline / 基线
- 后续不要删除或改写 README 现有解释
- 后续 README 更新只追加到 `Update Log / 更新记录`
- 如果旧想法不准确，标记为 `Deprecated / 已废弃` 或 `Refined / 已修正`
- 敏感信息永远不能写进 README 或 Update Log

---

## 七、快速判断 / Quick Decision

当不知道该用哪个入口时，可以这样判断：

- 要“写、整理、总结、生成、修改草稿” -> 用 Codex App
- 要“看状态、看差异、提交、推送、打开目录” -> 用 Terminal
- 要“核对远程版本、Issue、提交历史” -> 用 GitHub
- 要“未来从 Discord 捕获想法并分流” -> 用 Hermes
- 要“未来做 AI 原型实验” -> 用 Google AI Studio

最重要的默认动作：

```text
写作和整理交给 Codex App。
机械命令交给 Terminal。
远程事实回 GitHub 核对。
秘密信息哪里都不要写。
```
