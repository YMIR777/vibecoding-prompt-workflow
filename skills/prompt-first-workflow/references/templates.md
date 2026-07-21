# Prompt Templates

Use the shortest template that makes the task executable. Always show the completed template before acting. Replace brackets with facts; delete irrelevant fields. If a material choice remains, show its options and wait rather than selecting one silently.

## New Project

```text
Outcome: Build [product] so [audience] can [core job].
Core flow: [start] -> [key action] -> [successful result].
Context: [existing repository, references, data, brand or technical conventions].
Scope: Include [first-release capabilities]. Exclude [explicit non-goals].
Constraints: [platform, performance, privacy, budget, compatibility, design].
Acceptance: [observable behaviors and evidence].
Deliverable: [code, plan, prototype, document] in [format].
Autonomy: [safe local actions] are authorized; confirm before [boundaries].
```

## Change Or Build

```text
Goal: Change [current behavior] to [desired behavior].
Context: [relevant files, current behavior, examples, logs].
Constraints: Preserve [compatibility or invariant]; do not change [out-of-scope areas].
Acceptance: [tests, UI states, API behavior, performance threshold].
Please read the current implementation, propose the smallest viable change, implement it, run the relevant checks, and report evidence and remaining risk.
```

## Debug

```text
Problem: [full error or incorrect behavior].
Reproduction: [steps, inputs, environment].
Expected / actual: [comparison].
Context: [logs, code, recent changes].
Constraints: [what must be preserved].
Verify the leading hypotheses with evidence. Fix only after finding the root cause, rerun the original path, and report the result and residual risk.
```

## Review

```text
Review target: [code, plan, document, design].
Decision needed: [merge, prioritize risks, choose an approach].
Review lens: [correctness, security, maintainability, performance, UX, factual accuracy].
Constraints: [compatibility, policy, deadline].
Output: Rank material findings by severity, cite the exact evidence, state assumptions, and list missing verification. Do not make edits unless requested.
```

## Research Or Explanation

```text
Question / decision: [what needs to be known or decided].
Audience and depth: [who will use it and required level].
Scope: [included and excluded topics, geography, timeframe].
Evidence: Use [source types]; label facts, interpretations, and uncertainty.
Output: [brief, comparison, recommendation, report] with [citations, table, action].
```

## Writing Or Design

```text
Deliverable: [article, page, deck, interface, image].
Audience and purpose: [reader/user and desired outcome].
Inputs: [facts, examples, brand, references].
Constraints: [length, voice, format, accessibility, forbidden claims].
Acceptance: [rubric: clarity, required sections, visual states, factual checks].
Output: [format and variants needed].
```

## Direct-Execution Override

```text
Execute directly. Do not rewrite the prompt or ask nonessential questions.
Use these fixed constraints: [constraints].
Stop and ask only if [specific high-impact ambiguity or approval boundary].
```
