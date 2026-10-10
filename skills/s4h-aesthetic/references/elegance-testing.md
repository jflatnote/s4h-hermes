# s4h-aesthetic-elegance-testing

Loaded through `skill_view(name="s4h-aesthetic", file_path="references/elegance-testing.md")`. Apply the complete procedure below to the current task.


# Aesthetic Elegance Testing

Complexity is the default outcome of design by committee, incremental revision, and
deference to edge cases. Each addition is locally defensible. The cumulative result is
a system no one would have designed on purpose. Elegance is not simplicity for its own
sake — it is the property of a solution where every element earns its place and nothing
obscures the core. This skill tests for that property.

---

## Your Process

**Step 1: State the Solution**
Describe the design, plan, system, or solution in enough detail to evaluate its parts.
If it's a process, name the steps. If it's a system, name the components. If it's a
strategy, name the moves.

**Framing check:** Confirm the specific solution before continuing. State what you've identified — the actual artifact being tested and its apparent purpose — in one sentence, then use a plain-text question with the options below, then wait for the user’s answer:
- **Question:** "I'm reading this as: [your one-sentence framing of the solution and what it is meant to accomplish]. Is that right?"
- **Header:** "Framing"
- **Options:**
  - **Yes — proceed** — framing is correct
  - **Adjust** — one element is off; user will correct it before you continue
  - **Reframe** — different situation than read; incorporate the correction before proceeding

**Step 2: Define the Irreducible Core**
What is the minimum that does the job? State in one sentence what the solution must
accomplish to succeed. Every element that doesn't directly serve this core is a
candidate for removal. If you can't state the core in one sentence, the solution may
not have one — which is itself a finding.

**Step 3: Element Audit**
For each component, mechanism, layer, or step: is it necessary for the core job, or
did it accrete over time to handle edge cases, satisfy stakeholder requests, hedge
against unlikely scenarios, or address problems that may not exist? Label each
clearly: **necessary** or **accreted**.

**Step 4: Concept Count**
How many distinct concepts must a new person learn to understand and use this
solution fully? Elegant solutions have fewer. Count them explicitly. Compare against
the irreducible minimum — the number of concepts required if every accreted element
were removed. The gap is the complexity overhead.

**Step 5: Thirty-Second Explanation Test**
Can you explain the solution in 30 seconds to someone intelligent but unfamiliar
with it? Attempt the explanation. If it requires more than 30 seconds, complexity
may be genuine — or it may be a sign the design hasn't been thought through clearly
enough to be simple. Both are worth knowing.

**Step 6: Sources of Unnecessary Complexity**
For each accreted element: what introduced it, and what would removing it cost? Some
removals are free — the element was pure noise. Some involve real trade-offs — the
element serves a secondary purpose worth naming. Distinguish them explicitly.

---

## Human Check-in

Before proceeding, use the a plain-text question with the options below, then wait for the user’s answer tool. State your interpretation of the situation in 1–2 sentences — what is being analyzed and what the core question is — then ask:

- **Question:** "My read: [your 1–2 sentence interpretation]. How do you want to proceed?"
- **Header:** "Scope"
- **Options:**
  - **Full analysis** — Complete all steps, reasoning shown throughout
  - **Key findings only** — Bottom-line output, skip step-by-step detail
  - **Accidental complexity only** — What could be removed without losing anything that matters
  - **Reframe** — The read is off; correct it and the analysis will follow the corrected framing

Proceed based on their selection. If the user reframes, incorporate the correction before running any analysis.

## Output Format

**Core Job:** [one sentence — what the solution must accomplish to succeed]

**Element Audit**

| Element | Necessary or Accreted | Rationale |
|---|---|---|
| [component/mechanism/step] | [necessary / accreted] | [why it does or doesn't serve the core] |

**Concept Count:** [n currently required] vs [n at irreducible minimum] — overhead: [gap]

**30-Second Explanation Test:** [pass / fail — include the actual attempt]

**Sources of Unnecessary Complexity**

| Accreted Element | How It Was Introduced | Cost of Removal |
|---|---|---|
| [element] | [origin] | [what is lost if removed] |

**Recommended Simplifications:** [specific removals or reductions, with trade-offs named]

---

## Notes

The question is not "can we defend every element" but "does every element earn its
place." Elements that can be defended are not the same as elements that are necessary
— hold the higher bar. Elegance is achieved not when there is nothing left to add,
but when there is nothing left to remove.

---

## What's Next

After delivering this output, use a plain-text question with the options below, then wait for the user’s answer to offer the next move:

- **Question:** "Elegance tested. What's next?"
- **Header:** "Next"
- **Options:**
  - `skill_view(name="s4h-aesthetic", file_path="references/simplicity-analysis.md")` — Simplify what elegance testing flagged as complex
  - `skill_view(name="s4h-writing", file_path="references/prose-elevation.md")` — Elevate prose flagged as inelegant
  - `skill_view(name="s4h-aesthetic", file_path="references/coherence-check.md")` — Verify that elegance is coherent with the whole
  - **Done** — Wrap up and synthesise what we have so far
