# Work package reference

Use this only when a worker needs a structured handoff.

Keep the package short. Include only what materially helps the worker complete the bounded task.

## ROUTE

Record `gpt-5.6-luna` / `max` for implementation, corrections, verification and
implementation review. Astra and Sol are restricted to planning. Verify actual
routing rather than assuming a role nickname guarantees a model. Use an available
native worker role with these settings; do not invent a role or change model silently.

## GOAL

One concrete outcome.

## CONTEXT

Only the repository and product context needed for this task.

When TypeSafe helped prepare the task, include the relevant evidence, typed
judgment, uncertainty and the parent's resulting decision. Treat suggestions as
review inputs, not new requirements unless the parent adopted them. Do not pass
credentials or unnecessary transcripts to the worker.

## SCOPE

Files, components or behaviour the worker owns.

## CONSTRAINTS

Important interfaces, invariants, boundaries or behaviour that must remain intact.

Avoid long generic rule lists.

## DONE WHEN

State the observable completion condition.

## VALIDATION

Specify only checks that materially verify the change.

For tiny reversible edits, a focused inspection or narrow check may be enough. For risky changes, require the relevant tests, build, lint, type checks or smoke tests.

## RETURN

Ask for a concise handover containing:
1. files changed;
2. what changed;
3. meaningful verification and result;
4. any remaining risk, assumption or blocker.

Luna inspects the diff and runs the checks. For semantic review with Jev,
provide the relevant implementation excerpts and actual verification evidence,
ask bounded questions against acceptance criteria, and verify any finding before
requesting a correction. Record what changed because of the review, or that no
change was justified. Do not describe a summary-only consultation as code review.

## Escalation

If a worker fails, first decide whether the task was unclear or too broad.

Quota, authentication and service errors are availability failures. Preserve work
and report the blocker; do not switch implementation models automatically.

For scope or architecture ambiguity, Astra or Sol may revise the plan and return a
bounded package to Luna Max. They do not take over coding, tests or code review.
