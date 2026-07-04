# AFTER (Architect First, Test Everything Rigorously)

AFTER (Architect First, Test Everything Rigorously) is a methodology for AI-assisted software development.

> AI generation is cheap, engineering judgment is expensive. The engineer's value concentrates at the two ends of the workflow, before generation and after it, hence the name.

## The two pillars

| Pillar | Summary |
| --- | --- |
| Architect First | No code is generated before the human has made the decisions that matter. |
| Test Everything Rigorously | Nothing ships on trust. Generated output is treated as unverified until proven. |

## Use it in 30 seconds

| Interface | One-line setup |
| --- | --- |
| Claude Code / `CLAUDE.md` | Copy `AFTER.md` to `CLAUDE.md` at the project root. |
| `AGENTS.md` | Copy `AFTER.md` to `AGENTS.md` at the project root. |
| Cursor rules | Paste `AFTER.md` into your Cursor project rules file. |
| Plain system prompt | Paste `AFTER.md` as the system prompt for the agent. |

## Workflows

| Workflow | Use when |
| --- | --- |
| Greenfield | Starting a new project and you need specification, architecture, and a plan before implementation. |
| Feature | Adding or changing behavior in an existing project. |
| Debug | You need a failing reproduction first, then a root cause, then a minimal fix. |
| Refactor | You need to improve code that already exists without changing the intended behavior. |

## Ecosystem

- `AFTER.md` is the lightweight tier. It is the drop-in protocol file for day-to-day use.
- `METHODOLOGY.md` is the full specification.
- `Morialkar/yvcdb` is the enforcement tier. It adds structural human gates for larger work and tighter review control.

## FAQ

### Does this slow me down?

> AFTER scales to the stakes. For a throwaway experiment, the human may waive phases; waiving must be their explicit call, never your silent shortcut. For anything meant to be maintained, shipped, or signed, the full workflow applies.

### What about throwaway prototypes?

Use the scaling rule above. Skip ceremony only when the human explicitly waives it for a throwaway experiment.

The AI writes most of the code. The human makes every decision.
