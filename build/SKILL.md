---
name: build
description: Execute an approved direction with a spec, a verifier designed before building, evidence-based verification, and an honest handoff. Use when Anthoney says "/build", "build this properly", "spec this first", or hands over something that survived /algorithm. Not for one-file edits or quick fixes.
---

# /build — Spec → Verifier → Build → Verify → Handoff

`/algorithm` decides what should exist. `/build` makes sure it gets built correctly.
Fast by default. Deep only when he says "deep" or the change touches production, spans
systems, or a prior AI attempt looked done and wasn't.

## 1. Spec
Write it with him, not for him. Ask only what the repo, dossier, memory, or prior
decisions cannot answer, and never more than five questions. Small checkpoints, not one
waterfall dump. The spec is four lines:
- **Goal** — the outcome, not the task.
- **Done when** — observable statements that can be checked.
- **Non-goals** — what is deliberately out.
- **Assumptions** — anything unresolved, marked, not hidden.

## 2. Verifier, before building
For each Done-when line, name the check and its pass condition. Strongest available:
tests, types/lint, run it, drive it in a browser, compare to reference, a different
model as critic, his judgment last. A verifier must be able to fail the build. "Reviewed
it and it looks right" is not a verifier. For anything visual, render it and look at it.
Source code is not the product.

## 3. Build
Smallest sequence of checkpoints that each leave something inspectable. Extend what
exists; do not build a parallel system. **Drift rule:** never turn "could not satisfy the
requirement" into "changed the requirement." If the spec turns out wrong, stop and say so.

## 4. Verify
Run the verifier. Every Done-when line gets PASS, FAIL, PARTIAL, or NOT TESTED, with
evidence: output, screenshot, measured value, file:line. A failure is information; fix
it and rerun, do not explain it away. Deep mode adds an independent critique from a
fresh context or different model, tracing every finding to the spec, before repair.
Stop when Done-when passes. Do not polish past it.

## 5. Handoff
Status: PASS / PASS WITH CAVEATS / NEEDS DECISION / BLOCKED. Then the normal Done/Next
close. He decides only the irreducibly subjective calls and any requirement change.
