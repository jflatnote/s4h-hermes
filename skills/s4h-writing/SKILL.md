---
name: s4h-writing
description: "Routes to the right writing skill for any fiction, non-fiction, or professional writing challenge. Use when you say 'my character feels flat', 'the story isn't working', 'this scene falls flat', 'the dialogue sounds wrong', 'the prose is clunky', 'the argument isn't landing', 'write a report', 'executive summary', 'the tone keeps shifting', 'line editing', 'my world feels thin', 'POV problems', 'inconsistency check', 'write copy', 'technical documentation', 'audience calibration', 'rhetorical analysis', or any time you have a writing problem but aren't sure which specific tool fits."
---

## Hermes execution contract

Use Hermes `skill_view` to load toolkit instructions and specific supporting files. Individual methods are references, not separately installed skills. Read the full selected method before applying it; domain summaries are not substitutes. Do not load every method at once. Carry the user's framing, constraints and previous outputs into each step. Ask the listed confirmation questions in ordinary text and wait for the user; never call a Claude-specific question tool. Treat skill execution as reasoning, not permission to run commands or change external systems.

Load only the method reference selected by the routing decision. For examples use files under `references/docs/` through the same `skill_view` interface. Cross-domain routes are listed in the master catalog.

## Method loading index

- arc-design: `skill_view(name="s4h-writing", file_path="references/arc-design.md")`
- argument: `skill_view(name="s4h-writing", file_path="references/argument.md")`
- audience-calibration: `skill_view(name="s4h-writing", file_path="references/audience-calibration.md")`
- character-development: `skill_view(name="s4h-writing", file_path="references/character-development.md")`
- copy: `skill_view(name="s4h-writing", file_path="references/copy.md")`
- dialogue: `skill_view(name="s4h-writing", file_path="references/dialogue.md")`
- executive-summary: `skill_view(name="s4h-writing", file_path="references/executive-summary.md")`
- inconsistency-audit: `skill_view(name="s4h-writing", file_path="references/inconsistency-audit.md")`
- line-editing: `skill_view(name="s4h-writing", file_path="references/line-editing.md")`
- plot-structure: `skill_view(name="s4h-writing", file_path="references/plot-structure.md")`
- pov: `skill_view(name="s4h-writing", file_path="references/pov.md")`
- prose-elevation: `skill_view(name="s4h-writing", file_path="references/prose-elevation.md")`
- report: `skill_view(name="s4h-writing", file_path="references/report.md")`
- restructure: `skill_view(name="s4h-writing", file_path="references/restructure.md")`
- rhetoric: `skill_view(name="s4h-writing", file_path="references/rhetoric.md")`
- scene-construction: `skill_view(name="s4h-writing", file_path="references/scene-construction.md")`
- technical: `skill_view(name="s4h-writing", file_path="references/technical.md")`
- tone-alignment: `skill_view(name="s4h-writing", file_path="references/tone-alignment.md")`
- voice-consistency: `skill_view(name="s4h-writing", file_path="references/voice-consistency.md")`
- worldbuilding: `skill_view(name="s4h-writing", file_path="references/worldbuilding.md")`


# Writing

Every writing problem has a name. Name it precisely, and the fix becomes obvious. The most common mistake is treating a structural problem as a prose problem, or a character problem as a plot problem — applying the wrong tool while the real issue goes unaddressed.

This routing skill reads your situation, identifies the problem type, and connects you to the right technique immediately.

---

## Your Process

### Step 1: Read the Situation

If the user hasn't described their writing challenge yet, ask:

> What's the writing problem? Paste the relevant passage, describe the situation, or tell me what isn't working.

Wait for their response before diagnosing.

---

### Step 2: Diagnose the Problem Type

**Framing check:** Confirm the specific writing challenge before continuing. State what you've identified — the content being worked on and its core problem type — in one sentence, then use a plain-text question with the options below, then wait for the user’s answer:
- **Question:** "I'm reading this as: [your one-sentence framing of the specific writing challenge, content type, and what isn't working]. Is that right?"
- **Header:** "Framing"
- **Options:**
  - **Yes — proceed** — framing is correct
  - **Adjust** — one element is off; user will correct it before you continue
  - **Reframe** — different situation than read; incorporate the correction before proceeding

Read the situation and classify it against these problem clusters:

**Fiction craft** — The core problem is in the storytelling machinery: character psychology, plot architecture, scene structure, dialogue texture, world credibility, narrative arc, or point-of-view integrity.
→ Route to: `skill_view(name="s4h-writing", file_path="references/character-development.md")`, `skill_view(name="s4h-writing", file_path="references/plot-structure.md")`, `skill_view(name="s4h-writing", file_path="references/scene-construction.md")`, `skill_view(name="s4h-writing", file_path="references/dialogue.md")`, `skill_view(name="s4h-writing", file_path="references/worldbuilding.md")`, `skill_view(name="s4h-writing", file_path="references/arc-design.md")`, `skill_view(name="s4h-writing", file_path="references/pov.md")`

**Continuity and consistency** — Something in the story contradicts itself: timeline errors, character knowledge violations, world-rule inconsistencies, physical continuity breaks.
→ Route to: `skill_view(name="s4h-writing", file_path="references/inconsistency-audit.md")`

**Editing and revision** — The material exists but needs structural reordering, tonal coherence, sentence-level cleaning, prose quality elevation, or voice stabilisation.
→ Route to: `skill_view(name="s4h-writing", file_path="references/restructure.md")`, `skill_view(name="s4h-writing", file_path="references/tone-alignment.md")`, `skill_view(name="s4h-writing", file_path="references/line-editing.md")`, `skill_view(name="s4h-writing", file_path="references/prose-elevation.md")`, `skill_view(name="s4h-writing", file_path="references/voice-consistency.md")`

**Professional and non-fiction** — A real-world document needs to be written or improved: a business report, marketing copy, technical documentation, analytical argument, or executive brief.
→ Route to: `skill_view(name="s4h-writing", file_path="references/report.md")`, `skill_view(name="s4h-writing", file_path="references/copy.md")`, `skill_view(name="s4h-writing", file_path="references/technical.md")`, `skill_view(name="s4h-writing", file_path="references/argument.md")`, `skill_view(name="s4h-writing", file_path="references/executive-summary.md")`

**Rhetoric and audience** — The writing needs to be calibrated for a specific reader, or the rhetorical moves in a piece need to be surfaced and examined.
→ Route to: `skill_view(name="s4h-writing", file_path="references/audience-calibration.md")`, `skill_view(name="s4h-writing", file_path="references/rhetoric.md")`

---

### Step 3: Identify 3–4 Best-Fit Skills

**Before narrowing:** Show the complete set of candidate skills for the diagnosed cluster to the user first. Use a plain-text question with the options below, then wait for the user’s answer:
- **Question:** "I've identified [N] skills in the [cluster name] cluster. Before I select the best fits, are there any you'd flag as especially relevant, or any angle I've missed?"
- **Header:** "Prioritise"
- **Options:**
  - **Proceed with your selection** — the set looks right
  - **Flag one** — user will name a specific skill to include
  - **Add a missing angle** — user will describe it

Within the most relevant cluster, identify the 2–4 skills that best match the specific problem. Use the routing guide below.

Prioritize skills that match the **type of output** the user needs:
- They need a diagnosis → audit skills (`skill_view(name="s4h-writing", file_path="references/inconsistency-audit.md")`, `skill_view(name="s4h-writing", file_path="references/pov.md")`, `skill_view(name="s4h-writing", file_path="references/scene-construction.md")`)
- They need a rebuild → design skills (`skill_view(name="s4h-writing", file_path="references/plot-structure.md")`, `skill_view(name="s4h-writing", file_path="references/arc-design.md")`, `skill_view(name="s4h-writing", file_path="references/character-development.md")`)
- They need a revision → editing skills (`skill_view(name="s4h-writing", file_path="references/restructure.md")`, `skill_view(name="s4h-writing", file_path="references/line-editing.md")`, `skill_view(name="s4h-writing", file_path="references/tone-alignment.md")`)
- They need a produced piece → production skills (`skill_view(name="s4h-writing", file_path="references/report.md")`, `skill_view(name="s4h-writing", file_path="references/executive-summary.md")`, `skill_view(name="s4h-writing", file_path="references/copy.md")`)
- They need a rhetorical read → analysis skills (`skill_view(name="s4h-writing", file_path="references/rhetoric.md")`, `skill_view(name="s4h-writing", file_path="references/argument.md")`)

---

### Step 4: Present Options

Use the a plain-text question with the options below, then wait for the user’s answer tool to present your diagnosis. Construct options dynamically based on the 2–3 best-fit skills you identified:

- **Question:** "Here's what I think you need. Which fits your situation best?"
- **Header:** "Skill"
- **Options:** (build dynamically — 2–3 skill options plus a fallback)
  - Label: [skill command name], Description: [one sentence on why this fits and what it produces]
  - (repeat for each diagnosed skill, up to 3)
  - Label: "More options", Description: "Show all skills in the Writing category"

Proceed based on their selection.

---

### Step 5: Execute

When the user picks an option:
- **A selected skill:** Run it immediately. Do not ask them to type another command. Use the context already gathered as the input.
- **More options:** Show the full skill table for the Writing category. Let them pick from the complete list, then execute.

---

## Routing Guide

| Situation | Top skills to offer |
|---|---|
| "My character feels flat / doesn't feel real" | `skill_view(name="s4h-writing", file_path="references/character-development.md")` |
| "The story isn't working / the plot sags" | `skill_view(name="s4h-writing", file_path="references/plot-structure.md")`, `skill_view(name="s4h-writing", file_path="references/arc-design.md")` |
| "This scene isn't working / feels flat" | `skill_view(name="s4h-writing", file_path="references/scene-construction.md")`, `skill_view(name="s4h-writing", file_path="references/dialogue.md")` |
| "The dialogue sounds wrong / on the nose" | `skill_view(name="s4h-writing", file_path="references/dialogue.md")`, `skill_view(name="s4h-writing", file_path="references/character-development.md")` |
| "The world feels thin / like a backdrop" | `skill_view(name="s4h-writing", file_path="references/worldbuilding.md")` |
| "The arc feels unearned / the ending doesn't land" | `skill_view(name="s4h-writing", file_path="references/arc-design.md")`, `skill_view(name="s4h-writing", file_path="references/plot-structure.md")` |
| "POV problems / head-hopping / narration inconsistent" | `skill_view(name="s4h-writing", file_path="references/pov.md")`, `skill_view(name="s4h-writing", file_path="references/inconsistency-audit.md")` |
| "Contradictions / continuity errors" | `skill_view(name="s4h-writing", file_path="references/inconsistency-audit.md")` |
| "The piece is in the wrong order / buries the lede" | `skill_view(name="s4h-writing", file_path="references/restructure.md")`, `skill_view(name="s4h-writing", file_path="references/executive-summary.md")` |
| "The tone keeps shifting / voice drift" | `skill_view(name="s4h-writing", file_path="references/tone-alignment.md")`, `skill_view(name="s4h-writing", file_path="references/voice-consistency.md")` |
| "The sentences are clunky / wordy / passive" | `skill_view(name="s4h-writing", file_path="references/line-editing.md")` |
| "The prose is flat / competent but not compelling" | `skill_view(name="s4h-writing", file_path="references/prose-elevation.md")` |
| "Different contributors / brand voice inconsistent" | `skill_view(name="s4h-writing", file_path="references/voice-consistency.md")` |
| "Write or fix a report / briefing document" | `skill_view(name="s4h-writing", file_path="references/report.md")`, `skill_view(name="s4h-writing", file_path="references/executive-summary.md")` |
| "Marketing copy / landing page / ad copy" | `skill_view(name="s4h-writing", file_path="references/copy.md")`, `skill_view(name="s4h-writing", file_path="references/audience-calibration.md")` |
| "Technical documentation / API docs / user guide" | `skill_view(name="s4h-writing", file_path="references/technical.md")`, `skill_view(name="s4h-writing", file_path="references/audience-calibration.md")` |
| "Build an argument / op-ed / make the case" | `skill_view(name="s4h-writing", file_path="references/argument.md")`, `skill_view(name="s4h-writing", file_path="references/rhetoric.md")` |
| "Executive summary / 1-page brief for leadership" | `skill_view(name="s4h-writing", file_path="references/executive-summary.md")`, `skill_view(name="s4h-writing", file_path="references/report.md")` |
| "Write for a specific audience / calibrate" | `skill_view(name="s4h-writing", file_path="references/audience-calibration.md")` |
| "Rhetorical analysis / what is this piece doing" | `skill_view(name="s4h-writing", file_path="references/rhetoric.md")`, `skill_view(name="s4h-writing", file_path="references/argument.md")` |

---

## Notes

- **Don't confuse problem types.** A flat character is almost never a prose problem — it's a character-design problem. Line-editing flat prose won't fix it. Diagnose the layer first.
- **Structure before style.** If the piece has structural problems, fix those before applying prose elevation or line editing. Rewriting sentences in the wrong order is wasted work.
- **The context gathered in Step 1 is the input.** When the user selects a skill, run it on that context — they shouldn't have to re-explain the situation.
- **If the situation spans multiple problem types** (e.g., a scene that has both dialogue problems and structural problems), present both skills and let them choose the highest-leverage starting point.
