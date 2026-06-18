# Jeff Otterson

**I build and *operate* production AI agent systems — like [Bow](https://github.com/Jott2121/bow), an always-on, self-healing chief-of-staff that runs at ~$0/mo over a plan I already pay for.**

---

## What I build

Production agent infrastructure and applied ML/data tools that run, not slide decks. What I bring is the architecture and the gates: I design the system, then direct fleets of Claude (Opus 4.8) subagents to implement and adversarially review every piece — nothing ships until a deterministic check and an independent reviewer both pass. I'd rather show the build and the failure I caught than a polished demo.

## Featured

### [Bow](https://github.com/Jott2121/bow) — flagship
An all-Claude (Opus 4.8) chief-of-staff agent I architected, built, and run — reachable from my phone, at ≈ $0/mo marginal cost. A single always-on daemon wraps the headless `claude -p` CLI as first-party usage, routes phone messages, runs autonomous builds, fires scheduled routines, and self-heals. Built and adversarially reviewed by fleets of Claude subagents I directed and gated; an independent QC pass caught a soft-lock the happy-path tests never saw. Sanitized engineering case study — receipts over hype.

### [agent-gate](https://github.com/Jott2121/agent-gate)
A fail-closed quality gate for agent workflows, shipped as an installable MCP server (`pip install mcp-agent-gate`). Work doesn't pass on a hope — it passes a deterministic check, and every run writes a hash-chained, tamper-evident receipt. 19 tests, including tests that exercise the MCP tools, not just import them.

### [rag-guard](https://github.com/Jott2121/rag-guard)
A guarded RAG pipeline that refuses when the retrieved context doesn't support an answer: groundedness check, PII redaction, and an eval harness. Published eval run with its misses named instead of hidden — refusal accuracy 0.90, grounded rate 0.88. Stdlib core, bring your own model.

### [agent-cost-attribution](https://github.com/Jott2121/agent-cost-attribution)
A token-efficiency meter and playbook for agentic coding: a per-stage token/$ waterfall, plus a detector for runs that report success while silently broken. Cut one workflow's cost by 67%. Honest part: the meter overturned my own plan — I assumed Fetch was the cost whale; the telemetry proved it was the verify step.

### [attrition-risk-ml](https://github.com/Jott2121/attrition-risk-ml) · [live demo](https://hr-attrition-predictor-jotterson.streamlit.app/)
Explainable ML for retention-risk modeling. Three models benchmarked (Logistic Regression, Random Forest, XGBoost) under 5-fold stratified CV; the well-specified linear model wins on this sample size, and the writeup says why. Per-prediction SHAP attributions, surfaced in a multi-page Streamlit dashboard.

### [funnel-disparity-stats](https://github.com/Jott2121/funnel-disparity-stats) · [live demo](https://hiring-funnel-analytics-jotterson.streamlit.app/)
Multi-stage funnel conversion analytics with statistical disparity detection — a two-proportion z-test and 4/5ths-rule screening run over cohort data to flag stages where pass-rate gaps cross significance.

More analytics: [workforce-planning-demand-forecast](https://github.com/Jott2121/workforce-planning-demand-forecast) ([live demo](https://workforce-planning-jotterson.streamlit.app/)) · [pay-equity-regression](https://github.com/Jott2121/pay-equity-regression) · [ai-career-threat-index](https://github.com/Jott2121/ai-career-threat-index)

## How I work — Fleet Mode

Default to a single agent; fan out only for read-heavy parallel work that demonstrably earns it (adding agents has a negative average payoff). Writes stay single-threaded; deterministic machine checks run first, then an independent refute-first reviewer that no agent grades for itself — the gate fails closed, irreversible acts are human-gated, and every run logs a receipt with the real number. Packaged as a live skill: [fleet-mode](https://github.com/Jott2121/fleet-mode).

## Engineering practices

The bar I'd set for a team, enforced on my own repos. Every flagship project ships with:

- **CI on every push** — multi-version test matrices (Python 3.9–3.13).
- **Coverage-gated builds** — the build fails if coverage drops below the floor, so the suite can't quietly rot (rag-guard 99%, agent-gate 97%, agent-cost-attribution 96%).
- **CodeQL static analysis** — `security-extended` queries on every push, PR, and weekly.
- **Dependabot** — automated dependency and Actions updates, with security alerts on.
- **Pinned supply chain** — every GitHub Action pinned to a commit SHA.
- **Protected `main` + a security policy** — nothing merges until the checks pass; private vulnerability reporting enabled on each repo.

Receipts, not claims: every badge is backed by a gate that actually runs and can fail.

## Background

A decade in talent and org leadership at Oracle, Amazon, and Lockheed Martin Space — hiring and scaling teams inside messy, governed, high-consequence environments. I came to AI as an operator, not an ML engineer, and I build accordingly: I own the architecture, the evals, and the gates, and I direct AI to do the typing. The applied ML/data work here is mine — SHAP-explained classifiers, regression-based audits, two-proportion z-tests and the 4/5ths rule — built and gated against real constraints, not on a whiteboard.

## Links

- GitHub: https://github.com/Jott2121
- LinkedIn: https://www.linkedin.com/in/jeffotterson/
