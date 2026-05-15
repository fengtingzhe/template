# AI Game Demo Project Template

本仓库是一套通用的 AI 辅助游戏 Demo 开发模板。

它用于帮助策划、制作人和 AI 工具快速搭建一个可试玩、可展示、可验证的游戏原型项目。

当前工作流不以“让 AI 全自动开发完整复杂商业游戏”为目标，而是以“借助 AI 快速搭建高表达力 Demo”为目标。

Demo 阶段的重点不是完整，而是充分展示。

---

# 1. 项目基本信息

## 项目名称

待填写。

## 游戏一句话描述

待填写。

示例：

> 一款【目标平台】上的【游戏类型】Demo，玩家通过【核心操作】完成【核心目标】，用于验证【核心玩法 / 界面流程 / 表现方向 / 数值雏形】是否成立。

---

# 2. 项目目录结构

```text
ProjectName/
├── README.md
├── PROJECT_STATUS.md
├── DESIGN_HUB/
├── AI_RULES/
├── AI_TASKS/
├── WEB_DEMO/
├── UNITY_SOURCE/
├── UNITY_PROJECT/
├── Docs/
├── Builds/
└── Temp/
```

核心原则：

```text
PROJECT_STATUS 是当前状态仪表盘；
DESIGN_HUB 管方向；
AI_RULES 管 AI；
AI_TASKS 管执行；
WEB_DEMO 管 Web 原型及其 Data / Assets / Tools / Tests；
UNITY_SOURCE 管 Unity 源码学习 / 改造及其项目内部文件；
UNITY_PROJECT 管未来自建 Unity 原型及其项目内部文件；
Docs 管跨阶段资料和分析文档；
Builds 管构建输出；
Temp 管临时文件。
```

根目录不再默认创建 `Scenes/`、`Scripts/`、`Data/`、`Assets/`、`Tools/`、`Tests/` 等具体工程目录。对应文件应放在当前阶段的工作区内部。

---

# 3. 新项目启动流程

每个新项目建议开启一个 ChatGPT 项目专属对话。

新对话启动后，ChatGPT 应先读取 GitHub 仓库中的模板文件，尤其是：

```text
PROJECT_STATUS.md
DESIGN_HUB/00_PROJECT_CANVAS.md
DESIGN_HUB/17_AUXILIARY_TOOLS_PLAN.md
DESIGN_HUB/18_VERSION_GATE.md
DESIGN_HUB/19_NOT_NOW.md
```

然后先进行立项访谈，不直接进入开发。

推荐流程：

```text
新建 ChatGPT 项目专属对话
↓
ChatGPT 读取 GitHub 模板仓库
↓
ChatGPT 读取 PROJECT_STATUS 与 00_PROJECT_CANVAS
↓
ChatGPT 向用户提问：类型、题材、目标用户、核心玩法、参考产品、最小 Demo 目标
↓
ChatGPT 同时分析：这个项目需要哪些辅助工具，才能让策划高效迭代
↓
用户回答
↓
ChatGPT 整理立项档案草案、辅助工具规划草案、暂不做清单
↓
用户确认
↓
ChatGPT 写入 00_PROJECT_CANVAS.md、17_AUXILIARY_TOOLS_PLAN.md、19_NOT_NOW.md
↓
ChatGPT 提炼 01_PROJECT_BRIEF / 02_CORE_GAMEPLAY / 03_PLAYER_EXPERIENCE / 12_DEMO_SCOPE
↓
ChatGPT 更新 PROJECT_STATUS.md
↓
确认后生成 AI_TASKS/NEXT_CODEX_PROMPT.md
↓
Codex 开始 WEB_DEMO/ 开发
```

关键原则：

```text
先讨论；
再确认；
再写入 GitHub；
最后才进入开发。
```

---

# 4. AI 开始工作前必须阅读

每次新会话、上下文重置或开始新任务前，AI 必须按顺序阅读：

```text
1. README.md
2. PROJECT_STATUS.md
3. AI_RULES/00_MASTER_PROMPT.md
4. AI_RULES/01_AI_READ_ORDER.md
5. AI_RULES/02_AI_EDIT_PERMISSION.md
6. AI_RULES/07_AI_ROLE_SPLIT.md
7. AI_RULES/08_OUTPUT_FORMATS.md
8. AI_RULES/09_CONFIG_FIRST_RULE.md
9. DESIGN_HUB/00_DESIGN_INDEX.md
10. DESIGN_HUB/00_PROJECT_CANVAS.md
11. DESIGN_HUB/01_PROJECT_BRIEF.md
12. DESIGN_HUB/02_CORE_GAMEPLAY.md
13. DESIGN_HUB/03_PLAYER_EXPERIENCE.md
14. DESIGN_HUB/09_DECISIONS.md
15. DESIGN_HUB/10_OPEN_QUESTIONS.md
16. DESIGN_HUB/12_DEMO_SCOPE.md
17. DESIGN_HUB/14_DEFAULT_DEV_FEATURES.md
18. DESIGN_HUB/15_WEB_DEMO_WORKSPACE.md
19. DESIGN_HUB/16_UNITY_SOURCE_WORKFLOW.md
20. DESIGN_HUB/17_AUXILIARY_TOOLS_PLAN.md
21. DESIGN_HUB/18_VERSION_GATE.md
22. DESIGN_HUB/19_NOT_NOW.md
23. DESIGN_HUB/20_DEMO_PRESENTATION_STANDARD.md
24. AI_TASKS/CURRENT_TASK.md
25. AI_TASKS/NEXT_CODEX_PROMPT.md
26. AI_TASKS/DEEPSEEK_TASKS.md
27. AI_TASKS/FEEDBACK_TO_TASK.md
28. AI_RULES/06_VALIDATION_CHECKLIST.md
```

阅读后，AI 必须先回复：

```text
我已理解当前项目目标、目录结构、设计边界、技术规则和本轮任务约束。
```

如果是新项目立项阶段，AI 应继续说明：

```text
我将先进行立项访谈，暂不进入开发，并会同时分析本项目可能需要的辅助工具。
```

如果执行者是 Codex，还必须先输出任务归属判断。

---

# 5. 当前推荐主工作流

```text
ChatGPT：制作人 / 总策划 / 立项访谈 / 辅助工具规划 / 任务拆解 / 产品复审
Codex：Web Demo 主开发 / Unity 源码体检 / 兼容性修复 / 代码审核 / AI 任务调度者
DeepSeek：模块开发 / 批量配置 / 重复性代码 / 文档整理
Figma：UI 原型和界面表达
Image 2 / 即梦：图片和素材方向
Seedance / 即梦：动画和投放视频
Excel / Python：数值与数据分析
Notion：工作流、文档、知识库、任务沉淀
GitHub：代码版本管理
Unity：v1.x 之后用于源码学习、改造和未来独立原型
```

---

# 6. 阶段路线

```text
v0.x = Web Demo 原型阶段
v1.x = Unity 源码学习 / 改造阶段
v2.x = Unity 独立原型阶段
v3.x = 可展示垂直切片阶段
v4.x = 商业化验证阶段
```

版本推进条件见：

```text
DESIGN_HUB/18_VERSION_GATE.md
```

当前阶段暂不做清单见：

```text
DESIGN_HUB/19_NOT_NOW.md
```

Demo 展示标准见：

```text
DESIGN_HUB/20_DEMO_PRESENTATION_STANDARD.md
```

---

# 7. Codex 任务归属判断规则

Codex 不只是执行者，也是项目主程和任务调度者。

每次 Codex 阅读完 `AI_TASKS/NEXT_CODEX_PROMPT.md` 后，必须先判断本轮任务的执行归属。

Codex 必须在正式开发前输出：

```text
任务归属判断：
- 本轮由 Codex 自己开发 / 拆分给 DeepSeek / Codex + DeepSeek 协作
- 判断理由：
- Codex 负责：
- DeepSeek 负责：
- Codex 审核方式：
```

如本轮需要 DeepSeek 执行子任务，必须在以下文件记录任务卡：

```text
AI_TASKS/DEEPSEEK_TASKS.md
```

---

# 8. 配置优先原则

策划可能频繁调整的内容，不得硬编码。

Web Demo 阶段优先使用：

```text
WEB_DEMO/Data/config/
```

详细规则见：

```text
AI_RULES/09_CONFIG_FIRST_RULE.md
```

---

# 9. 试玩反馈转任务

试玩反馈不应直接变成开发冲动，必须先分类、定级，再生成任务。

流程见：

```text
AI_TASKS/FEEDBACK_TO_TASK.md
```

---

# 10. Unity 源码筛选

进入 Unity 源码学习阶段前，必须先对候选源码评分。

评分表见：

```text
UNITY_SOURCE/SOURCE_CANDIDATES.md
```

---

# 11. 当前已确认的通用边界摘要

```text
当前目标：先做 Demo，不直接追求完整游戏。
项目启动：新项目先通过 00_PROJECT_CANVAS.md 完成立项访谈，并通过 17_AUXILIARY_TOOLS_PLAN.md 分析辅助工具需求。
状态同步：每轮关键任务后更新 PROJECT_STATUS.md。
版本推进：按 18_VERSION_GATE.md 控制阶段推进。
暂不做：按 19_NOT_NOW.md 防止 AI 过度发散。
配置优先：策划可能频繁调整的内容，不得硬编码。
Demo 展示：Demo 必须能让美术、程序、制作人或外部评审快速看懂。
开发顺序：Web Demo → Unity 源码学习 / 改造 → Unity 独立原型。
Web Demo 路径原则：Web Demo 使用 WEB_DEMO/ 独立工作区。
Unity 路线原则：先做源码学习 / 改造，不默认从 0 创建 Unity 项目。
根目录瘦身原则：不要在根目录默认创建具体工程目录，具体文件应放入 WEB_DEMO/、UNITY_SOURCE/ 或 UNITY_PROJECT/ 内部。
```