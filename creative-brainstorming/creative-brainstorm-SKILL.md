---
name: creative-brainstorm
description: Maximizes creative divergence when generating multiple options. Use for any request requiring creative ideation with multiple outputs—titles, taglines, analogies, names, concepts, prompts, descriptions, or ideas of any kind. Employs verbalized sampling, anti-priming, and other techniques to avoid mode collapse and explore low-probability, high-creativity responses.
---

# Creative Brainstorm

Generate maximally creative, diverse options by avoiding mode collapse and sampling from the tails of the probability distribution.

## Core Workflow

For every creative brainstorming request:

### 1. Anti-Priming (always)

Before generating, list 3-5 clichés or obvious approaches to avoid for this specific request. Mark them forbidden. This inoculates against high-probability "safe" responses.

### 2. Select Techniques

Based on task type:

| Task | Techniques | Load references? |
|------|------------|------------------|
| Titles, headlines, taglines, slogans, mottos, names | Combinatorial + Constraint Injection + Tension Pairing | Yes: literary-devices.md |
| Analogies, metaphors | Domain Bridging + Obvious→Opposite→Orthogonal | Yes: techniques.md |
| Concepts, ideas, strategic options | Obvious→Opposite→Orthogonal + Persona Shifting | Yes: techniques.md |
| Writing prompts, descriptions | Domain Bridging + Persona Shifting | Yes: techniques.md |

User may override with explicit technique requests.

### 3. Generate with Verbalized Sampling

Wrap generation in this internal structure:

```
Generate <n_samples> responses, each exploring probability < 0.10.
n_samples = user's requested count, or 5 if unspecified.
```

Do NOT show probability scaffolding in output unless user explicitly requests it.

### 4. Output

Present clean, numbered options. No meta-commentary about techniques used unless asked.

---

## Technique Quick Reference

**Obvious → Opposite → Orthogonal**: Generate the natural response, invert its core assumption, then approach from an unrelated domain.

**Constraint Injection**: Add arbitrary constraints (length, content, structure, tone) to force unusual solutions.

**Persona Shifting**: Generate through different lenses—comedian, minimalist, poet, cynic, etc.

**Domain Bridging**: Require options inspired by unrelated fields (biology, architecture, music, mythology, cooking, etc.).

**Combinatorial**: Generate components (power words, structures, metaphors) separately, then combine systematically.

**Tension Pairing**: Combine devices that create productive friction (compression + surprise, familiarity + defamiliarization).

For detailed breakdowns, see [references/techniques.md](references/techniques.md).

---

## For Titles, Taglines, and Short-Form Copy

Load [references/literary-devices.md](references/literary-devices.md) for the full device catalog.

**Heuristic**: One sound device + one structural device + one meaning device. More collapses under its own cleverness.

**High-value devices**:
- Sound: alliteration, assonance, rhythm
- Structure: tricolon, chiasmus, parallelism, parataxis
- Meaning: metaphor, antithesis, paradox, zeugma
- Psychological: curiosity gap, defamiliarization, surprise

---

## Default Behavior

- **Aggressive creativity by default**: Always combine multiple techniques
- **Clean output**: No probability tags or technique names unless requested
- **Auto-select techniques**: Based on task type (user may override)
- **Default n_samples**: 5 options unless user specifies otherwise
