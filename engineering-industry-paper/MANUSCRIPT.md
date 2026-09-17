# The manuscript

Written in the submission language. `manuscript.md` is the source of truth: the DOCX is built from it, never alongside it.

## Voice

An engineer explaining a concrete piece of work to technical peers. Concrete actors, components, actions, data flow, decisions, observations, consequences, tradeoffs — the specific instance ahead of the general statement: which component, which message, which threshold, which failure mode, at what cost.

Write for the peer. Phrasing squeezed to look human-made costs the clarity a technical reader depends on.

Chinese drafts: fix a term once and keep it, give sentences concrete subjects rather than opening paragraphs with template phrasing such as 综上所述 or 本文提出了一种…方案, and let the verbs carry the engineering.

## Section jobs

The material decides the sections. A shape that usually fits a practice paper:

- The problem as it appears in real work, and where ordinary practice stops short.
- The mechanism, with the choices inside it: what was chosen, the pressure behind it, what it cost.
- What was done, and what was observed.
- Where the mechanism holds, and where it does not.

Treat these as jobs, not as a heading list. Merge, split, and reorder to follow the argument. A fixed count of contributions, innovations, or sections is scaffolding the material did not ask for.

**The peer test** governs every section: a technical peer should learn something concrete and non-obvious — a constraint they had not accounted for, a failure mode, a tradeoff with a price, an applicability limit, an implementation difficulty. A section that only restates what a competent engineer would already write is too thin for its space; deepen it, or cut it and give the space to the section that earns it.

## Implementation

Implementation detail earns space when it exposes a consequential choice, a constraint, a tradeoff, a failure path, an interface, or experience a peer could reuse. Class and module inventories, object definitions, and directory structures are artifacts of the implementation; they appear where they carry one of those, and describing what exists is not the same as explaining why it is that way and what it cost.

## Mathematics

LaTeX in the Markdown. An equation earns its place by carrying a constraint, a tradeoff, a bound, or a relation the prose would take longer to state; three lines of algebra that replace a paragraph and a half of careful wording are a good trade. Keep one authoritative form of each equation — the DOCX renders it rather than restating it.

## Tables

Tables carry comparisons, parameters, and mappings that prose would make hard to read: what differs, by how much, under what conditions. Content comes from the manuscript or from an explicit structured source in the ledger. Authorship belongs to the manuscript; assembly formats what is there.

## Figures

Optional, and frequently the wrong choice — prose, a table, or three lines of pseudocode often carry the same information in less space. A figure earns its place when it shows structure or behaviour that words leave the reader reconstructing.

Constructed diagrams and plots get a reproducible programmable source where practical, and publication-quality output at the size the final document uses; no particular tool or file format is required. Original evidence images — photographs, screenshots, captures — are used as they are.

Generating a figure and assembling the document are separate jobs. Produce the asset first; assembly places a finished asset.

## Checking the draft

Before review, read the draft once against the commitment page in `scope.md`: does each section still serve the chosen center, and has any part drifted back into survey — related concerns covered evenly and shallowly?
