# Claims and evidence

Every claim sits at or below the strength of the evidence behind it, and the paper's own wording is where that shows.

## Rungs

1. **Operating record** — the author's real deployment or first-hand operating experience.
2. **Captured observation** — logs, traces, screenshots, incident records, measurements from the real system.
3. **Independent material** — third-party data, a standard, a published measurement, a regulator's finding.
4. **Prototype run** — real execution you configured and ran yourself.
5. **Conformance test** — an implementation checked against rules the author specified.
6. **Reasoning** — analysis from published practice and constraints.

Record each paper claim with its rung in `evidence.md`. The rung is assigned from the primary artifact that produced the evidence — code, logs, data, captures, or source passage — not from the name given to it in the ledger or manuscript. The ledger is an index, not proof.

A prototype run is evidence about the prototype, and it is written that way: measured on the prototype, not observed in production. A conformance test is evidence that the implementation matches the specified rules — legitimate, and worth space when the rules themselves are the interesting part; otherwise it states its fact and moves on. Samples generated from the same rules they test show rule conformance, not detection effectiveness on independent cases. Hard-coded, randomly added, or assumed values are inputs or simulations, not measurements. An argument built from published practice is not dressed as a measurement.

## Validation

Validation answers a specific uncertainty about the center. Name the uncertainty first: what would we not know without this?

Passing tests, exact percentages, and latency percentiles do not by themselves make a result important. Precision earns its place when the provenance of the number and its engineering meaning justify it: a figure measured on a prototype, at one configuration, whose relation to the claim is unclear, is weaker than a bounded statement about what the run showed.

When the evidence is thin, these keep the paper honest, in order of preference:

1. Narrow the claim to what the evidence shows.
2. Shorten the validation to the part that answers the uncertainty.
3. Use different evidence — a real observation beats a constructed benchmark.
4. Reconsider whether the center was substantial enough to need the check at all.

Building a heavier experiment to make a thin center look strong is the academic-pipeline reflex, and it produces length without substance.

## Numbers

No number enters the manuscript without provenance and meaning: where it came from (run, log, source document, calculation), what it measures, and the configuration or conditions it belongs to. Follow the number to the line, field, formula, or passage that produced it; if that path ends in a constant, generator, assumption, or fabricated timing term, describe that fact instead of calling the value measured. Derived values are computed from the ledger's structured sources, so the text, tables, and result files cannot drift apart. Prototype configuration values are stated as configuration, never as findings.

## Facts

Every fact in the paper traces to the author, to a checked source, or to a run you performed. Where the paper needs a fact you do not have, it goes to `open.md` for the author; where the author cannot supply it, the claim changes or the section goes. Fabricated deployment facts, enterprise data, project experience, measurements, users, or results are the one failure this workflow cannot repair afterwards.

## Bounded statements

State a claim's bound once, where the claim is made — measured on a prototype of this size, under this configuration, in this regulatory setting — then say what the result means and move on. Repeated commentary about what the paper does not prove spends space on defence and reads to a peer as doubt about the work.
