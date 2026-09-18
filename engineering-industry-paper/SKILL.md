---
name: engineering-industry-paper
description: Write or revise an engineering-practice paper (工程实践论文 / 技术应用论文) from an approved topic, developing one focused engineering problem in depth. Use for technical or industry papers, including Chinese submissions and the DOCX they require.
---

# Engineering practice paper

A paper for engineering application: an engineer explaining a concrete piece of work to technical peers, built around **one focused engineering problem developed in depth**.

This skill begins with an **approved topic**. It may come from `engineering-industry-paper-topics` or directly from the user; no handoff artifact is required. The approved topic fixes the substantive territory. Preserve any scope boundaries the user or topic-selection output states explicitly; where detailed boundaries are absent, establish them while grilling the center. Execution refines the paper's center, commitments, mechanism, claims, evidence, depth, and fit inside that topic. A move outside the topic's territory or an explicit boundary is a topic change: return it to the user or the topics skill rather than making it silently.

The default failure is **survey drift**: the topic contains many engineering problems, the draft covers many of them, and the result is structurally complete with nothing a peer can reuse. Every step below exists to hold the paper against that pull.

Submission requirements — length, section list, template, reference format — come from the user or the call for papers. Length is never assumed: with none stated, it is a question for the author, and the center is not committed before the space is known or the author waives it.

Depth is not more formulas, citations, experiments, statistics, terminology, or code. Depth is concrete constraints, consequential choices, mechanisms, tradeoffs, failure modes, application difficulty, and experience a peer could carry to their own problem.

Steps are not ceremonies. Where trustworthy work already exists — a scope decision, a verified source list, a manuscript — it is reused and only the missing steps run.

**Verification is direct contact.** A check completes only when the underlying object has been inspected in the form relevant to the claim: the opened source and supporting passage, the producer artifact behind an empirical claim, or the rendered page at delivery size. Ledgers and reports preserve locations, findings, and dispositions; they do not establish that the inspection occurred, and generating an artifact does not establish that anyone inspected it. Where independence is required, only the independent read satisfies the step. Without direct contact, leave the check open or narrow the claim.

## Ledger

Long-lived facts live in a `paper/` directory in the project, not only in the conversation.

| Path | Holds |
|---|---|
| `brief.md` | Submission requirements; the author's facts the paper relies on, and where the author's material lives |
| `scope.md` | Candidate centers, the grill log, the chosen center and its fit and depth argument |
| `sources.md` | Every external source, what it was checked for, the passage supporting each claim |
| `evidence.md` | Each paper claim, the rung its evidence sits on, the provenance of each number |
| `open.md` | The single home for open questions: what only the author can answer, and their answers as they arrive |
| `review.md` | The truth and substance findings, their disposition, and whether the truth read used fresh context |
| `manuscript.md` | The editable paper — the single source of truth for the deliverable |
| `figures/` | Generated assets and the sources that produced them |

Adapt the set to the job. What matters: a later session, a subagent, or the author picks the work up without re-deriving it, and no fact the paper relies on lives only in context. Point at material that already exists rather than copying it — the ledger holds what later steps need, not a second copy of the author's documents.

## Steps

### 1. Read the brief

Identify the approved topic from the user's instruction or supplied material and record it with any stated boundaries. A topic file from `engineering-industry-paper-topics` is one possible input, not a prerequisite. If the material supplies only a broad direction, project, or dataset and no topic has been approved, stop and ask the user to provide one or use the topics skill; do not select one here.

Extract the requirements and the facts the author supplied — including the ones dropped in passing, which are the ones most often lost. Write them down first; where the author supplied material that already exists as a document, record where it is and the facts the paper will draw from it, rather than a copy of it. Classify each supplied artifact by role: evidence, author material, submission requirement, or format calibration. A format-calibration artifact contributes layout and format properties only; its claims, identities, numbers, subject matter, citations, and bibliography are outside the paper's content sources. A requirement the brief does not state — length above all — is a question for the author, not a default.

**Done when** the approved topic and any stated boundaries, the requirement set, and artifact roles are in `brief.md`; the facts the paper relies on are in the ledger marked as the author's or traceable to the author's material by location; and any missing requirement is in `open.md`. Everything else is yours to establish.

### 2. Grill the center

The load-bearing step. Within the approved topic, propose candidate centers and interrogate each against **fit**, and for the depth that makes it worth the space. Gather the facts yourself; put to the author only what turns on author intent, real-world facts you cannot reach, project experience, private material, or a choice that would move the center.

The center is the one decision that always goes to the author, unless they have explicitly delegated it; where they have, decide it yourself and do not send it back for confirmation. Refining the center or title must preserve the approved topic's substantive territory and any explicitly stated boundaries. Where detailed boundaries were not supplied, establish them through this grilling. A candidate outside the territory or an explicit boundary is a proposed topic change and requires explicit user approval. Narrowing the title is part of this step: the title follows the center.

Read [GRILLING.md](GRILLING.md).

**Done when** one center inside the approved topic is chosen and argued, every rejected candidate carries a reason, and every open question is answered or recorded in `open.md`. Drafting waits on the center being settled — by the author's answer, or by your own decision where they delegated it.

### 3. Check standing practice

Before a mechanism is written as worth reading, find how working engineers already solve it — to place the paper's mechanism against practice and name the gap in engineering terms, not to claim novelty.

Read [RESEARCH.md](RESEARCH.md).

**Done when** every mechanism the paper presents as its contribution stands against standing practice, the gap is named, every source behind it was opened and recorded in `sources.md`, and further searching would not move the center, the main claims, or the background the paper needs.

### 4. Engineer the work

Whatever the center needs: an implementation, a measurement, an analysis, a design, an operating record, a failure investigation. The center chooses; there is no default menu.

Read [EVIDENCE.md](EVIDENCE.md).

**Done when** every commitment in the paper has evidence you actually hold, its rung has been assigned from the primary artifact that produced it, every number reaches its producer, and every claim that outran its evidence has been narrowed rather than defended.

### 5. Draft the manuscript

Write `paper/manuscript.md` in the submission language, with LaTeX mathematics.

Read [MANUSCRIPT.md](MANUSCRIPT.md).

**Done when** every section passes the peer test and the draft carries no scaffolding the material did not ask for. Expect to cut: freed space goes to the deepest section, not to a new topic.

### 6. Review

Read [REVIEW.md](REVIEW.md). Separate the truth read from the substance read. When the environment provides fresh context, run the truth read there: the reviewer has not seen the authoring conversation and receives the primary evidence as well as the ledger.

**Done when** `review.md` records the two reads and their dispositions, every load-bearing empirical claim has been checked at its producer, every major section carries a verdict — keep, deepen, or cut — reached on substance as well as truth, and every finding is fixed in the manuscript or recorded as an accepted limit. A center that review shows to be too thin sends the work back to step 2.

### 7. Deliver

When the deliverable is a DOCX, assemble it from `manuscript.md`.

Read [ASSEMBLY.md](ASSEMBLY.md).

**Done when** the DOCX holds nothing the manuscript does not, every table and figure traces to its source, extracted text and structure pass a mechanical parity scan, and a retained render of the final DOCX has been inspected page by page at delivery size with equations, punctuation, tables, and figures intact.

## Subagents

Dispatch one focused, bounded question per subagent — a clause's applicability, a vendor's documented behaviour, a regulator's position, an independent read of a section — and have each return findings and sources into the ledger. The main agent owns the center, the tradeoffs, and what enters the paper. Finding more related material is not a reason to widen the center.
