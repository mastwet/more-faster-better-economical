---
name: more-faster-better-economical
description: Apply More, Fast, Good, and Frugal engineering principles when defining project rules, choosing architecture, planning implementation, or reviewing changes. Use to resolve tradeoffs among composability, runtime performance, maintainability, and total cost.
---
# More · Fast · Good · Frugal

Build capability with smallest coherent system meeting product contract. Decision criteria, not workflow. Apply independently or inside Supermanagement/Superpowers. Do not activate either merely to apply this skill.

## Scope, precedence

Apply to work already required. Simple edits leaving behavior, interfaces, state, dependencies unchanged need focused checks, not full assessment. Unrelated questions, ordinary prose edits do not trigger this skill.

Follow host instruction hierarchy, authorization boundaries. Within limits: explicit authorized user requirements > repository constraints > this skill defaults. Surface material conflicts. Change repository constraints only when explicitly authorized. General request to work faster not waive mandatory gates.

Correctness, security, data integrity, agreed product contract = acceptance conditions. Make intentional contract changes explicit. Exceptions below concern design defaults, never these conditions. Among acceptable solutions prefer minimum total lifecycle cost, then speed within that frugal design.

## Four principles

Use defaults routinely. Explain exceptions only when consequential. Evidence = confirmed requirement, inspected behavior, or measurement. Fields are decision aids, not form to fill per task.

**More: Less is more**
Default: small cohesive capabilities, clear boundaries, useful defaults, meaningful composition. Not fixed workflows or feature counts.
Exception: confirmed variation or independently supplied capabilities justify targeted extension interface. Not automatically plugin framework.
Evidence: name actual consumer, requirement, or variation boundary supports. Hypothetical future flexibility insufficient.

**Fast: Frugality before optimization**
Default: keep execution paths direct. Cut unnecessary I/O, copying, allocation, repeated work before adding machinery.
Exception: add caches, concurrency, or services when measurements or established runtime constraint show simpler approaches insufficient and benefits justify lifecycle costs.
Evidence: relevant latency, throughput, memory, or startup measurements, or documented constraint. Label estimates. Invent neither targets nor performance gains.

**Good: Lean development, accountable design**
Default: keep code readable, work small. Clarify scope, boundaries, ownership, failure behavior, acceptance before consequential delegation. Resolve shared decisions before parallel work. Limit active work to review capacity.
Exception: cross-component, persistence, concurrency, or security risks require broader design and verification than isolated changes.
Evidence: behavior, failure-path, integration checks proportionate to actual risks, plus required gates. Supervisors retain architectural and end-to-end acceptance responsibility.

**Frugal: Minimum sufficient total cost**
Default: deliver requested behavior plus necessary implementation details only. Reuse or safely delete before adding code, dependencies, configuration, or process.
Exception: extra machinery must address identified requirement or reduce total lifecycle cost versus viable alternatives.
Evidence: account maintained LOC across solution, runtime, maintenance, operations, user effort, agent time/tokens. LOC = design pressure, not quota. Preserve readability, meaningful verification.

## Red flags

Investigate signals. Not automatic findings:

- Performance complexity without measurements or established constraint.
- Hypothetical abstractions, or coupling blocking required composition.
- Unrequested features, configuration growth without concrete need, unrelated cleanup.
- Apparent LOC savings hiding complexity in dependencies, generated code, user effort.
- Contract regressions, silent failures, claims beyond available verification.
- Duplicated plans, mandatory delegation, process without demonstrated benefit.

Complexity signals, not automatic violations. Inspect hand-maintained code around thresholds: function nesting >4; conditionals (if/ternary) >8 per function; parameters >6; classes >20 methods; files >600 lines or sprawling exports with mixed responsibilities; duplicated blocks 10+ lines occurring twice; direct access to internals of >3 unrelated objects.

Report finding only when signal reveals concrete comprehension, coupling, change, or correctness risk. Prefer smallest in-scope fix. Do not split code, wrap parameters, or invent abstractions merely to satisfy counts. Respect repository-specific thresholds. Account for generated code, declarative tables, intentional repetition. Routine work: inspect only change plus direct impact. Broaden review only when requested.

## Output contracts

Use only relevant format inside existing workflow:

**Project rules:** normally 5–10 actionable project-specific rules. Fewer when sufficient. Read existing instructions and relevant architecture first. State defaults, exception conditions, evidence where applicable. Modify only established or user-selected instruction file when requested. Keep one authoritative version.

**Design:** one paragraph: simplest viable choice, material alternative, tradeoff, supporting evidence. Summarizes decision, not entire architecture. Keep interfaces, ownership, failure behavior, acceptance details in existing plan. No parallel paperwork.

**Review:** findings ordered by impact. Each: location, evidence, consequence, smallest useful correction. No substantiated issues = say so. Do not invent findings or unrelated rewrites.

Distinguish implemented, verified, unverified outcomes. Stop expanding validation when acceptance evidence sufficient, concrete risks covered, required gates pass. Disclose remaining limitations.

Replace or remove rules before appending more. Add rules for recurring decisions or demonstrated failures, not to grow this skill.
