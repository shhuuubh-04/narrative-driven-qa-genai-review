# Narrative-Driven QA with GenAI

> **The field is building, not checking.**
> A structured review of 12 studies (2022 to 2025) on LLM-assisted software
> quality assurance, and what they collectively miss.

**Paper:** [`paper/narrative-driven-qa-genai.pdf`](narrative-driven-qa-genai.pdf)
**Authors:** Shubhan Singh, Jagdish Shukla, Tejaswini J. Chavan
*STME, NMIMS Navi Mumbai · 2026*

---

## What This Paper Argues

Agile QA depends on a chain of artifacts. Epic, user story, acceptance
criteria, test, code review, bug report, documentation. Each link is
supposed to carry consistent intent from product vision all the way to
delivery.

LLM research has handled each link separately. Test generation is one
problem. Code review is another. Bug reporting is a third. Every
subcommunity benchmarks against its own metrics. Whether LLMs can keep
meaning intact *across* the chain, what we call **cross-artifact narrative
coherence**, has received almost no attention.

This paper introduces a four-dimensional taxonomy, applies it to 12 core
studies, and shows where the literature concentrates and where it leaves
gaps. The strongest takeaway:

> The dominant pattern is single-direction, tool-level, generative work.
> Feedback loops are missing. Nobody has proposed metrics for cross-artifact
> coherence. One empirical result already in the literature suggests the gap
> matters: upstream narrative source quality measurably affects downstream
> artifact quality. If that holds, it compounds across the entire QA chain.

---

## Why This Matters

The irony is hard to miss. Agile QA suffers from artifact disconnection in
practice, and LLM research reproduces that exact disconnection in its study
designs. Tests pass without verifying what the originating story asked for.
Code reviews happen without acceptance criteria. Each research community
measures within its own silo. The literature is busy building, not checking
whether the artifacts it builds say the same thing as each other.

This review names that gap, defines it, and proposes six concrete research
questions to close it.

---

## The Taxonomy

We classify 12 studies along four dimensions chosen to surface connections
rather than reproduce the subdiscipline fragmentation found in existing
surveys.

| Dimension | What It Asks |
|-----------|--------------|
| **D1: Artifact Scope** | How many distinct artifact types does the study involve? (Single / Multi / Pipeline) |
| **D2: Narrative Direction** | Which way does information flow? (Forward / Backward / Bidirectional) |
| **D3: LLM Role** | What role does the LLM play? (Generator / Refiner / Linker / Validator) |
| **D4: Agile Integration Depth** | How deeply does it integrate with the workflow? (Tool / Process / Culture) |

Full classification of all 12 studies in [`taxonomy/taxonomy.md`](taxonomy/taxonomy.md).

---

## Findings

Six patterns came out of the corpus. Each one points at a specific gap.

- **F1. The pipeline gap.** No primary study examines coherence across three or more connected artifact types.
- **F2. Forward dominance.** The literature strongly favours forward propagation. Backward tracing and bidirectional feedback are underrepresented.
- **F3. Generator bias.** LLMs are cast as artifact producers far more than as linkers or validators. Building, not checking.
- **F4. Tool-level saturation.** Most studies plug LLMs into existing workflows without engaging with how QA processes or team dynamics might need to change.
- **F5. No coherence metrics.** Nobody has proposed or applied metrics for cross-artifact narrative coherence. This is a hard stop for rigorous future work.
- **F6. Source quality propagates.** Upstream narrative source type measurably affects downstream artifact quality.

Each finding maps directly to a research question. See [`findings/findings.md`](findings/findings.md) and [`findings/research-questions.md`](findings/research-questions.md) for the full set.

---

## Research Agenda

Six open questions, each grounded in a specific gap from the taxonomy.

- **RQ1.** Can LLMs maintain semantic coherence across three or more connected QA artifact types?
- **RQ2.** How should backward narrative tracing, from bug to originating story, be designed?
- **RQ3.** Can LLM-based coherence validators reduce defect escape rates?
- **RQ4.** How does LLM-assisted QA change agile team communication and process dynamics?
- **RQ5.** What metrics can evaluate cross-artifact narrative coherence beyond binary traceability link recovery?
- **RQ6.** What is the optimal narrative source type for LLM-based downstream QA artifact generation?

None of these are speculative. Each one is tied to a documented gap, and
each can be pursued with existing LLM technology and standard SE research
methods.

---

## Scope and Method

- Structured narrative review (not a systematic review).
- Six databases searched: IEEE Xplore, ACM Digital Library, Scopus, Google Scholar, arXiv, Semantic Scholar.
- Date window: 2022 to 2025, plus one foundational paper (Lucassen et al., 2016) referenced by multiple studies in the corpus.
- ~90 candidates screened, narrowed to 12 core papers and 8 supporting references.
- Each paper mapped across all four taxonomy dimensions, with the dimensions themselves refined as patterns emerged.

Limitations and threats to validity are covered in §V.E of the paper.

---

## Repository Contents

```
├── paper/
│   └── narrative-driven-qa-genai.pdf    # full paper
├── taxonomy/
│   └── taxonomy.md                       # Table I expanded
├── findings/
│   ├── findings.md                       # F1 to F6
│   └── research-questions.md             # RQ1 to RQ6
├── LICENSE
└── README.md
```
---

## License

Documentation, diagrams, and content in this repository are licensed under
[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
