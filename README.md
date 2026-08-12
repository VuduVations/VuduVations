<div align="center">

# VuduVations

**Consulting-as-Code™: strategy work as verifiable software.**

We build MCOS, an autonomous consulting engine that turns business conversations and documents into board-ready analysis, with every dollar figure traceable to its source and every run carrying a record of its own integrity.

[Website](https://www.vuduvations.io) · [Research](https://vuduvations.github.io/mcos-reliability-paper/) · [Contact](mailto:hello@vuduvations.io)

</div>

---

## 📄 Published Research

**Two companion studies of the same production system, both DOI-archived on Zenodo with their raw evidence.**

### 1 · When the Model Isn't the Problem: Degradation Accounting in Fallback-Enabled Production LLM Pipelines (August 2026)

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.21903064.svg)](https://doi.org/10.5281/zenodo.21903064)

We instrumented our own production system and found that an AI pipeline can post near-perfect quality scores while the AI silently fails behind the scenes: in our baseline, the scoreboard looked flawless while the model completed its own work in only 4 of 10 runs. The study introduces degradation accounting, a run-level integrity record that separates what a system produced from whether the AI actually produced it, and reports a premium model whose measured cost per clean run was 47x a budget model, against a 17x sticker gap.

Every prediction was registered before testing. One was falsified by its own registered threshold, and we published that too. An independent reviewer reproduced every headline number from the released artifacts before publication.

**[Read the paper](https://vuduvations.github.io/mcos-reliability-paper/paper.pdf)** · **[Repository + artifacts](https://github.com/VuduVations/mcos-reliability-paper)** · **[Zenodo record](https://doi.org/10.5281/zenodo.21903064)**

### 2 · Economic Integrity in Production LLM Pipelines: Measuring Attempt Amplification, Discarded Reasoning, and Retry Cost (August 2026)

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.21903218.svg)](https://doi.org/10.5281/zenodo.21903218)

The companion study moves the meter below the retry logic: a transport-boundary ledger that records every physical model invocation, including the attempts that recovery logic normally erases from the record. Across 1,244 measured attempts serving 1,046 logical jobs, 9.6% of ledger-computed spend in this study went to attempts whose output was discarded, rising to 48.9% in the worst adversarial-debate cell, and 228,889 of 228,890 discarded output tokens were reasoning tokens: the model was thinking, billing, and being thrown away. The paper introduces the Inference Amplification Factor (IAF) and Economic Contamination Index (ECI), computed with measured rather than estimated denominators, and publishes the raw per-attempt ledgers behind every number.

**[Repository + ledgers](https://github.com/VuduVations/mcos-economic-integrity)** · **[Zenodo record](https://doi.org/10.5281/zenodo.21903218)**

---

## The MCOS Engine

MCOS (Management Consulting Operating System) is a five-layer protocol stack. The design principle: **let rules do what rules do best, and make the AI prove the rest.**

| Layer | Role |
|---|---|
| **L1 · Input Transport** | Deterministic parsing of transcripts, documents, SOPs, and audio into one clean format |
| **L2 · Extraction Primitives** | Rule-based ground truth: every dollar figure, name, date, and calculation, derived solely from the input itself. No LLM, no external database |
| **L3 · Consulting Core** | Ten specialized AI agents plus an adversarial validation layer where findings must survive cross-examination before they ship |
| **L4 · Domain Protocols** | Seven finished products: AI Discovery, Sales Intelligence, Key Person Audit, M&A Diligence, Contract Analysis, Workflow Transformation, RFC Quality |
| **L5 · Sentinel** | Contract governance: extracted obligations become live, monitored gates |

Money discipline is structural, not aspirational: a figure in the output either traces to a stated source or is labeled as an estimate. Public demos run on certified known-answer corpora, and every production run carries its own integrity record.

*Patent pending. U.S. provisional patent applications have been filed covering aspects of these systems and methods.*

**[Try the live demos](https://www.vuduvations.io)** · **[AI Discovery](https://www.vuduvations.io/ai-discovery)** · **[The manifesto](https://www.vuduvations.io/whitepaper)**

---

## Public Work

- **[mcos-reliability-paper](https://github.com/VuduVations/mcos-reliability-paper)**: the reliability study, LaTeX source, and reproducibility bundle with SHA-256 manifest
- **[mcos-economic-integrity](https://github.com/VuduVations/mcos-economic-integrity)**: the economic integrity study, raw per-attempt ledgers, result files, and compiled report
- **[Consulting-as-Code](https://github.com/VuduVations/Consulting-as-Code)**: architecture documentation for the Consulting-as-Code™ approach
- **[itil-reflexion-agent](https://github.com/VuduVations/itil-reflexion-agent)**: LangGraph-based ITIL change management agent using Reflexion-style self-critique

---

## About

VuduVations is an independent innovation studio founded by Sean Halverson, built on 15+ years of management consulting for Fortune 500 organizations. That experience exposed a consistent pattern: enterprises do not fail at strategy for lack of ideas. They fail because execution runs on slideware, subjective interpretation, and human bandwidth.

Our answer is to encode the consulting method itself into deterministic, auditable software, and to hold the AI components to a standard most of the industry does not yet measure: not just "was the answer right," but "did the AI actually do the work."

**Stack:** Python, TypeScript, LangGraph, Next.js, GCP, Vercel · Model-portable by design across Anthropic, DeepSeek, Moonshot, OpenAI, and xAI.

---

<div align="center">

[![Website](https://img.shields.io/badge/vuduvations.io-0A8F66?style=for-the-badge&logo=google-chrome&logoColor=white)](https://www.vuduvations.io)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/company/vuduvations)
[![Email](https://img.shields.io/badge/hello@vuduvations.io-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:hello@vuduvations.io)

<sub>Consulting-as-Code™ is a trademark of VuduVations. © 2026 VuduVations.</sub>

</div>
