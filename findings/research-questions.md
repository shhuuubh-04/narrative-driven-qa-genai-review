# Research Agenda (RQ1 to RQ6)

Six open questions. None of them are speculative. Each one is tied to a
documented gap from the taxonomy analysis, and each can be pursued with
existing LLM technology and standard software engineering research methods.

## RQ1. Pipeline coherence

*From F1.* Can LLMs maintain semantic coherence when generating QA artifacts
across three or more artifact types in a connected pipeline?

Multi-agent systems already span the pipeline structurally. Whether the
artifacts they produce at each stage remain semantically aligned, and how
to measure that alignment, is unknown. A controlled experiment comparing
independently generated artifacts against pipeline-generated ones,
evaluated by human judges for cross-artifact consistency, would be a
natural starting point.

## RQ2. Backward narrative tracing

*From F2.* How should backward narrative tracing be designed, from bug
reports through code to originating user stories and epics, using LLMs?

Forward propagation has received attention. The reverse path, tracing a
downstream failure back to its upstream narrative root, is largely
uncharted. Building it is what closes the QA feedback loop.

## RQ3. Coherence validators

*From F3.* Can LLM-based coherence validators (systems that check whether
generated tests semantically align with their originating stories) reduce
defect escape rates?

We know LLMs can produce artifacts. Whether they can reliably verify
cross-artifact consistency is an open question with direct practical
consequences.

## RQ4. Process and team dynamics

*From F4.* How does LLM-assisted QA change agile team communication
patterns and process dynamics?

Tool-level integration dominates the literature. The process-level and
culture-level implications of embedding LLMs into QA workflows are
unstudied. If an LLM automatically traces a bug report to its originating
story, does the tester still need to attend the sprint retrospective to
explain the defect? These second-order effects matter before organisations
adopt LLM-based QA at scale.

## RQ5. Coherence metrics

*From F5.* What metrics can evaluate cross-artifact narrative coherence
beyond binary traceability link recovery?

Right now, metrics measure either individual artifact quality or the
presence of a link. Metrics for semantic alignment across artifact types,
measuring *degree* of coherence rather than mere existence of a link, do
not yet exist. Embedding-based similarity between story-test pairs,
acceptance-criteria coverage ratios, and LLM-as-judge consistency scores
are all plausible candidates, but nobody has formally proposed or validated
any of them.

## RQ6. Optimal narrative source

*From F6.* What is the optimal narrative source type for LLM-based
downstream QA artifact generation?

Morimoto's finding that product documentation outperforms user stories and
requirement specs as a test generation source raises a practical question
nobody has studied systematically: which narrative artifact, at which level
of detail and formality, produces the best downstream QA outcomes?

---

See also: [findings](findings.md) ·
[full paper](../paper/narrative-driven-qa-genai.pdf)
