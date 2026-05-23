# Material Domain Problem Patterns

Use this file to transform a material-domain review into the field-specific lead-in and problem discovery part of the Introduction.

## Domain Problem Discovery Questions

Before drafting, extract answers to these questions from the user's review:

1. What is the material system and why does it matter scientifically or technologically?
2. Which variables define a single sample: composition, precursor, synthesis route, processing history, morphology, surface state, structure, testing condition, or application?
3. Which variables control performance but are usually scattered across text, tables, figures, and supplementary files?
4. Which relationships must be preserved: composition-structure-property, process-structure-property, precursor-surface-performance, or structure-application?
5. What does existing manual curation or database work miss?
6. Why would a rule/NER/parser approach mis-bind fields or fail to transfer?
7. What evidence must each extracted field retain for expert verification?

## Cross-Material Patterns

| Pattern | Typical Materials | Writing Use |
|---|---|---|
| Vast design space | high-entropy alloys, MOFs, carbon dots, catalysts | Establish why exhaustive experiments and manual reading are insufficient. |
| Process sequence controls properties | alloys, catalysts, carbon dots, glass, surface reactions | Argue for step-level extraction instead of isolated field extraction. |
| Host/dopant or surface-state coupling | phosphors, carbon dots, optical materials | Show why entity extraction must bind dopant/surface state to optical performance. |
| Multi-property screening | batteries, solid electrolytes, superconductors | Show why records need multiple properties and test conditions. |
| Multimodal evidence | nanomaterials, microscopy-heavy materials, table-rich domains | Justify text-table-figure evidence integration. |
| Knowledge graph need | framework materials, MOFs/COFs/HOFs | Introduce entity-relation extraction and logical relation preservation. |
| Sparse labels or scarce data | emerging fields, surface reactions, niche material systems | Motivate few-shot/prompt/local LLM workflows. |
| Hypothesis generation beyond expert priors | complex materials with fragmented literature | Motivate cross-source synthesis and evidence-preserving reasoning. |

## Extracted Material-Specific Problem Bank

Use these as analogies when the user's target field resembles one of the surveyed domains.

| No. | Material Object | Specific Problem To Transfer |
|---:|---|---|
| 01 | High-entropy alloys | Multi-principal-element design space; strength, phase, grain size, and processing history must be linked. |
| 05 | Luminescent phosphors | Host, dopant ion, dopant concentration, and emission peak relationships are fragmented and easy to mis-bind. |
| 09 | Battery materials | Capacity, voltage, Coulombic efficiency, energy, conductivity, and safety constraints must be captured together. |
| 11 | Alloy synthesis/processing | Synthesis and processing are action sequences with flexible language and few gold annotations. |
| 12 | Optical materials | Domain vocabulary, symbols, and numeric tables differ sharply from general corpora. |
| 14 | Gold nanoparticles | Size and morphology depend on large reagent and synthesis-condition spaces. |
| 20 | Inorganic glass | Composition alone is insufficient; processing and testing conditions affect properties. |
| 22 | Superalloys | Composition, element fractions, properties, and treatments are scattered across text and tables. |
| 24 | MOFs | Synthesis, structure, performance, and stability information expands quickly and resists systematic extraction. |
| 29 | Nanomaterials | Structure, synthesis, characterization, and performance are distributed across text, tables, and figures. |
| 30 | Framework materials | Large literature lacks an integrated knowledge graph across entities and relations. |
| 31 | MOF solid-state electrolytes | Complex materials and limited design rules require mining application-specific candidates. |
| 35 | Metallurgy/system charts | Processing-microstructure-mechanism-property relations cannot be represented by simple value extraction. |
| 36 | Complex materials hypotheses | Design hypotheses are limited by expert knowledge and need cross-source synthesis. |

## Field Validation Mini-Cards

Use these cards as concrete anchors when the user's target resembles one of these fields.

### Luminescent Phosphors

- Output object: `host-dopant-emission relationship`.
- Core relation: host lattice + activator ion/valence + dopant concentration + excitation/emission pair + efficiency/test condition.
- Evidence locations: formulas in text/tables, spectra and captions, measurement paragraphs, supplementary datasets.
- Mis-binding consequence: a model learns a false structure-property relation or compares emission peaks measured under incompatible conditions.
- Prior-route bottleneck: generic chemical parsers recognize formulas and numbers but struggle with doped formula parsing, implicit subjects, valence, concentration series, and measurement-condition binding.
- Method object: evidence-linked phosphor sample record.

### Organic Synthesis Literature Mining

- Output object: `reaction record`.
- Core relation: reactants/products + molecular roles + reagents/catalysts/solvents + conditions + yield + characterization evidence.
- Evidence locations: reaction schemes, molecule labels, arrows, experimental procedures, tables, captions, and supplementary files.
- Mis-binding consequence: a compound is assigned the wrong role or a condition is attached to the wrong reaction step.
- Prior-route bottleneck: databases, HTE, OCSR, rules, and NLP each cover part of the data object but do not reliably align image structures with procedural text and standardized reaction parameters.
- Method object: multimodal, evidence-linked reaction record.

### Metallurgy System Charts

- Output object: `P-M-S-M-P system chart`.
- Core relation: processing -> mechanism -> microstructure -> mechanism -> property.
- Evidence locations: experimental methods, microstructure figures, mechanism discussion, property tables, figure captions.
- Mis-binding consequence: the chart attributes a property improvement to the wrong mechanism, such as confusing precipitation strengthening with grain refinement or phase transformation.
- Prior-route bottleneck: entity/value extraction captures terms and numbers but cannot preserve direction, mechanism source, or whether a mechanism came from the paper text or external knowledge.
- Method object: auditable system chart with source labels and missing-relation markers.

## Carbon-Dot Transfer Template

Use this only when the user provides carbon-dot review evidence or explicitly asks for carbon dots. Do not treat non-carbon-dot benchmarks as proof that a carbon-dot Introduction has been validated in-domain.

1. Carbon dots have broad applications such as sensing, bioimaging, optoelectronics, photocatalysis, and anti-counterfeiting.
2. Their optical behavior depends on precursors, solvents, pH, reaction temperature/time, passivation, doping, purification, particle size, surface functional groups, oxidation state, and measurement conditions.
3. The same paper may report these variables across synthesis paragraphs, characterization figures, optical tables, application sections, and supplementary files.
4. Simple NER can identify chemicals or numbers but cannot reliably bind `sample -> synthesis route -> surface/doping state -> emission peak/QY/lifetime -> application`.
5. A carbon-dot Introduction should therefore justify LLM-prompt extraction as a way to produce evidence-linked sample records, not as a generic use of LLMs.

Reusable Chinese sentence pattern:

碳点并不是由单一化学式定义的材料对象。同一“碳点”名称下，前驱体组合、溶剂环境、热处理路径、表面钝化和掺杂状态都可能改变粒径、发射峰、量子产率和应用响应。因此，碳点文献挖掘的核心不是识别若干化学实体，而是把样品、合成过程、结构/表面态和光学性能绑定为可追溯的证据链。
