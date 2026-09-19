---
name: more-faster-better-economical
description: Apply More, Fast, Good, and Frugal engineering principles when defining project rules, choosing architecture, planning implementation, or reviewing changes. Use to resolve tradeoffs among composability, runtime performance, maintainability, and total cost.
---

# More · Fast · Good · Frugal

Build useful capability with the smallest coherent system that meets the product contract. Treat these principles as engineering judgment, not a prescribed technology stack or mandatory ceremony.

## Four principles

### More — Less is more

Use simple, composable architecture so users can shape capabilities through their creativity instead of being confined to predefined workflows.

- Prefer a small set of cohesive capabilities with clear inputs, outputs, and boundaries.
- Separate reusable mechanisms from product-specific policy when a real variation requires it.
- Provide useful defaults and allow meaningful composition without making users assemble everything themselves.
- Introduce extension points at demonstrated variation boundaries. Composability does not require a plugin framework, microservices, or a universal abstraction.
- Evaluate capability by useful outcomes enabled, not feature counts, configuration counts, or abstraction layers.

### Fast — Low overhead, focused delivery

Keep runtime overhead low enough for the intended infrastructure role. Deliver efficiently through focused work and proportionate verification.

- Identify relevant latency, throughput, memory, startup, or resource constraints before optimizing. Do not invent numerical targets.
- Keep common execution paths direct; avoid unnecessary I/O, serialization, copying, allocation, and repeated work where they materially affect the goal.
- Prefer simple architectural reductions in work before introducing caches, concurrency, or distributed components.
- Optimize measured bottlenecks or clearly established constraints. Report estimates as estimates.
- Inspect the relevant context, complete a coherent change, and verify its actual risks. Stop expanding validation once sufficient evidence exists and required gates pass.

### Good — Coherent architecture, verifiable outcomes

Treat clear architecture and maintainable code as a craft. Preserve the product contract and produce evidence that the result works.

- Make responsibilities, dependency direction, state ownership, and failure behavior explicit where they matter.
- Keep code readable and locally understandable. Prefer domain clarity to cleverness or artificial uniformity.
- Preserve agreed behavior, interfaces, compatibility, security, and data integrity. Make intentional contract changes explicit.
- Handle failures at appropriate boundaries; avoid silent fallback that hides broken behavior.
- Verify externally meaningful behavior and concrete failure risks. Test implementation details only when they are themselves a necessary invariant.
- Distinguish implemented, verified, and unverified outcomes. State material limitations without claiming unsupported certainty.

### Frugal — Minimum sufficient total cost

Use the least code, complexity, dependencies, and process necessary to achieve the goal.

- Consider lifecycle cost: implementation, runtime resources, maintenance, operations, user effort, and agent time/tokens.
- Reuse existing capabilities when they fit. Compare a dependency's ongoing burden with the real cost of maintaining a custom implementation.
- Add abstractions, dependencies, services, configuration, and process only when they solve an identified problem.
- Prefer reversible, incremental changes. Avoid speculative generalization and unrelated cleanup.
- Use tools and delegation when their expected benefit exceeds coordination and context costs; do not make them mandatory for simple work.
- Remove obsolete machinery made unnecessary by the change when it is safe and in scope.
- Do not minimize line count by making code harder to understand, omitting necessary behavior, or shifting hidden work onto users.

## Resolve tradeoffs

Use this order of reasoning, not a numerical score:

1. Establish the requested outcome and non-negotiable constraints. Correctness, security, data integrity, and agreed product contracts define acceptable solutions.
2. Among acceptable solutions, prefer the lowest total lifecycle cost and smallest coherent design.
3. Meet the actual runtime requirements with proportionate complexity. A measured performance constraint can justify more code or a dependency.
4. Preserve useful composition at real variation boundaries; avoid paying for hypothetical future flexibility.

When options have materially different consequences, explain the simplest viable option, the alternative, and the evidence behind the choice. A short paragraph is usually sufficient. Do not generate an alternatives document for routine decisions.

Examples:
- A simple direct implementation is preferable to an unneeded plugin framework. A proven need for independently supplied capabilities may justify a small extension interface.
- A mature dependency can be more frugal than a shorter custom implementation if it substantially reduces maintenance and correctness risks.
- A cache is justified when evidence shows it is needed and invalidation is manageable; it is not a default architecture component.
- A small copy edit needs focused inspection. A persistence or concurrency change may require failure-path and integration checks.

## Apply to the current task

### Define or update project rules

Read the existing project instructions and relevant architecture first. Preserve project-specific requirements and the user's scope.

Translate the four principles into a concise set of actionable rules grounded in that project:
- What behavior or boundary must be preserved?
- What is the default design choice?
- What concrete condition justifies an exception?
- What evidence would establish success?

Use only applicable questions; do not turn them into a form for every rule. Avoid generic slogans, duplicated guidance, arbitrary quotas, and requirements that cannot affect a decision.

When asked to write project instructions, update the repository's established instruction file or the user-selected destination. Do not silently install global rules or modify unrelated projects. Keep one authoritative version of each rule.

### Design and plan

Apply these principles to the architecture and the plan already required by the task. For consequential choices, make component boundaries, contract changes, costs, and acceptance evidence clear enough for an implementer.

Do not force every task through epics, stories, DAGs, design documents, or approval rounds. If a planning workflow is already in use, incorporate the criteria there instead of creating parallel artifacts.

### Implement and review

Choose the smallest complete change that meets the outcome. Review for:
- Unnecessary coupling or restrictions on useful composition.
- Material runtime waste or unsupported performance claims.
- Contract regressions, unclear ownership, or unhandled failure behavior.
- Complexity, dependencies, configuration, or process without a demonstrated benefit.

Report concrete findings with their impact and the smallest useful correction. Do not manufacture findings, demand unrelated rewrites, or require a four-part report when there is nothing meaningful to discuss.

## Cooperation and precedence

This skill supplies decision criteria. It can work independently or alongside Supermanagement for planning and Superpowers for execution; neither is a dependency.

Honor applicable instruction priority, explicit user choices, repository constraints, and authorization boundaries. This skill does not grant itself higher priority by calling its principles foundational.

Do not copy another workflow into this skill or trigger an entire workflow merely to apply these principles. Incorporate them into the work already needed.

## Evolve without accumulating bureaucracy

Add a rule when a recurring decision or demonstrated failure reveals a useful missing constraint. Prefer improving or replacing an existing rule to appending another one. Remove redundant or obsolete rules.

Keep the four principles stable and project-specific mechanisms local. Judge the skill by better decisions and verifiable outcomes, not by its length.
