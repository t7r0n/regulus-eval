# Regulus Eval

A regulatory document evaluation harness + citation integrity runtime for AI drafted FDA submissions. Quantifies hallucination, orphan citation, and edit decay rates — and produces the GxP evidence pack a pharma CISO will actually sign off on.

![Regulus Eval working dashboard](outputs/project_working.svg)

## Why it exists

Their product page promises "word level traceability linking every statement to source documents." Anyone who has shipped a RAG system into a regulated environment knows the awkward truth: traceability at draft time is easy; it's preserved under edit traceability that breaks the contract. A reg writer accepts the AI's first draft, edits one sentence in.

The project is intentionally built as a local replay harness instead of a slide. It creates fixtures, plants realistic failure modes, produces citation-locked evidence, and turns the result into a dashboard a reviewer can inspect without credentials or hosted services.

## What is inside

- Deterministic fixture generation for the company-specific risk surface.
- Strategy code in `src/regulus_eval/strategy.py` with project-specific scoring and visual evidence.
- Citation-locked reports where every decision claim points to a generated evidence ID.
- Two regenerated visual artifacts: `outputs/project_working.svg` and `outputs/evidence_map.svg`.
- A portable demo pack with JSON, CSV, Markdown, HTML, SVG, benchmark, and test artifacts.

![Regulus Eval evidence map](outputs/evidence_map.svg)

## Signals it measures

- `product coverage`
- `promises risk`
- `level precision`
- `traceability latency`

## Failure modes it plants

- product drift
- promises gap
- level misroute
- traceability blindspot

## Run it locally

```bash
uv sync
uv run regulus-eval all
uv run pytest -q
uv run ruff check .
```

## Outputs worth opening

- `outputs/dashboard.html`
- `outputs/project_working.svg`
- `outputs/evidence_map.svg`
- `outputs/operator_brief.md`
- `outputs/decision_report.md`
- `outputs/strategy_model.json`
- `outputs/demo_pack.zip`

## Sources

- https://www.ycombinator.com/launches/PJn-ritivel-ai-native-platform-for-regulatory-document-submission
- https://www.ritivel.com/blog
- https://fondo.com/blog/ritivel-launches
- https://www.linkedin.com/in/tankalapavankalyan/
- https://www.linkedin.com/in/nirmitarora/
- https://scholar.google.com/citations?user=hogvPo8AAAAJ&hl=en
- https://www.linkedin.com/in/gunin-gupta-3a5775194/
- https://www.falconebiz.com/company/RITIVEL-AI-PRIVATE-LIMITED-U62011KA2025PTC212044
- https://intuitionlabs.ai/articles/ai-medical-writing-ctd-module-2-summaries
- https://intuitionlabs.ai/articles/ectd-submission-ind-nda-guide

## Boundary

Everything runs locally against synthetic fixtures. There are no credentials, no customer records, no outreach files, and no hosted API dependency.
