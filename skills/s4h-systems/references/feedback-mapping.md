# s4h-systems-feedback-mapping

Loaded through `skill_view(name="s4h-systems", file_path="references/feedback-mapping.md")`. Apply the complete procedure below to the current task.


# Systems Feedback Mapping

Most system failures come from unrecognized feedback loops — especially delayed balancing loops that cause overshoot and collapse. Reinforcing loops amplify change in one direction; balancing loops push back toward a target. Until both types are visible and named, diagnosis and intervention are guesswork.

---

## Your Process

**Step 1: Define System Boundary**
State what is inside the system and what is outside it. Name the time horizon and the key behavior to explain (growth, oscillation, collapse, stagnation).

**Framing check:** Confirm the specific system and the feedback relationship in focus before continuing. State what you've identified — the actual system being analyzed, its time horizon, and the behavior you're mapping — in one sentence, then use a plain-text question with the options below, then wait for the user’s answer:
- **Question:** "I'm reading this as: [your one-sentence framing of the system, time horizon, and behavior to explain]. Is that right?"
- **Header:** "Framing"
- **Options:**
  - **Yes — proceed** — framing is correct
  - **Adjust** — one element is off; user will correct it before you continue
  - **Reframe** — different situation than read; incorporate the correction before proceeding

**Step 2: List Key Variables**
Identify 5–10 variables that change over time and drive the behavior in question. These are stocks (levels that accumulate) or flows (rates of change). Be specific — "customer trust" not "sentiment".

**Before narrowing:** Show the complete generated set of candidate variables to the user first. Use a plain-text question with the options below, then wait for the user’s answer:
- **Question:** "I've identified [N] candidate variables. Before I narrow to the 5–10 most relevant for mapping feedback loops, are there any you'd flag as especially important, or any I've missed?"
- **Header:** "Prioritise"
- **Options:**
  - **Proceed with your selection** — the set looks right
  - **Flag one** — user will name a specific variable to include
  - **Add a missing one** — user will describe it

**Step 3: Map Causal Links**
For each variable pair where a relationship exists: does A increasing cause B to increase (same direction, +) or decrease (opposite direction, −)? Mark the polarity of each link.

**Step 4: Trace Loops**
Follow causal chains until they close back on themselves. Count the number of negative (−) links in the loop. Even number of negatives = reinforcing loop (R). Odd number = balancing loop (B). Name each loop.

**Step 5: Mark Delays**
Identify where cause is separated from effect in time. Delays are the primary source of oscillation and overshoot — a balancing loop with a long delay will overcorrect.

**Step 6: Identify the Dominant Loop**
Which loop is currently driving system behavior? The dominant loop changes as conditions change — map the transition conditions.

---

## Human Check-in

Before proceeding, use the a plain-text question with the options below, then wait for the user’s answer tool. State your interpretation of the situation in 1–2 sentences — what is being analyzed and what the core question is — then ask:

- **Question:** "My read: [your 1–2 sentence interpretation]. How do you want to proceed?"
- **Header:** "Scope"
- **Options:**
  - **Full analysis** — Complete all steps, reasoning shown throughout
  - **Key findings only** — Bottom-line output, skip step-by-step detail
  - **Reinforcing loops only** — What's accelerating in this system, skip balancing loops
  - **Reframe** — The read is off; correct it and the analysis will follow the corrected framing

Proceed based on their selection. If the user reframes, incorporate the correction before running any analysis.

## Output Format

**System Boundary:** [scope + time horizon + behavior to explain]

**Feedback Loop Table**

| Loop Name | Type (R/B) | Variables in Loop | Delay? | Current Strength |
|-----------|-----------|-------------------|--------|-----------------|
| | | | | |

**Dominant Loop:** [name] — [what behavior it produces]

**Delay Risks:** [which delays are creating overshoot or oscillation]

**What This Predicts:** [expected system behavior if current structure holds]

---

## Notes

Loops are not permanent — the dominant loop shifts as variables hit limits or thresholds. Map the transition condition that would shift dominance from one loop to another.

---

## What's Next

After delivering this output, use a plain-text question with the options below, then wait for the user’s answer to offer the next move:

- **Question:** "Feedback loops mapped. What's next?"
- **Header:** "Next"
- **Options:**
  - `skill_view(name="s4h-systems", file_path="references/leverage-analysis.md")` — Find leverage points within the feedback loops
  - `skill_view(name="s4h-temporal", file_path="references/cycle-detection.md")` — Detect cycles the feedback loops create
  - `skill_view(name="s4h-strategy", file_path="references/positioning.md")` — Position to exploit or break the key feedback loops
  - **Done** — Wrap up and synthesise what we have so far
