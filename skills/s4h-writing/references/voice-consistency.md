# s4h-writing-voice-consistency

Loaded through `skill_view(name="s4h-writing", file_path="references/voice-consistency.md")`. Apply the complete procedure below to the current task.


# Writing: Voice Consistency

Voice is the sum of choices: sentence length preference, vocabulary range, degree of formality, stance toward the reader, use of metaphor and analogy, tolerance for digression, the character that comes through even in functional writing. It is recognisable even when you can't name what you're recognising. When it's absent or fractured, the reader feels it as a nagging sense that the writing has no centre — that no one is actually speaking to them.

The critical insight: voice can be *extracted* and *characterised* from strong existing passages, and that characterisation becomes an auditable standard. This means voice consistency is not a mysterious quality that can only be felt — it is a set of identifiable, describable choices that can be held constant across contributors, sections, and time.

For brand and organisational writing, this extracted voice fingerprint becomes the foundation of a practical style brief — not a list of rules about comma usage, but a description of who is speaking and how they sound, with examples that any contributor can use as a reference.

---

## Your Process

**Step 1: Extract Defining Characteristics**
From the strongest existing passages — the sections that feel most alive, most like the brand or the writer's best work — identify 5–7 defining characteristics. These should be specific enough to be testable. Not "clear and friendly" but:

**Framing check:** Confirm the specific voice and document before continuing. State what you've identified — the actual text being analyzed, whether this is a single-author or multi-author document, and the primary goal (audit, repair, or guide creation) — in one sentence, then use a plain-text question with the options below, then wait for the user’s answer:
- **Question:** "I'm reading this as: [your one-sentence framing of the document, its authorship context, and the goal]. Is that right?"
- **Header:** "Framing"
- **Options:**
  - **Yes — proceed** — framing is correct
  - **Adjust** — one element is off; user will correct it before you continue
  - **Reframe** — different situation than read; incorporate the correction before proceeding
- Sentence length: typically 12–20 words; occasional short declaratives for emphasis (under 8 words)
- Vocabulary: specific and concrete; avoids jargon; uses domain terms but never without context
- Formality: conversational but not casual; writes to a peer, not down to a student
- Stance: confident, never hedging; does not over-qualify claims
- Metaphor: uses one extended metaphor per piece; ground-level comparisons not elevated ones
- Rhythm: often ends sections with a short sentence that lands a point
- Attitude to reader: assumes reader is intelligent and pressed for time; doesn't repeat

**Before narrowing:** Show the complete generated set of characteristics to the user first. Use a plain-text question with the options below, then wait for the user’s answer:
- **Question:** "I've identified [N] voice characteristics. Before I select the 5–7 most defining ones, are there any you'd flag as especially important, or any I've missed?"
- **Header:** "Prioritise"
- **Options:**
  - **Proceed with your selection** — the set looks right
  - **Flag one** — user will name a specific characteristic to include
  - **Add a missing one** — user will describe a characteristic not yet captured

**Step 2: Create a Voice Fingerprint**
Write a representative passage (or select the strongest existing one) that exemplifies all 5–7 characteristics simultaneously. This is the voice fingerprint — the reference point that any subsequent section can be held against. It should feel unmistakably like the voice.

**Step 3: Scan for Departures**
Read through the full document and flag sections that depart from the fingerprint. For each departure:
- Quote the passage
- Identify which characteristic(s) it violates
- Describe the direction of departure (toward formal / toward casual / toward hedging / toward corporate / etc.)

**Step 4: Build a Voice Guide (for brand/multi-author use)**
For documents that will have multiple contributors or ongoing updates, translate the fingerprint into a brief, practical guide:
- The voice in one paragraph (descriptive, not prescriptive)
- 5–7 DO / DON'T pairs with examples
- The representative fingerprint passage as the reference sample
- The 3 most common departures to watch for, with before/after examples

---

## Human Check-in

Before proceeding, use the a plain-text question with the options below, then wait for the user’s answer tool. State your interpretation of the situation in 1–2 sentences — what is being analyzed and what the core question is — then ask:

- **Question:** "My read: [your 1–2 sentence interpretation]. How do you want to proceed?"
- **Header:** "Scope"
- **Options:**
  - **Full analysis** — Complete all steps, reasoning shown throughout
  - **Key findings only** — Bottom-line output, skip step-by-step detail
  - **Specific focus** — Zoom in on one aspect of this analysis
  - **Reframe** — The read is off; correct it and the analysis will follow the corrected framing

Proceed based on their selection. If the user reframes, incorporate the correction before running any analysis.

---

## Output Format

### Voice Analysis

**Fingerprint (5–7 Characteristics):**
1. [Characteristic: specific and testable]
2. [And so on]

**Representative Sample Passage:** [The passage that exemplifies all characteristics — quoted from existing text or composed if no strong existing passage exists]

**Departures:**
- [Location] — [Quoted passage] — Characteristic(s) violated: [list] — Direction of departure: [description]
- [Repeat]
- NONE FOUND if clean

**Voice Guide (for brand/multi-author use):**
- [Voice in one paragraph]
- [DO/DON'T pairs with examples]
- [Most common departures to watch for]

---

## Notes

- The voice fingerprint works only if it is extracted from the best existing work, not invented. A voice brief built from aspirational writing that doesn't match the actual document will not solve the consistency problem — it will create a new one.
- For single-author documents, voice departures are usually caused by energy, time, or tone shifts. For multi-author documents, they're usually caused by each contributor's natural voice overriding the house voice.
- Pairs with `skill_view(name="s4h-writing", file_path="references/tone-alignment.md")` — tone is one dimension of voice. Voice consistency addresses the full identity of the speaker; tone alignment addresses one specific dimension (register).
- Pairs with `skill_view(name="s4h-writing", file_path="references/audience-calibration.md")` — voice must be calibrated to the audience; a perfectly consistent voice that is calibrated to the wrong reader is still failing.
- Pairs with `skill_view(name="s4h-writing", file_path="references/prose-elevation.md")` — elevation must stay in voice; an elevated passage that sounds like a different writer has traded one problem for another.

---

## What's Next

After delivering this output, use a plain-text question with the options below, then wait for the user’s answer to offer the next move:

- **Question:** "Voice consistency checked. What's next?"
- **Header:** "Next"
- **Options:**
  - `skill_view(name="s4h-writing", file_path="references/line-editing.md")` — Edit for consistent voice throughout
  - `skill_view(name="s4h-writing", file_path="references/tone-alignment.md")` — Align tone with the voice
  - `skill_view(name="s4h-writing", file_path="references/prose-elevation.md")` — Elevate the consistent voice
  - **Done** — Wrap up and synthesise what we have so far
