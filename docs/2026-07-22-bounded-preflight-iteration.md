# 2026-07-22: Bounded Preflight Before Task Definition

## Context

The first release required a visible executable prompt before every request. In a real design-research task, the agent first inspected project rules and artifact filenames, then framed the task before substantive PDF analysis and web research. That sequence produced a more accurate brief but appeared to violate the workflow because the initial read-only discovery was not distinguished from execution.

## Finding

An absolute "rewrite first" rule creates three failure modes:

1. **Premature convergence:** before touching project facts, the rewritten prompt can formalize false assumptions.
2. **Repetition cost:** simple, already-clear requests gain ceremony without additional control or information.
3. **Goal substitution:** prompt refinement can displace contact with real artifacts and completion of verifiable work.

Removing visible task framing entirely would create the opposite risk: an agent could perform analysis and silently choose consequential branches before the user sees the operative assumptions.

## Decision

Adopt a three-stage protocol:

1. **Bounded read-only preflight:** inspect only applicable rules, filenames, directories, repository status, metadata, supplied artifact types, and available tools.
2. **Visible task definition:** before substantive work on complex, open-ended, state-changing, or decision-bearing requests, state the outcome, relevant facts, constraints, evidence, deliverable, and approval boundary.
3. **Evidence-driven execution:** work in small verifiable slices. If new evidence materially changes scope, architecture, risk, acceptance, publishing, or cost, revise the task definition visibly before continuing.

Simple, already-clear answers and low-risk actions do not require a ceremonial rewrite.

## Preflight Boundary

Preflight may not include:

- file or external-state modification;
- broad content analysis or external research;
- architecture, product-scope, or visual-direction decisions;
- any substantive work hidden behind the label "preflight."

## Governing Principle

> Touch the minimum amount of reality needed to frame the work; make consequential boundaries visible before substantive execution.

In Chinese:

> 先接触最少量的现实，再定义任务；先定义任务，再做实质工作。

## Scope Of This Iteration

This decision updates the reusable skill, universal system prompts, Chinese guide, public README, and the author's cross-agent preferences and methodology memory. It does not change the repository's authorship, canonical location, CC BY-NC-ND 4.0 license, or contribution policy.
