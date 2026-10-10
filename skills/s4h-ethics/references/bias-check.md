# s4h-ethics-bias-check

Loaded through `skill_view(name="s4h-ethics", file_path="references/bias-check.md")`. Apply the complete procedure below to the current task.


# Ethics Bias Check

Algorithms that treat everyone the same can still discriminate. A ranking that optimises for engagement may systematically deprioritise certain groups. A model trained on historical data may encode historical injustice. A feature that works well on average may fail badly for users who aren't the implicit default.

This check surfaces those patterns before they ship.

---

## Your Process

**Step 1: Define the system**
What is the algorithm, model, or automated decision? What is its input? What is its output? Who does it make decisions *about*? What happens to people based on its output?

**Framing check:** Confirm the specific system before continuing. State what you've identified — the actual system being audited, its outputs, and the population it affects — in one sentence, then use a plain-text question with the options below, then wait for the user’s answer:
- **Question:** "I'm reading this as: [your one-sentence framing of the system, its outputs, and who it affects]. Is that right?"
- **Header:** "Framing"
- **Options:**
  - **Yes — proceed** — framing is correct
  - **Adjust** — one element is off; user will correct it before you continue
  - **Reframe** — different situation than read; incorporate the correction before proceeding

**Step 2: Identify the implicit default**
Every system has a default user in mind — often implicitly. Ask:
- Who was this optimised for?
- Whose behaviour or data was used to train or calibrate it?
- Who is absent from the training set or design process?

The implicit default is often the demographic that experiences least friction. Others bear the cost of that assumption.

**Step 3: Check for direct bias**
Does the system use protected characteristics (age, gender, race, disability, location as proxy for race, etc.) as features, or correlates that map closely to them? Does it produce different outcomes for different demographic groups? Is that difference *justified* (e.g. a medical dosage model that accounts for body weight) or *unjustified* (e.g. a loan model that penalises postcodes that correlate with race)?

**Step 4: Check for proxy bias**
Protected characteristics don't need to be explicit to create discriminatory outcomes. Audit the features used:
- Which features correlate with protected characteristics?
- Could the model achieve similar accuracy without the proxy, and if so, is there a reason it uses it?
- What's the *historical source* of the training data? Does it encode past discriminatory practices?

**Step 5: Check the feedback loop**
Many deployed systems create the conditions that confirm their own predictions. A recommendation system that shows users content they're predicted to engage with can entrench filter bubbles. A fraud model that flags more accounts from a certain demographic leads to more investigations of that demographic, which produces more evidence that "justifies" the bias. Ask: does this system create or amplify the patterns it's trying to predict?

**Step 6: Assess the harm distribution**
When the system makes errors, who bears the cost?
- False positives and false negatives are not equally distributed — who experiences more of each?
- What happens to a person when the system is wrong about them? Is the cost significant?
- Do people have recourse? Can they appeal or correct the system's decision about them?

---

## Human Check-in

Before proceeding, use the a plain-text question with the options below, then wait for the user’s answer tool. State your interpretation of the situation in 1–2 sentences — what is being analyzed and what the core question is — then ask:

- **Question:** "My read: [your 1–2 sentence interpretation]. How do you want to proceed?"
- **Header:** "Scope"
- **Options:**
  - **Full analysis** — Complete all steps, reasoning shown throughout
  - **Key findings only** — Bottom-line output, skip step-by-step detail
  - **Disparate impact only** — Flag differential outcomes without full root-cause analysis
  - **Reframe** — The read is off; correct it and the analysis will follow the corrected framing

Proceed based on their selection. If the user reframes, incorporate the correction before running any analysis.

## Output Format

**System Being Audited:**
[What it does, inputs, outputs, who it affects]

**Implicit Default**
[Who the system is optimised for; who may be disadvantaged by that assumption]

**Bias Findings**

| Dimension | Finding | Severity |
|---|---|---|
| Direct bias (protected characteristics) | [finding] | 🔴 / 🟡 / 🟢 |
| Proxy bias (correlated features) | [finding] | 🔴 / 🟡 / 🟢 |
| Training data issues | [finding] | 🔴 / 🟡 / 🟢 |
| Feedback loop risk | [finding] | 🔴 / 🟡 / 🟢 |
| Error cost distribution | [finding] | 🔴 / 🟡 / 🟢 |

**Most Significant Concern**
[One specific, concrete finding that warrants most attention]

**Recommended Actions**
- [Specific mitigation per finding, or "escalate to ethics-council" for significant concerns]

---

## Notes

A clean bias check is not a guarantee of fairness — it is evidence of serious effort. Bias is often subtle and emerges at scale. Where this check surfaces concerns, treat them as decisions to be made consciously, not problems to be explained away.

For systems with high-stakes outputs (credit, hiring, healthcare, content moderation), this check is a minimum. Consider ongoing monitoring post-deployment, not just a pre-ship audit.

---

## What's Next

After delivering this output, use a plain-text question with the options below, then wait for the user’s answer to offer the next move:

- **Question:** "Biases identified. What's next?"
- **Header:** "Next"
- **Options:**
  - `skill_view(name="s4h-ethics", file_path="references/check.md")` — Run a full ethical assessment of the bias-affected reasoning
  - `skill_view(name="s4h-logic", file_path="references/fixer.md")` — Correct bias-induced logic errors
  - `skill_view(name="s4h-decision", file_path="references/criteria-weighting.md")` — Re-weight decision criteria after removing bias
  - **Done** — Wrap up and synthesise what we have so far
