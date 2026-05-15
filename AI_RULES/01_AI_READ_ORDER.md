# 01_AI_READ_ORDER：AI 阅读顺序

每次新会话、上下文重置或开始新任务前，AI 必须按以下顺序阅读。

---

## 必读顺序

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
17. DESIGN_HUB/17_AUXILIARY_TOOLS_PLAN.md
18. AI_TASKS/CURRENT_TASK.md
19. AI_TASKS/NEXT_CODEX_PROMPT.md
20. AI_TASKS/DEEPSEEK_TASKS.md
21. AI_RULES/06_VALIDATION_CHECKLIST.md
```

---

## 新项目立项时的额外要求

如果当前是新项目立项阶段，AI 必须优先读取：

```text
DESIGN_HUB/00_PROJECT_CANVAS.md
DESIGN_HUB/17_AUXILIARY_TOOLS_PLAN.md
```

然后根据 `00_PROJECT_CANVAS.md` 中的“ChatGPT 立项访谈问题清单”向用户提问。

立项访谈不仅要明确游戏类型、题材、目标用户和核心玩法，还要主动分析本项目可能需要哪些配套辅助工具。

在用户确认前，不要直接进入开发，也不要直接生成 Codex 开发任务。

推荐流程：

```text
先提问；
用户回答；
AI 总结立项档案草案；
AI 分析辅助工具需求；
用户确认；
写入 GitHub；
提炼正式设计文档；
提炼辅助工具规划；
再生成 NEXT_CODEX_PROMPT。
```

---

## NEXT_CODEX_PROMPT 说明

`AI_TASKS/NEXT_CODEX_PROMPT.md` 用于保存下一轮交给 Codex 执行的完整提示词。

当 ChatGPT 长对话过长、网页卡顿或上下文过重时，应将最终确认的 Codex 提示词写入该文件，避免继续在聊天中堆积超长提示词。

Codex 执行任务时，必须读取该文件。

---

## 阅读后必须回复

阅读后，AI 必须先回复：

```text
我已理解当前项目目标、目录结构、设计边界、技术规则和本轮任务约束。
```

如果是新项目立项阶段，AI 应继续说明：

```text
我将先进行立项访谈，暂不进入开发，并会同时分析本项目可能需要的辅助工具。
```

然后开始向用户提问。

---

## 禁止行为

- 不阅读规则就直接改代码；
- 只看当前任务，不看设计边界；
- 忽略 `DESIGN_HUB/00_PROJECT_CANVAS.md`；
- 忽略 `DESIGN_HUB/17_AUXILIARY_TOOLS_PLAN.md`；
- 忽略 `DESIGN_HUB/09_DECISIONS.md`；
- 忽略 `AI_TASKS/NEXT_CODEX_PROMPT.md`；
- 新项目未完成立项访谈就直接开发；
- 新项目未进行辅助工具需求分析就直接开发；
- 遇到不明确问题时擅自决定。