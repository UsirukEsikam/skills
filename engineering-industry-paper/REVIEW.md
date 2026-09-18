# Review

Two axes, both required. A paper can be entirely accurate and still not worth reading.

Run truth and substance as distinct reads. The truth read needs independence from the authoring context: when fresh context is available, give a fresh reviewer `manuscript.md`, the ledger, and the primary artifacts that produced the evidence. It starts from those artifacts and reconstructs the load-bearing claim-to-producer paths; the ledger may locate evidence but cannot settle what the evidence is. The substance read takes the position of a skeptical technical peer. Independence is the reason to separate the reads, not parallelism or reviewer count.

Write `review.md` as the reads run. Completion evidence is the truth claim-to-producer findings, the substance verdict for every major section, each finding's disposition, and whether fresh context was used; when it was unavailable, record that limit.

## Truth

- Does each claim's wording sit at the rung established by its primary artifact — prototype results stated as prototype results, conformance cases as conformance cases?
- Does the implementation or environment described in the manuscript match what the code, configuration, data, and captures actually implement?
- Does every number reach a real producer, retain the same value across artifact and manuscript, and mean what the prose says it means?
- Are technical terms, units, equations, thresholds, and isolation or performance claims correct and defined at the precision asserted?
- Was every cited source actually opened, and does it support the claim as written?
- Are standards and regulations used for constraints and operating conditions rather than as proof that a mechanism works?
- Does every reference carry a role in the paper, cited where it bears, with none present only to reach a count?

Finish a **two-way citation trace**: each load-bearing external claim reaches an opened source and supporting passage in `sources.md`; each bibliography entry reaches a place where it bears in the manuscript and the same checked source record. Discovery results and snippets do not close either direction.

Any statement the paper makes about its sources having been checked is backed by `sources.md`. The truth read is complete when every load-bearing empirical claim has been checked at its producer, not merely matched to a ledger row.

## Substance

Apply **the peer test** ([MANUSCRIPT.md](MANUSCRIPT.md)) to every major section. The shapes of a section that fails it, however true each sentence is:

- **Generic** — true of almost any system in the field, with no specifics from this work.
- **Obvious** — the conclusion any competent engineer reaches without the work.
- **Thin** — one claim rehearsed at length, or a mechanism stated without what it cost, what it failed on, or how it is recognised.
- **Conformance-dominated** — space given to evidence that the implementation matches rules the author wrote, at the cost of material a peer would want.

Give each major section a verdict: **keep**, **deepen**, or **cut**. A section that cannot be deepened within the space is cut, and the freed space goes to the deepest section rather than to a new topic. If cutting leaves too little, the center was too thin and the work returns to step 2.

Then make one clean prose pass using **show, then stop**: where the paper praises, certifies, or announces the quality of its own solution, keep the engineering fact, evidence, boundary, or tradeoff and remove the verdict. Remove workflow terminology that does no work for the reader.

## The center, at the end

Read the finished draft against the commitment page in `scope.md`:

- Is there still one center, or has the paper become a survey of its topic?
- Does the title name the center the paper argues?
- Did any section acquire a fixed-count structure the material does not have?
- Is each claim bounded once, or hedged repeatedly?

## Findings

Every finding is fixed in the manuscript or recorded as an accepted limit with its reason. A limit that changes what the paper claims belongs in the paper; a limit that only matters to the workflow belongs in the ledger.
