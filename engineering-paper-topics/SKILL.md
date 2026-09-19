---
name: engineering-paper-topics
description: Select a focused topic for an engineering or industry application paper and hand the approved problem territory to engineering-paper. Use when a user needs to choose, narrow, assess, or title a paper topic before research and paper development begin.
disable-model-invocation: true
---

# Engineering Paper Topics

Choose a **problem territory**, not a prewritten paper: the engineering problem, application context, and boundaries that make it coherent. Stop before research, the paper's exact center or argument, solution design, implementation, datasets, validation, metrics, or manuscript structure; `engineering-paper` owns those decisions.

## Process

1. **Read the supplied material directly.** Extract established submission constraints, relevant facts, and available material. Keep these separate from your inferences. Preserve each source's established role; incidental content has no downstream authority unless that role is also established.

2. **Fix the space constraint first.** Establish the paper's available length or an equivalent limit before recommending topics. If it is absent, ask for it and wait. Judge every candidate by whether that space permits meaningful engineering depth without survey drift or filler.

3. **Resolve only consequential unknowns.** Ask the smallest next question whose answer could change topic suitability or honest wording, then reassess. In particular, establish real access to data, systems, implementations, operational experience, or other evidence when a candidate would depend on it. When intended contribution mode could materially change candidate selection, scope, or title strength, establish it before locking the topic rather than inferring it from capability or available evidence. Treat missing access as a constraint, not permission to assume it.

4. **Shortlist.** Develop a small set of genuinely strong problem territories, usually 1–3. Do not fill a quota with weaker options. Each must have:
   - one engineering problem;
   - a concrete application context;
   - boundaries tight enough for the available space;
   - a credible path to depth under the established material constraints.

   Prefer a current problem only when an established, decision-relevant change makes the engineering problem materially different or more important now. Fashionable terminology is not a rationale.

5. **Screen the wording.** Titles, descriptions, and claim strength must match what has actually been established. Do not turn feasibility judgments or recommendations into facts.

6. **Present candidates concisely.** First state the established constraints. Then give the strong candidates, each with a working title, bounded problem territory, and a brief suitability judgment labeled as agent synthesis. The user makes the final selection and may revise its wording or scope.

7. **Write the handoff after explicit approval.** Create a minimal Markdown topic file for `engineering-paper`:

```markdown
# <approved working title>

## Approved problem territory
- <approved engineering problem in its application context>

## Source references
- <source that downstream needs to locate>
```

Omit empty optional sections. A source reference carries only its established provenance and authority; its inclusion establishes no broader role. Topic approval applies only to the approved territory, not surrounding agent synthesis. `engineering-paper` owns all downstream interpretation and paper-development decisions.

Completion means every selected topic has been explicitly approved, and each topic file contains the approved territory plus only needed source references.
