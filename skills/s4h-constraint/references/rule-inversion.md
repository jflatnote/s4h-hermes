# s4h-constraint-rule-inversion

Loaded through `skill_view(name="s4h-constraint", file_path="references/rule-inversion.md")`. Apply the complete procedure below to the current task.


# Constraint Rule Inversion

Most constraints are treated as walls. This skill treats them as foundations. The limit that
seems like an obstacle is often the thing that forces the insight — the moment you stop
trying to work around it and start designing with it, better solutions appear.

---

## Your Process

**Step 1: Name the Constraint Precisely**
State the constraint in a single, unambiguous sentence. Vague constraints produce vague
inversions. "We have no budget" is too loose. "We have $0 for external tooling for Q3" is
something you can work with.

**Framing check:** Confirm the specific constraint before continuing. State what you've identified — the actual constraint and the goal it is blocking — in one sentence, then use a plain-text question with the options below, then wait for the user’s answer:
- **Question:** "I'm reading this as: [your one-sentence framing of the constraint and the goal it blocks]. Is that right?"
- **Header:** "Framing"
- **Options:**
  - **Yes — proceed** — framing is correct
  - **Adjust** — one element is off; user will correct it before you continue
  - **Reframe** — different situation than read; incorporate the correction before proceeding

**Step 2: Ask What the Constraint Forces**
What does this constraint make you do that you'd otherwise avoid? What comfortable defaults
does it eliminate? The constraint is doing work — what work?

**Step 3: Invert — Restate as a Design Requirement**
Convert the limit into a positive requirement: "must cost nothing" becomes "must work with
only what we already have." The constraint is now the spec, not the problem.

**Step 4: Generate Solutions That Only Work Because of the Constraint**
Produce 3-5 solutions that are impossible or inferior without the constraint. These are not
workarounds — they are solutions the constraint made visible.

**Step 5: Select for Unexpected Value**
**Before narrowing:** Show the complete generated set to the user first. Use a plain-text question with the options below, then wait for the user’s answer:
- **Question:** "I've identified [N] solutions that only work because of the constraint. Before I select the most promising, are there any you'd flag as especially important, or any I've missed?"
- **Header:** "Prioritise"
- **Options:**
  - **Proceed with your selection** — the set looks right
  - **Flag one** — user will name a specific solution to include
  - **Add a missing one** — user will describe it

Pick the solution where the constraint creates the most unexpected advantage — the one that
would not have been found without the limit.

---

## Human Check-in

Before proceeding, use the a plain-text question with the options below, then wait for the user’s answer tool. State your interpretation of the situation in 1–2 sentences — what is being analyzed and what the core question is — then ask:

- **Question:** "My read: [your 1–2 sentence interpretation]. How do you want to proceed?"
- **Header:** "Scope"
- **Options:**
  - **Full analysis** — Complete all steps, reasoning shown throughout
  - **Key findings only** — Bottom-line output, skip step-by-step detail
  - **One inversion only** — The single most powerful constraint flip
  - **Reframe** — The read is off; correct it and the analysis will follow the corrected framing

Proceed based on their selection. If the user reframes, incorporate the correction before running any analysis.

## Output Format

**Constraint (precise):**
> [Single sentence, unambiguous]

**Inverted form (as design requirement):**
> [Positive restatement]

**Solutions that use the constraint:**

| # | Solution | Why it requires the constraint | Strength |
|---|----------|-------------------------------|----------|
| 1 | | | |
| 2 | | | |
| 3 | | | |

**Most promising:**
> [Solution name] — [1-2 sentences on why the constraint creates unexpected value here]

---

## Notes

Every analogy breaks somewhere — so does every inversion. If the inverted form produces
solutions that would work equally well without the constraint, the inversion wasn't deep
enough. Go back to Step 2.

---

## What's Next

After delivering this output, use a plain-text question with the options below, then wait for the user’s answer to offer the next move:

- **Question:** "Rules inverted. What's next?"
- **Header:** "Next"
- **Options:**
  - `skill_view(name="s4h-creativity", file_path="references/lateral-thinking.md")` — Use the inverted rules as springboards for lateral moves
  - `skill_view(name="s4h-decision", file_path="references/option-mapping.md")` — Map new decision options the inversions open up
  - `skill_view(name="s4h-constraint", file_path="references/hardness-testing.md")` — Test whether the inverted rules reveal softer constraints
  - **Done** — Wrap up and synthesise what we have so far
