# Lenny 产品策略 Skills

这是一个公开项目，核心内容是两份正式技能：

- `lenny-product-positioning`
- `lenny-product-plan`

它们不是临时拼出来的提示词，而是从真实构建、试跑、收敛后的正式方法里整理出来的。

这个仓库既包含最终技能，也包含这两份技能是如何被设计出来、如何收敛边界、如何加入评估层、如何从探索版演化成正式版的过程文档。

## 仓库内容

```text
.
├── README.md
├── skills/
│   ├── lenny-product-positioning/
│   └── lenny-product-plan/
├── examples/
└── docs/
```

### `skills/lenny-product-positioning`
用于把一个模糊产品想法收敛成清晰定位，包括：
- 目标客户
- 核心问题
- 替代方案
- 价值主张
- 品类定位
- 切入口
- 差异化
- 为什么现在值得做
- 战略路径

### `skills/lenny-product-plan`
用于把一个产品假设或产品定位扩展成结构化产品策划书，包括：
- 市场机会
- 用户、购买者、付款者逻辑
- 商业模式
- 定价思路
- 市场进入路径
- 竞争与替代分析
- 风险与里程碑

## 这两个技能的关系

推荐顺序：

1. 先用 `lenny-product-positioning`
2. 再用 `lenny-product-plan`

原因很简单：
如果定位没有收敛，产品策划书通常会写得很空、很泛、很像模板作文。

## 这套技能的内部结构

两份技能都不是单层提示词，而是四层结构：

- **方法层**：方法论、判断框架、核心观点
- **执行层**：多分析视角的执行、质疑与收敛流程
- **输出层**：标准化输出结构与写作要求
- **评估层**：先打分，不达标就回炉，而不是直接交稿

## 为什么这个项目值得公开

这个仓库不只是给别人“拿去用”。
它也尽量保留了构建过程，让外部读者能看懂：

- 为什么从一组探索版技能收敛成两份正式技能
- 为什么不直接把访谈原文当成技能的大脑
- 为什么要加方法层、执行层、输出层、评估层
- 为什么要加批量筛选模式
- 为什么要把边界收在“定位 + 产品策划书”，而不是一路滑向产品需求文档与实现方案

## 下载与安装

### 方式一：直接克隆

```bash
git clone https://github.com/pandaclaw-bot/product-design-from-lenny.git
cd product-design-from-lenny
```

### 方式二：只复制某一个技能

如果你只想用其中一个技能，可以只复制对应目录，例如：

- `skills/lenny-product-positioning/`
- `skills/lenny-product-plan/`

## 在 OpenClaw 中使用

推荐目录结构：

```text
skills/
├── lenny-product-positioning/
│   ├── SKILL.md
│   └── references/
└── lenny-product-plan/
    ├── SKILL.md
    └── references/
```

使用方式：

1. 将本仓库克隆到本地
2. 把 `skills/` 下需要的技能目录复制或软链接到 OpenClaw 的技能目录
3. 如有需要，重启或重新加载智能体环境

示例提示词：

```text
使用 lenny-product-positioning 技能，把下面这个想法整理成清晰的产品定位，重点给出目标客户、价值主张、切入口、差异化和为什么现在值得做。
```

```text
使用 lenny-product-plan 技能，基于已有产品定位，输出一份结构化产品策划书，重点分析市场机会、商业模式、定价、市场进入路径、竞争与风险。
```

## 如何适配 Claude Code

Claude Code 不走 OpenClaw 原生技能机制，更适合把这两个技能当成仓库内可复用的提示词模块。

推荐做法：

### 方式一：直接读取 `SKILL.md`

```text
先阅读 ./skills/lenny-product-positioning/SKILL.md，并按其中的方法完成这次任务。
```

或者：

```text
先阅读 ./skills/lenny-product-plan/SKILL.md，并把它作为本次任务的工作框架。
```

### 方式二：连同参考文件一起读取

如果任务更复杂，可以明确要求智能体连同参考文件一起读：

```text
先阅读 ./skills/lenny-product-positioning/SKILL.md 及其 references，再输出最终的产品定位文档。
```

## 如何适配 Codex、Cursor、Windsurf 等开发环境智能体

这套仓库适合用作一个仓库内的策略技能模块。

推荐放法：

```text
.ai/
  skills/
    lenny-product-positioning/
    lenny-product-plan/
```

然后提示智能体：

```text
先阅读 ./.ai/skills/lenny-product-positioning/SKILL.md，再基于这个框架收敛产品方向，然后再讨论实现。
```

或：

```text
先阅读 ./.ai/skills/lenny-product-plan/SKILL.md，再判断这个想法能否成为一门生意，然后再讨论执行计划。
```

如果你需要英文版适配说明，请看：

- `docs/en/adapter-guide.md`

## 当你给一个产品想法时，这个技能会怎么跑

### `lenny-product-positioning`
大致执行顺序是：

1. 标准化输入说明
2. 收敛目标用户与核心场景
3. 分析问题强度与替代方案
4. 提炼价值主张与品类定位
5. 生成主定位与备选定位
6. 输出结构化定位文档
7. 按评估标准打分
8. 不达标则内部修订后再交付

### `lenny-product-plan`
大致执行顺序是：

1. 接收已有定位，或先做轻量定位收敛
2. 分析市场机会与用户、购买者、付款者逻辑
3. 推导商业模式、定价、市场进入路径和竞争逻辑
4. 生成主商业路径与备选路径
5. 输出结构化产品策划书
6. 按评估标准打分
7. 不达标则内部修订后再交付

## 示例

如果你想先快速看怎么使用，请看：

- `examples/01-单个产品想法-产品定位.md`
- `examples/02-从定位到产品策划书.md`
- `examples/03-多个想法-批量筛选.md`

## 过程文档

如果你不只是想直接使用，而是想看这两个技能是怎么被构建出来的，请看：

- `docs/process-archive/03-new-skill-blueprint-v1.md`
- `docs/process-archive/04-three-layer-skill-architecture-v2.md`
- `docs/process-archive/06-v1-refinement-notes.md`
- `docs/process-archive/07-official-skill-usage-guide-v1.md`
- `docs/process-archive/08-shareable-summary-v1.md`
- `docs/process-archive/09-build-retrospective.md`
