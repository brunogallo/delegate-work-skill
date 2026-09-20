---
name: delegate-work
description: Delegate bounded coding work, with TypeSafe Jev assisting preparation and evidence-based review.
---

# Delegate Work

Use this skill only when implementation should be handed to a worker.

## TypeSafe-assisted preparation and review

The planning parent defines scope, decisions and the work package. Use TypeSafe
Jev as an auxiliary source of typed judgments when available and a semantic
question can materially improve preparation or review. Read the sibling
[typesafe-ai skill](../typesafe-ai/SKILL.md) and its relevant live documentation
before the first consultation. Keep exact parsing, calculations and test execution
in deterministic tools.

Before delegation, inspect the relevant project evidence and identify unresolved
questions: ambiguous scope, competing approaches, overlooked acceptance criteria
or risk priorities. Give Jev the concrete evidence, constraints and candidate
answers. Incorporate supported findings into the package; the parent resolves
contradictions against project sources and user decisions.

After implementation, the selected worker inspects the actual diff and runs the
required checks. Use Jev for focused checks against that evidence, such as whether a specific
requirement is covered or whether a proposed edge case remains untested. A review
of a plan or worker summary is not a review of the implemented code. Cite the
relevant excerpts in the state; Jev cannot read a local path merely because it is
mentioned. The selected worker verifies findings and implements necessary corrections. Astra and
Sol do not perform implementation review, run validation or give a technical
sign-off; unresolved scope questions return to them for planning only.

- Use Choice for mutually exclusive alternatives, including no-match or
  insufficient-evidence outcomes when applicable; Noul for independent yes/no
  claims; Score for a clearly defined ordered dimension.
- Ask independent questions over shared evidence together. Do not repeat calls
  without new evidence or a changed question, and avoid ceremonial calls for
  straightforward mechanical work.
- Confidence describes the answer distribution, not proof of correctness or
  authorization. Do not introduce a universal passing threshold or let a Jev
  answer replace source inspection, required checks or human content approval.
- Prefer the available TypeSafe tool. If it fails, an already configured API path
  may be used within the same scope. Keep credentials in the environment and send
  only necessary authorized context, excluding secrets and player data.
- If Jev is unavailable, report the limitation and continue evidence-based worker
  review unless the user explicitly requires a Jev result before proceeding.
  Distinguish provider failure from worker failure; neither warrants blind retries.
- Briefly record the question, evidence scope, returned model, typed result and
  uncertainty, and what influenced the decision. Report usage when available.
  Label the consulting agent's reasoning separately; do not attribute invented explanations to Jev.

## Worker selection

Use Astra or Sol only for planning: inspecting context needed for the plan,
decomposing tasks, defining interfaces and preparing work packages.
Use Spark for tiny deterministic edits when Spark is available: a fully specified,
local mechanical change with an obvious expected result and a narrow check, such
as correcting a typo or replacing an explicitly named literal. Spark may perform
the focused verification of its own edit. A small diff alone does not qualify;
changes requiring debugging, architecture or consequential behavior decisions go
to Luna Max.

Use `gpt-5.6-luna` with `max` for other implementation, code fixes, tests,
verification and implementation review, assisted by Jev as described above.
If Spark is unavailable or its task exceeds the tiny deterministic scope, use
Luna Max. Resolve the actual available Spark model/role from tool metadata; do not
invent a model ID or an effort setting.
Verify the requested model/effort through available runtime metadata; do not
claim a skill changes the current parent model. If that lane is unavailable or
quota-limited, preserve partial work, continue independent planning when useful,
and report the implementation blocker. Do not use Spark to bypass Luna's scope or
quota restriction. Do not substitute Astra, Sol or a
different effort level without a new explicit user instruction.

Give the selected worker one clear outcome, bounded ownership and useful verification criteria.
If the task proves unclear or too broad, return to planning and refine the package;
keep implementation on Luna Max. Do not loop blindly or escalate coding to Sol.

For the detailed work-package template, read `references/work-package.md` only when you need to prepare the package.
