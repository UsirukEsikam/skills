---
name: engineering-paper-topics
description: Select and approve focused topics for engineering or industry application papers.
disable-model-invocation: true
---

# Engineering paper topics

Select a **problem territory** for an engineering paper, obtain the user's approval, and write a compact handoff to `engineering-paper`.

Territory comprises the engineering problem, application context, and boundaries needed to keep the paper coherent. Leave the route—research, exact center and argument, solution design, implementation, datasets, validation, metrics, and manuscript structure—to `engineering-paper`.

## Selection rules

- **Length governs.** A suitable topic supports meaningful engineering depth within the available space. It is too broad if it would become a survey or catalogue, and too narrow if it would require filler. Prefer one problem or a tightly coupled problem set.
- **Reality governs wording.** Establish relevant access to systems, projects, data, implementations, operating experience, and other evidence. Missing evidence is a constraint, not permission to invent a downstream plan. Titles and descriptions must not imply implementation, deployment, established practice, validation, results, or evidence strength that has not been established.
- **Provenance governs facts.** Keep user statements, submission requirements, supplied material, existing-system facts, and verified sources distinct from agent synthesis. Recommendations, feasibility judgments, and candidate approval do not establish inferred facts or route choices.
- **Current pressure must earn its place.** Prefer a current engineering problem when a specific, supported change in standards, regulation, operating conditions, scale, cost, reliability, security, workflow, or deployment constraints materially changes its importance or scope. Fashionable terminology and generic “why now” claims do not count.
- **Approval belongs to the user.** Present only genuinely strong candidates and treat them as proposals until explicitly approved.

## Process

### 1. Build the selection brief

Read relevant supplied files and material directly. Extract only what can change topic selection:

- venue, audience, eligible paper type, exclusions, and durable submission constraints;
- length or another explicit space limit, including layout rules that materially affect usable space;
- the user's goals, interests, preferences, and candidate ideas;
- systems, projects, data, tools, experience, implementations, and evidence the user actually holds or can access;
- deadlines, capabilities, or access limits that affect feasibility.

Ask only for missing information that would materially change the candidate set, one blocking uncertainty at a time. Establish the available length or space constraint before recommending topics. Establish evidence or material access before retaining a candidate when that access affects suitability or the strength of its wording.

**Done when** the governing length and every known constraint, preference, asset, or evidence gap that could materially change selection are clear.

### 2. Select territories

Treat each candidate as a concrete engineering problem in context, not a technology label or a proposed solution. Test it for:

1. **Application fit** — useful to the intended engineering or industry audience.
2. **Substance** — available or realistically obtainable material can support consequential engineering treatment.
3. **Boundary** — its context, included problem, and exclusions form coherent territory without choosing the route.
4. **Length-fit** — it permits depth without survey drift or filler.
5. **Feasibility** — the user's evidence, access, capabilities, and time can support it.

Narrow broad ideas through the engineering setting, system boundary, operating constraint, or failure mode. Broaden thin ideas only with tightly coupled problems that deepen the same territory.

Check for a current pressure only when it could change selection, scope, or priority. Verify decision-changing factual questions with trustworthy sources; otherwise avoid research. Retain a source in the final handoff only when it is needed to understand the approved territory or a durable constraint.

Reject or weaken candidates whose required evidence is unavailable. Keep every title no stronger than the established facts and material support.

**Done when** a small set of distinct candidates passes all five tests and every evidence-dependent or current-pressure claim is appropriately supported.

### 3. Obtain approval

Present **1–3** strong candidates; present fewer rather than fill a quota. For each, state concisely:

- a working title naming the problem and context;
- the concrete focus and main boundary;
- why it fits the submission, user context, and available length;
- any material feasibility condition or uncertainty;
- a “why now” reason only when a supported current pressure is decision-relevant.

Do not outline the manuscript, choose its argument, or propose its solution, implementation, dataset, validation, or metrics. Ask which candidate the user approves or wants changed. After a material scope change, reapply all five tests.

**Done when** the user explicitly approves each selected topic and its scope, and every approved version is unambiguous.

### 4. Write the handoff

Create `paper-topics/` and write one Markdown file per approved topic, using a short filesystem-safe slug. Do not write files for unapproved candidates.

Use only the applicable headings and omit empty ones:

```markdown
# <Approved topic>

## Submission constraints
<Durable venue, audience, paper type, length, and material-format constraints>

## Engineering focus
<Approved engineering problem in its application context>

## Scope boundaries
<Included territory and adjacent territory deliberately excluded>

## Established context
<Material assets, evidence, existing-system facts, access limits, and unresolved constraints needed to begin downstream work; link sources or supplied file paths>
```

Point to supplied material instead of copying it. Exclude selection rationale, rejected candidates, exploratory discussion, generic background, feasibility recommendations, and process notes.

Apply the territory/route boundary to every entry. Include a route-specific detail only when it is already a user-supplied constraint, submission requirement, or existing-system fact. Preserve missing assets and evidence gaps as constraints; do not convert them into research, design, implementation, dataset, validation, metric, or manuscript decisions.

**Done when** every approved topic has one compact file containing its length constraint, approved problem and scope, and only the established material or constraints needed for `engineering-paper`; no entry or title claims unestablished work, status, or evidence.
