# NEXT_CODEX_PROMPT：下一轮 Codex 任务

## 任务名称

待填写。

---

## 给 Codex 的提示词

你正在继续开发一个基于本模板创建的 AI 游戏 Demo 项目。

请先阅读：

1. `README.md`
2. `AI_RULES/00_MASTER_PROMPT.md`
3. `AI_RULES/07_AI_ROLE_SPLIT.md`
4. `DESIGN_HUB/01_PROJECT_BRIEF.md`
5. `DESIGN_HUB/02_CORE_GAMEPLAY.md`
6. `DESIGN_HUB/03_PLAYER_EXPERIENCE.md`
7. `DESIGN_HUB/05_ECONOMY_AND_BALANCE.md`
8. `DESIGN_HUB/07_ART_AND_AUDIO_DIRECTION.md`
9. `DESIGN_HUB/08_UX_FLOW.md`
10. `DESIGN_HUB/09_DECISIONS.md`
11. `DESIGN_HUB/12_DEMO_SCOPE.md`
12. `DESIGN_HUB/13_DEBUG_CONSOLE.md`
13. `DESIGN_HUB/14_DEFAULT_DEV_FEATURES.md`
14. `DESIGN_HUB/15_WEB_DEMO_WORKSPACE.md`
15. `AI_TASKS/CURRENT_TASK.md`
16. `AI_TASKS/CHANGELOG.md`
17. `AI_TASKS/DEV_LOG.md`
18. `AI_TASKS/DEEPSEEK_TASKS.md`
19. `AI_RULES/06_VALIDATION_CHECKLIST.md`

---

## 任务归属判断

阅读完本提示词后，Codex 必须先输出任务归属判断，再开始开发。

必须输出：

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

如本轮需要 DeepSeek 执行子任务，必须在：

```text
AI_TASKS/DEEPSEEK_TASKS.md
```

中记录任务卡。

---

## 当前版本状态

待填写。

说明当前 Demo 已经完成了什么、哪些问题需要修正、下一轮优先目标是什么。

---

## 本轮目标

本轮只做：

```text
待填写版本号 / 待填写任务名称
```

目标：

1. 待填写；
2. 待填写；
3. 待填写。

---

## 允许修改文件

```text
待填写。
```

如果本轮涉及 Web Demo，默认应优先使用：

```text
WEB_DEMO/
AI_TASKS/
DESIGN_HUB/11_PLAYTEST_FEEDBACK.md
DESIGN_HUB/12_DEMO_SCOPE.md
```

---

## 禁止事项

默认禁止：

- 不要擅自修改 `DESIGN_HUB/09_DECISIONS.md`；
- 不要擅自修改 `AI_RULES/`；
- 不要新增与本轮目标无关的大型系统；
- 不要把 Demo 宣称为最终游戏；
- 不要引入复杂依赖，除非任务明确允许；
- 不要擅自改变核心玩法方向；
- 不要把 Web Demo 源码写入 `Builds/`；
- 不要把 Web Demo 配置、工具、测试散落到根目录 `Data/`、`Tools/`、`Tests/`；
- 不要在 Web Demo 阶段修改 Godot 工程文件，除非任务明确允许。

---

## Web Demo 独立工作区要求

如果本轮涉及 Web Demo，默认应参考：

```text
DESIGN_HUB/15_WEB_DEMO_WORKSPACE.md
```

默认路径：

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

---

## 默认开发辅助功能要求

如果本轮涉及 Web Demo，默认应参考：

```text
DESIGN_HUB/14_DEFAULT_DEV_FEATURES.md
```

默认要求：

```text
提供 WEB_DEMO/run_web_demo.bat，或明确说明本轮暂不需要；
WEB_DEMO/run_web_demo.bat 用于启动 Vite 或等价本地 Web 服务；
WEB_DEMO/run_web_demo.bat 启动后应自动打开 Demo 网页；
WEB_DEMO/run_web_demo.bat 不得依赖个人电脑绝对路径；
不要要求用户直接双击 WEB_DEMO/index.html 运行 Demo；
如本轮包含测试，应提供或更新 WEB_DEMO/Tests/ 下的 Smoke Test。
```

---

## 通用 Console 要求

如果本轮涉及可运行 Demo 界面，默认应包含 `Console` / `Dev` 按钮。

通用功能只包括：

```text
音乐开关；
音效开关；
暂停 / 继续；
重置场景 / 重置 Demo；
显示 FPS。
```

当开启 FPS 显示后，FPS 数值应显示在游戏画面的右下角。

不要默认加入项目特定调试功能，例如加资源、跳转时间、生成敌人、解锁节点等。若需要，必须在任务目标中明确写出。

---

## 验收标准

完成后必须满足：

1. 待填写；
2. 待填写；
3. 如涉及 Web Demo，文件位于 `WEB_DEMO/` 独立工作区；
4. 默认开发辅助功能符合 `DESIGN_HUB/14_DEFAULT_DEV_FEATURES.md`；
5. 通用 Console 功能符合 `DESIGN_HUB/13_DEBUG_CONSOLE.md`；
6. 开启 FPS 后，FPS 数值显示在游戏画面的右下角；
7. 已完成任务归属判断；
8. 如拆给 DeepSeek，已更新 `AI_TASKS/DEEPSEEK_TASKS.md`；
9. 如合并 DeepSeek 产物，已更新 `AI_TASKS/REVIEW_LOG.md`；
10. 已更新 `AI_TASKS/CHANGELOG.md`；
11. 已更新 `AI_TASKS/DEV_LOG.md`；
12. 已更新 `AI_TASKS/CURRENT_TASK.md`。

---

## 完成后请更新

1. `AI_TASKS/CHANGELOG.md`
2. `AI_TASKS/DEV_LOG.md`
3. `AI_TASKS/CURRENT_TASK.md`
4. `AI_TASKS/DEEPSEEK_TASKS.md`，如涉及任务拆分
5. `AI_TASKS/REVIEW_LOG.md`，如涉及 DeepSeek 产物审核

必要时，将下一轮建议写入本文件。