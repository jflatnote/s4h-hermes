---
name: s4h-strategy
description: "Routes to the right strategy skill for any adversarial or competitive reasoning situation. Triggers: 'how do I beat X', 'competitive strategy', 'outmaneuver', 'I'm up against', 'position myself', 'what's my play here', any situation involving competitive pressure, adversarial dynamics, negotiation, or resource-constrained contest."
---

## Hermes execution contract

Use Hermes `skill_view` to load toolkit instructions and specific supporting files. Individual methods are references, not separately installed skills. Read the full selected method before applying it; domain summaries are not substitutes. Do not load every method at once. Carry the user's framing, constraints and previous outputs into each step. Ask the listed confirmation questions in ordinary text and wait for the user; never call a Claude-specific question tool. Treat skill execution as reasoning, not permission to run commands or change external systems.

Load only the method reference selected by the routing decision. For examples use files under `references/docs/` through the same `skill_view` interface. Cross-domain routes are listed in the master catalog.

## Method loading index

- alliance: `skill_view(name="s4h-strategy", file_path="references/alliance.md")`
- deception: `skill_view(name="s4h-strategy", file_path="references/deception.md")`
- force-economy: `skill_view(name="s4h-strategy", file_path="references/force-economy.md")`
- intelligence: `skill_view(name="s4h-strategy", file_path="references/intelligence.md")`
- positioning: `skill_view(name="s4h-strategy", file_path="references/positioning.md")`
- terrain: `skill_view(name="s4h-strategy", file_path="references/terrain.md")`
- timing: `skill_view(name="s4h-strategy", file_path="references/timing.md")`
- victory: `skill_view(name="s4h-strategy", file_path="references/victory.md")`


# Strategy

Sun Tzu's central insight: "The victorious warrior wins first and then goes to war, while the defeated warrior goes to war first and then seeks to win." Strategy is what happens before the contest. It is the discipline of creating conditions — position, intelligence, timing, alliances — so that when the contest begins, the outcome is already determined.

The strategy skills in this category draw on Sun Tzu (*The Art of War*), Clausewitz (*On War*), Miyamoto Musashi (*Book of Five Rings*), and competitive theory. They are not about aggression. They are about reading competitive contexts clearly and acting with economy, intelligence, and timing.

---

## Your Process

Read the user's situation carefully. Identify which strategic challenge is primary, then present the options below — briefly and specifically — and ask which fits. Execute immediately on selection.

**Framing check:** Confirm the competitive situation before continuing. State what you've identified — the actor, the opponent or competitive pressure, and the primary objective at stake — in one sentence, then use a plain-text question with the options below, then wait for the user’s answer:
- **Question:** "I'm reading this as: [your one-sentence framing of the actor, the adversarial dynamic, and the goal]. Is that right?"
- **Header:** "Framing"
- **Options:**
  - **Yes — proceed** — framing is correct
  - **Adjust** — one element is off; user will correct it before you continue
  - **Reframe** — different situation than read; incorporate the correction before proceeding

**Reading the landscape — where should I compete, and where should I avoid?**
→ `skill_view(name="s4h-strategy", file_path="references/terrain.md")` — Maps available positions, identifies favorable and dangerous ground, tells you which battles are worth fighting.

**What do I actually know, and what am I assuming?**
→ `skill_view(name="s4h-strategy", file_path="references/intelligence.md")` — Audits what you know vs. what you're assuming about yourself and your opponent. Closes the intelligence gaps that cause strategic failures.

**When should I act — now, or wait?**
→ `skill_view(name="s4h-strategy", file_path="references/timing.md")` — Analyzes conditions favoring action vs. patience. Reads your opponent's rhythm. Identifies trigger conditions for the right moment.

**How do I do more with less — I'm outgunned?**
→ `skill_view(name="s4h-strategy", file_path="references/force-economy.md")` — Finds the minimum intervention that achieves the objective. Identifies leverage points where a small input creates a large output.

**How do I create a position that's hard to attack?**
→ `skill_view(name="s4h-strategy", file_path="references/positioning.md")` — Builds the conditions for unassailability before the contest. What must be true for a rational opponent to choose a different arena?

**What should I reveal vs. conceal — information asymmetry?**
→ `skill_view(name="s4h-strategy", file_path="references/deception.md")` — Manages information asymmetry in legitimate competitive contexts. Protects your position; identifies what your opponent may be concealing from you.

**What does winning actually mean here?**
→ `skill_view(name="s4h-strategy", file_path="references/victory.md")` — Defines victory before the contest begins. Prevents the pyrrhic trap: winning in ways that lose the larger goal.

**Who do I need on my side — coalition and alliance?**
→ `skill_view(name="s4h-strategy", file_path="references/alliance.md")` — Maps parties, identifies natural allies and swing parties, assesses alliance stability. Alliances built on shared interest vs. goodwill alone.

---

## Routing Confirmation

After diagnosing, use a plain-text question with the options below, then wait for the user’s answer before routing:
- **Question:** "My read: this is a [type] situation — [one sentence why]. Run `/[sub-skill]`?"
- **Header:** "Direction"
- **Options:**
  - **Yes — run `/[sub-skill]`** — diagnosis is correct
  - **Show all options** — list all eight sub-skills with one-line descriptions
  - **Different angle** — describe which aspect of the competitive situation is most pressing

Adapt [type], [why], and [sub-skill] based on the primary strategic challenge identified.

---

## Output Format

Present the 3–4 most relevant options for the user's specific situation (not all eight every time). For each option, one sentence on why it fits. Ask which they want. Execute immediately on selection without further preamble.

---

## Notes

If the objective itself is unclear, start with `skill_view(name="s4h-strategy", file_path="references/victory.md")` — you cannot select terrain, timing, or force economy without knowing what winning means. If the situation is genuinely complex, terrain is usually the right first move: it establishes the ground on which all other choices operate.

Strategy skills are for competitive and adversarial contexts. For purely cooperative situations where parties share objectives, the decision and systems categories are more appropriate.
