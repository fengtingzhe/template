# NEXT_CODEX_PROMPT：下一轮 Codex 任务

## 任务名称

待填写。

---

## 给 Codex 的提示词

你正在继续开发一个基于本模板创建的 AI 游戏 Demo 项目。

请先阅读：

1. `README.md`
2. `PROJECT_STATUS.md`
3. `AI_RULES/00_MASTER_PROMPT.md`
4. `AI_RULES/03_TECHNICAL_RULES.md`
5. `AI_RULES/07_AI_ROLE_SPLIT.md`
6. `AI_RULES/08_OUTPUT_FORMATS.md`
7. `AI_RULES/09_CONFIG_FIRST_RULE.md`
8. `DESIGN_HUB/00_PROJECT_CANVAS.md`
9. `DESIGN_HUB/01_PROJECT_BRIEF.md`
10. `DESIGN_HUB/02_CORE_GAMEPLAY.md`
11. `DESIGN_HUB/03_PLAYER_EXPERIENCE.md`
12. `DESIGN_HUB/05_ECONOMY_AND_BALANCE.md`
13. `DESIGN_HUB/07_ART_AND_AUDIO_DIRECTION.md`
14. `DESIGN_HUB/08_UX_FLOW.md`
15. `DESIGN_HUB/09_DECISIONS.md`
16. `DESIGN_HUB/10_OPEN_QUESTIONS.md`
17. `DESIGN_HUB/12_DEMO_SCOPE.md`
18. `DESIGN_HUB/13_DEBUG_CONSOLE.md`
19. `DESIGN_HUB/14_DEFAULT_DEV_FEATURES.md`
20. `DESIGN_HUB/15_WEB_DEMO_WORKSPACE.md`
21. `DESIGN_HUB/16_UNITY_SOURCE_WORKFLOW.md`
22. `DESIGN_HUB/17_AUXILIARY_TOOLS_PLAN.md`
23. `DESIGN_HUB/18_VERSION_GATE.md`
24. `DESIGN_HUB/19_NOT_NOW.md`
25. `DESIGN_HUB/20_DEMO_PRESENTATION_STANDARD.md`
26. `AI_TASKS/CURRENT_TASK.md`
27. `AI_TASKS/CHANGELOG.md`
28. `AI_TASKS/DEV_LOG.md`
29. `AI_TASKS/DEEPSEEK_TASKS.md`
30. `AI_TASKS/FEEDBACK_TO_TASK.md`
31. `AI_RULES/06_VALIDATION_CHECKLIST.md`

---

## 开发前置条件

在正式开发前，必须确认项目已经完成立项访谈，并且以下文件已经从 `DESIGN_HUB/00_PROJECT_CANVAS.md` 中提炼出基本内容：

```text
DESIGN_HUB/01_PROJECT_BRIEF.md
DESIGN_HUB/02_CORE_GAMEPLAY.md
DESIGN_HUB/03_PLAYER_EXPERIENCE.md
DESIGN_HUB/12_DEMO_SCOPE.md
```

还必须确认：

```text
PROJECT_STATUS.md 已更新；
DESIGN_HUB/17_AUXILIARY_TOOLS_PLAN.md 已完成辅助工具需求初判；
DESIGN_HUB/18_VERSION_GATE.md 中的当前版本进入条件已满足；
DESIGN_HUB/19_NOT_NOW.md 中没有被本轮任务违反的暂不做项；
AI_RULES/09_CONFIG_FIRST_RULE.md 中的配置优先规则已纳入实现约束；
DESIGN_HUB/20_DEMO_PRESENTATION_STANDARD.md 中的展示标准已纳入验收。
```

如果项目尚未完成立项访谈、辅助工具需求分析或版本进入条件不清楚，Codex 不应开始开发游戏本体。

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

## 当前项目阶段

- [ ] v0.x / Web Demo 原型
- [ ] v1.x / Unity 源码学习 / 改造
- [ ] v2.x / Unity 独立原型
- [ ] v3.x / 可展示垂直切片
- [ ] v4.x / 商业化验证

---

## 允许修改文件

```text
待填写。
```

如果本轮涉及 Web Demo，默认应优先使用：

```text
WEB_DEMO/
AI_TASKS/
PROJECT_STATUS.md
DESIGN_HUB/11_PLAYTEST_FEEDBACK.md
DESIGN_HUB/12_DEMO_SCOPE.md
DESIGN_HUB/17_AUXILIARY_TOOLS_PLAN.md
```

如果本轮涉及辅助工具，默认应优先使用：

```text
WEB_DEMO/Tools/
DESIGN_HUB/17_AUXILIARY_TOOLS_PLAN.md
AI_TASKS/
```

如果本轮涉及 Unity 源码学习 / 改造，默认应优先使用：

```text
UNITY_SOURCE/
UNITY_SOURCE/SOURCE_CANDIDATES.md
AI_TASKS/
Docs/UnitySourceAnalysis/
```

---

## 禁止事项

默认禁止：

- 不要擅自修改 `DESIGN_HUB/09_DECISIONS.md`；
- 不要擅自修改 `AI_RULES/`；
- 不要违反 `DESIGN_HUB/19_NOT_NOW.md`；
- 不要新增与本轮目标无关的大型系统；
- 不要把 Demo 宣称为最终游戏；
- 不要引入复杂依赖，除非任务明确允许；
- 不要擅自改变核心玩法方向；
- 不要把策划可能频繁调整的内容硬编码；
- 不要把 Web Demo 源码写入 `Builds/`；
- 不要把 Web Demo 配置、工具、测试散落到根目录 `Data/`、`Tools/`、`Tests/`；
- 不要默认创建其他引擎工程；
- 不要在没有明确进入 v2.x 前从 0 创建 Unity 项目；
- 不要绕过 Unity 源码许可证或授权限制；
- 不要在项目尚未完成立项访谈时开始开发；
- 不要在未分析辅助工具需求时直接开发大量关卡、数值或内容；
- 不要让辅助工具开发规模超过当前 Demo 本体。

---

## Web Demo 独立工作区要求

如果本轮涉及 Web Demo，默认应参考：

```text
DESIGN_HUB/15_WEB_DEMO_WORKSPACE.md
DESIGN_HUB/18_VERSION_GATE.md
DESIGN_HUB/20_DEMO_PRESENTATION_STANDARD.md
AI_RULES/09_CONFIG_FIRST_RULE.md
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

## 配置优先要求

如果本轮涉及数值、关卡、目标、奖励、难度、UI 文案或策划可能频繁调整的内容，默认应配置化。

配置优先路径：

```text
WEB_DEMO/Data/config/
```

除 v0.1 最小验证外，不应把关键数值硬编码在逻辑代码中。

---

## 辅助工具要求

如果本轮涉及关卡编辑器、数值模拟器、配置工具、内容批量生成、自动测试、难度评估或其他配套工具，默认应参考：

```text
DESIGN_HUB/17_AUXILIARY_TOOLS_PLAN.md
```

默认原则：

```text
先做最小可用版本；
优先 Web 工具；
优先放在 WEB_DEMO/Tools/；
优先让策划能独立配置；
优先支持导入 / 导出 JSON；
如策划常用 Excel，可考虑 CSV / Excel 导入导出；
不要过早做复杂后台；
不要让工具开发超过游戏 Demo 本体；
工具必须服务当前验证目标。
```

---

## Unity 源码学习 / 改造要求

如果本轮涉及 Unity 源码学习 / 改造，默认应参考：

```text
DESIGN_HUB/16_UNITY_SOURCE_WORKFLOW.md
UNITY_SOURCE/SOURCE_CANDIDATES.md
```

默认要求：

```text
先做候选源码评分；
Unity 源码项目放在 UNITY_SOURCE/；
先做源码体检，再做改造；
检查 Unity 版本、许可证、依赖插件、缺失资源、后端依赖；
首次运行报错必须记录；
兼容性修复记录到 UNITY_SOURCE/COMPATIBILITY_LOG.md；
源码结构分析记录到 UNITY_SOURCE/STRUCTURE_NOTES.md 或 Docs/UnitySourceAnalysis/；
源码未跑通前不做大规模改造；
不绕过许可证或授权限制。
```

---

## 试玩反馈转任务要求

如果本轮任务来自试玩反馈，必须先参考：

```text
AI_TASKS/FEEDBACK_TO_TASK.md
```

先做反馈分类、优先级判断，再生成开发任务。

---

## 验收标准

完成后必须满足：

1. 待填写；
2. 待填写；
3. `PROJECT_STATUS.md` 已更新；
4. 项目已经完成立项访谈，或本轮明确是“完善立项档案”任务；
5. 项目已经完成辅助工具需求分析，或本轮明确是“完善辅助工具规划”任务；
6. 本轮任务不违反 `DESIGN_HUB/19_NOT_NOW.md`；
7. 本轮版本推进符合 `DESIGN_HUB/18_VERSION_GATE.md`；
8. 如涉及 Web Demo，文件位于 `WEB_DEMO/` 独立工作区；
9. 如涉及 Web Demo，展示标准符合 `DESIGN_HUB/20_DEMO_PRESENTATION_STANDARD.md`；
10. 如涉及配置，符合 `AI_RULES/09_CONFIG_FIRST_RULE.md`；
11. 如涉及辅助工具，文件优先位于 `WEB_DEMO/Tools/` 或对应阶段工作区；
12. 如涉及 Unity 源码学习，文件位于 `UNITY_SOURCE/`，且已完成源码体检或候选评分；
13. 已完成任务归属判断；
14. 如拆给 DeepSeek，已更新 `AI_TASKS/DEEPSEEK_TASKS.md`；
15. 如合并 DeepSeek 产物，已更新 `AI_TASKS/REVIEW_LOG.md`；
16. 已更新 `AI_TASKS/CHANGELOG.md`；
17. 已更新 `AI_TASKS/DEV_LOG.md`；
18. 已更新 `AI_TASKS/CURRENT_TASK.md`。

---

## 完成后请更新

1. `PROJECT_STATUS.md`
2. `AI_TASKS/CHANGELOG.md`
3. `AI_TASKS/DEV_LOG.md`
4. `AI_TASKS/CURRENT_TASK.md`
5. `AI_TASKS/DEEPSEEK_TASKS.md`，如涉及任务拆分
6. `AI_TASKS/REVIEW_LOG.md`，如涉及 DeepSeek 产物审核
7. `DESIGN_HUB/17_AUXILIARY_TOOLS_PLAN.md`，如涉及辅助工具新增、调整或延期
8. `UNITY_SOURCE/SOURCE_CANDIDATES.md`，如涉及 Unity 源码候选筛选
9. `UNITY_SOURCE/COMPATIBILITY_LOG.md`，如涉及 Unity 兼容性修复
10. `UNITY_SOURCE/STRUCTURE_NOTES.md`，如涉及 Unity 源码结构学习

必要时，将下一轮建议写入本文件。