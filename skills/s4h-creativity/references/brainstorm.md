# s4h-creativity-brainstorm

Loaded through `skill_view(name="s4h-creativity", file_path="references/brainstorm.md")`. Apply the complete procedure below to the current task.


You are running an orchestrated creative thinking session. Rather than applying a single tool, this session selects and sequences the most appropriate thinking methods for the user's specific situation, then synthesizes across their outputs.

## How to read the situation

Before selecting methods, diagnose what kind of thinking challenge this is:

**Is the problem itself unclear or stuck?**
→ Start with `skill_view(name="s4h-creativity", file_path="references/assumption-excavator.md")`. The problem framing may be what's blocking progress, not the problem itself.

**Is the user locked into one approach?**
→ Start with `skill_view(name="s4h-creativity", file_path="references/lateral-thinking.md")`. The dominant idea needs to be named and escaped before other tools are useful.

**Is it early-stage exploration?**
→ Start with `skill_view(name="s4h-creativity", file_path="references/water-logic.md")` or `skill_view(name="s4h-creativity", file_path="references/random-entry.md")`. Generate movement and map the territory before applying structured tools.

**Does the user need to see the full solution space?**
→ Use `skill_view(name="s4h-creativity", file_path="references/concept-fan.md")` or `apc`. Expand options systematically before evaluating any of them.

**Does the user need to evaluate something?**
→ Use `cort-pmi` (for a specific idea) or `skill_view(name="s4h-creativity", file_path="references/six-hats.md")` (for a full multi-perspective analysis).

**Are people and their reactions central?**
→ Include `cort-ops` to map the perspectives of those affected.

**Does the situation need a provocation to break it open?**
→ Use `po` for a deliberate jolt into non-obvious territory.

## Human Check-in

Before proceeding, use the a plain-text question with the options below, then wait for the user’s answer tool. State your interpretation of the situation in 1–2 sentences — what is being analyzed and what the core question is — then ask:

- **Question:** "My read: [your 1–2 sentence interpretation]. How do you want to proceed?"
- **Header:** "Scope"
- **Options:**
  - **Full analysis** — Complete all steps, reasoning shown throughout
  - **Key findings only** — Bottom-line output, skip step-by-step detail
  - **Two methods only** — Most relevant pair of tools applied at full depth, skip synthesis across more
  - **Reframe** — The read is off; correct it and the analysis will follow the corrected framing

Proceed based on their selection. If the user reframes, incorporate the correction before running any analysis.

## Session structure

### Opening: Diagnose the challenge
Briefly state your read of the situation: what kind of thinking challenge is this, and why? This surfaces your reasoning and gives the user a chance to correct it before work begins.

**Framing check:** Confirm the specific challenge before continuing. State what you've identified — the actual problem being explored and its key parameters — in one sentence, then use a plain-text question with the options below, then wait for the user’s answer:
- **Question:** "I'm reading this as: [your one-sentence framing of the specific challenge and what's at stake]. Is that right?"
- **Header:** "Framing"
- **Options:**
  - **Yes — proceed** — framing is correct
  - **Adjust** — one element is off; user will correct it before you continue
  - **Reframe** — different situation than read; incorporate the correction before proceeding

### Middle: Apply 2–4 methods in sequence
Select the methods that best fit the diagnosis.

**Before narrowing:** Show the full set of candidate methods to the user first. Use a plain-text question with the options below, then wait for the user’s answer:
- **Question:** "I've identified [N] methods that fit this challenge: [list them with one-line rationale each]. Before I select the most relevant 2–4, are there any you'd flag as especially important, or any I've missed?"
- **Header:** "Prioritise"
- **Options:**
  - **Proceed with your selection** — the set looks right
  - **Flag one** — user will name a specific method to include
  - **Add a missing one** — user will describe it

Apply each selected method fully — do not abbreviate to get through more methods. A thorough application of 2 methods produces more value than a superficial pass through 5.

**Between methods, make the connection explicit:** "The lateral thinking session revealed [X]. Now the concept fan will explore [Y] by treating [X] as the starting point." Methods should build on each other, not run in parallel.

### Close: Synthesize
**Before synthesising:** State what each method surfaced in one sentence each. Use a plain-text question with the options below, then wait for the user’s answer:
- **Question:** "Here's what each method found: [one bullet per method]. Before I synthesise, does any direction stand out, or is anything missing?"
- **Header:** "Synthesis direction"
- **Options:**
  - **Synthesise as planned** — methods covered the ground
  - **Weight [direction]** — user will name which thread to emphasise
  - **Add a missing angle** — user will name a dimension not yet covered

After the methods are complete, synthesize across the outputs. This is not a summary — it is an integration. What do the different methods, taken together, reveal that no single method showed on its own?

The synthesis should answer:
- What is the most important insight this session produced?
- What direction deserves the most attention, and why?
- What should happen next?

## Output format

**Reading the situation:**
[Your diagnosis — what kind of challenge is this, what methods you're selecting and why]

---

## [Method 1 name]
[Full application of the method]

---

## [Method 2 name]
[Full application, building on method 1 where relevant]

---

## [Method 3 name if used]
[Full application]

---

## Synthesis
**What this session revealed:**
[2–3 paragraphs integrating across all methods — what the full picture shows]

**Most important direction:**
[The single most valuable direction to pursue, with reasoning]

**Recommended next step:**
[A specific, concrete action]

## Notes on quality

The session's value depends on the depth of each method application, not the number of methods used. It is better to run `skill_view(name="s4h-creativity", file_path="references/assumption-excavator.md")` and `skill_view(name="s4h-creativity", file_path="references/lateral-thinking.md")` thoroughly than to touch six methods superficially.

The synthesis is the hardest and most important part. Most sessions produce insights in the individual method sections. The synthesis should produce an insight that only becomes visible when those outputs are held together.

If the user's challenge shifts during the session — if the assumption excavator reveals that the real problem is different from the stated one — follow the actual problem, not the original framing.

---

## What's Next

After delivering this output, use a plain-text question with the options below, then wait for the user’s answer to offer the next move:

- **Question:** "Brainstorm complete. What's next?"
- **Header:** "Next"
- **Options:**
  - `skill_view(name="s4h-decision", file_path="references/criteria-weighting.md")` — Evaluate the brainstorm output against weighted criteria
  - `skill_view(name="s4h-creativity", file_path="references/plus-minus-interesting.md")` — Assess the top ideas fairly before committing
  - `skill_view(name="s4h-constraint", file_path="references/hardness-testing.md")` — Test which ideas are actually feasible
  - **Done** — Wrap up and synthesise what we have so far
