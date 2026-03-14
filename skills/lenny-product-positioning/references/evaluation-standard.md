# Evaluation Layer: Product Positioning

Use this file to score the positioning draft before delivery.

## 1. Purpose

Do not treat evaluation as an appendix. Use it as a gate.
The goal is to prevent weak positioning drafts from being delivered as final output.

This evaluation is not a vibe check.
It is a structured review of whether the positioning is stable enough to become:
- a final positioning deliverable
- the input to a downstream product plan
- a reusable strategy narrative

## 2. Default threshold

- Use the user's threshold if explicitly provided.
- Otherwise default to **7/10**.

## 3. How scoring works

Score 8 dimensions.
Each dimension gets a score from **1 to 10**.

Use the anchor points below as the primary guide:
- **1** = almost unusable
- **3** = weak / vague
- **5** = partially formed but not stable
- **7** = solid internal-strategy quality
- **9** = unusually sharp and reusable

Scores such as 6 or 8 are allowed when the draft sits between two anchors.

### Overall score

Compute the overall score as the **average of the 8 dimensions**, rounded to one decimal place.

## 4. Required scoring dimensions

### A. ICP clarity
Question: Is the target customer concrete, narrow, and commercially usable?

**1**
- target customer is missing or nearly meaningless
- sounds like "everyone" or a giant market bucket

**3**
- mentions a broad user category
- no clear first wedge or first customer segment

**5**
- user type is visible
- but first customer segment is still too wide or mixed

**7**
- first customer wedge is reasonably clear
- organization type and key roles are mostly specific

**9**
- first customer wedge is very sharp
- organization traits, key roles, buying context, and likely first adopters are all visible

### B. Problem sharpness
Question: Is the problem real, costly, specific, and described in market language?

**1**
- problem is unclear or generic
- mostly buzzwords or abstract dissatisfaction

**3**
- problem exists, but is described vaguely
- cost of the pain is not clear

**5**
- the pain is real, but still not sharp enough to feel urgent
- language is partly abstract

**7**
- problem is concrete and credible
- the cost, friction, or risk is visible

**9**
- problem is sharp enough that the buyer urgency is obvious
- the draft makes clear why this is painful, costly, and hard to ignore

### C. Alternative awareness
Question: Does the draft clearly show what users do today and why they would switch?

**1**
- no current alternatives identified
- no switching logic

**3**
- gestures at alternatives, but without specificity
- switching reason is weak

**5**
- some alternatives are named
- but the transition logic remains incomplete

**7**
- current alternatives are clearly identified
- the reason to switch is mostly explicit

**9**
- alternatives are mapped clearly
- the switch logic is compelling, concrete, and hard to misunderstand

### D. Category frame quality
Question: Can the market quickly understand what kind of product this is?

**1**
- no category frame at all
- or frame is actively confusing

**3**
- frame exists, but is fuzzy or overloaded
- likely to confuse users or buyers

**5**
- frame is serviceable
- but not yet clearly advantageous

**7**
- frame is understandable and useful
- it helps people place the product quickly

**9**
- frame is unusually effective
- it makes the product feel both understandable and strategically distinct

### E. Differentiation quality
Question: Is the differentiation structural, not adjective-based?

**1**
- no real differentiation
- relies on empty claims like better / smarter / easier

**3**
- differentiation is mostly cosmetic or slogan-based

**5**
- some real differences exist
- but they are not yet strong enough to anchor positioning

**7**
- differentiation is real and mostly structural
- it is tied to workflow, model, data, process, trust, or execution advantage

**9**
- differentiation is sharp, structural, and memorable
- the product feels meaningfully distinct from alternatives

### F. Why-now strength
Question: Does the draft explain why this matters now, not just in theory?

**1**
- no timing logic
- could have been written at any time

**3**
- weak timing language such as trends or hype
- no real trigger behind urgency

**5**
- timing rationale exists
- but still feels generic or under-supported

**7**
- timing logic is specific and believable
- the draft shows why this is newly possible or newly urgent

**9**
- why-now is unusually strong
- technical, policy, organizational, or cost shifts clearly create a window

### G. Narrative compression
Question: Can the positioning be compressed into a memorable one-liner?

**1**
- no usable one-liner
- cannot be repeated accurately

**3**
- one-liner exists, but is bloated or forgettable

**5**
- one-liner is understandable
- but not yet crisp or reusable

**7**
- one-liner is reasonably sharp and repeatable
- the main narrative can be retold without losing meaning

**9**
- one-liner is compact, memorable, and reusable
- it could survive in meetings, decks, and sales conversations

### H. Strategic coherence
Question: Do wedge, problem, frame, differentiation, and expansion path fit together?

**1**
- major contradictions across the document
- the strategy does not hang together

**3**
- several parts look plausible individually
- but they do not form a coherent whole

**5**
- broad coherence exists
- but there are still visible tensions or mismatches

**7**
- the strategy is mostly coherent end to end
- wedge, frame, differentiation, and next-step expansion support each other

**9**
- the whole positioning feels tightly integrated
- each section reinforces the others with very little internal tension

## 5. Pass / fail logic

### Pass
- overall score >= threshold
- no dimension below **6/10**

### Conditional fail
- overall score >= threshold
- but one or more dimensions are below **6/10**
- revise the weak dimensions and re-evaluate

### Fail
- overall score < threshold
- revise and re-evaluate

## 6. Revision protocol

If the draft fails:
1. identify the weakest 2-3 dimensions
2. explain why they are weak in plain language
3. revise the draft specifically for those weaknesses
4. re-score
5. only deliver once it passes

If it still cannot pass because inputs are missing, state:
- what information is missing
- which dimensions are blocked
- what minimum input is needed to pass

## 7. Delivery format

When delivering to the user, include a short evaluation summary with:
- final overall score
- threshold used
- pass / conditional fail / fail
- weakest remaining area
- suitability: internal strategy / external use

Also include a compact score breakdown in this form:

```md
## 评估摘要

- 综合分：7.4 / 10
- 阈值：7 / 10
- 结论：通过

### 维度评分
- ICP 清晰度：7/10 — 用户轮廓清楚，但首批行业切口还可再收窄
- 问题尖锐度：8/10 — 痛点具体，且与成本/风险挂钩
- 替代方案认知：7/10 — 已识别主要替代，但切换路径还能更明确
- 品类框架质量：8/10 — framing 清楚，利于传播
- 差异化质量：7/10 — 有结构差异，但还可更锋利
- why-now 强度：7/10 — 逻辑成立，但部分论据仍偏泛
- 叙事压缩度：7/10 — 一句话可复述，但记忆点还可更强
- 战略一致性：8/10 — 主线基本连贯

```

## 8. Usage note

Treat this score as a structured review result, not false precision.
The purpose is not to pretend the number is objective.
The purpose is to make evaluation consistent, debuggable, and revision-friendly.
