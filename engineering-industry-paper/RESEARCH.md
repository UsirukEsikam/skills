# Standing practice and sources

## Standing practice

Before a mechanism is written as the paper's contribution, find out how working engineers already solve that problem. The check is about placement: it keeps the paper from presenting common practice as its finding.

Look where practice lives — standards and their amendments, vendor and platform documentation, regulator guidance and enforcement notes, reference implementations and their issue trackers, engineering write-ups from teams running the system, published practice reports.

Then name the gap in engineering terms. Not "no prior work exists", but the specific way current practice stops short: an assumption that fails under this constraint, a control that does not cover this data path, a technique that does not survive this scale, a documented behaviour the documentation omits. When standing practice already covers the problem, the honest outcomes are that the paper's contribution is the part that is genuinely different, however small, or that the center moves.

## Enough

Stop when further searching would not move the paper. The practice question is answered when these are settled:

- How do working engineers already handle this problem, and in what setting?
- Is this work then an ordinary implementation of a known approach, or does something in it differ?
- If it differs, is that difference the thing the paper explains, placed in engineering terms against what practice does?

Once those hold, another vendor page, amendment, or write-up changes the background, not the center or the claims. Keep searching while a specific question still gates a claim — a clause's applicability, one vendor's documented behaviour — and stop when none does. Coverage is the criterion, not a count of sources, vendors, or papers.

## Applicability

A source counts when the situation matches: comparable scale, same kind of system, same regulatory environment, similar operating constraints. An enterprise deployment story, a hyperscaler write-up, and a standard clause are not interchangeable. Where you rely on material from an adjacent setting, say so in the manuscript next to the claim.

## The role of standards and regulation

Regulations and standards support engineering constraints, governance requirements, and operating conditions — the shape of the problem and the rules a solution must live inside. They are evidence about what the system must satisfy, not evidence that a mechanism works. A standard cited as proof that a design reduces risk is a category error.

## Checking a source

Open it. Record in `sources.md` what it is, what you checked it for, the passage that supports the claim, and the date you read it. A source you could not open is not cited. A claim held at second hand is traced to the original or dropped.

## Subagents

One focused, bounded question per subagent, returning findings with their sources; the main agent folds them in and owns what the paper claims. Two disciplines:

- Research answers the chosen center's questions. More related material is not a reason to widen the center or add a section.
- Read the ledger first. Work already done is reused rather than redone.
