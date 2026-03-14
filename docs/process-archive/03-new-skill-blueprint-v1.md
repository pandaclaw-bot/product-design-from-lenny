# 基于 Lenny 访谈摘要层的新 Skill 蓝图 v1

- 日期：2026-03-12
- 状态：重构版蓝图（已被 v2 三段式架构补充和上位替代）
- 目的：替代上一版“多 persona 产品辩论 skill 组”方案

---

## 1. 重构结论

上一版 skill 设计过于偏“产品讨论工作台”，范围容易继续滑向：
- PRD
- 页面流程
- 字段设计
- 实现方案

而当前已经明确新的边界：

> Skill 的职责只到：
> 1. 产品研讨后的明确定位
> 2. 商业计划书

因此，新版 skill 不再沿用之前那组：
- lenny-product-debate-orchestrator
- lenny-pmf-critic
- lenny-experience-architect
- lenny-growth-strategist
- lenny-business-modeler
- lenny-ai-product-thinker

这些旧 skill 视为**探索版方案**，不再作为正式蓝图。

---

## 2. 新版 skill 体系

新版只保留 **2 个正式用户侧 skill + 1 个内部支撑层**。

### 正式 skill A
`lenny-product-positioning`

### 正式 skill B
`lenny-business-plan`

### 内部支撑层（不是主要用户入口）
`derived-insight-layer`

说明：
- `derived-insight-layer` 不是直接给最终用户调用的 skill，而是 skill 所依赖的“观点蒸馏参考层”
- 它的产物是摘要型 reference 文档，而不是 transcript 原文

---

## 3. 总体原则

### 原则 1：不直接把 transcript.md 当常驻 reference
skill reference 应优先使用“观点摘要层”。
只有必要时，才回溯具体 transcript。

### 原则 2：产品定位和商业计划书拆开
两者相关，但不是一回事。
- 产品定位关注：做什么、给谁做、为什么成立
- 商业计划书关注：怎么成为一门生意、如何增长、为何能赢

### 原则 3：skill 到战略层为止
不向下游延伸到：
- PRD
- 原型
- 数据模型
- 页面与字段
- 技术实现

### 原则 4：先形成稳定方法论摘要，再驱动 skill
技能不是“访谈原文检索器”，而是“基于提炼观点的决策辅助器”。

---

## 4. 共享 reference 层蓝图

后续 reference 分三层：

### Layer 1：分类摘要层
已开始形成：
- `docs/lenny-derived-insights/01-核心观点分类摘要-v1.md`
- `docs/lenny-derived-insights/02-skill-reference-拆分建议.md`

### Layer 2：skill 专用摘要层
后续应拆成：
- `references/positioning-core-views.md`
- `references/business-plan-core-views.md`
- `references/gtm-core-views.md`
- `references/pricing-core-views.md`
- `references/ai-product-core-views.md`

### Layer 3：按需回溯 transcript 层
只在以下情况使用：
- 某位嘉宾的特殊案例很关键
- 某个类别观点不够清晰
- 需要验证摘要是否遗漏差异

---

## 5. Skill A：lenny-product-positioning

## 5.1 目标
把一个模糊产品想法，收敛成：
- 明确产品定位
- ICP
- 核心价值主张
- 切入场景
- 差异化表达
- 战略路径

## 5.2 边界
### 包含
- 问题定义
- 用户与场景选择
- category frame / positioning frame
- 为什么现在做
- 切口与扩展路径

### 不包含
- PRD
- 页面设计
- 功能清单细化到执行层
- 字段与流程拆解

## 5.3 主要 reference
优先读取：
- `positioning-core-views.md`
- `pmf-core-views.md`
- `ai-product-core-views.md`（如果 AI 是核心）

必要时回溯：
- April Dunford
- Casey Winters
- Mike Maples Jr
- Gibson Biddle
- Brian Chesky
- Karri Saarinen

## 5.4 适用问题
当用户想回答以下问题时触发：
- 这个产品到底怎么定位？
- 先切哪个客户和场景？
- 为什么现在值得做？
- 和现有替代方案相比，差异在哪？
- 一句话应该怎么讲清？

## 5.5 输出结构
固定输出：
1. 一句话定位
2. 目标客户（ICP）
3. 核心问题与替代方案
4. 核心价值主张
5. 切入场景
6. 差异化表达
7. 为什么现在成立
8. 三阶段战略路径

## 5.6 内部 persona 视角
不是拆成多个独立 skill，而是在 skill 内部采用 4 个固定分析镜头：
- PMF 镜头
- 定位镜头
- AI 镜头（如适用）
- 产品叙事镜头

这样比一堆独立 persona skill 更收敛。

## 5.7 建议 skill description 方向
应强调触发词：
- 产品定位
- 产品方向
- ICP
- 价值主张
- 切入场景
- 差异化
- 为什么现在做

---

## 6. Skill B：lenny-business-plan

## 6.1 目标
把已相对清晰的产品定位，扩展为一份结构完整的商业计划书。

## 6.2 输入前提
理想情况：先有 `lenny-product-positioning` 的输出。

如果用户直接给一个产品想法，也可以工作，但应先做轻量定位收敛，再进入商业计划书阶段。

## 6.3 边界
### 包含
- 市场机会
- 商业模式
- 定价逻辑
- GTM
- 竞争分析
- 风险与里程碑

### 不包含
- PRD
- 销售执行手册
- 财务模型精算版
- 研发实施路线

## 6.4 主要 reference
优先读取：
- `business-plan-core-views.md`
- `gtm-core-views.md`
- `pricing-core-views.md`
- `ai-product-core-views.md`（如适用）

必要时回溯：
- Gibson Biddle
- Madhavan Ramanujam
- Jeanne Grosser
- Brian Balfour
- Sean Ellis
- Tamar Yehoshua
- Mike Krieger

## 6.5 适用问题
当用户想回答以下问题时触发：
- 这是不是一门生意？
- 市场空间怎么讲？
- 商业模式怎么设计？
- 怎么收费？
- GTM 怎么走？
- 为什么能赢？
- 风险和里程碑怎么写？

## 6.6 输出结构
固定输出：
1. 执行摘要
2. 市场痛点与机会
3. 产品方案概述
4. 目标市场与客户画像
5. 商业模式与定价思路
6. GTM 策略
7. 竞争与替代分析
8. 风险与应对
9. 里程碑规划
10. 当前结论

## 6.7 内部 persona 视角
同样不拆成多个公开 persona skill，而是内部使用 5 个分析镜头：
- 市场机会镜头
- 商业模式镜头
- GTM 镜头
- 竞争战略镜头
- AI/产品可扩展性镜头

## 6.8 建议 skill description 方向
应强调触发词：
- 商业计划书
- 商业模式
- GTM
- 定价
- 市场机会
- 竞争分析
- 风险与里程碑

---

## 7. 两个 skill 的衔接方式

建议采用强顺序：

### Step 1
先跑 `lenny-product-positioning`

### Step 2
把其输出作为 `lenny-business-plan` 的标准输入

### 原因
因为商业计划书不应该替代产品定位。
如果上游定位模糊，下游商业计划书通常会变空、变泛、变像模板作文。

---

## 8. 需要废弃的旧设计思路

新版蓝图明确不再采用以下思路：

### 不再采用 1：大量 persona skill 并行辩论
问题：
- 太容易扩散
- 输出不够收敛
- 更像 brainstorming，不像正式 skill

### 不再采用 2：skill 里直接挂大量 transcript reference
问题：
- 上下文成本高
- 不稳定
- 容易退化成“检索访谈原文”

### 不再采用 3：skill 继续往 PRD 和实现层延伸
问题：
- 边界失控
- 产出混杂
- 不利于复用

---

## 9. 下一步最合理的动作

按照这个蓝图，后续应这样推进：

### 第一步：补 skill 专用摘要层
优先补 4 份：
1. `positioning-core-views.md`
2. `business-plan-core-views.md`
3. `gtm-core-views.md`
4. `pricing-core-views.md`

### 第二步：写两个新 skill 的 SKILL.md 草案
- `lenny-product-positioning`
- `lenny-business-plan`

### 第三步：设计两个 skill 的输入/输出模板
保证稳定触发与稳定输出。

---

## 10. 最终结论

新版 skill 蓝图应从“多 persona 产品推演器”收缩为：

### 正式对外的 2 个 skill
- `lenny-product-positioning`
- `lenny-business-plan`

### 一个共享的观点蒸馏 reference 层
- 不直接堆 transcript
- 先摘要，再供 skill 复用

这套结构更稳、边界更清晰，也更符合你现在想要的结果。