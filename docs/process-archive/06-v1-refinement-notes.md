# Skill v1 精修记录

- 日期：2026-03-13

## 本轮精修内容

### 1. 探索版 skill 已归档
正式保留：
- `skills/lenny-product-positioning`
- `skills/lenny-business-plan`

### 2. Evaluation layer 已内置
两个正式 skill 都支持：
- 用户自定义阈值
- 默认阈值
- 不达标则回炉重构
- 最终交付附 evaluation summary

### 3. 根据批量试跑结果增加 Batch Screening / Portfolio Mode
原因：
- 两个 skill 原本更擅长“单题深挖”
- 当用户一次给多个候选方向时，需要先组合筛选，再深挖 Top N

已改造内容：
- `lenny-product-positioning`：支持多候选方向先做轻量定位评分与 shortlist
- `lenny-business-plan`：支持多候选方向先做轻量商业评分与 shortlist
- `lenny-business-plan` evaluation：支持多方向比较的 comparative score table

## 当前状态
正式 skill 已进入 v1 可用状态，具备：
- 单题深挖能力
- Evaluation gating
- Batch screening 能力

下一步更适合做：
- description/wording 最后一轮压缩
- 使用顺序规范
- 代表性样例沉淀
