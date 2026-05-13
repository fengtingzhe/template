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
├── Docs/
├── Data/
├── Assets/
├── Scenes/
├── Scripts/
├── Tools/
├── Tests/
├── Builds/
└── Temp/
```

核心原则：

```text
DESIGN_HUB 管方向；
AI_RULES 管 AI；
AI_TASKS 管执行；
Docs 管资料；
Data 管配置；
Scripts / Scenes 管实现。
```

---

# 3. AI 开始工作前必须阅读

每次新会话、上下文重置或开始新任务前，AI 必须按顺序阅读：

```text
1. README.md
2. AI_RULES/00_MASTER_PROMPT.md
3. AI_RULES/01_AI_READ_ORDER.md
4. AI_RULES/02_AI_EDIT_PERMISSION.md
5. DESIGN_HUB/00_DESIGN_INDEX.md
6. DESIGN_HUB/01_PROJECT_BRIEF.md
7. DESIGN_HUB/02_CORE_GAMEPLAY.md
8. DESIGN_HUB/03_PLAYER_EXPERIENCE.md
9. DESIGN_HUB/09_DECISIONS.md
10. DESIGN_HUB/10_OPEN_QUESTIONS.md
11. AI_TASKS/CURRENT_TASK.md
12. AI_TASKS/NEXT_CODEX_PROMPT.md
13. AI_RULES/06_VALIDATION_CHECKLIST.md
```

阅读后，AI 必须先回复：

```text
我已理解当前项目目标、目录结构、设计边界、技术规则和本轮任务约束。
```

然后才能开始修改文件。

---

# 4. AI 工作基本原则

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
擅自替换已经确认的方案。
```

如果 AI 不确定，应写入：

```text
DESIGN_HUB/10_OPEN_QUESTIONS.md
```

等待人类制作人决策。

---

# 5. 当前推荐主工作流

```text
ChatGPT：制作人 / 总策划 / 任务拆解 / 产品复审
Godot：游戏编辑器，Demo 阶段主引擎
Codex：主程 / 架构 / 代码审核 / Bug 修复
DeepSeek：模块开发 / 批量配置 / 重复性代码
Figma：UI 原型和界面表达
Image 2 / 即梦：图片和素材方向
Seedance / 即梦：动画和投放视频
Excel / Python：数值与数据分析
Notion：工作流、文档、知识库、任务沉淀
GitHub：代码版本管理
```

---

# 6. 引擎选择原则

当前工作流的目标是快速搭建可试玩、可展示、可验证的游戏 Demo，而不是一开始完成复杂商业化游戏。

因此，默认推荐使用 Godot 作为 Demo 阶段的主引擎。

原因：

```text
1. Godot 更轻量，适合快速启动和快速迭代；
2. Godot 的 2D 能力适合移动端竖屏原型；
3. GDScript 简洁，便于 AI 生成、阅读和修改；
4. Godot 项目文本化程度较高，适合 Codex / DeepSeek 处理；
5. 策划更容易理解场景、脚本和数据之间的关系。
```

Unity 更适合进入商业化开发阶段后再评估。

---

# 7. Demo 阶段划分

本项目采用“先 Web Demo，后 Godot Demo”的开发策略。

## Web Demo 阶段

版本号：`v0.x`

目标：

- 快速验证核心玩法；
- 快速验证 UI 信息层级；
- 快速验证资源循环；
- 快速进行试玩反馈；
- 为 Godot Demo 提供明确方向。

默认目录：

```text
Builds/web-demo/
Data/config/
Tools/
Tests/
```

## Godot Demo 阶段

版本号：`v1.x`

目标：

- 将已经验证过的核心玩法迁移到 Godot；
- 加入正式场景结构；
- 加入 Godot UI；
- 加入角色、动画、反馈和资源管理；
- 为后续可展示垂直切片做准备。

---

# 8. NEXT_CODEX_PROMPT 使用规则

`AI_TASKS/NEXT_CODEX_PROMPT.md` 用于保存下一轮交给 Codex 执行的完整提示词。

当 ChatGPT 长对话过长、网页卡顿或上下文过重时，不应继续在聊天中堆积提示词，而应将最终确认的任务提示词写入该文件。

Codex 执行任务时，应优先读取：

- `AI_TASKS/NEXT_CODEX_PROMPT.md`
- `AI_TASKS/CURRENT_TASK.md`
- `AI_TASKS/CHANGELOG.md`
- `AI_TASKS/DEV_LOG.md`

执行完成后，Codex 应更新：

- `AI_TASKS/CURRENT_TASK.md`
- `AI_TASKS/CHANGELOG.md`
- `AI_TASKS/DEV_LOG.md`
- 必要时更新 `AI_TASKS/NEXT_CODEX_PROMPT.md`

---

# 9. 通用 Debug Console 规则

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

# 10. 默认开发辅助功能

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
run_web_demo.bat
```

作用：

```text
启动 Vite 或等价本地 Web 服务；
自动打开 Demo 网页；
避免直接双击 index.html 导致路径或权限问题；
不依赖个人电脑绝对路径。
```

详细规则见：

```text
DESIGN_HUB/14_DEFAULT_DEV_FEATURES.md
```

---

# 11. 当前已确认的通用边界摘要

```text
当前目标：先做 Demo，不直接追求完整游戏。
Demo 重点：核心玩法、界面流程、关键反馈、表现方向。
开发顺序：先 Web Demo，后 Godot Demo。
AI 分工：ChatGPT 管方案，Codex 管工程，DeepSeek 管模块，策划管方向和体验。
修改原则：AI 不确定时写入 OPEN_QUESTIONS，不得擅自改核心方向。
Console 原则：只默认包含通用开发者工具，项目特定调试功能需单独确认。
默认开发辅助功能：Web Demo 默认应提供一键启动 bat、本地服务、Smoke Test 和基础版本识别能力。
```