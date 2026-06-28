# Findings (F1 to F6)

Six patterns came out of classifying the 12 core studies across the
taxonomy. Each one names a specific gap, and each one maps to a research
question in [research-questions.md](research-questions.md).

## F1. The pipeline gap

No primary study in the corpus examines semantic coherence across three or
more connected QA artifact types. Multi-agent systems like ChatDev and
AgileCoder span the pipeline structurally (one agent per SDLC phase), but
their evaluations focus on agent collaboration mechanics, not on whether
artifacts at each stage stay semantically consistent with each other. The
pipeline exists. The coherence question goes unasked.

## F2. Forward dominance

Five studies propagate information forward, from upstream artifacts (epics,
stories) toward downstream outputs (tests, reviews). Four work backward,
from code or bugs toward originating requirements. Only one supports
bidirectional flow. A healthy QA process needs both directions: a bug found
during testing should travel back to inform the story it came from, not
simply get logged and forgotten. The full feedback cycle has no
representation in the corpus.

## F3. Generator bias

Five of twelve studies cast the LLM primarily as a generator. Refiners (2),
validators (2), and linkers (2) are substantially less represented. The
skew tells us something about where attention has gone: the field is busy
checking whether LLMs can *produce* QA artifacts, much less invested in
whether those artifacts *align* with the narrative context they should
derive from. Building, not checking.

## F4. Tool-level saturation

Nine of twelve studies operate at the tool level. They introduce an LLM
capability that plugs into an existing workflow without changing it. Three
engage with process-level change. None examine culture-level impact. How
does LLM-assisted QA alter communication between product owners and
testers? Does automated traceability reduce the need for cross-team
synchronisation meetings? For a methodology that explicitly values
"individuals and interactions over processes and tools," that is a
significant omission.

## F5. No coherence metrics

Individual studies measure task-specific quality: test coverage, review
accuracy, report completeness. Nobody has proposed or applied a metric for
cross-artifact narrative coherence. There is no benchmark for whether a
test actually reflects its originating user story. Until there is,
cross-artifact work will not get rewarded, and will not get measured
rigorously.

## F6. Source quality propagates

Morimoto and Haraguchi (C8) compared E2E tests generated from three
different upstream sources: product documentation, requirement
specifications, and user stories. Tests generated from product
documentation achieved higher compilation success and broader functional
coverage than those generated from the other two. The upstream source
measurably shaped what came out downstream. If that finding generalises,
narrative source quality is not just a starting point. It is a quality
multiplier that compounds across the entire QA chain.

---

See also: [research questions](research-questions.md) ·
[full paper](../paper/narrative-driven-qa-genai.pdf)
