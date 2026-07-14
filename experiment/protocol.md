# Experiment protocol

## Research question

How does the framing of a policy and design problem affect the diversity, feasibility, and evaluability of solutions proposed by generative AI systems?

This experiment does **not** test whether AI can prove that one bottle-cap policy is environmentally superior. It tests whether different prompts encourage broader or narrower search over a solution space.

## Hypotheses

- **H1 — Prescriptive framing:** Models given an attached-cap requirement will mostly optimize the mandated mechanism.
- **H2 — Outcome framing:** Models given a technology-neutral environmental objective will propose a wider range of product, infrastructure, incentive, and system-level interventions.
- **H3 — Evaluation framing:** Requiring pilots, failure modes, and rejection criteria will reduce unsupported novelty and improve testability.
- **H4 — Context effect:** Revealing that the task concerns beverage caps may make outputs less diverse because models retrieve familiar regulatory patterns.

## Conditions

Use the same model settings and number of runs in every condition.

### A. Blind, outcome-based

Use `problem-brief-blind.md`. Do not reveal that the component is a bottle cap.

### B. Revealed, outcome-based

Use the same brief but replace “closure component” with “plastic bottle cap” and “main container” with “plastic beverage bottle.”

### C. Prescriptive regulation

Tell the model that caps must remain attached during intended use. Ask it to propose the best compliant design and implementation plan.

### D. Outcome-based plus adversarial evaluator

Run condition B, then give the concepts to a second model or separate context. Ask it to identify hidden assumptions, lifecycle trade-offs, accessibility failures, gaming, rebound effects, and missing evidence.

### E. Human baseline

Ask a small group of people with mixed backgrounds to complete condition B individually. This is not a representative population; it provides a useful comparison for idea categories and blind spots.

## Models and repetitions

A modest first run:

- 3 models from at least 2 providers or model families;
- 5 independent runs per model and condition;
- fixed temperature and output format within each model;
- record model version, date, system prompt, sampling parameters, and raw response.

This yields 3 × 4 × 5 = 60 AI responses before the optional human baseline.

## Primary outcomes

### Solution-space breadth

Count distinct intervention categories represented:

- product geometry;
- materials;
- manufacturing;
- recycling and sorting;
- collection infrastructure;
- deposit or economic incentive;
- information or behavioural intervention;
- regulation or compliance mechanism;
- monitoring and measurement;
- system-level combination.

### Within-response diversity

Measure whether five proposed concepts are genuinely different rather than cosmetic variants.

### Testability

Score whether each concept contains a measurable hypothesis, pilot design, comparison baseline, and rejection condition.

### Feasibility

Use independent human ratings for technical plausibility, implementation complexity, likely cost, accessibility, and compatibility with existing systems.

### Unsupported confidence

Record strong empirical or environmental claims that lack evidence or are not explicitly labelled as assumptions.

## Secondary outcomes

- novelty relative to other responses;
- presence of lifecycle thinking;
- attention to accessibility;
- attention to behavioural adaptation;
- explicit uncertainty;
- whether the model recommends a portfolio rather than a single “magic” solution.

## Evaluation procedure

1. Randomize and anonymize responses.
2. Remove model and condition identifiers.
3. Have at least two raters score a subset independently.
4. Resolve unclear rubric definitions before scoring the full dataset.
5. Report agreement for categorical and ordinal ratings.
6. Keep raw outputs and final scores public when licensing and provider terms permit.

## Analysis

The most credible result is descriptive, not grandiose:

- compare category coverage by condition;
- compare mean and median rubric scores;
- show distributions and representative examples;
- report overlap between raters;
- discuss prompt sensitivity and model-version limitations.

Avoid presenting small rating differences as proof of general AI creativity or as evidence that a policy was wrong.

## Stronger optional extension

Turn the best concepts into a structured concept-selection exercise with packaging, recycling, accessibility, and lifecycle specialists. Ask experts not only which ideas they like, but which assumptions fail and what experiments would discriminate between alternatives.

## Reproducibility checklist

Store:

- exact prompts;
- raw model responses;
- timestamps and model identifiers;
- generation settings;
- anonymized rating sheets;
- rubric version;
- analysis scripts;
- exclusions and protocol deviations.

## Ethical and interpretive limits

- Generated ideas are hypotheses, not validated engineering designs.
- Environmental impact requires lifecycle and system-level evidence.
- A language model may reproduce well-known ideas rather than invent new ones.
- The experiment compares prompting conditions, not Europe with another region.
- The essay may use the experiment as an illustration, but should distinguish measured findings from political interpretation.