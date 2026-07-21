---
name: prompt-first-workflow
description: Apply first-principles task framing with a bounded read-only preflight before substantive work. Use for projects, changes, debugging, reviews, research, writing, design, and other tasks where goals, context, constraints, approval boundaries, acceptance criteria, or output requirements need to be explicit. Show an executable task definition before substantive work on complex, open-ended, state-changing, or decision-bearing requests; do not force ceremonial rewrites for simple, already-clear answers or low-risk actions.
---

# Prompt-First Workflow

Turn intent into an evidence-driven task without defining it in a vacuum. Touch the minimum amount of reality needed to frame the work, then make consequential boundaries visible before substantive execution.

## First-Principles Check

Do not use "first principles" as a slogan. Reduce the request to the information needed for a reliable decision:

1. Separate known facts, unverified assumptions, and subjective preferences.
2. Identify the outcome and the constraints that cannot be violated.
3. Define observable success and the evidence that would prove it.
4. Surface choices that materially change the result and let the user decide.
5. Choose the smallest testable path after those foundations are clear.

## Operating Rules

1. Identify the outcome, user or audience, and task type before choosing an implementation path.
2. Gather only context that changes the current decision: relevant files, current behavior, examples, logs, constraints, conventions, and prior attempts.
3. Separate hard boundaries from preferences. State what is in scope, what must not change, what actions are pre-authorized, and what requires confirmation.
4. Replace subjective words such as "good," "simple," or "beautiful" with observable criteria whenever they affect acceptance.
5. Define evidence before work: tests, build output, API response, visual check, review checklist, or another concrete proof.
6. For multi-step changes, read first, plan the smallest viable slice, change it, verify it, and iterate from the result.
7. Never claim completion from plausibility. Report actual evidence, remaining risks, and the smallest useful next action.

## Bounded Read-Only Preflight

Before framing a substantive task, gather only enough local context to avoid restating false assumptions.

Allowed preflight actions:

- Read applicable instructions and project rules.
- Inspect filenames, directories, repository status, metadata, and available materials or tools.
- Confirm obvious environment constraints and whether supplied artifacts exist.

Do not use preflight to:

- Modify files or external state.
- Perform broad content analysis or external research.
- Select architecture, visual direction, product scope, or another material branch.
- Hide substantive work behind the label "preflight."

## Intake Protocol

Classify the request before choosing the amount of framing:

1. For complex, open-ended, state-changing, or decision-bearing work, run a bounded preflight when needed.
2. Restate the inferred outcome and provide a compact `Executable task definition` before substantive work.
3. Run the material-choice check below and wait only when a material branch remains.
4. For a simple, already-clear answer or low-risk action, use a one-line confirmation or answer directly. Do not restate the request ceremonially.
5. If later evidence materially changes scope, architecture, risk, acceptance, publishing, or cost, revise the task definition visibly before continuing.

Use this skeleton. Omit fields that do not affect the task rather than inventing content:

```text
Outcome:
Audience / scenario:
Relevant context:
Scope and constraints:
Success criteria / evidence:
Requested deliverable:
Autonomy and approval boundary:
```

## Material-Choice Check

Before implementation, identify decisions whose answers would materially change the deliverable, scope, safety, architecture, acceptance evidence, integration, deployment, cost, or publishing outcome.

- If no such decision remains, state the assumptions in the executable prompt and proceed.
- If one or more remain, list the choices plainly, explain the impact in one clause, and wait for the user to choose. Do not select a branch silently.
- Ask only material questions. Do not turn routine details into a questionnaire.

For reusable artifacts, check at least when relevant: artifact type(s), intended users and platforms, invocation mode, behavioral scope, language(s), installation/distribution, examples/evaluation, packaging, licensing, publishing, and maintenance.

Read [templates.md](references/templates.md) for task templates and [decision-gates.md](references/decision-gates.md) for examples of material choices. For any public release, repository creation, open-source, licensing, package publishing, or external distribution request, also read [project-release-moat.md](references/project-release-moat.md) before writing the executable prompt.

## Choose The Workflow

| Task shape | First move | Completion evidence |
|---|---|---|
| New project | Define user journey, smallest release, exclusions, and acceptance criteria | Usable core flow and relevant checks |
| Change or build | Read current state; plan the smallest change | Diff plus build/test/browser or manual check |
| Debug | Capture reproduction and expected behavior; test hypotheses | Reproduction path passes after root-cause fix |
| Review | Define review lens and severity threshold | Findings tied to concrete evidence; test gaps stated |
| Research or explanation | Define question, decision, sources, recency, and output | Claims trace to sources; uncertainty labeled |
| Writing or design | Define audience, purpose, constraints, examples, and acceptance rubric | Deliverable meets the rubric and requested format |

## Execution Boundaries

- For answer, explanation, review, diagnosis, or planning requests: inspect and report; do not make changes unless asked.
- For change, build, or fix requests: make in-scope local changes and run relevant non-destructive checks.
- Require confirmation before external writes, destructive actions, purchases, publishing, or material scope expansion.
- Keep instructions and tool descriptions lean. State a rule once; remove repeated examples or irrelevant context.
- Treat the task definition as a control surface, not a deliverable that can replace contact with real artifacts.

## Handoff Checklist

Before delivery, answer only the relevant items:

1. What changed or was concluded, and why?
2. What user behavior or decision does it affect?
3. What evidence was checked, and what was the result?
4. What remains untested, uncertain, or out of scope?
5. What is the smallest next step?
