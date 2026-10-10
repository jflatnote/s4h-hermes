# s4h-resource-allocation-analysis

Loaded through `skill_view(name="s4h-resource", file_path="references/allocation-analysis.md")`. Apply the complete procedure below to the current task.


# Resource Allocation Analysis

Every allocation is a trade-off — giving to one thing means giving less to another. The problem is that most allocations are made implicitly, leaving the trade-offs invisible. Making trade-offs explicit forces honest prioritisation and prevents the political habit of pretending everything can be fully funded.

---

## Your Process

**Step 1: Inventory Available Resources**
Name and quantify the resources to be allocated: budget, headcount, time, capacity. Be precise about what is actually available — not what is desired.

**Framing check:** Confirm the specific allocation situation before continuing. State what resources you've identified and the decision context they apply to in one sentence, then use a plain-text question with the options below, then wait for the user’s answer:
- **Question:** "I'm reading this as: [your one-sentence framing — e.g. 'Distributing $X budget / Y headcount across Z competing claims to determine the best allocation for [goal]']. Is that right?"
- **Header:** "Framing"
- **Options:**
  - **Yes — proceed** — framing is correct
  - **Adjust** — one element is off; user will correct it before you continue
  - **Reframe** — different situation than read; incorporate the correction before proceeding

**Step 2: List All Competing Claims**
Every demand on the resource. Include maintenance and ongoing commitments, not just new initiatives. Claims that are implicitly assumed to be funded should be made explicit here.

**Step 3: Assess Each Claim**
For each claim: what is the strategic priority (how directly does this serve the most important goals)? What is the cost of under-resourcing it (what breaks, slows, or is lost if it receives less)?

**Step 4: Identify Constraints**
Are there minimums (must have at least X to function), maximums (more than Y produces no additional value), or dependencies (A must be funded before B makes sense)?

**Step 5: Draft an Allocation**
Distribute the available resource across claims. At this stage, make the trade-offs explicit: write down what each claim gives up under this draft allocation.

**Step 6: Sense-Check Against Overall Goals**
Does this allocation, taken as a whole, serve the most important outcomes? Where is the allocation driven by politics or inertia rather than strategic priority?

---

## Human Check-in

Before proceeding, use the a plain-text question with the options below, then wait for the user’s answer tool. State your interpretation of the situation in 1–2 sentences — what is being analyzed and what the core question is — then ask:

- **Question:** "My read: [your 1–2 sentence interpretation]. How do you want to proceed?"
- **Header:** "Scope"
- **Options:**
  - **Full analysis** — Complete all steps, reasoning shown throughout
  - **Key findings only** — Bottom-line output, skip step-by-step detail
  - **Trade-off table only** — What each allocation gives up, skip the full recommendation
  - **Reframe** — The read is off; correct it and the analysis will follow the corrected framing

Proceed based on their selection. If the user reframes, incorporate the correction before running any analysis.

## Output Format

### Available Resources
| Resource | Total Available |
|----------|----------------|
| ... | ... |

### Competing Claims
| Claim | Strategic Priority | Cost of Under-Resourcing | Constraints |
|-------|------------------|-------------------------|-------------|
| ... | High / Medium / Low | ... | Min / Max / Dependency |

### Draft Allocation
| Claim | Allocation | Trade-off (what it gives up) |
|-------|-----------|------------------------------|
| ... | ... | ... |

### Strategic Alignment Check
Does this allocation serve the most important outcomes? Where does it diverge from strategic priority — and is that divergence justified?

---

## Notes

The most useful output is the trade-off column — if the trade-offs can't be written clearly, the allocation hasn't been thought through. Force each trade-off to be named before the allocation is finalised.

---

## What's Next

After delivering this output, use a plain-text question with the options below, then wait for the user’s answer to offer the next move:

- **Question:** "Allocation analysed. What's next?"
- **Header:** "Next"
- **Options:**
  - `skill_view(name="s4h-resource", file_path="references/bottleneck-analysis.md")` — Find bottlenecks in the current allocation
  - `skill_view(name="s4h-decision", file_path="references/criteria-weighting.md")` — Weight criteria by resource constraints
  - `skill_view(name="s4h-resource", file_path="references/waste-audit.md")` — Audit for waste in the current allocation
  - **Done** — Wrap up and synthesise what we have so far
