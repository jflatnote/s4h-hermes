# s4h-narrative-audience-modeling

Loaded through `skill_view(name="s4h-narrative", file_path="references/audience-modeling.md")`. Apply the complete procedure below to the current task.


# Narrative Audience Modeling

Communication fails at the receiver, not the sender. The most common communication failure is not poor evidence or unclear logic — it is delivering a message the audience was not ready to receive, about a problem they do not recognize, to a goal they do not hold. Modeling the audience before communicating means identifying not what you want to say, but what they are able to hear.

---

## Your Process

**Step 1: Name Specific People**
Resist generic categories. Not "senior leadership" but "the CFO and CTO who approved last quarter's roadmap". The more specific the audience, the more useful the model.

**Framing check:** Confirm the specific audience and communication context before continuing. State what you've identified — the actual people being modeled and the communication situation — in one sentence, then use a plain-text question with the options below, then wait for the user’s answer:
- **Question:** "I'm reading this as: [your one-sentence framing of the specific audience and the communication they need to receive]. Is that right?"
- **Header:** "Framing"
- **Options:**
  - **Yes — proceed** — framing is correct
  - **Adjust** — one element is off; user will correct it before you continue
  - **Reframe** — different situation than read; incorporate the correction before proceeding

**Step 2: Current Belief**
What do they already think about this topic? Include their current confidence level. This is the starting point — you are moving them from here, not from zero.

**Step 3: Real Goal**
What do they actually care about — the underlying motivation, not their stated preference? "Wants a decision" often means "wants to not be blamed for a bad outcome". Stated goals are proxies; find the underlying one.

**Step 4: Fear**
What do they need not to lose? Status, control, consistency with a prior decision, a relationship, a budget. Fear shapes reception more than aspiration does.

**Step 5: What Moves Them — and What Doesn't**
What evidence, framing, or messenger would change their mind? What definitely will not work, regardless of quality? Understanding the latter saves time.

**Step 6: Threshold Condition**
What must they hear or believe first, before they can receive anything else? If the threshold is not met, all subsequent communication fails regardless of content.

---

## Human Check-in

Before proceeding, use the a plain-text question with the options below, then wait for the user’s answer tool. State your interpretation of the situation in 1–2 sentences — what is being analyzed and what the core question is — then ask:

- **Question:** "My read: [your 1–2 sentence interpretation]. How do you want to proceed?"
- **Header:** "Scope"
- **Options:**
  - **Full analysis** — Complete all steps, reasoning shown throughout
  - **Key findings only** — Bottom-line output, skip step-by-step detail
  - **Threshold conditions only** — What would make this audience act or change their view
  - **Reframe** — The read is off; correct it and the analysis will follow the corrected framing

Proceed based on their selection. If the user reframes, incorporate the correction before running any analysis.

## Output Format

**Audience Table**

| Segment | Current Belief | Real Goal | Fear | What Moves Them | Threshold Condition |
|---------|---------------|----------|------|----------------|---------------------|
| | | | | | |

**Message Implications**
- Lead with: [threshold condition]
- Frame around: [real goal]
- Avoid: [what won't work]
- Primary ask: [what they need to do or decide]

---

## Notes

If the threshold condition is not met first, nothing else lands. Sequence matters as much as content. Address the threshold before making your argument.

---

## What's Next

After delivering this output, use a plain-text question with the options below, then wait for the user’s answer to offer the next move:

- **Question:** "Narrative audience modelled. What's next?"
- **Header:** "Next"
- **Options:**
  - `skill_view(name="s4h-communication", file_path="references/audience-modeling.md")` — Translate the narrative audience model into a communication plan
  - `skill_view(name="s4h-writing", file_path="references/tone-alignment.md")` — Align tone to what the narrative audience model revealed
  - `skill_view(name="s4h-narrative", file_path="references/tension-mapping.md")` — Map the tension points for this audience
  - **Done** — Wrap up and synthesise what we have so far
