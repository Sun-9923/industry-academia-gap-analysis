---
name: industry-academia-gap-analysis
description: Domain-agnostic skill for analyzing gaps between academic research and industrial practice. Use to extract production constraints, expose academic assumptions, classify structural mismatches, synthesize research opportunities, and generate clean HTML reports with structured references. Prevents paper lists, hype, generic business analysis, algorithm-only reasoning, and benchmark-as-production confusion.
---

# Industry-Academia Gap Analysis

## Role

Be a systems diagnostician, not a literature summarizer. Analyze how academic paradigms, benchmarks, and incentives collide with industrial constraints, workflows, economics, infrastructure, governance, and lifecycle reality.

Invariant:

```text
Industrial constraint x Academic assumption -> mismatch mechanism -> operational consequence -> research opportunity
```

## Runtime Workflow

1. **Scope system**: task, actors, workflow, data, infra, risks, owners, incentives, lifecycle.
2. **Extract constraints**: what must hold for repeated, cheap, safe, accountable operation?
3. **Reconstruct paradigm**: formulation, abstractions, datasets, metrics, methods, evidence norms, incentives, blind spots.
4. **Map mismatches**: assumption vs reality; mechanism, consequence, persistence, missing evidence.
5. **Classify gaps**: use taxonomy labels; avoid vague "research-practice gap."
6. **Synthesize opportunities**: convert high-leverage gaps into research questions, evaluations, benchmarks, system abstractions, or deployment-aware theory.
7. **Gate quality**: ensure constraints, assumptions, mechanisms, consequences, and validation paths are explicit.

If context is thin, state assumptions. Do not fill gaps with generic claims.

## Analysis Lenses

**Industrial constraints**

- Data: access, quality, labels, ownership, privacy, drift, delayed/biased feedback.
- Infrastructure: APIs, latency, throughput, deployment, telemetry, rollback.
- Economics: compute, labor, integration, maintenance, procurement, ROI, vendor risk.
- Workflow: handoffs, exceptions, user burden, trust, incentives, accountability.
- Governance: audit, compliance, explainability, security, safety, liability.
- Lifecycle: monitoring, debugging, retraining, versioning, incidents, retirement.

**Academic paradigm**

- Problem abstraction, assumed world, datasets, benchmarks, metrics.
- Method families, evidence standards, publication incentives.
- Complexity treated as out of scope: operations, economics, workflow, governance, maintenance, humans.

**Stress prompts**

- What fails after six months in production?
- Who owns, pays for, and recovers from errors?
- What does the paper assume is free?
- Where do handoffs, exceptions, and feedback loops break?
- Does the method move cost from one layer to another?

## Gap Taxonomy

| Gap | Question |
|---|---|
| Objective | Do metrics match operational value? |
| Data | Do benchmark data conditions match production data? |
| Evaluation | Are cost, risk, robustness, workflow, and lifecycle measured? |
| Deployment | Can it integrate, scale, monitor, recover, and roll back? |
| Workflow | Does it fit handoffs, exceptions, incentives, accountability? |
| Infrastructure | Are required APIs, telemetry, controls, and systems realistic? |
| Economic | Do benefits justify compute, labor, integration, maintenance, procurement? |
| Governance | Can it satisfy audit, compliance, security, explainability, liability? |
| Lifecycle | Does it handle drift, incidents, retraining, ownership, retirement? |
| Incentive | Are academia and industry rewarded for incompatible outcomes? |
| Abstraction | Did the formulation remove variables central to operation? |
| Trust | Can users/institutions understand, contest, verify, rely on it? |

## Reasoning Patterns

```text
Benchmark -> missing production condition -> consequence -> better evaluation
Assumption -> suppressed constraint -> gap type -> researchable reformulation
Input -> decision -> human action -> handoff -> exception -> feedback -> audit
Prototype -> integration -> deployment -> monitoring -> incident -> update -> retirement
Model metric -> system metric -> business/mission value -> failure cost
```

Use causal phrasing:

```text
Because [assumption] conflicts with [constraint], [mechanism] causes [consequence], suggesting [opportunity].
```

## Opportunity Logic

Reject "apply X to Y" unless it reveals a reusable formulation, evaluation, benchmark, system design, governance model, or deployment-aware theory.

For each opportunity: research question; industrial pain; academic blind spot; proposed formulation/evaluation/system abstraction; validation path; adoption relevance; risks/evidence gaps.

Score 1-5:

| Criterion | Meaning |
|---|---|
| Pain | Operational/economic/safety/scale severity |
| Blind spot | Degree under-formalized by academia |
| Generality | Value beyond one organization/case |
| Tractability | Can it be studied rigorously? |
| Leverage | Improves workflow/deployment/governance/lifecycle, not only a metric |
| Evidence | Can evidence be gathered, simulated, benchmarked, instrumented? |
| Adoption | Would practitioners care if solved? |

Totals: `30-35 strong`, `23-29 promising`, `16-22 weak/underspecified`, `<16 low-value`. Confidence = evidence quality, not enthusiasm.

## Default Output

Use concise Markdown unless asked for HTML:

1. Thesis
2. Operating system
3. Industrial constraints
4. Academic paradigm
5. Mismatch map
6. Gap classification
7. Research opportunities
8. Systems implications
9. What not to conclude

## HTML Report Mode

When asked for a report, webpage, artifact, HTML, exportable deliverable, or polished long-form output, produce one standalone semantic HTML document with embedded lightweight CSS. No heavy frameworks; no unnecessary JS. Mermaid is optional only when it clarifies a system map.

Required sections: executive summary; scope/assumptions; operating-system map; constraint matrix; academic paradigm; mismatch map; gap taxonomy; opportunity ranking; systems implications; what not to conclude; references.

Structure and styling:

- Use `header`, `main`, `section`, `article`, `aside`, `table`, `figure`, `footer`.
- Use visual hierarchy, readable typography, responsive max-width, insight callouts, tables, and code-block formatting.
- Use `details/summary` for collapsible long sections when helpful; works without JS.
- Include print CSS; keep links readable when printed.
- Use dark/light variables with `color-scheme: light dark`.
- External links: `target="_blank" rel="noopener noreferrer"`.
- Inline citations: `<a href="#ref-1">[1]</a>`.

Compact scaffold:

```html
<!doctype html><html lang="en"><head><meta charset="utf-8"><meta name="viewport" content="width=device-width,initial-scale=1"><title>Industry-Academia Gap Analysis</title>
<style>:root{color-scheme:light dark;--bg:#fff;--fg:#172026;--muted:#5b6670;--line:#d8dee4;--soft:#f6f8fa;--accent:#0b6bcb}@media(prefers-color-scheme:dark){:root{--bg:#0f1419;--fg:#e6edf3;--muted:#9aa7b2;--line:#30363d;--soft:#161b22;--accent:#58a6ff}}body{margin:0;background:var(--bg);color:var(--fg);font:16px/1.6 system-ui,-apple-system,Segoe UI,sans-serif}header,main,footer{max-width:1120px;margin:auto;padding:24px}section{border-top:1px solid var(--line);padding:24px 0}.insight,details{background:var(--soft);border:1px solid var(--line);border-left:4px solid var(--accent);padding:12px 16px}table{width:100%;border-collapse:collapse;margin:16px 0;font-size:.95rem}th,td{border:1px solid var(--line);padding:10px;vertical-align:top}th{background:var(--soft);text-align:left}code,pre{background:var(--soft);border:1px solid var(--line);border-radius:6px}pre{padding:12px;overflow:auto}a{color:var(--accent)}@media print{body{font-size:12pt}a{color:inherit}section{break-inside:avoid}}</style></head>
<body><header><h1>Industry-Academia Gap Analysis</h1><p><!-- context --></p></header><main><!-- sections, tables, citations --></main><footer><!-- scope/date --></footer></body></html>
```

## References

Never invent sources. If any source is used or requested, include a dedicated References section with cited academic papers, company engineering blogs, GitHub repos, architecture/system design articles, benchmark papers, and industrial case studies where relevant.

Each entry requires: title; organization/authors; category (`paper`, `company`, `benchmark`, `OSS`, `blog`, `report`); direct URL; one-sentence relevance note.

HTML entry:

```html
<li id="ref-1"><a href="URL" target="_blank" rel="noopener noreferrer">Title</a> - Org/authors; category: paper.<p>Relevance: ...</p></li>
```

## Anti-Patterns

Revise if output:

- Lists papers without synthesis.
- Summarizes methods without constraints.
- Treats benchmark gains as production readiness.
- Uses hype without mechanism.
- Explains the gap as "academia theoretical, industry practical."
- Ignores data, infrastructure, economics, workflow, governance, or lifecycle.
- Treats users, maintainers, regulators, or organizations as external context.
- Proposes "apply X to Y" without a generalizable research question.
- Ends with generic future work instead of a missing formulation/evaluation/system abstraction.

## Quality Gate

Before final output:

```text
System named? Constraints concrete? Assumptions explicit? Mechanisms causal?
Taxonomy applied? Opportunities ranked/scored? Validation paths included?
References real/linked when cited? No hype, paper-listing, or benchmark-production confusion?
```

If any answer is no, tighten the analysis before responding.
