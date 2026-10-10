# 🎯 Probability

> *Your confidence and your evidence are rarely in the same proportion.*

---

## What this category is

Probability tools apply quantitative reasoning to uncertainty — calibrating confidence against evidence, anchoring estimates in base rates before adjusting for specifics, calculating expected value across options, and building explicit probability-weighted scenarios. These tools exist because human intuition about probability is systematically biased: we're overconfident about our predictions, underweight base rates, and make different decisions about the same choice depending on how it's framed.

The toolkit doesn't eliminate uncertainty. It makes the uncertainty explicit and reasoned rather than implicit and guessed.

---

## When to reach for it

- Making a decision where the outcome is uncertain and the stakes are high
- Estimating something important — time, cost, probability of success — and you want to check your calibration
- Comparing options with different risk/reward profiles
- Multiple scenarios could unfold and you want to think explicitly about each
- Someone (or you) expresses high confidence about something that might not warrant it

---

## When *not* to reach for it

**Don't use probability tools when the uncertainty is irreducible and the decision is values-based.** Calculating expected value requires assigning value to outcomes — and when those value assignments are contested (e.g., how to weigh financial gain against stakeholder harm), you're in [Ethics](https://github.com/human-avatar/skills-for-humanity/blob/main/docs/ethics) territory.

**Don't manufacture false precision.** Assigning a 73% probability to something when you have weak evidence is worse than saying "I'm moderately confident." Probability tools should surface genuine uncertainty, not disguise it with numbers.

The nearest neighbor: [Decision](https://github.com/human-avatar/skills-for-humanity/blob/main/docs/decision) — which handles the choice process, while probability tools handle the uncertainty quantification that feeds into choices.

---

## Skills in this category

| Skill | What it does | Trigger when... |
|---|---|---|
| **`skill_view(name="s4h-probability")`** | Routes to the right probability skill for your situation | Not sure which tool fits; describe your situation |
| [`skill_view(name="s4h-probability", file_path="references/base-rate-anchoring.md")`](base-rate-anchoring.md) | Anchors estimates in historical base rates before adjusting | Estimate feels optimistic; "outside view"; "how often does this actually happen?" |
| [`skill_view(name="s4h-probability", file_path="references/confidence-calibration.md")`](confidence-calibration.md) | Tests whether stated confidence matches available evidence | "Am I overconfident?" "How sure should I be?" "Is this as certain as it seems?" |
| [`skill_view(name="s4h-probability", file_path="references/expected-value-calculation.md")`](expected-value-calculation.md) | Calculates expected value to compare options under uncertainty | "Is this risk worth taking?" "Expected value?" Comparing asymmetric options |
| [`skill_view(name="s4h-probability", file_path="references/scenario-weighting.md")`](scenario-weighting.md) | Assigns explicit probabilities to distinct scenarios before deciding | Multiple plausible futures; "assign probabilities"; "quantify the uncertainty" |

**Not sure which tool?** → Invoke `skill_view(name="s4h-probability")` — it diagnoses your situation and picks the right skill.

---

## Related categories

- [Decision](https://github.com/human-avatar/skills-for-humanity/blob/main/docs/decision) — for the full decision process using probability outputs
- [Temporal](https://github.com/human-avatar/skills-for-humanity/blob/main/docs/temporal) — for scenario and futures thinking at a strategic level
- [Logic](https://github.com/human-avatar/skills-for-humanity/blob/main/docs/logic) — for the logical structure of reasoning under uncertainty
