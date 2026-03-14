---
name: lenny-product-plan
description: Turn a product idea or positioning into a structured product plan. Use when the user needs help turning a product direction into a concrete planning document covering market opportunity, who pays, pricing logic, market entry, competition, major risks, and strategic milestones. Trigger even when the user does not explicitly ask for a product plan but is really asking for commercial logic, GTM strategy, pricing, market opportunity framing, competitive analysis, or how to turn a product direction into a viable plan.
---

# Lenny Product Plan

Use this skill to convert a product thesis or positioning into a structured product plan focused on product strategy, market opportunity, pricing, GTM, competition, and key risks.

This skill has four internal layers:
- **Brain**: business logic, GTM principles, pricing logic, defensibility and AI commercialization checks
- **Hands**: multi-analyst debate and convergence workflow
- **Output**: professional product-plan generation and review
- **Evaluation**: score the draft, decide whether it passes, and force revision when needed

## Read in this order

1. `references/brain.md`
2. `references/gtm.md`
3. `references/pricing.md`
4. `references/workflow.md`
5. `references/output-standard.md`
6. `references/evaluation-standard.md`

Prefer derived insights and method files over raw transcripts.

## Scope

### In scope
- market opportunity framing
- buyer and user logic
- commercial model and pricing direction
- GTM strategy
- competitive and substitute analysis
- key risks and milestones

### Out of scope
- PRD
- detailed sales playbooks
- implementation plans
- detailed financial model spreadsheets
- org charts and execution planning below strategy level

## Execution protocol

### Step 0: Start from a product thesis
Use the output of `lenny-product-positioning` if available.
If not available, first do a light positioning pass before writing the product plan.

If the user provides multiple candidate ideas, switch to **batch screening mode** first:
- do a light commercial assessment across all ideas
- score them comparatively
- shortlist the strongest candidates
- only write full product plans for the finalists

### Step 1: Run the internal analysts
Use five internal lenses:
1. Market Analyst
2. Business Model Analyst
3. GTM Analyst
4. Competition Analyst
5. AI Commercialization Analyst (if AI is core)

Each lens must produce:
- strongest reason the business could work
- biggest weakness
- the most important assumption to validate

### Step 2: Force disagreement
Require each lens to challenge another lens.
Examples:
- a large market does not imply a realistic entry path
- a working product does not imply a healthy revenue model
- AI capability does not imply defensibility
- initial traction does not imply scalable GTM

### Step 3: Converge
Produce:
- one recommended commercial path
- one fallback path
- the top three risks
- the claims that should not be overstated

### Step 4: Write the product plan
Use the structure in `references/output-standard.md`.

### Step 5: Evaluate before delivery
Use `references/evaluation-standard.md`.

- If the user provides an explicit evaluation threshold, use it.
- Otherwise default to **7/10** for internal-strategy quality.
- If the user explicitly asks for an external/investor-facing version, default to **8/10**.
- Score the draft across the required dimensions.
- If the overall score is below threshold, revise internally and re-evaluate.
- Do not deliver a final product plan that fails the threshold unless missing inputs make passing impossible. In that case, clearly say what evidence or inputs are missing.

## Quality bar

A strong product plan must:
- connect value to willingness to pay
- distinguish user, buyer, and economic decision maker
- explain the initial GTM wedge
- show how the business expands after the first wedge
- avoid using TAM and AI as lazy substitutes for commercial reasoning
- name the primary commercial path and one fallback path
- treat internal use or dogfooding as an initial wedge, not as proof of broad demand
- stay commercially rigorous rather than drifting back into product-spec writing

## Final check

Before finishing, verify:
- does the business model fit the value logic?
- is the GTM path realistic for the current stage?
- are the key risks honest rather than ceremonial?
- is the pricing logic defensible?
- would this document survive a skeptical review?
- are buyer, user, and payer clearly separated?
- does the document avoid pretending that "AI" is the moat by itself?
