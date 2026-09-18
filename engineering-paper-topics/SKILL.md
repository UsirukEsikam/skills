---
name: engineering-paper-topics
description: Develop and approve focused topics for engineering or industry application papers.
disable-model-invocation: true
---

# Engineering paper topics

Select topics through discussion, then preserve each approved topic as a compact input to `engineering-paper`.

Topic selection fixes the **territory**: the engineering problem, its application context, necessary scope boundaries, and established constraints. It leaves the **route** to `engineering-paper`: research, the paper's exact center and argument, models or algorithms, technical approach, system mechanisms, implementation design, datasets, validation metrics or protocols, manuscript structure, and word allocation.

A title obeys the same boundary. It may name a technology when that technology is the application context, object under study, or an established constraint; it must not turn an agent-proposed solution into part of the approved topic.

Apply a **provenance gate** throughout candidate discussion and topic files. State a fact or constraint as established only when it is traceable to the user, submission requirements, supplied material, an existing system, or a trustworthy source. Agent synthesis may propose territory and assess fit, but it remains a proposal or assessment; it does not establish inferred facts or downstream choices.

The governing test is **length-fit**: the topic must support meaningful engineering depth inside the allowed paper length. Favor concrete engineering problems for which enough engineering substance and evidence are available or realistically obtainable. Academic novelty is not required.

A topic is:

- **too broad** when the available length would force a field survey, a catalogue of concepts or problems, or superficial coverage;
- **too narrow** when filling the available length would require repetition, padding, or needless expansion;
- **length-fit** when its important problems can be treated properly and the available space can be filled with consequential engineering content. This usually means one problem or a small, tightly related problem set rather than an entire technology area.

## Process

### 1. Build the selection brief

Read the supplied material relevant to topic selection, including calls for papers, submission rules, references, project material, professional context, technical capabilities, interests, and existing ideas. Inspect relevant supplied files rather than asking the user to restate them.

Extract only information that can affect selection:

- submission theme, audience, eligible paper type, and exclusions;
- length limit and any formatting rules that materially change usable space;
- accessible systems, projects, data, tools, experience, and evidence;
- the user's interests, goals, preferences, and candidate ideas;
- deadlines or feasibility constraints that limit what can be implemented or validated.

Ask only for missing facts or decisions that would materially change the candidates. Ask progressively: resolve the next blocking uncertainty rather than presenting a generic questionnaire. If the allowed length is absent, ask for it before recommending topics; accept words, characters, pages plus relevant layout rules, or another explicit space constraint.

**Done when** the usable length and the constraints, assets, and preferences that materially shape topic selection are known.

### 2. Find length-fit territories

Treat each candidate as proposed **territory**: a concrete engineering problem in context, not a technology label or proposed solution.

For each plausible territory, test:

1. **Application fit** — it addresses a real engineering or industry problem for the intended audience.
2. **Substance** — available or realistically obtainable material can support a useful engineering treatment at depth.
3. **Boundary** — the problem, context, and exclusions define coherent territory without choosing the downstream route.
4. **Length-fit** — the important work can be covered at useful depth within the allowed space, without survey drift or filler.
5. **Feasibility** — the user's access, capabilities, evidence, and time can support the proposed treatment.

Narrow broad ideas by choosing the engineering setting, system boundary, operating constraint, failure mode, or tightly related problem set that carries the most substance. Broaden thin ideas only with closely coupled problems or evidence that deepen the same territory; do not attach unrelated subtopics merely to fill space.

Run a **pressure scan** across the plausible territories: look for recent or emerging changes in operating conditions, standards, regulation, scale, cost, reliability, security, workflows, or deployment constraints that create or materially alter the engineering problem. Use a pressure only when it is concrete and supported; a fashionable technology label is not a reason to prefer a candidate. Among territories that pass all five tests, prefer those with a stronger application consequence, sharper unresolved tension, or better-supported reason the problem is worth addressing now. A conventional territory remains valid when no more distinctive current problem genuinely fits.

When a current factual question about a technology, practice, trend, or problem could change a candidate's suitability, verify that fact with available trustworthy sources. Research only the decision-changing question, and retain the source and supported fact for the eventual topic file. Skip external research when the supplied material already supports the selection decision.

**Done when** a small set of distinct candidates passes all five tests and any claimed current pressure is supported.

### 3. Propose and discuss candidates

Present a small number of distinct candidates, usually **1–3**, according to how many genuinely fit. Do not fill a quota with weaker candidates. For each, give:

- a working topic or title that names the problem and context without committing to an unestablished route;
- the concrete focus;
- why it fits the submission and the user's context;
- why the problem is worth addressing now, when a supported current pressure gives it that edge;
- why its scope fits the allowed length, including the main boundary that keeps it focused;
- any material feasibility condition or uncertainty.

Keep these explanations short and pass every factual statement through the provenance gate. Describe feasibility in terms of available access, evidence, capability, and time rather than by inventing an implementation or validation route. Do not outline sections, design the paper's argument, or begin the downstream paper work.

The user owns acceptance. Ask which candidate they approve or want changed. If they question, reject, combine, narrow, or broaden a candidate, address the concern and revise the candidate set. Reapply all five tests after every material scope change; do not treat an earlier fit judgment as carrying over automatically.

**Done when** the user explicitly approves one or more topics and each approved version is unambiguous.

### 4. Write approved topic files

Create `paper-topics/` in the current project and write one Markdown file per approved topic. Use a short filesystem-safe slug; when collision is possible, add a distinguishing suffix. Do not create files for merely proposed topics.

Each file contains only established downstream context under these headings, omitting empty headings:

```markdown
# <Approved topic>

## Submission constraints
<Relevant venue, audience, paper type, length, and material format constraints>

## Engineering focus
<Concrete problem or tightly related problem set, in its application context>

## Scope boundaries
<What is included and the adjacent territory deliberately excluded>

## Why this topic fits
<Concise rationale covering application value, substance, feasibility, length-fit, and any supported current pressure that materially strengthens the topic>

## Established facts and decisions
<Material user-supplied facts or constraints and selection-relevant verified facts, with source links or supplied-material locations where applicable>
```

Point to supplied material by path instead of copying it. Preserve only facts and decisions needed to start `engineering-paper`; leave exploratory conversation, rejected candidates, generic background, and selection-process notes out of the file.

Apply the territory/route boundary to every entry, including the title. A route-specific detail belongs only when it enters selection as a user-supplied constraint, a submission requirement, or the reality of an existing system. Feasibility analysis, an agent recommendation, discussion of a possible route, or approval of an agent-proposed candidate does not make that route an established fact or decision. Leave all other downstream choices to `engineering-paper`, and include no paper outline or prose intended for the manuscript.

**Done when** every approved topic has one file in `paper-topics/`, every file records the applicable length constraint and scope boundary, no unapproved topic appears, and every route-specific detail is traceable to a user-supplied constraint, submission requirement, or existing-system fact.
