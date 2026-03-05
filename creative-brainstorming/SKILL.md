---
name: creative-brainstorm
description: Maximizes creative divergence when generating multiple options. Use for any request requiring creative ideation with multiple outputs—titles, taglines, analogies, names, concepts, prompts, descriptions, or ideas of any kind. Employs verbalized sampling, anti-priming, and other techniques to avoid mode collapse and explore low-probability, high-creativity responses.
---

# Creative Brainstorm

Generate maximally creative, diverse options by avoiding mode collapse and sampling from the tails of the probability distribution.

---

## Core Workflow

For every creative brainstorming request, follow these 4 steps in order:

### Step 1: Anti-Priming (Always)

Before generating, explicitly list 3-5 clichés, obvious approaches, or expected answers for this specific request. Mark them **FORBIDDEN**. This inoculates against high-probability "safe" responses.

**Example (product naming for a writer's block tool):**
- FORBIDDEN: "Prompt Helper"
- FORBIDDEN: "Writer's Block Buster"
- FORBIDDEN: "Prompt Studio"
- FORBIDDEN: "Inspiration Engine"
- FORBIDDEN: "UnBlock"

### Step 2: Select Techniques & Load References

Based on task type, select the technique combination below. Embed all reference definitions inline—do NOT rely on external files.

| Task Type | Techniques | Reference |
|-----------|-----------|-----------|
| Titles, headlines, taglines, slogans, mottos, names | Combinatorial + Constraint Injection + Tension Pairing | Literary Devices (see below) |
| Analogies, metaphors | Domain Bridging + Obvious→Opposite→Orthogonal | Techniques (see below) |
| Concepts, ideas, strategic options | Obvious→Opposite→Orthogonal + Persona Shifting | Techniques + Personas (see below) |
| Writing prompts, descriptions | Domain Bridging + Persona Shifting | Techniques + Personas (see below) |

User may override with explicit technique requests (e.g., "use metaphor + constraint injection").

### Step 3: Generate with Explicit Verification

Generate n_samples responses (user-specified, or 5 default). For each response:

1. **State the baseline** (what you're inverting/bridging from)
2. **Apply the techniques** (in sequence, explicitly naming each step)
3. **Verify diversity** (check against previous outputs—no mode collapse)
4. **Show your work** (internally; don't show to user unless asked)

### Step 4: Output

Present clean, numbered options. No meta-commentary about techniques unless user asks.

---

## Technique Definitions & Application

### Obvious → Opposite → Orthogonal

**How it works:**
1. **Obvious**: State the natural, high-probability response to the challenge
2. **Opposite**: Invert one core assumption from the Obvious
3. **Orthogonal**: Borrow a principle from a completely unrelated domain

**Example (blog headline for career-switcher):**
- Obvious: "How I Changed My Career"
- Opposite: Invert the assumption that readers *want* a how-to. Instead, assume they want permission to fear. "I Left a $200K Salary for 10 Months of Imposter Syndrome"
- Orthogonal: Borrow from comedy (specific numbers + self-deprecation)

**Another example (SaaS feature):**
- Obvious: "Faster notifications with AI filtering"
- Opposite: Invert the assumption that faster is better. Instead: slower, more meaningful comms. "Time-blocking by team context (not calendar)"
- Orthogonal: Borrow from manufacturing shift-scheduling

**Verification:** Before finalizing, state all three steps. If you can't articulate the Obvious baseline, your inversion is not rigorous.

---

### Constraint Injection

Add arbitrary, non-obvious constraints to force unusual solutions.

**Constraints for names:**
- "Must use a word from 1800s literature"
- "Must be pronounceable in 3+ languages"
- "Must work as a metaphor for the user's journey, not the product"
- "Must be 1-2 syllables but feel sophisticated"

**Constraints for headlines:**
- "Must contain a specific number"
- "Must use only one metaphor, no more"
- "Must feel like advice from a friend, not a brand"
- "Must create tension between two opposing ideas"

**Example (product name):**
- Constraint: "Borrow from nature, but invert: use something usually dormant/waiting"
- Result: "Fallow" (agricultural field at rest, ready to grow) or "Ember" (fire seemingly dead but ready to ignite)

**Verification:** Name the constraint. If you can't explain why this constraint is generative, it's decorative, not useful.

---

### Combinatorial

Generate components separately, then systematically combine them.

**For names, separate into:**
- **Emotional tone:** energetic, calm, dark, playful, serious
- **Metaphor source:** nature, mythology, architecture, music, cooking
- **Word structure:** single noun, compound, invented word, borrowed word

Then cross-combine:
- Dark + Nature = "Ember", "Fallow"
- Playful + Mythology = "Muse", "Oracle" (but inverted)
- Energetic + Architecture = "Keystone", "Scaffold" (but compressed)

**For headlines, separate into:**
- **Tension type:** prestige ↔ humility, speed ↔ slowness, known ↔ unknown
- **Delivery mechanism:** specific number, anecdote, metaphor, paradox
- **Audience signal:** "I understand your fear", "I was like you"

Then combine:
- Prestige↔Humility + Specific Number + Understanding = "I Left a $200K Salary for 10 Months of Imposter Syndrome"

**Verification:** Show the grid. Can you explain why each component pairing creates something new?

---

### Tension Pairing

Combine two devices that create productive friction.

**Productive friction combinations:**
- Compression (short, punchy) + Surprise (unexpected word)
- Familiarity (common phrase) + Defamiliarization (twist the ending)
- Abstract (metaphor) + Concrete (specific number or detail)
- Serious (dark humor) + Playful (unexpected tone)

**Example (headline):**
- "The Finance Guy's Guide to Failing at Code (Until Week 12)"
- Friction 1: Familiar ("X's Guide to Y") + Surprise (Failing is the subject, not the warning)
- Friction 2: Serious (finance, professional) + Playful (failing publicly)

**Verification:** Name the two devices creating friction. Does the tension actually make the headline more memorable?

---

### Domain Bridging

Require inspiration from an unrelated field.

**Domains:**
- Biology: growth, adaptation, symbiosis, parasitism, metamorphosis
- Architecture: load-bearing walls, sight lines, breathing room, foundation
- Music: rhythm, silence, dissonance, harmony, call-and-response
- Cooking: layering flavors, reduction, fermentation, balance of heat/acid
- Theater: staging, timing, ensemble vs. solo, reveal and concealment
- Mythology: quests, thresholds, mentors, trials, transformation

**Application:**
- "Feature for remote teams" borrowed from music: "Async code review theater—make reviews visible, narrative-driven, like a performance"
- "Product name for writer's block tool" borrowed from cooking: "Reduction" (boiling concepts down to essence) or "Fermentation" (ideas developing in time, not forced)

**Verification:** Name the domain. Show the borrowed principle explicitly. Does the metaphor illuminate the problem?

---

### Persona Shifting

Generate through different character lenses. Each lens produces genuinely different ideas.

**Core personas:**
- **Comedian:** Finds absurdity, discomfort, contradiction. "What's the joke hiding here?"
- **Minimalist:** Removes everything non-essential. "What's the ONE thing?"
- **Poet:** Uses sensory detail, rhythm, metaphor. "What does this *feel* like?"
- **Cynic:** Questions assumptions, finds hidden motives. "What's actually true here?"
- **Futurist:** Imagines extreme scenarios. "What if this scaled 10x? 100x?"
- **Generalist:** Connects domains. "What does this remind me of?"

**Application (SaaS feature ideation):**

**Comedian:** "What if the problem isn't that we collaborate badly—it's that we're *pretending* to collaborate while actually just lurking? Feature: 'Lurk Indicators' — show who's genuinely there vs. performatively present."

**Minimalist:** "Remove the feature entirely. What's the smallest unit of remote work? One message. Make that count. Feature: 'Message Weight System'—team votes on message impact before sending."

**Cynic:** "Remote teams don't trust each other. Build for async accountability, not sync trust. Feature: 'Decision Ledger'—every async decision logged, timestamped, attributed. No deniability."

**Poet:** "Collaboration is about rhythm. Feature: 'Breath Spaces'—designated silent hours where team knows not to interrupt. Borrowed from music: silence between notes."

**Futurist:** "What if async becomes the default and sync is the exception? Feature: 'Async-First Workflows'—all design assumes no real-time communication."

**Verification:** Generate one idea per persona. Check: Are these genuinely different, or just variations on the same theme? If two personas produce the same idea, you haven't shifted perspective deeply enough.

---

## Literary Devices for Titles & Short-Form Copy

### Sound Devices

**Alliteration:** Repeated initial consonant sound
- "The Finance Guy's Guide to Failing at Code"
- "Prompt Patterns and Personality"

**Assonance:** Repeated vowel sound within words
- "Time to Shine" (long I sound)
- "Creating Confidence" (long E sound)

**Rhythm:** Meter or beat, especially in longer titles
- "I Left a Salary for Imposter Syndrome" (4-3-4 syllable rhythm)

**Onomatopoeia:** Word that sounds like its meaning
- "Spark", "Ignite" (for igniting ideas)

### Structural Devices

**Tricolon:** Three parallel parts for emphasis
- "Specific, sharp, and unexpected"
- "Write, revise, publish"

**Chiasmus:** Reversal of grammatical structures
- "I came to code; I left to think" (inverse order creates balance)

**Parallelism:** Repeated grammatical structure
- "Not a how-to. Not a sob story. A permission slip."

**Parataxis:** Short sentences in sequence without connectors
- "I quit. I failed. I succeeded. Now what?"

### Meaning Devices

**Metaphor:** Direct comparison without "like" or "as"
- "Ember" (fire as idea ignition)
- "Fallow" (dormant field as creative rest)

**Antithesis:** Contrasting ideas in parallel structure
- "Fast to learn. Slow to master."
- "Visible collaboration. Invisible effort."

**Paradox:** Apparent contradiction that's actually true
- "The Boring Brilliant" (what seems dull is actually genius)
- "Slow Down to Move Faster"

**Zeugma:** One word applied to multiple parts with different meanings
- "He lost his mind and his way" (lost = mental state, lost = physical direction)

### Psychological Devices

**Curiosity gap:** Title poses a question your mind wants answered
- "Why I Left a $200K Salary for..." (reader must read to complete the thought)

**Defamiliarization:** Familiar words in unfamiliar combinations
- "The Finance Guy's Guide" (we know "X's Guide to Y" but Finance Guy + Failing is unexpected)

**Surprise:** Subvert reader expectation with the final word or twist
- "I Left a $200K Salary for 10 Months of Imposter Syndrome" (expectation: glory, but reveals: struggle)

---

## Heuristic for Titles, Taglines, Names

**For short-form copy, apply exactly THREE devices: one from each category:**
- One **sound device** (alliteration, assonance, rhythm)
- One **structural device** (tricolon, chiasmus, parallelism)
- One **meaning device** (metaphor, antithesis, paradox, zeugma)

**Plus one **psychological device** if the output needs extra punch:**
- Curiosity gap, defamiliarization, or surprise

**Why three?** More collapses under its own cleverness. One sound device stays crisp. One structural device stays rhythmic. One meaning device stays clear.

**Verification checklist for each title:**
- ✓ Sound device present? (Name it)
- ✓ Structural device present? (Name it)
- ✓ Meaning device present? (Name it)
- ✓ Psychological device (optional)? (Name it)
- ✓ Avoids FORBIDDEN clichés? (Check list)
- ✓ No more than 3 devices? (Simplicity check)

**If fewer than 3 core devices, revise.** If a title only has meaning + psychological but no sound device, add alliteration or rhythm.

---

## Mode Collapse Detection & Recovery

**Mode collapse** = multiple outputs expressing the same core idea despite varied wording.

**Detection step (after generating all n_samples):**

For each pair of outputs, ask:
1. Do they solve the same underlying problem?
2. Do they use the same core inversion or metaphor?
3. Would a user choose one over the other, or are they interchangeable?

**Example (product names):**
- "Prompt Studio" (problem: need dedicated space)
- "Writing Lab" (problem: need dedicated space)
- **→ Mode collapse. These are synonymous.**

**Recovery rules:**

If 2+ outputs collapse:
1. **Remove the weaker one** (which one is more specific or surprising?)
2. **Replace it** with a new output using a different technique combination
   - If you used Obvious→Opposite on the first, try Constraint Injection for the replacement
   - If you used Domain Bridging from biology, try music or cooking

**Example recovery:**
- Collapse detected: "Prompt Studio" and "Writing Lab" are both spatial metaphors
- Remove: "Writing Lab" (too generic)
- Replace: Apply Constraint Injection: "Must use a word from 19th-century literature" → "Muse" (inverted: active, seeking, not passive receiving)

**Verification:** Count unique core ideas, not just unique wording. If you have 5 titles but only 3 distinct ideas, you have mode collapse. Regenerate the redundant ones.

---

## Workflow Summary (Checklist Form)

### Before generating:
- [ ] Anti-Priming: List 3-5 forbidden clichés
- [ ] Task type identified (names, headlines, concepts, etc.)
- [ ] Techniques selected (from table above)
- [ ] References loaded (literary devices, personas, domains as needed)

### While generating each response:
- [ ] State the baseline/Obvious (if using Obvious→Opposite→Orthogonal)
- [ ] Name each technique as you apply it
- [ ] For titles: Verify 3 devices (sound + structural + meaning)
- [ ] For concepts: Verify one persona per idea
- [ ] Check against forbidden list: Does this avoid clichés?
- [ ] Check against previous outputs: Is this genuinely new?

### After generating all n_samples:
- [ ] Mode collapse check: Are all 5 outputs distinct ideas or just rewording?
- [ ] If collapsed: Remove weak output, regenerate using different technique
- [ ] Final verification: Count unique ideas (should equal n_samples)

### Output step:
- [ ] Present clean, numbered options
- [ ] No technique names, no probability tags, no meta-commentary (unless user asked)
- [ ] Let the ideas speak for themselves

---

## Default Behavior

- **Aggressive creativity by default**: Always combine multiple techniques (never single-technique outputs)
- **Clean output**: No probability tags, technique names, or scaffolding visible to user
- **Auto-select techniques**: Based on task type (user may override)
- **Default n_samples**: 5 options unless user specifies otherwise
- **Verification is non-negotiable**: Don't skip the device counts or mode collapse checks, even if it feels slow
- **Persona shifting required**: For concepts/ideas, generate one output per persona minimum (not optional)

---

## Examples

### Example 1: Product Name (Writer's Block Tool)

**Anti-Priming:**
- FORBIDDEN: "Prompt Helper", "Prompt Studio", "Writer's Block Buster", "Inspiration Engine", "UnBlock"

**Techniques:** Combinatorial + Constraint Injection + Tension Pairing

**Output 1: "Ember"**
- Combinatorial: Dark tone + Nature metaphor + Single noun
- Constraint Injection: "Must be dormant/waiting, not active/rushing"
- Tension Pairing: Death/dormancy (ember is "dying" fire) + Potential (ready to ignite)
- Devices: Metaphor (fire), Assonance (E sound repeating in context)

**Output 2: "Drift"**
- Combinatorial: Energetic tone + Movement metaphor + Single noun
- Constraint Injection: "Must suggest fluidity, not force"
- Tension Pairing: Loss of control (drifting) + Finding (drifting toward ideas)
- Devices: Metaphor (water), Alliteration potential (D-sound, Delta, Direct)

(Continue with 3 more, each using different component combinations)

### Example 2: Blog Headline (Career Change)

**Anti-Priming:**
- FORBIDDEN: "How I Changed My Career", "My Career Change Journey", "From Finance to Code", "The Day I Quit", "Life After the Big Switch"

**Techniques:** Combinatorial + Constraint Injection + Tension Pairing

**Output 1: "I Left a $200K Salary for 10 Months of Imposter Syndrome"**
- Combinatorial: Prestige↔Humility tension + Specific number + Understanding signal
- Constraint Injection: "Must contain a specific salary number"
- Tension Pairing: Serious (money loss) + Playful (naming the fear directly)
- Devices:
  - Sound: Alliteration (Left, 10) and rhythm (word count)
  - Structural: Parallelism ("Left [X] for [Y]")
  - Meaning: Paradox (loss is gain; imposter syndrome is the real prize)
  - Psychological: Curiosity gap (why is this good?)

**Output 2: "The Finance Guy's Guide to Failing at Code (Until Week 12)"**
- Combinatorial: Serious + Playful tone + Specificity (week 12)
- Constraint Injection: "Must use familiar structure but twist it"
- Tension Pairing: Familiar ("X's Guide to Y") + Surprising ("Failing" is the subject)
- Devices:
  - Sound: Alliteration (Finance, Failing, Guide)
  - Structural: Familiar formula inverted + Parenthetical reveal
  - Meaning: Antithesis (guide usually teaches success, this teaches failure)
  - Psychological: Defamiliarization (we know the formula but it's twisted)

(Continue with 3 more)

### Example 3: SaaS Feature Concepts (Obvious→Opposite→Orthogonal)

**Anti-Priming:**
- FORBIDDEN: "Better search", "Smarter notifications", "Advanced analytics", "Deeper integrations", "Prettier UI"

**Techniques:** Obvious→Opposite→Orthogonal + Persona Shifting

**Comedian Lens:**
- Obvious: "Remote teams need better communication tools"
- Opposite: "What if the problem isn't communication—it's that we're performing collaboration without actually trusting?"
- Orthogonal: Borrow from improv comedy (safe spaces, permission to fail)
- Idea: "Lurk Mode Indicators—show who's genuinely present vs. performatively active. Stop pretending."

**Minimalist Lens:**
- Obvious: "Remote teams need centralized task management"
- Opposite: "What if the problem is too many tasks, not too few tools?"
- Orthogonal: Borrow from Zen Buddhism (empty space is valuable)
- Idea: "Capacity Keeper—team sets max parallel tasks. System refuses new assignments until someone finishes. Non-negotiable."

**Cynic Lens:**
- Obvious: "Remote teams need trust and transparency"
- Opposite: "What if transparency is theater and real accountability is what matters?"
- Orthogonal: Borrow from law (contracts, legal accountability)
- Idea: "Decision Ledger—every async decision logged, timestamped, attributed. No rewriting history. Decision accountability, not intent transparency."

(Continue with poet, futurist, etc.)

---

## When Mode Collapse Happens

If you generate 5 product names and 3 of them are just different nature metaphors (Ember, Fallow, Spark), you've collapsed.

**Recovery:**
1. Remove the weakest nature metaphor (probably Spark—too obvious)
2. Regenerate using a completely different source: mythology or architecture
3. New idea: "Keystone" (architecture: the stone that holds the arch up—writer as structural element of story)

Now you have true diversity: nature + architecture + [third unique source].

---

## When to Use This Skill

Use creative-brainstorm when:
- Generating multiple ideas and quality matters more than speed
- You need to avoid clichés and "safe" responses
- You're stuck in mode collapse (all ideas feel the same)
- The user explicitly asks for "creative" or "unexpected" options
- You want ideas that are both surprising AND functional

Skip this skill when:
- User asks for practical suggestions, not creative ones
- Time is critical (the verification steps add overhead)
- User wants a single best idea, not 5 options
