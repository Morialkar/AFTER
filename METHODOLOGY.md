# The AFTER Methodology

AFTER (Architect First, Test Everything Rigorously) is a methodology for AI-assisted
software development. Its premise: AI generation is cheap, engineering judgment is
expensive. The engineer's value concentrates at the two ends of the workflow, before
generation and after it, hence the name.

## Architect First

No code is generated before the human has made the decisions that matter.

- Every significant piece of work starts from a written specification: architecture,
  data schemas, API signatures, and a phased plan.
- Technology choices are made by the human, with documented reasoning, before any
  generation begins.
- Specs include an explicit constraints section covering the decisions an AI would
  otherwise drift from (storage choices, ID formats, forbidden dependencies,
  non-negotiable patterns).
- Work is decomposed into self-contained tasks with acceptance criteria. Each prompt
  carries all the context it needs. Nothing relies on the AI remembering prior intent.
- Project-level quality standards live in a standards file (e.g. CLAUDE.md) loaded
  into every session, so expectations are enforced structurally instead of repeated
  manually.

## Test Everything Rigorously

Nothing ships on trust. Generated output is treated as unverified until proven.

- Tests are generated alongside production code, never after. Minimum coverage per
  unit of logic: the nominal case, at least one edge case, at least one error case.
- Generated code must be explainable line by line by the human. If a line can't be
  explained, it doesn't get merged.
- Security-sensitive code (auth, payments, permissions, personal data) is flagged
  with explicit markers (REQUIRES_REVIEW) forcing human review before merge.
- Assumptions made during generation are marked in code (ASSUMPTION) rather than
  left implicit.
- Large efforts proceed in phases with human validation gates between them. Each
  phase is reviewed, approved, or re-iterated before the next begins. Version
  control isolates each phase for safe rollback.
- The final phase is adversarial: a devil's advocate review against a checklist,
  validated by the human, before anything is considered done.

## The one-line version

The AI writes most of the code. The human makes every decision.
