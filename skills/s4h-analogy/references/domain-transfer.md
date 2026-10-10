# s4h-analogy-domain-transfer

Loaded through `skill_view(name="s4h-analogy", file_path="references/domain-transfer.md")`. Apply the complete procedure below to the current task.


# Analogy Domain Transfer

Your field has blind spots that your field created. The best solutions to structural
problems often exist already — in biology, military strategy, architecture, sport, logistics,
emergency medicine — because the underlying problem is not domain-specific. The work is
abstraction: strip away the domain details until the pattern is visible, then find where
that pattern is already solved.

---

## Your Process

**Step 1: Abstract the Problem to Structural Essence**
Describe the problem without any domain vocabulary. What is actually happening? What are
the actors, their relationships, the failure mode, the goal? The moment you can describe
it without industry jargon, you can search for it anywhere.

**Framing check:** Confirm the specific problem being transferred before continuing. State what you've identified — the actual challenge, its actors, and the failure mode or goal — in one sentence, then use a plain-text question with the options below, then wait for the user’s answer:
- **Question:** "I'm reading this as: [your one-sentence framing of the problem stripped of domain vocabulary]. Is that right?"
- **Header:** "Framing"
- **Options:**
  - **Yes — proceed** — framing is correct
  - **Adjust** — one element is off; user will correct it before you continue
  - **Reframe** — different situation than read; incorporate the correction before proceeding

**Step 2: Search Candidate Domains**
Consider where this structural pattern appears: biology (systems, adaptation, immunity),
military (logistics, command, deception), architecture (load, flow, resilience), sport
(coordination, pressure, strategy), gaming (rules, incentives, escalation), logistics
(sequencing, bottlenecks, routing), medicine (diagnosis, triage, recovery).

**Step 3: Extract the Core Mechanism**
For each candidate domain: what is the actual mechanism that solves the problem? Not the
surface story — the operational logic. How does it work, step by step?

**Step 4: Map Mechanism Back**
Translate the mechanism into your problem. What plays what role? What would be the
equivalent of each element? This is where analogies either click or reveal themselves as
superficial.

**Step 5: Test Where the Analogy Holds and Breaks**
Every analogy breaks somewhere. Where does the mechanism still work when mapped? Where does
it stop working? The break points tell you where to be careful and where the insight ends.

---

## Human Check-in

Before proceeding, use the a plain-text question with the options below, then wait for the user’s answer tool. State your interpretation of the situation in 1–2 sentences — what is being analyzed and what the core question is — then ask:

- **Question:** "My read: [your 1–2 sentence interpretation]. How do you want to proceed?"
- **Header:** "Scope"
- **Options:**
  - **Full analysis** — Complete all steps, reasoning shown throughout
  - **Key findings only** — Bottom-line output, skip step-by-step detail
  - **One domain transfer** — The single most structurally similar domain, fully developed
  - **Reframe** — The read is off; correct it and the analysis will follow the corrected framing

Proceed based on their selection. If the user reframes, incorporate the correction before running any analysis.

## Output Format

**Problem (abstracted — no domain vocabulary):**
> [Structural description]

**Candidate domains and mechanisms:**

| Domain | Analogous problem | Core mechanism | Strength of match |
|--------|------------------|----------------|-------------------|
| | | | |
| | | | |

**Best mapping:**
- Domain element → Your problem element (for each key pair)

**Where the analogy holds:**
> [Specific aspects]

**Where the analogy breaks:**
> [Specific aspects — don't skip this]

**Insight to import:**
> [The actionable mechanism translated back into your problem]

---

## Notes

A weak abstraction in Step 1 produces weak domain matches. If the domains found feel
obvious or already-familiar, the abstraction still contains domain assumptions — strip
further.

---

## What's Next

After delivering this output, use a plain-text question with the options below, then wait for the user’s answer to offer the next move:

- **Question:** "Domain transfer complete. What's next?"
- **Header:** "Next"
- **Options:**
  - `skill_view(name="s4h-logic", file_path="references/check.md")` — Validate that the transfer holds and conclusions follow
  - `skill_view(name="s4h-analogy", file_path="references/boundary-testing.md")` — Test where the analogy breaks down
  - `skill_view(name="s4h-creativity", file_path="references/alternatives.md")` — Use the transferred ideas to generate new alternatives
  - **Done** — Wrap up and synthesise what we have so far
