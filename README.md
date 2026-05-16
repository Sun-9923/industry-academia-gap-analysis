# Industry-Academia Gap Analysis Skill

A Hermes skill for diagnosing the gap between academic research and industrial practice. It is domain-agnostic and focuses on the causal path from production constraints to academic assumptions, mismatch mechanisms, operational consequences, and research opportunities.

## What It Does

This skill helps analyze why research ideas, benchmarks, or methods may not translate cleanly into deployed systems. Instead of producing a literature summary, it reconstructs both sides of the system:

- Industrial reality: data, infrastructure, economics, workflow, governance, lifecycle, ownership, and risk.
- Academic paradigm: abstractions, datasets, metrics, evidence standards, incentives, and blind spots.
- Gap mechanism: how a specific assumption conflicts with a specific constraint.
- Research opportunity: what new formulation, evaluation, benchmark, system abstraction, or deployment-aware theory would close the gap.

Core invariant:

```text
Industrial constraint x Academic assumption -> mismatch mechanism -> operational consequence -> research opportunity
```

## When To Use

Use this skill when you need to:

- Analyze a research area against real industrial deployment conditions.
- Turn practitioner pain points into rigorous research questions.
- Evaluate whether academic benchmarks reflect production constraints.
- Identify missing evaluation dimensions such as cost, risk, robustness, workflow, governance, or lifecycle behavior.
- Produce a structured gap analysis for a report, strategy memo, research agenda, or HTML deliverable.

Do not use it for generic paper lists, hype summaries, algorithm-only comparisons, or broad business analysis without concrete system constraints.

## Core Analysis Workflow

1. **Scope the system**: define the task, actors, workflow, data, infrastructure, risks, owners, incentives, and lifecycle.
2. **Extract industrial constraints**: identify what must hold for repeated, cheap, safe, accountable operation.
3. **Reconstruct the academic paradigm**: name the assumptions, abstractions, datasets, metrics, methods, and evidence norms.
4. **Map mismatches**: connect assumptions to reality through mechanism, consequence, persistence, and missing evidence.
5. **Classify gaps**: apply explicit taxonomy labels rather than using a vague "research-practice gap."
6. **Synthesize opportunities**: convert high-leverage gaps into researchable questions, evaluations, benchmarks, system designs, or theory.
7. **Run the quality gate**: verify that constraints, assumptions, mechanisms, consequences, validation paths, and references are explicit.

## Output Modes

### Markdown

Default mode. Produces concise structured Markdown with:

1. Thesis
2. Operating system
3. Industrial constraints
4. Academic paradigm
5. Mismatch map
6. Gap classification
7. Research opportunities
8. Systems implications
9. What not to conclude

### HTML Report

Use when the user asks for a report, webpage, artifact, exportable deliverable, or polished long-form output. The skill produces one standalone semantic HTML document with embedded lightweight CSS, print styles, responsive layout, tables, callouts, and references.

Required report sections include executive summary, scope and assumptions, operating-system map, constraint matrix, academic paradigm, mismatch map, gap taxonomy, opportunity ranking, systems implications, what not to conclude, and references.

## Gap Taxonomy

| Gap | Diagnostic Question |
|---|---|
| Objective | Do metrics match operational value? |
| Data | Do benchmark data conditions match production data? |
| Evaluation | Are cost, risk, robustness, workflow, and lifecycle measured? |
| Deployment | Can it integrate, scale, monitor, recover, and roll back? |
| Workflow | Does it fit handoffs, exceptions, incentives, and accountability? |
| Infrastructure | Are required APIs, telemetry, controls, and systems realistic? |
| Economic | Do benefits justify compute, labor, integration, maintenance, and procurement? |
| Governance | Can it satisfy audit, compliance, security, explainability, and liability? |
| Lifecycle | Does it handle drift, incidents, retraining, ownership, and retirement? |
| Incentive | Are academia and industry rewarded for incompatible outcomes? |
| Abstraction | Did the formulation remove variables central to operation? |
| Trust | Can users and institutions understand, contest, verify, and rely on it? |

## Hermes Example

```text
Use the industry-academia-gap-analysis skill.

Topic: Retrieval-augmented generation for enterprise customer support.
Goal: Identify gaps between current academic RAG evaluation and production support operations.
Output: HTML report with opportunity ranking and references.
Focus on: data drift, support workflow handoffs, latency/cost tradeoffs, auditability, incident handling, and user trust.
```

## Quality Bar

Strong outputs name the system, make assumptions explicit, connect constraints to academic assumptions causally, classify each gap, rank opportunities with validation paths, and avoid treating benchmark gains as production readiness.
