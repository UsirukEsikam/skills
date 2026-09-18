---
name: engineering-paper-topics
description: Develop and approve focused topics for engineering or industry application papers.
disable-model-invocation: true
---

# Engineering paper topics

Select topics through discussion, then preserve each approved topic as a compact input to `engineering-paper`.

The governing test is **length-fit**: the topic must support meaningful engineering depth inside the allowed paper length. Favor concrete engineering problems that can sustain substantive analysis, implementation, validation, operating experience, or another useful technical treatment. Academic novelty is not required.

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

### 2. Find length-fit centers

Treat each candidate as a proposed **center**: the concrete engineering problem the paper would examine, not a technology label.

For each plausible center, test:

1. **Application fit** — it addresses a real engineering or industry problem for the intended audience.
2. **Substance** — available or realistically obtainable material can support meaningful analysis, implementation, validation, operational lessons, or tradeoff discussion.
3. **Boundary** — the included problem is explicit, and adjacent problems can be excluded without making the topic incoherent.
4. **Length-fit** — the important work can be covered at useful depth within the allowed space, without survey drift or filler.
5. **Feasibility** — the user's access, capabilities, evidence, and time can support the proposed treatment.

Narrow broad ideas by choosing the engineering setting, system boundary, operating constraint, failure mode, decision, or tightly related problem set that carries the most substance. Broaden thin ideas only with closely coupled problems or evidence that deepen the same center; do not attach unrelated subtopics merely to fill space.

When a current factual question about a technology, practice, trend, or problem could change a candidate's suitability, verify that fact with available trustworthy sources. Research only the decision-changing question, and retain the source and supported fact for the eventual topic file. Skip external research when the supplied material already supports the selection decision.

**Done when** a small set of distinct candidates passes all five tests.

### 3. Propose and discuss candidates

Present a small number of distinct candidates, usually **1–3**, according to how many genuinely fit. Do not fill a quota with weaker candidates. For each, give:

- a working topic or title;
- the concrete focus;
- why it fits the submission and the user's context;
- why its scope fits the allowed length, including the main boundary that keeps it focused;
- any material feasibility condition or uncertainty.

Keep these explanations short. Do not outline sections, design the paper's argument, or begin the downstream paper work.

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
<Concrete problem or tightly related problem set>

## Scope boundaries
<What is included and the adjacent territory deliberately excluded>

## Why this topic fits
<Concise rationale covering application value, substance, feasibility, and length-fit>

## Established facts and decisions
<Material user decisions and verified facts, with source links or supplied-material locations where applicable>
```

Point to supplied material by path instead of copying it. Preserve only facts and decisions needed to start `engineering-paper`; leave exploratory conversation, rejected candidates, generic background, and selection-process notes out of the file.

Do not add an outline, section plan, thesis, argument structure, research plan, implementation design, validation design, or prose intended for the paper. Those belong to `engineering-paper`.

**Done when** every approved topic has one file in `paper-topics/`, every file records the applicable length constraint and scope boundary, and no unapproved topic or downstream paper work appears in the files.
