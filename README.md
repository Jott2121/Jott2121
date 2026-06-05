# Jeff Otterson

**I build and *operate* production AI agent systems — like [Bow](https://github.com/Jott2121/bow), an always-on, self-healing chief-of-staff that runs at ~$0/mo over a plan I already pay for.**

---

## What I build

Production agent infrastructure and applied ML/data tools that run, not slide decks. What I bring is the architecture and the gates: I design the system, then direct fleets of Claude (Opus 4.8) subagents to implement and adversarially review every piece — nothing ships until a deterministic check and an independent reviewer both pass. I'd rather show the build and the failure I caught than a polished demo.

## Featured

### [Bow](https://github.com/Jott2121/bow) — flagship
An all-Claude (Opus 4.8) chief-of-staff agent I architected, built, and run — reachable from my phone, at ≈ $0/mo marginal cost. A single always-on daemon wraps the headless `claude -p` CLI as first-party usage, routes phone messages, runs autonomous builds, fires scheduled routines, and self-heals. Built and adversarially reviewed by fleets of Claude subagents I directed and gated; an independent QC pass caught a soft-lock the happy-path tests never saw. Sanitized engineering case study — receipts over hype.

### [ai-career-threat-index](https://github.com/Jott2121/ai-career-threat-index)
Open dataset of AI displacement risk across 76 professions — a transparent three-factor methodology, quarterly review, MIT licensed.

### [attrition-risk-ml](https://github.com/Jott2121/attrition-risk-ml)
Explainable ML for retention-risk modeling. Three models benchmarked (Logistic Regression, Random Forest, XGBoost) under 5-fold stratified CV; the well-specified linear model wins on this sample size, and the writeup says why. Per-prediction SHAP attributions, surfaced in a multi-page Streamlit dashboard.

### [pay-equity-regression](https://github.com/Jott2121/pay-equity-regression)
Regression-based equity audit — a two-stage OLS model on log-pay that isolates unexplained variation after controlling for level, function, location, tenure, and performance, with residual drilldown and budget-aware remediation modeling (statsmodels).

### [funnel-disparity-stats](https://github.com/Jott2121/funnel-disparity-stats)
Multi-stage funnel conversion analytics with statistical disparity detection — a two-proportion z-test and 4/5ths-rule screening run over cohort data to flag stages where pass-rate gaps cross significance.

## How I work — Fleet Mode

Default to a single agent; fan out only for read-heavy parallel work that demonstrably earns it (adding agents has a negative average payoff). Writes stay single-threaded; deterministic machine checks run first, then an independent refute-first reviewer that no agent grades for itself — the gate fails closed, irreversible acts are human-gated, and every run logs a receipt with the real number.

## Background

A decade shipping production ML/data tools at Oracle, Amazon, and Lockheed — against messy, governed real-world data: benchmarked classifiers with SHAP explainability, regression-based audits with residual analysis, and statistical inference (two-proportion z-tests, the 4/5ths rule). The constraints were real — review, governance, consequences — which is why the agent work above is grounded against the wall, not on a whiteboard.

## Links

- GitHub: https://github.com/Jott2121
- LinkedIn: https://www.linkedin.com/in/jeffotterson/
