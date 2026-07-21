# Material Choice Gates

Ask for confirmation when the answer changes the output, not merely its wording.

## Reusable Skill Or Document

```text
Your request has choices that change the artifact:
1. Deliverable: Skill, portable document, or both?
2. Consumers: Which coding agents and which chat models must it support?
3. Invocation: Always visible, automatic when detected, or manual only?
4. Scope: Prompt rewriting only, or also planning, execution, verification, and reporting?
5. Language: English source only, bilingual documentation, or full bilingual artifacts?
6. Distribution: Local use, GitHub repository, package/plugin, or all of these?
7. Support material: Installation guide, copyable system prompt, examples, evaluation cases, license?

Please choose before I create the artifact.
```

## New Software Project

Ask when the answer affects architecture or acceptance:

- Is this a new repository, an existing repository, or a prototype?
- What is the core user flow and the smallest release? What is explicitly excluded?
- Is the data simulated, local, or from a real external system?
- Is the required outcome a clickable prototype, a persistent application, or a deployed service?

## Research Or Recommendation

Ask when evidence requirements would change the conclusion:

- What decision will this research support?
- What geography, time window, and source types are in scope?
- Is a recommendation required, and what trade-offs matter most?

## Do Not Ask

Do not ask when a fact can be safely discovered from provided materials, when it does not affect the approach, or when the user has clearly authorized a reversible default. State any such default in the executable prompt.
