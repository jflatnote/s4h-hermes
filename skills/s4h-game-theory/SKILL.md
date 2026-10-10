---
name: s4h-game-theory
description: "Routes to the right game-theory skill for your strategic situation. Triggers: 'game theory', 'strategic interaction', 'what will they do', 'payoff analysis', 'how do I think about this strategically', 'incentive design', 'cooperation problem', 'bidding strategy', any situation where the best choice depends on what others choose."
---

## Hermes execution contract

Use Hermes `skill_view` to load toolkit instructions and specific supporting files. Individual methods are references, not separately installed skills. Read the full selected method before applying it; domain summaries are not substitutes. Do not load every method at once. Carry the user's framing, constraints and previous outputs into each step. Ask the listed confirmation questions in ordinary text and wait for the user; never call a Claude-specific question tool. Treat skill execution as reasoning, not permission to run commands or change external systems.

Load only the method reference selected by the routing decision. For examples use files under `references/docs/` through the same `skill_view` interface. Cross-domain routes are listed in the master catalog.

## Method loading index

- auction: `skill_view(name="s4h-game-theory", file_path="references/auction.md")`
- coalition: `skill_view(name="s4h-game-theory", file_path="references/coalition.md")`
- equilibrium: `skill_view(name="s4h-game-theory", file_path="references/equilibrium.md")`
- iterated: `skill_view(name="s4h-game-theory", file_path="references/iterated.md")`
- mechanism-design: `skill_view(name="s4h-game-theory", file_path="references/mechanism-design.md")`
- prisoners-dilemma: `skill_view(name="s4h-game-theory", file_path="references/prisoners-dilemma.md")`
- signaling: `skill_view(name="s4h-game-theory", file_path="references/signaling.md")`


# Game Theory

Your best move depends on what they'll do — and their best move depends on what you'll do. This interdependence is the defining feature of strategic interaction. Game theory provides formal tools for reasoning through it: mapping payoffs, finding stable outcomes, designing incentives, and analysing how cooperation forms and breaks down.

---

## Your Process

**Step 1: Diagnose the interaction type**

Read the situation and identify which of the following patterns applies.

**Framing check:** Confirm the specific strategic situation before continuing. State what you've identified — the actual interaction, who the players are, and what decision is at stake — in one sentence, then use a plain-text question with the options below, then wait for the user’s answer:
- **Question:** "I'm reading this as: [your one-sentence framing of the strategic situation and the players involved]. Is that right?"
- **Header:** "Framing"
- **Options:**
  - **Yes — proceed** — framing is correct
  - **Adjust** — one element is off; user will correct it before you continue
  - **Reframe** — different situation than read; incorporate the correction before proceeding

- **One-shot strategic choice** — players make a single decision simultaneously or sequentially, and payoffs depend on the combination of choices. You need to identify the stable outcome (equilibrium) and whether it's efficient.
  → Use `skill_view(name="s4h-game-theory", file_path="references/equilibrium.md")`

- **Cooperation vs. defection** — each player is individually tempted to defect even though mutual cooperation would be better for everyone. You're facing a race to the bottom, collective action failure, or asking whether to cooperate or hold back.
  → Use `skill_view(name="s4h-game-theory", file_path="references/prisoners-dilemma.md")`

- **Credibility problem** — you have private information and need others to believe your claim, or you're being told something and aren't sure whether to believe it. Cheap talk, costly signalling, commitment devices.
  → Use `skill_view(name="s4h-game-theory", file_path="references/signaling.md")`

- **Rule design** — you're not playing the game, you're designing it. You want to create rules, incentives, or mechanisms that make players behave in a desired way — especially to elicit honest information or align self-interest with collective benefit.
  → Use `skill_view(name="s4h-game-theory", file_path="references/mechanism-design.md")`

- **Long-run repeated relationship** — the same two or more parties will interact repeatedly over time. Reputation, trust, retaliation, and the shadow of the future are all active.
  → Use `skill_view(name="s4h-game-theory", file_path="references/iterated.md")`

- **Coalition and fair division** — multiple players could form alliances and share gains. Which coalition will form? How should value be divided fairly? Who holds power?
  → Use `skill_view(name="s4h-game-theory", file_path="references/coalition.md")`

- **Competitive bidding** — a structured auction or procurement process where you're either bidding or designing the process. How much to bid? How to avoid the winner's curse? How to design a revenue-maximising or efficient auction?
  → Use `skill_view(name="s4h-game-theory", file_path="references/auction.md")`

**Step 2: Confirm and route**

Present the diagnosis clearly — what kind of interaction this is and which skill fits — then use a plain-text question with the options below, then wait for the user’s answer:
- **Question:** "My read: this is a [interaction type] situation — [one sentence explaining why, e.g. which payoff structure or strategic feature makes it so]. Run `/[sub-skill]`?"
- **Header:** "Direction"
- **Options:**
  - **Yes — run `/[sub-skill]`** — diagnosis is correct
  - **Show all options** — list the available sub-skills with one-line descriptions
  - **Different angle** — describe which aspect of the situation is most pressing

If the situation spans multiple types (e.g., a cooperation problem inside a long-run relationship), note both in the question and ask which dimension is most pressing before routing.

---

## Important distinction

Game theory provides formal payoff structure: it tells you what a rational player will do given the rules, payoffs, and other players. Strategy (see `skill_view(name="s4h-strategy")`) provides contextual wisdom: how to position, when to act, how to use terrain and timing. They are complementary — use game theory to understand the structure of the interaction, and strategy to act effectively within it. When both apply, use game theory first to clarify what the incentives actually are, then strategy to decide how to play.

---

## Notes

The category skills are: `skill_view(name="s4h-game-theory", file_path="references/equilibrium.md")`, `skill_view(name="s4h-game-theory", file_path="references/prisoners-dilemma.md")`, `skill_view(name="s4h-game-theory", file_path="references/signaling.md")`, `skill_view(name="s4h-game-theory", file_path="references/mechanism-design.md")`, `skill_view(name="s4h-game-theory", file_path="references/iterated.md")`, `skill_view(name="s4h-game-theory", file_path="references/coalition.md")`, `skill_view(name="s4h-game-theory", file_path="references/auction.md")`.

Related categories: `skill_view(name="s4h-strategy")` (contextual wisdom for acting within games), `skill_view(name="s4h-decision")` (single-player choice without strategic interaction), `skill_view(name="s4h-social")` (power dynamics and coalition politics).
