# Vibe Coding Prompt Workflow

> A first-principles prompt engineering skill for AI agents and chat models.

`Vibe Coding Prompt Workflow` is a publicly available, portable workflow for people who want better results from Codex, Claude Code, Grok, Cursor, ChatGPT, and other AI agents or chat models without memorizing prompt tricks. It lets an agent inspect the minimum amount of reality needed to avoid false assumptions, then makes consequential task boundaries visible before substantive work begins.

- **Author:** 小黒秋 ([YMIR777](https://github.com/YMIR777))
- **First published:** 2026-07-22
- **Canonical repository:** [YMIR777/vibecoding-prompt-workflow](https://github.com/YMIR777/vibecoding-prompt-workflow)

中文版请见 [通用提示词工作流.md](通用提示词工作流.md)。

## Why This Exists

Most failures attributed to AI are task-definition failures:

- The desired result is vague.
- Important context is withheld or buried in irrelevant context.
- Constraints and approval boundaries are implicit.
- “Done” has no observable or testable meaning.
- The agent quietly makes product or architecture choices that the user never approved.

This workflow addresses those failure modes with a bounded read-only preflight followed by an `Executable task definition` for complex, open-ended, state-changing, or decision-bearing work. It does not force a ceremonial rewrite for a simple, already-clear answer. It makes assumptions, choices, evidence, and remaining uncertainty inspectable when they matter.

## First Principles

The hard part of AI-assisted work is not syntax or a magic prompt. It is translating human intent into rules a machine can execute and evidence a human can verify.

This skill turns “think from first principles” into five concrete actions:

1. Separate known facts, unverified assumptions, and subjective preferences.
2. Identify the outcome and constraints that cannot be violated.
3. Define observable success and the evidence that would prove it.
4. Surface choices that materially change the result instead of choosing silently.
5. Choose the smallest testable path after the foundations are clear.

The operational loop is:

```text
Intent -> Bounded preflight -> Task definition -> Small slice -> Evidence -> Iteration
```

## What The Agent Must Do

For substantive work, the agent may first inspect only applicable rules, filenames, repository status, artifact metadata, and available tools. This preflight must not include edits, broad analysis, external research, or material design decisions.

After preflight and before substantive execution, show the relevant parts of:

```text
Outcome:
Audience / scenario:
Relevant context:
Scope and constraints:
Success criteria / evidence:
Requested deliverable:
Autonomy and approval boundary:
```

For a simple, already-clear answer or low-risk action, use a one-line confirmation or answer directly. Do not restate the request merely to satisfy a template.

When an unanswered question would materially change the deliverable, scope, safety, architecture, acceptance, integration, publishing, cost, or maintenance responsibility, list the choices and wait for confirmation. Do not choose a branch for the user.

If later evidence materially changes the scope, architecture, risk, acceptance, publishing outcome, or cost, revise the task definition visibly before continuing.

## Install Or Use

### Agents With Skills

Copy [`skills/prompt-first-workflow`](skills/prompt-first-workflow) to the agent's configured skills directory, preserving its contents. The skill is intentionally written in English because models generally follow operational instructions most reliably in English.

For Codex, a typical global installation is:

```bash
cp -R skills/prompt-first-workflow ~/.codex/skills/
```

For Claude Code, Grok, Cursor, or another agent, install the same directory using that product's configured skill-discovery mechanism. If the agent supports project-local skills, keep the folder inside the repository and point its instructions at the `SKILL.md` file.

### Any Chat Model

Copy the English instruction from [`prompts/universal-system-prompt.en.md`](prompts/universal-system-prompt.en.md) into Custom Instructions, a project instruction, or the first message of a new chat. Use the Chinese companion when the reader needs a Chinese explanation.

## Example

Raw request:

> Build a useful learning-management website.

The workflow should not immediately generate code. It should expose the missing decisions:

```text
Executable prompt
Outcome: Build a learning-management product that helps [audience] plan and complete study tasks.
Relevant context: No repository, data source, or design reference supplied.
Material choices to confirm:
1. Is this a new project, an existing project, or a prototype?
2. What is the smallest core flow, and which features are explicitly excluded?
3. Should the first version use mock data, local persistence, or a real backend?
4. Is the deliverable a plan, a clickable prototype, working code, or a deployed site?
```

After those choices are confirmed, the agent can plan a minimal slice, implement it, and verify it with real evidence.

## What It Is Not

- Not a long-form prompt template that must be fully filled out every time.
- Not a requirement to rewrite every clear, low-risk request ceremonially.
- Not permission for the agent to expand a task, publish work, or make external changes.
- Not a replacement for domain expertise, source checking, testing, or human judgment.
- Not a reason to ask questions that do not change the result.
- Not a substitute for contact with real files, systems, users, or evidence.

## Foundations

This workflow synthesizes two complementary sources:

- [IFQ.AI Vibe Coding](https://vibe.ifq.ai/en): intent, context, slicing, verification, and iteration; AI writes code, but evidence decides whether the work is done.
- [OpenAI GPT-5.6 Model Guidance](https://developers.openai.com/api/docs/guides/latest-model?model=gpt-5.6): outcome-focused prompts, relevant and lean context, explicit autonomy and approval boundaries, precise output requirements, and validation on representative work.

The combined principle is simple: provide enough relevant context to make the right decision, but no more than needed; make consequential choices explicit; and let evidence, not confidence, close the task.

## Repository Layout

```text
skills/prompt-first-workflow/    Reusable agent skill
prompts/                         Copyable universal instructions
docs/project-release-moat.md     Project release and authorship protection checklist
docs/2026-07-22-bounded-preflight-iteration.md  Decision record for the bounded-preflight iteration
通用提示词工作流.md                Chinese learning and usage guide
```

## Publishing Strategy

Projects should not treat “public,” “open source,” and “permitted to modify” as synonyms. Before publishing, use the [Project Release Moat](docs/project-release-moat.md) to confirm authorship, the canonical version, brand narrative, openness boundaries, license, contribution model, and irreversible downstream scenarios.

## License And Contributions

Copyright (c) 2026 小黒秋 (GitHub: YMIR777).

This work is licensed under [CC BY-NC-ND 4.0](LICENSE): attribution is required; commercial use and distribution of adapted versions are not permitted without the author's prior written permission.

Issues and suggestions are welcome. Unsolicited pull requests are not accepted at this stage; see [CONTRIBUTING.md](CONTRIBUTING.md).

## Discovery Topics

`vibe-coding` · `first-principles` · `prompt-engineering` · `prompt-workflow` · `ai-agents` · `coding-agents` · `agent-skills` · `codex` · `claude-code` · `chatgpt`
