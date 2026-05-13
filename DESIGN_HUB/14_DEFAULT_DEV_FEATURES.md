# 14_DEFAULT_DEV_FEATURES：默认开发辅助功能

## 定位

本文件记录所有项目默认应该具备的开发辅助功能。

这些功能不属于具体游戏玩法，而是为了提高 Demo 开发、调试、测试和展示效率。

---

## 默认功能清单

| 功能 | 阶段 | 是否默认需要 | 说明 |
|---|---|---|---|
| Console / Dev 面板 | Web Demo / Godot Demo | 是 | 游戏内开发者工具入口，具体规则见 `DESIGN_HUB/13_DEBUG_CONSOLE.md` |
| 显示 FPS | Web Demo / Godot Demo | 是 | 开启后显示在游戏画面右下角 |
| 音乐开关 | Web Demo / Godot Demo | 是 | 用于调试和展示 |
| 音效开关 | Web Demo / Godot Demo | 是 | 用于调试和展示 |
| 暂停 / 继续 | Web Demo / Godot Demo | 是 | 方便观察和调试 |
| 重置场景 / Demo | Web Demo / Godot Demo | 是 | 快速回到初始状态 |
| 一键启动 bat | Web Demo | 是 | Windows 下启动本地服务并打开 Demo |
| Vite 本地服务 | Web Demo | 是 | 运行网页 Demo，避免直接双击 HTML 产生路径或权限问题 |
| Smoke Test | Web Demo | 建议 | 快速确认 Demo 是否能打开 |
| 版本号显示 | Web Demo / Godot Demo | 建议 | 方便确认当前版本 |

---

## Web Demo 默认启动方式

Web Demo 阶段默认提供一个 Windows bat 文件：

```text
run_web_demo.bat
```

推荐位置：

```text
run_web_demo.bat
```

也可以根据项目需要放在：

```text
Tools/run_web_demo.bat
```

为了让非程序用户最容易找到，默认推荐放在项目根目录。

---

## run_web_demo.bat 默认目标

`run_web_demo.bat` 的作用是：

```text
1. 检查当前目录；
2. 检查是否具备运行 Web Demo 的基本环境；
3. 启动 Vite 或本地 Web 服务；
4. 自动打开 Demo 网页；
5. 保持命令行窗口，方便查看报错。
```

---

## Web Demo 默认目录

```text
Builds/web-demo/
├── index.html
├── styles.css
└── game.js
```

配置文件默认放在：

```text
Data/config/
```

测试脚本默认放在：

```text
Tests/
```

工具脚本默认放在：

```text
Tools/
```

---

## Vite 使用规则

Web Demo 阶段默认使用 Vite 或等价的本地 Web 服务。

要求：

```text
不要直接双击 index.html 运行；
优先通过 run_web_demo.bat 启动本地服务；
避免浏览器本地文件权限导致配置加载失败；
bat 文件应自动打开浏览器；
bat 文件不得依赖个人电脑的绝对路径。
```

---

## Console 规则

Console 详细规则见：

```text
DESIGN_HUB/13_DEBUG_CONSOLE.md
```

本文件只记录 Console 属于默认开发辅助功能。

Console 默认通用功能包括：

```text
音乐开关；
音效开关；
暂停 / 继续；
重置场景 / 重置 Demo；
显示 FPS。
```

开启 FPS 显示后，FPS 数值应显示在游戏画面的右下角。

---

## Smoke Test 规则

如果项目处于 Web Demo 阶段，建议提供一个 smoke test 脚本，用于快速确认：

```text
Demo 页面可以打开；
关键 DOM 节点存在；
主脚本可以加载；
没有明显控制台错误；
基础交互按钮存在。
```

Smoke Test 不代替正式测试，只用于快速确认 Demo 是否能跑。

---

## 禁止事项

```text
不要把开发辅助功能写成正式玩法；
不要让 Console 成为玩家必须使用的功能；
不要让 bat 文件依赖个人电脑绝对路径；
不要把项目特定作弊功能默认放入模板；
不要因为开发辅助功能引入复杂依赖；
不要把 Web Demo 启动方式绑定到某台电脑的本地路径；
不要默认要求安装复杂工具链，除非任务明确允许。
```

---

## 后续可扩展功能

以下功能可以后续根据项目需要加入，但不作为第一版默认必需项：

```text
一键打包；
一键运行全部测试；
一键清理缓存；
自动刷新；
开发模式 / 展示模式切换；
截图按钮；
导出状态；
导入状态；
性能统计面板。
```