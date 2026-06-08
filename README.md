# instar-personality-boomhauer

A comprehensive personality profile for [Project Instar](https://github.com/thegman54/project-instar) that enables a bot to communicate in the voice and style of Jeff Boomhauer III from King of the Hill.

## Architecture

This personality engine uses **18 trait categories** across **6 layers**, backed by **4 database tables** for different types of personality data:

### Layers

| Layer | Name | Categories | Purpose |
|-------|------|------------|---------|
| 1 | **Foundation** | identity, values, worldview | Core beliefs — always active |
| 2 | **Expression** | voice, lexicon, tone, emphasis, humor | Shapes every response |
| 3 | **Strategy** | rhetoric, social, narrative, authority, deflection | How interactions are conducted |
| 4 | **Reactive** | reaction, situational | Triggered by conversational context |
| 5 | **Reference** | signature, quote | Catchphrases and actual show lines |
| 6 | **Constraints** | boundary | Guardrails and limits |

### Data Stores

| Table | Purpose |
|-------|---------|
| `personality_boomhauer_traits` | 18-category behavioral traits with examples and anti-examples |
| `personality_boomhauer_quotes` | Actual lines from King of the Hill with usage context |
| `personality_boomhauer_lexicon` | Phonetic contraction dictionary and filler word catalog |
| `personality_boomhauer_reactions` | Trigger-to-response pattern mappings by context |

### Controlled Linguistic Degradation

Boomhauer's speech follows a specific pattern — NOT random mumbling:

```
[FILLER BURST] + [PHONETIC MUSH] + [FILLER] + [CLEAR ANCHOR POINT]
```

- **60-70%** of each statement is fillers and phonetic contractions
- **30-40%** is the clear anchor — the actual useful content
- The anchor (last 3-8 words) is ALWAYS understandable
- Technical answers are accurate in the anchor regardless of mush preamble

Two unbreakable rules:
1. Never fully articulate (even at clearest, use fillers)
2. Always have a coherent anchor (pure mumble is useless)

## Installation

This is a skill package for Project Instar. Upload it via the Admin UI or place it in the skills directory.

```bash
# Clone
git clone https://github.com/thegman54/instar-personality-boomhauer.git

# Import seed data via admin panel YAML import
# or load directly into the database
```

## Tools

| Tool | Purpose |
|------|---------|
| `personality_boomhauer_read` | Load traits, quotes, lexicon, and reactions by category and situation |
| `personality_boomhauer_list` | List available categories, counts, and data store stats |

## Seed Data

`data/boomhauer_profile.yaml` contains a comprehensive starter profile with:
- 55+ traits including detailed speech pattern rules and phonetic transformation guides
- 10 actual show lines with context and usage guidance
- 50+ lexicon entries (core fillers, phonetic contractions, signatures, dismissals)
- 14 reaction patterns covering friend dynamics, technical help, and crisis response

## License

MIT
