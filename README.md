# Product Design from Lenny

一个可复用的产品设计 Skill。它从 Lenny’s Podcast 的高质量产品讨论中提炼而来，并被重新整理成适合 OpenClaw、Claude Code、Codex 等 agent / IDE 工作流使用的公开项目。

这个项目不只放最终 Skill 成品，也保留了这个 Skill 是如何被构建、收敛、修订和整理成可复用模块的过程。

## 这个项目包含什么

- `SKILL.md`：Skill 主文件
- `references/`：参考材料与可复用方法笔记
- `docs/`：设计思路、演化过程、构建方法
- `examples/`：示例 prompt 与用法

## 这个 Skill 是做什么的

当你希望 agent 帮你做更结构化的产品规划、功能设计、MVP 范围收敛时，可以使用这个 Skill。

典型场景包括：
- 把一个模糊产品想法整理成更清晰的产品方案
- 为某个功能或工作流做结构化设计
- 生成适合讨论的产品 proposal
- 借鉴高质量产品访谈中的方法论，而不是只做泛泛 brainstorming

## 这个 Skill 不打算做什么

这个项目刻意保持边界，不打算变成：
- 一个包打天下的产品全栈系统
- 任何场景都通吃的 PRD 生成器
- 用户研究的替代品
- 原始 transcript 的资料仓库

## 下载与安装

### 方式一：直接克隆仓库

```bash
git clone <你的公开仓库地址>
cd product-design-from-lenny
```

### 方式二：只复制 Skill 文件

最少需要保留：

- `SKILL.md`
- `references/`

如果你的运行环境支持 Skill 文件夹加载，请保持目录结构不变。

## 如何在 OpenClaw 中使用

推荐目录结构：

```text
skills/
└── product-design-from-lenny/
    ├── SKILL.md
    └── references/
```

你可以把这个项目整个克隆到本地后，再将 `product-design-from-lenny/` 复制或软链接到你的 OpenClaw skills 目录。

推荐步骤：

1. 克隆这个仓库到本地
2. 将 Skill 目录复制或软链接到 OpenClaw 的 `skills/` 目录
3. 如有需要，重启或重新加载 agent 环境

在 OpenClaw 中的典型调用方式：

```text
使用 product-design-from-lenny skill，把下面这个想法整理成结构化产品方案，重点分析用户、痛点、MVP 范围、工作流、风险和成功指标。
```

## 如何适配 Claude Code

Claude Code 不使用 OpenClaw 原生 Skill 打包机制，所以更实用的方式是：把这个项目当作一个可复用的 prompt + reference 模块。

推荐两种方式：

### 方式一：作为本地参考目录

- 把这个仓库放在你的项目旁边
- 在任务开始前，让 Claude Code 先读取 `SKILL.md` 和相关 docs

示例：

```text
Read ./product-design-from-lenny/SKILL.md and use it as the working framework for this task. Then design an MVP for the following product idea...
```

### 方式二：作为团队通用 prompt 资产

- `SKILL.md` 作为核心指令文件
- `references/` 作为可选补充阅读
- `examples/` 作为团队 onboarding 示例

这样适合把它沉淀成团队内部统一的产品设计工作流。

## 如何适配 Codex / 其他 IDE Agent

对于 Codex 风格的 coding agent，最适合把这个项目当成 repo-local 的工作流模块。

推荐方式：

### 方式一：放到仓库内部

```text
.ai/
  skills/
    product-design-from-lenny/
```

然后这样提示 agent：

```text
Read ./.ai/skills/product-design-from-lenny/SKILL.md and use that framework to design the product plan before writing implementation tasks.
```

### 方式二：指令层 / 方法层 / 示例层拆开

- `SKILL.md` = 操作指令
- `docs/` = 设计 rationale 与构建思路
- `references/` = 更深的方法笔记
- `examples/` = few-shot 示例

这种结构适合 Codex、Claude Code、Cursor、Windsurf 等文件驱动的 agent 环境。

## 为什么它能跨环境复用

这个项目之所以适合在不同 agent 环境中复用，是因为它把内容拆成了几层：

- 可复用的指令层
- 方法与设计思路层
- 示例层

这意味着你可以：
- 在支持 Skill 文件夹的环境里把它当成原生 Skill 使用
- 在不支持原生 Skill 的环境里把它当成 prompt framework 使用
- 在团队内部把它当作一个通用产品设计模块使用

## 建议的公开仓库结构

```text
product-design-from-lenny/
├── README.md
├── SKILL.md
├── docs/
├── references/
└── examples/
```

## 如果你想看这个 Skill 是怎么构建出来的

建议从这些文档开始：

- `docs/01-project-overview.md`
- `docs/02-how-the-skill-was-built.md`
- `docs/03-design-evolution.md`
- `docs/04-public-repo-boundary.md`

如果你想看更细的过程记录，可以继续看：

- `docs/process-archive/`

## 发布前检查清单

在把它长期公开分享之前，建议确认：

- 没有混入私有客户材料
- 没有混入个人 workspace 文件
- 没有混入大文件或原始数据文件
- 示例内容适合公开
- README 与最终目录结构一致

## 当前状态

这是从一个更大的私有工作仓库中整理出来的公开项目版本。
后续还可以继续补：

- 更正式的 README 结构
- LICENSE
- 更完整的示例
- 更清晰的版本记录
