# Taxonomy of LLM-Assisted QA Research

Twelve core studies (2022 to 2025), classified across four dimensions. The
dimensions were chosen deliberately to surface *connections* between QA
activities, not to reproduce the subdiscipline fragmentation found in
existing LLM-for-SE surveys.

## Dimensions

| Dimension | What it asks | Categories |
|-----------|--------------|------------|
| **D1: Artifact Scope** | How many distinct artifact types does the study touch? | Single / Multi / Pipeline |
| **D2: Narrative Direction** | Which way does information flow across the QA chain? | Forward / Backward / Bidirectional |
| **D3: LLM Role** | What role does the LLM play? | Generator / Refiner / Linker / Validator |
| **D4: Agile Integration Depth** | How deeply does the LLM integrate with workflow and team dynamics? | Tool / Process / Culture |

## Classification of the 12 Core Studies

| ID | Study | QA Domain | D1: Scope | D2: Direction | D3: LLM Role | D4: Depth |
|----|-------|-----------|-----------|---------------|--------------|-----------|
| C1 | Rahman et al. | Requirements + Testing | Multi | Forward | Generator | Tool |
| C2 | Zhang et al. | Requirements | Single | n/a | Refiner | Process |
| C3 | Alagarsamy et al. | Testing | Multi | Forward | Generator | Tool |
| C4 | Rasheed et al. | Code Review | Multi | Backward | Validator + Generator | Tool |
| C5 | Ebert et al. | Code Review | Multi | Backward | Validator | Process |
| C6 | Ali et al. | Traceability | Multi | Bidirectional | Linker | Tool |
| C7 | Khan et al. | Bug Reporting | Single | Backward | Refiner | Tool |
| C8 | Morimoto et al. | Docs + Testing | Multi | Forward | Generator | Tool |
| C9 | Casillo et al. | Documentation | Multi | Backward | Generator | Tool |
| C10 | Rasheed, Waseem et al. | Full SDLC (survey) | Pipeline | Forward | Generator | Process |
| C11 | QA Standards Review | QA Standards | Single | n/a | Mixed | Tool |
| C12 | Karanikolas et al. | Traceability | Multi | Forward | Linker | Tool |

## The Cross-Dimensional Pattern

Mapping D1 (Scope) against D2 (Direction) shows where the literature
clusters, and where it leaves blank space.

|              | Forward | Backward | Bidirectional | n/a |
|--------------|---------|----------|---------------|-----|
| **Single**   |         | C7       |               | C2, C11 |
| **Multi**    | C1, C3, C8, C12 | C4, C5, C9 | C6 |  |
| **Pipeline** | C10     |          |               |  |

The densest cell is Multi × Forward: four studies that cross one artifact
boundary downstream. Multi × Backward holds three. The Pipeline × Backward
and Pipeline × Bidirectional cells are empty. No study traces backward
through more than two artifact types, and bidirectional flow across a
complete QA pipeline does not appear anywhere in the corpus we reviewed.

That empty space is the gap this review is built around. It is also the
shape of what the six research questions go after.

See the [full paper](../paper/narrative-driven-qa-genai.pdf) for
per-dimension analysis and discussion.
