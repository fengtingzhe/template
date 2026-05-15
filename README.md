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

## 当前开发目标

当前阶段目标是完成第一版可运行 Demo，验证：

- 核心玩法闭环；
- 基础 UI 流程；
- 基础数值配置；
- 关键反馈表现；
- 可运行、可试玩、可展示版本。

## 当前版本不追求

- 最终美术品质；
- 完整商业化；
- 完整后端；
- 完整关卡数量；
- 完整上线品质；
- 复杂 SDK 接入；
- 完整长期工程架构。

---

# 2. 项目目录结构

```text
ProjectName/
├── README.md
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
DESIGN_HUB/00_PROJECT_CANVAS.md
```

然后先进行立项访谈，不直接进入开发。

推荐流程：

```text
新建 ChatGPT 项目专属对话
↓
ChatGPT 读取 GitHub 模板仓库
↓
ChatGPT 读取 DESIGN_HUB/00_PROJECT_CANVAS.md
↓
ChatGPT 向用户提问：类型、题材、目标用户、核心玩法、参考产品、最小 Demo 目标
↓
用户回答
↓
ChatGPT 整理立项档案草案
↓
用户确认
↓
ChatGPT 写入 00_PROJECT_CANVAS.md
↓
ChatGPT 提炼 01_PROJECT_BRIEF / 02_CORE_GAMEPLAY / 03_PLAYER_EXPERIENCE / 12_DEMO_SCOPE
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

`00_PROJECT_CANVAS.md` 是项目立项档案、想法池和持续 idea 记录区。

后续有新的想法时，应优先追加到：

```text
DESIGN_HUB/00_PROJECT_CANVAS.md
```

再根据确认结果提炼到正式设计文件。

---

# 4. AI 开始工作前必须阅读

每次新会话、上下文重置或开始新任务前，AI 必须按顺序阅读：

```text
1. README.md
2. AI_RULES/00_MASTER_PROMPT.md
3. AI_RULES/01_AI_READ_ORDER.md
4. AI_RULES/02_AI_EDIT_PERMISSION.md
5. AI_RULES/07_AI_ROLE_SPLIT.md
6. DESIGN_HUB/00_DESIGN_INDEX.md
7. DESIGN_HUB/00_PROJECT_CANVAS.md
8. DESIGN_HUB/01_PROJECT_BRIEF.md
9. DESIGN_HUB/02_CORE_GAMEPLAY.md
10. DESIGN_HUB/03_PLAYER_EXPERIENCE.md
11. DESIGN_HUB/09_DECISIONS.md
12. DESIGN_HUB/10_OPEN_QUESTIONS.md
13. DESIGN_HUB/12_DEMO_SCOPE.md
14. DESIGN_HUB/14_DEFAULT_DEV_FEATURES.md
15. DESIGN_HUB/15_WEB_DEMO_WORKSPACE.md
16. DESIGN_HUB/16_UNITY_SOURCE_WORKFLOW.md
17. AI_TASKS/CURRENT_TASK.md
18. AI_TASKS/NEXT_CODEX_PROMPT.md
19. AI_TASKS/DEEPSEEK_TASKS.md
20. AI_RULES/06_VALIDATION_CHECKLIST.md
```

阅读后，AI 必须先回复：

```text
我已理解当前项目目标、目录结构、设计边界、技术规则和本轮任务约束。
```

如果是新项目立项阶段，AI 应继续说明：

```text
我将先进行立项访谈，暂不进入开发。
```

如果执行者是 Codex，还必须先输出任务归属判断。

---

# 5. AI 工作基本原则

AI 可以：

```text
执行任务；
整理文档；
实现功能；
修复 Bug；
提出建议；
生成配置；
生成测试；
总结问题。
```

AI 不可以：

```text
擅自改变核心玩法；
擅自改变核心系统；
擅自改变核心数值方向；
擅自改变核心技术架构；
擅自重构项目目录结构；
擅自删除已确认设计；
擅自替换已经确认的方案；
新项目未完成立项访谈就直接进入开发。
```

如果 AI 不确定，应写入：

```text
DESIGN_HUB/10_OPEN_QUESTIONS.md
```

等待人类制作人决策。

---

# 6. 当前推荐主工作流

```text
ChatGPT：制作人 / 总策划 / 立项访谈 / 任务拆解 / 产品复审
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

判断原则：

```text
核心架构、跨文件整合、状态管理、复杂 Bug 修复、最终合并：优先 Codex；
普通 UI 组件、重复性代码、配置表、文案、简单工具函数：可以拆给 DeepSeek；
DeepSeek 产物必须由 Codex 审核后才能合并。
```

如本轮需要 DeepSeek 执行子任务，必须在以下文件记录任务卡：

```text
AI_TASKS/DEEPSEEK_TASKS.md
```

---

# 8. 引擎与工程路线原则

当前工作流不再默认要求 Web Demo 之后进入某个游戏引擎从 0 开发。

新的路线是：

```text
v0.x = Web Demo 原型阶段
v1.x = Unity 源码学习 / 改造阶段
v2.x = Unity 独立原型阶段
v3.x = 可展示垂直切片阶段
v4.x = 商业化验证阶段
```

原因：

```text
1. Web Demo 最适合策划快速表达核心玩法和界面流程；
2. 直接学习完整游戏引擎仍然需要代码基础和工程经验；
3. Unity 源码项目可以作为学习真实工程结构的中间层；
4. 通过 AI 修复兼容、解释结构、小步改造，比从 0 创建 Unity 项目更适合当前阶段；
5. 不再默认创建或维护其他引擎工程，避免路线冲突。
```

---

# 9. Demo 阶段划分

本项目采用“先 Web Demo，再 Unity 源码学习 / 改造”的开发策略。

## v0.x：Web Demo 原型阶段

目标：

- 快速验证核心玩法；
- 快速验证 UI 信息层级；
- 快速验证资源循环；
- 快速进行试玩反馈；
- 给美术和程序直观展示核心玩法；
- 为后续 Unity 源码学习 / 改造提供明确方向。

默认独立工作区：

```text
WEB_DEMO/
├── README.md
├── run_web_demo.bat
├── package.json
├── index.html
├── styles.css
├── game.js
├── Data/
├── Assets/
├── Tools/
├── Tests/
├── Docs/
└── Temp/
```

详细规则见：

```text
DESIGN_HUB/15_WEB_DEMO_WORKSPACE.md
```

## v1.x：Unity 源码学习 / 改造阶段

目标：

- 筛选可运行的 Unity 源码项目；
- 检查 Unity 版本、许可证、依赖插件和运行说明；
- 让 AI 协助修复兼容性问题；
- 学习项目结构、场景、Prefab、脚本、资源和 UI；
- 小步改造，让源码项目逐步接近 Web Demo 验证出的方向。

默认工作区：

```text
UNITY_SOURCE/
```

详细规则见：

```text
DESIGN_HUB/16_UNITY_SOURCE_WORKFLOW.md
```

## v2.x：Unity 独立原型阶段

目标：

- 在理解 Unity 基础后，再决定是否搭建自己的 Unity 原型项目；
- 不建议在没有完成 v1.x 源码学习前直接从 0 开始。

默认工作区：

```text
UNITY_PROJECT/
```

## v3.x：可展示垂直切片阶段

目标：

- 让项目具备对外展示价值；
- 包括美术方向、完整闭环、基础表现和演示材料。

## v4.x：商业化验证阶段

目标：

- 验证广告、内购、留存、打点、发行渠道、性能和平台适配。

---

# 10. NEXT_CODEX_PROMPT 使用规则

`AI_TASKS/NEXT_CODEX_PROMPT.md` 用于保存下一轮交给 Codex 执行的完整提示词。

当 ChatGPT 长对话过长、网页卡顿或上下文过重时，不应继续在聊天中堆积提示词，而应将最终确认的任务提示词写入该文件。

Codex 执行任务时，应优先读取：

- `AI_TASKS/NEXT_CODEX_PROMPT.md`
- `AI_TASKS/CURRENT_TASK.md`
- `AI_TASKS/CHANGELOG.md`
- `AI_TASKS/DEV_LOG.md`
- `AI_TASKS/DEEPSEEK_TASKS.md`

执行完成后，Codex 应更新：

- `AI_TASKS/CURRENT_TASK.md`
- `AI_TASKS/CHANGELOG.md`
- `AI_TASKS/DEV_LOG.md`
- 必要时更新 `AI_TASKS/NEXT_CODEX_PROMPT.md`
- 如涉及 DeepSeek 任务拆分，更新 `AI_TASKS/DEEPSEEK_TASKS.md`
- 如涉及 DeepSeek 产物审核，更新 `AI_TASKS/REVIEW_LOG.md`

---

# 11. 通用 Debug Console 规则

所有 Demo 默认应提供一个 `Console` / `Dev` 按钮，作为开发者工具入口。

Console 是 Demo 阶段的开发者工具面板，不代表最终玩家界面。

通用功能只包含跨游戏类型也常用的功能：

```text
音乐开关；
音效开关；
暂停 / 继续；
重置场景 / 重置 Demo；
显示 FPS。
```

FPS 显示规则：

```text
当 Console 中开启 FPS 显示后，FPS 数值应显示在游戏画面的右下角。
```

特定游戏相关功能，例如加资源、跳转时间、生成敌人、解锁节点等，不属于通用 Console 规则。如某个项目需要，应在该项目的任务卡或 `DESIGN_HUB/10_OPEN_QUESTIONS.md` 中单独确认。

详细规则见：

```text
DESIGN_HUB/13_DEBUG_CONSOLE.md
```

---

# 12. 默认开发辅助功能

所有项目默认应具备一组不属于具体玩法的开发辅助能力。

这些功能用于提高 Demo 开发、调试、测试和展示效率。

默认开发辅助功能包括：

```text
Console / Dev 面板；
FPS 显示；
音乐开关；
音效开关；
暂停 / 继续；
重置场景 / Demo；
Web Demo 一键启动 bat；
Vite 或等价本地 Web 服务；
Smoke Test；
版本号显示。
```

Web Demo 阶段默认提供：

```text
WEB_DEMO/run_web_demo.bat
```

作用：

```text
启动 Vite 或等价本地 Web 服务；
自动打开 Demo 网页；
避免直接双击 WEB_DEMO/index.html 导致路径或权限问题；
不依赖个人电脑绝对路径。
```

详细规则见：

```text
DESIGN_HUB/14_DEFAULT_DEV_FEATURES.md
```

---

# 13. 当前已确认的通用边界摘要

```text
当前目标：先做 Demo，不直接追求完整游戏。
项目启动：新项目先通过 00_PROJECT_CANVAS.md 完成立项访谈。
Demo 重点：核心玩法、界面流程、关键反馈、表现方向。
开发顺序：Web Demo → Unity 源码学习 / 改造 → Unity 独立原型。
AI 分工：ChatGPT 管立项访谈、方案和任务拆解，Codex 管工程和任务调度，DeepSeek 管模块，策划管方向和体验。
修改原则：AI 不确定时写入 OPEN_QUESTIONS，不得擅自改核心方向。
Console 原则：只默认包含通用开发者工具，项目特定调试功能需单独确认。
默认开发辅助功能：Web Demo 默认应提供一键启动 bat、本地服务、Smoke Test 和基础版本识别能力。
Web Demo 路径原则：Web Demo 使用 WEB_DEMO/ 独立工作区。
Unity 路线原则：先做源码学习 / 改造，不默认从 0 创建 Unity 项目。
根目录瘦身原则：不要在根目录默认创建具体工程目录，具体文件应放入 WEB_DEMO/、UNITY_SOURCE/ 或 UNITY_PROJECT/ 内部。
```