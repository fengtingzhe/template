# 02_AI_EDIT_PERMISSION：AI 修改权限

本文件定义 AI 可以修改、谨慎修改、不得擅自修改的文件和目录。

---

## AI 可以修改

前提是任务明确允许：

```text
WEB_DEMO/
Scripts/
Data/
AI_TASKS/CHANGELOG.md
AI_TASKS/DEV_LOG.md
AI_TASKS/REVIEW_LOG.md
AI_TASKS/CURRENT_TASK.md
AI_TASKS/NEXT_CODEX_PROMPT.md
AI_TASKS/DEEPSEEK_TASKS.md
Tests/
Tools/
Temp/
```

---

## NEXT_CODEX_PROMPT 修改限制

`AI_TASKS/NEXT_CODEX_PROMPT.md` 可以由 ChatGPT 或人类制作人生成和更新。

Codex 可以在任务完成后：

```text
补充执行结果；
记录下一轮建议；
将已完成提示词归档；
更新下一轮建议草案。
```

但 Codex 不得擅自改变人类已经确认的核心目标。

如 Codex 认为提示词存在冲突，应写入：

```text
DESIGN_HUB/10_OPEN_QUESTIONS.md
```

---

## DEEPSEEK_TASKS 修改限制

`AI_TASKS/DEEPSEEK_TASKS.md` 用于记录 Codex 拆分给 DeepSeek 的任务。

Codex 可以新增、更新 DeepSeek 任务卡，但不得用该文件绕过人类已确认的设计边界。

DeepSeek 产物必须由 Codex 审核后才能合并。

---

## AI 可以谨慎修改

修改前必须说明原因：

```text
Scenes/
Assets/
Docs/
AI_RULES/03_TECHNICAL_RULES.md
AI_RULES/04_DATA_RULES.md
AI_RULES/05_ASSET_RULES.md
AI_RULES/06_VALIDATION_CHECKLIST.md
```

---

## AI 不得擅自修改

如需修改，必须先获得人类制作人确认：

```text
README.md
DESIGN_HUB/
AI_RULES/00_MASTER_PROMPT.md
AI_RULES/01_AI_READ_ORDER.md
AI_RULES/02_AI_EDIT_PERMISSION.md
AI_RULES/07_AI_ROLE_SPLIT.md
project.godot
核心主场景
核心 Autoload 配置
```

---

## Godot 特别提醒

AI 修改 `.tscn` 文件前必须说明：

```text
为什么要修改；
修改哪些节点；
是否会影响已有引用；
如何验证场景仍然可以打开。
```

---

## Web Demo 特别提醒

Web Demo 阶段默认版本号为 `v0.x`。

Web Demo 是独立原型工程，默认位于：

```text
WEB_DEMO/
```

Web Demo 内部推荐结构：

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

Web Demo 阶段优先使用 HTML + CSS + 原生 JavaScript 快速验证核心玩法。

未经明确允许，不要引入 React、Phaser、Three.js 或复杂 npm 依赖。

未经明确允许，不要把 Web Demo 源码写入：

```text
Builds/web-demo/
根目录 Data/config/
根目录 Tools/
根目录 Tests/
```

`Builds/` 应优先作为构建输出目录，而不是 Web Demo 源码目录。