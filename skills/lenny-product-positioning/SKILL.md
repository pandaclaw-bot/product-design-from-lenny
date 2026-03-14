---
name: lenny-product-positioning
description: Clarify a product idea into a sharp strategy and positioning. Use when the user needs help deciding what to build, who it is for, which problem matters most, how to frame the product, what the initial wedge should be, how it differs from alternatives, or how an AI product should be positioned. Trigger even when the user does not explicitly ask for positioning but is really asking for product direction, target users, value proposition, differentiation, category framing, why-now logic, or a clearer product narrative.
---

# Lenny Product Positioning

Use this skill to convert a vague product idea into a sharp, reusable positioning thesis.

This skill has four internal layers:
- **Brain**: positioning principles, PMF logic, AI product framing, narrative checks
- **Hands**: multi-analyst debate and convergence workflow
- **Output**: professional product positioning document generation and review
- **Evaluation**: score the draft, decide whether it passes, and force revision when needed

## Read in this order

1. `references/brain.md`
2. `references/workflow.md`
3. `references/output-standard.md`
4. `references/evaluation-standard.md`

Only read extra transcript material if the references are insufficient. Prefer the derived insights over raw transcripts.

## Scope

### In scope
- clarify the target user and wedge
- define the core problem and current alternatives
- choose a category frame
- articulate differentiated value
- explain why the product is timely now
- create a strategic narrative and expansion path

### Out of scope
- PRD writing
- page or interaction design
- field schemas
- technical implementation
- execution plans below strategy level

## Execution protocol

### Step 0: Normalize the brief
If the user provides a single idea, convert it into a compact brief:
- product idea
- target user
- core scenario
- current stage
- key constraints
- biggest unknowns

If information is missing, infer minimally and label assumptions.

If the user provides multiple candidate ideas, first switch to **batch screening mode**:
- score each idea lightly rather than writing full long-form positioning documents for all of them
- compare them on the same positioning dimensions
- shortlist the top candidates
- only run the full positioning workflow on the finalists

### Step 1: Run the internal analysts
Use four internal lenses:
1. PMF Analyst
2. Positioning Analyst
3. AI Product Analyst (if AI is core)
4. Narrative Analyst

Each lens must produce:
- strongest insight
- biggest risk
- what is too broad or unclear
- what must be true for this positioning to work

### Step 2: Force disagreement
Require at least one challenge from each lens toward another lens.
Do not let the output collapse into fake consensus too early.

### Step 3: Converge
Use a synthesis step to produce:
- one recommended positioning
- one fallback positioning
- why the recommended one is better
- what assumptions still need validation

### Step 4: Write the positioning document
Use the structure in `references/output-standard.md`.

### Step 5: Evaluate before delivery
Use `references/evaluation-standard.md`.

- If the user provides an explicit evaluation threshold, use it.
- Otherwise default to **7/10**.
- Score the draft across the required dimensions.
- If the overall score is below threshold, revise internally and re-evaluate.
- Do not deliver a final positioning document that fails the threshold unless missing inputs make passing impossible. In that case, explicitly say what information is missing and why the score cannot improve without it.

## Quality bar

A strong output must:
- identify a concrete ICP, not a broad market
- describe current alternatives clearly
- explain the switching reason
- avoid feature-list positioning
- avoid using AI as a vague adjective
- reject at least one plausible but weaker positioning direction
- produce a one-sentence positioning that is memorable and reusable
- stay at the positioning layer rather than drifting into PRD or solution sprawl

## Final check

Before finishing, verify:
- Can a user repeat the one-line positioning?
- Is the wedge narrow enough?
- Is the category frame understandable?
- Is the differentiation structural, not cosmetic?
- Is the strategy narrative coherent from wedge to expansion?
- Does the document clearly say what this product is not?
- Would this still make sense if all buzzwords were removed?
