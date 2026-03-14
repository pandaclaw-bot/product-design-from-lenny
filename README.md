# Lenny Product Strategy Skills

这是一个公开项目，核心内容是两份正式 Skill：

- `lenny-product-positioning`
- `lenny-business-plan`

它们不是从零重新编的 prompt，而是从这几天真实构建、试跑、收敛出来的一套正式方法中整理出来的。

这个仓库既包含最终 Skill，也包含这两个 Skill 是如何被设计出来、如何收敛边界、如何加入 Evaluation layer、如何从探索版演化成正式版的过程文档。

## 仓库内容

```text
.
├── README.md
├── skills/
│   ├── lenny-product-positioning/
│   └── lenny-business-plan/
└── docs/
    └── process-archive/
```

### `skills/lenny-product-positioning`
用于把一个模糊产品想法收敛成清晰定位，包括：
- ICP
- 核心问题
- 替代方案
- 价值主张
- category frame
- wedge / 切口
- differentiation
- why now
- 战略路径

### `skills/lenny-business-plan`
用于把一个产品 thesis / 定位扩展成结构化商业计划书，包括：
- 市场机会
- buyer / user / payer 逻辑
- 商业模式
- 定价思路
- GTM
- 竞争与替代分析
- 风险与里程碑

## 这两个 Skill 的关系

推荐顺序：

1. 先用 `lenny-product-positioning`
2. 再用 `lenny-business-plan`

原因很简单：
如果定位没有收敛，商业计划书通常会写得很空、很泛、很像模板作文。

## 这套 Skill 的内部结构

两份 Skill 都不是单层 prompt，而是四层结构：

- **Brain**：方法论、判断框架、核心观点
- **Hands**：多分析镜头的执行与辩论收敛流程
- **Output**：标准化输出结构与写作要求
- **Evaluation**：先打分，不达标就回炉，而不是直接交稿

## 为什么这个项目值得公开

这个仓库不只是给别人“拿去用”。
它也尽量保留了构建过程，让外部读者能看懂：

- 为什么从一堆探索版 skill 收敛成两份正式 skill
- 为什么不直接把 transcript 原文当 Skill 大脑
- 为什么要加 Brain / Hands / Output / Evaluation 这几层
- 为什么要加 batch screening / portfolio mode
- 为什么要把边界收在“定位 + 商业计划书”，而不是一路滑向 PRD 与实现

## 下载与安装

### 方式一：直接克隆

```bash
git clone https://github.com/pandaclaw-bot/product-design-from-lenny.git
cd product-design-from-lenny
```

### 方式二：只复制某一个 Skill

如果你只想用其中一个 Skill，可以只复制对应目录，例如：

- `skills/lenny-product-positioning/`
- `skills/lenny-business-plan/`

## 在 OpenClaw 中使用

推荐目录结构：

```text
skills/
├── lenny-product-positioning/
│   ├── SKILL.md
│   └── references/
└── lenny-business-plan/
    ├── SKILL.md
    └── references/
```

使用方式：

1. 将本仓库克隆到本地
2. 把 `skills/` 下需要的 Skill 目录复制或软链接到 OpenClaw 的技能目录
3. 如有需要，重启或重新加载 agent 环境

示例提示词：

```text
使用 lenny-product-positioning skill，把下面这个想法整理成清晰的产品定位，重点给出 ICP、价值主张、切入口、差异化和 why now。
```

```text
使用 lenny-business-plan skill，基于已有产品定位，输出一份结构化商业计划书，重点分析市场机会、商业模式、定价、GTM、竞争与风险。
```

## 如何适配 Claude Code

Claude Code 不走 OpenClaw 原生 Skill 机制，更适合把这两个 Skill 当成 repo-local 的可复用 prompt 模块。

推荐做法：

### 方式一：直接读取 SKILL.md

```text
Read ./skills/lenny-product-positioning/SKILL.md and follow it for this task.
```

或者：

```text
Read ./skills/lenny-business-plan/SKILL.md and use it as the working framework.
```

### 方式二：把 references 一起带入

如果任务更复杂，可以明确要求 agent 连同 references 一起读：

```text
Read ./skills/lenny-product-positioning/SKILL.md and its references before producing the final positioning document.
```

## 如何适配 Codex / Cursor / Windsurf / 其他 IDE Agent

这套仓库适合用作一个 repo-local 的策略技能模块。

推荐放法：

```text
.ai/
  skills/
    lenny-product-positioning/
    lenny-business-plan/
```

然后提示 agent：

```text
Read ./.ai/skills/lenny-product-positioning/SKILL.md first. Use it to converge the product thesis before proposing implementation.
```

或：

```text
Read ./.ai/skills/lenny-business-plan/SKILL.md first. Use it to evaluate whether this idea can become a business before drafting execution plans.
```

## 当你给一个产品想法时，这个 Skill 会怎么跑

### `lenny-product-positioning`
大致执行顺序是：

1. 标准化输入 brief
2. 收敛目标用户与核心场景
3. 分析问题强度与替代方案
4. 提炼价值主张与 category frame
5. 生成主定位与备选定位
6. 输出结构化定位文档
7. 按 evaluation 标准打分
8. 不达标则内部修订后再交付

### `lenny-business-plan`
大致执行顺序是：

1. 接收已有定位或先做轻量定位收敛
2. 分析市场机会与 buyer / user / payer 逻辑
3. 推导商业模式、定价、GTM 和竞争逻辑
4. 生成主商业路径与备选路径
5. 输出结构化商业计划书
6. 按 evaluation 标准打分
7. 不达标则内部修订后再交付

## 过程文档

如果你不只是想直接使用，而是想看这两个 Skill 是怎么被构建出来的，请看：

- `docs/process-archive/03-new-skill-blueprint-v1.md`
- `docs/process-archive/04-three-layer-skill-architecture-v2.md`
- `docs/process-archive/06-v1-refinement-notes.md`
- `docs/process-archive/07-official-skill-usage-guide-v1.md`
- `docs/process-archive/08-shareable-summary-v1.md`
- `docs/process-archive/09-build-retrospective.md`

## 开源边界

本仓库只保留：
- 两份正式 Skill
- 它们的 references
- 可公开的过程文档

不保留：
- 旧探索版 skill
- 私有 workspace 文件
- 个人 memory 文件
- 客户或业务敏感材料
- 与这两个正式 Skill 无关的其他项目

## 当前状态

这是一个已可用的公开版本，但还可以继续增强：

- 更完整的 examples
- 更标准的 license
- 更丰富的英文化说明
- 更系统的案例展示
