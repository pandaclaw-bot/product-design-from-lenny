# Output Layer: Product Plan Standard

Write a polished product-plan document using this structure.

## Required structure

```md
# 产品策划书

## 1. 执行摘要

## 2. 市场痛点与机会

## 3. 产品方案概述

## 4. 目标市场与客户画像
- 用户
- 买方
- 决策者
- 第一批切入客户

## 5. 价值逻辑
- 客户买到的结果
- 为什么愿意切换
- 为什么愿意付费

## 6. 商业模式与定价逻辑
- 收费对象
- 收费单位
- 价格结构逻辑

## 7. GTM（Go-To-Market，市场进入）策略
- 第一批客户
- 信任机制
- 激活点
- 扩张路径

## 8. 竞争与替代分析

## 9. 风险与应对
- Top 3 风险
- 最脆弱假设

## 10. 里程碑规划

## 11. 当前结论
- 主商业路径
- 备选路径

## 12. 评估摘要
- 综合分
- 阈值
- 评估模式
- 结论
- 最弱项
- 适用性

### 维度评分
- 问题与市场张力：x/10 — 原因
- 产品价值逻辑：x/10 — 原因
- 商业模式质量：x/10 — 原因
- GTM 现实性：x/10 — 原因
- 定价合理性：x/10 — 原因
- 竞争与防御性：x/10 — 原因
- 风险诚实度：x/10 — 原因
- 证据水平：x/10 — 原因
- 团队 / 创始人可信度：x/10 — 原因（如适用）
- 财务合理性：x/10 — 原因（如适用）

### 修改建议
- 建议 1
- 建议 2
- 建议 3
```

## Writing rules

- Write like a sober strategic document, not a hype memo.
- Make commercial logic explicit.
- Keep claims tied to assumptions and evidence.
- Use professional, compact language.
- When using abbreviations such as GTM, spell out the full term on first mention and, when helpful, include a Chinese explanation.

## Review checklist

Before finishing, check:
- is there a real path from value to revenue?
- are buyer and user separated where necessary?
- is GTM more than a channel list?
- is pricing logic coherent?
- are the key risks real and concrete?
- does the plan avoid collapsing into PRD-level detail?
- does the plan state both a main path and a fallback path?

## Delivery rule

Default to a stable deliverable, not a chat-only answer.
When the user explicitly asks to use this skill, treat the output as a final artifact unless they clearly ask for draft-only or chat-only mode.

Preferred delivery behavior:
- produce the full document in final form
- if working inside a repository or document workspace, write it to a file in an appropriate project folder
- use the chat reply to summarize what was generated, not to replace the artifact itself

The evaluation summary is mandatory.
Do not deliver only a total score.
Always include:
- overall score
- threshold used
- evaluation mode used
- pass / conditional fail / fail
- weakest remaining area
- dimension-by-dimension score with one-line reasoning
- 2-3 concrete revision suggestions
