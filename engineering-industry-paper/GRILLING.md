# Grilling the center

The output of this conversation is a center, the depth that makes it worth the space, and the evidence that exists for it — not a research design. No research questions, no hypotheses, no formal models, no planned experiment schedule unless the chosen problem genuinely needs one.

The brief is an input, not the scope. A title, direction, project, dataset, outline, or draft says where to look; the center is chosen from what the material and evidence will actually carry.

Fit decides whether a candidate is affordable in the space; depth decides whether it is worth reading.

## Fit

Do the candidate's commitments fit the space and the evidence?

Write them on one page: for each, the **mechanism**, the **claim** the paper will make about it, and the **evidence** you hold for that claim. Then hold the page against the length.

The length is the one the brief states. With none stated, ask before committing: every verdict below is a verdict about a space.

- The page overflows → the center is too broad. Narrow the center and keep the depth. General background, high-level architecture, and a list of best practices are what breadth converts into.
- The page is nearly empty → the center is too shallow. Go deeper into it, and if going deeper keeps yielding nothing consequential, replace the center rather than growing this one.
- The page fits → check each row's rung in [EVIDENCE.md](EVIDENCE.md) before committing.

Length alone does not make the page fit. Every row must be affordable at the depth the paper promises: enough space to explain the mechanism, the pressure behind it, the evidence, and the bound that matters. A named mechanism that can receive only a label or paragraph is a commitment to remove, not a topic to compress.

Keep the page: step 6 reads the finished draft against it, and it is what makes survey drift visible at the end.

When no real material exists yet, the fit test includes what the author can supply. Step 4 may have to produce the material before the paper can be written, and that is a reason to size the center smaller.

## Depth

Fit says the center is affordable. This says it has something to teach. Ask what a peer would carry away: the engineering knowledge the paper exists to hand over.

The strongest form is a **fork** — a consequential choice where a competent engineer could plausibly go the other way. The lesson is the choice, the pressure that produced it, and the cost of the road not taken. Forks look like: which constraint to respect and which to relax; where to put a boundary; what to fail on and what to degrade; how to sequence a migration; what to keep out of the trusted path; which of two mechanisms to pay for; when to stop retrying.

A fork is not required. A center with no real choice in it still carries depth when it explains what a peer could not have worked out alone: a **mechanism** that is not obvious, a failure path and how it is recognised, a root cause, a constraint interaction that only shows up in operation. What fails is a center that only restates what a competent engineer would already do — replace it rather than expanding it, because padding a forced design produces length without substance.

Any fork you name is one the work actually faced. A choice invented to give the paper a lesson is a fabricated fact about the work.

## Coupling: how many problems

The count follows coupling and space, never a target. One may be enough. Two or three belong in the same paper only when they are genuinely coupled — when solving one changes what the other must do. Two problems sharing nothing but the topic are two papers; take the one with more depth to teach.

## Survey drift

The pull to resist. A broad topic such as enterprise generative-AI data-leakage protection contains many distinct engineering problems. At the space and evidence one practice paper allows, one narrow mechanism explained properly beats six concerns given a paragraph each: the six-concern version reads as a survey of its topic and leaves a peer with nothing to carry away, while the one-mechanism version is what another engineer can actually reuse.

## Rounds

Work the candidate set as a frontier: gather the facts yourself, then put the whole open set to the author in one round, numbered, each with your recommended answer. Wait for the answers before the next round, because later questions usually depend on earlier ones. The `grilling` skill carries this discipline in full — invoke it when the center deserves a longer interrogation than this step needs.

## What goes to the author

Decide routine matters yourself from the material you have. Send these:

- A choice that would move the center, unless the author delegated the center to you.
- A real-world fact you cannot reach: what their system actually does, what the deployment actually costs, what the regulator actually said.
- Project experience only they hold.
- Private material the paper would need.
- Anything that would change how credible the evidence reads.

Ask once, in a batch, with your recommendation attached. The author's time is the scarce input.

## Output

`scope.md`: candidates with their fit and depth verdicts and rejection reasons, the grill log, the chosen center, and the one-page commitment list. Author-only questions go to `open.md`.
