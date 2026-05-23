# Narrative Coherence Iteration

## Why This Iteration Was Needed

Recent use showed that the skill could generate an Introduction with the right parts but still feel unsatisfactory: the prose stacked many correct points, while paragraph-to-paragraph lead-ins and sentence-to-sentence logic were weak. The draft could sound complete yet not inevitable.

Earlier validation had already improved:

- early output object;
- prior-route pressure chain;
- material/task-specific mis-binding consequence;
- domain-specific method object;
- minimum Chinese body length.

The remaining gap was narrative continuity.

## Benchmark-Derived Observation

High-quality Introduction sections do not merely list field importance, literature difficulty, method limits, and LLM necessity. They make each part depend on the previous part:

1. The field need defines the kind of data that matters.
2. The literature paragraph shows that this data exists but is fragmented.
3. The prior-route paragraph shifts the problem from information existence to evidence binding.
4. The material-specific paragraph shows why that binding failure changes scientific meaning.
5. The method paragraph becomes necessary because the previous paragraphs have already defined the output object, evidence constraint, and refusal behavior.

The useful benchmark lesson is not a fixed paragraph count. It is the pressure chain between paragraphs.

## Skill Changes Added

This iteration added:

- `references/narrative_coherence.md`;
- required `Narrative spine` before drafting;
- paragraph lead-in rules;
- sentence-function chain: `claim -> reason -> evidence manifestation -> domain example -> consequence -> bridge`;
- anti-stacking diagnostics;
- coherence hard gates in `quality_control_iteration.md`;
- web-side Custom GPT instructions requiring quality scoring and low-score rewriting.

## New Failure Gates

A draft should be revised before final output if:

- paragraphs can be swapped without damaging the argument;
- sentence order inside a load-bearing paragraph can be shuffled freely;
- paragraph first sentences start new topics instead of inheriting the previous pressure;
- paragraph final sentences do not open the next paragraph;
- the method paragraph sounds like a generic LLM paragraph rather than the consequence of the target material's evidence-binding problem.

## Expected Effect

The next generated Introduction should not only be longer and more domain-specific. It should read as a guided argument in which each paragraph makes the next paragraph necessary.
