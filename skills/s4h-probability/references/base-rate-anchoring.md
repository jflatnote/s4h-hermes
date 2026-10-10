# s4h-probability-base-rate-anchoring

Loaded through `skill_view(name="s4h-probability", file_path="references/base-rate-anchoring.md")`. Apply the complete procedure below to the current task.


# Probability Base Rate Anchoring

The most common forecasting error is treating every situation as unique and ignoring what usually happens. Kahneman called this neglecting the outside view. Before adjusting for what makes this situation special, you must first establish what happens in situations like this one. The base rate is the outside view — the answer to "what fraction of attempts like this one succeed?" — and it is almost always more informative than inside-view reasoning about this particular case.

---

## Your Process

**Step 1: State the Prediction or Estimate**
Name the specific outcome being predicted and the current estimate or intuition. What is being forecast and at what implied probability?

**Framing check:** Confirm the specific prediction before continuing. State what you've identified — the outcome being forecast, the current intuitive estimate, and the time horizon — in one sentence, then use a plain-text question with the options below, then wait for the user’s answer:
- **Question:** "I'm reading this as: [your one-sentence framing of the prediction and implied probability]. Is that right?"
- **Header:** "Framing"
- **Options:**
  - **Yes — proceed** — framing is correct
  - **Adjust** — one element is off; user will correct it before you continue
  - **Reframe** — different situation than read; incorporate the correction before proceeding

**Step 2: Find the Reference Class**
What category of similar situations does this belong to? This is the most important and contested step. The reference class should be: (a) large enough to have stable base rates, (b) genuinely similar in the ways that matter, (c) not cherry-picked to flatter the prediction. If multiple reference classes apply, note them all.

**Step 3: Find the Base Rate**
How often does this outcome actually occur in that reference class? Use historical data where available. If the exact rate is unknown, estimate a range from the most similar data available. This is the outside view — state it plainly, even if it is uncomfortable.

**Step 4: Adjust for Differentiating Factors**
What specific, verifiable features of this situation distinguish it from the reference class? For each: does it push the probability up or down from the base rate? Explicitly consider factors that cut against your prior, not only those that support it.

**Step 5: State as a Range**
Combine the base rate with adjustments to produce a final probability range, not a point estimate. The range should reflect genuine uncertainty.

---

## Human Check-in

Before proceeding, use the a plain-text question with the options below, then wait for the user’s answer tool. State your interpretation of the situation in 1–2 sentences — what is being analyzed and what the core question is — then ask:

- **Question:** "My read: [your 1–2 sentence interpretation]. How do you want to proceed?"
- **Header:** "Scope"
- **Options:**
  - **Full analysis** — Complete all steps, reasoning shown throughout
  - **Key findings only** — Bottom-line output, skip step-by-step detail
  - **Base rate only** — Identify the historical rate without Bayesian adjustment
  - **Reframe** — The read is off; correct it and the analysis will follow the corrected framing

Proceed based on their selection. If the user reframes, incorporate the correction before running any analysis.

## Output Format

**Prediction:** [the specific outcome + current intuitive estimate]

**Reference Class:** [the category used + why it applies]

**Base Rate:** [historical frequency in this class + data source or basis]

**Adjustment Factors**

| Factor | Direction (↑/↓) | Magnitude | Rationale |
|--------|----------------|-----------|-----------|
| | | | |

**Final Estimate:** [range — low to high] — [brief rationale]

**Calibration Note:** [if final estimate differs substantially from base rate, explain why the differentiating factors justify the gap]

---

## Notes

Only adjust from the base rate when you have specific, verifiable reasons — not because the situation feels different. The inside view always feels justified; the outside view is the corrective.

---

## What's Next

After delivering this output, use a plain-text question with the options below, then wait for the user’s answer to offer the next move:

- **Question:** "Base rates anchored. What's next?"
- **Header:** "Next"
- **Options:**
  - `skill_view(name="s4h-probability", file_path="references/scenario-weighting.md")` — Weight scenarios against the established base rate
  - `skill_view(name="s4h-probability", file_path="references/confidence-calibration.md")` — Calibrate confidence given what the base rates revealed
  - `skill_view(name="s4h-decision", file_path="references/criteria-weighting.md")` — Feed adjusted probabilities into the decision criteria
  - **Done** — Wrap up and synthesise what we have so far
