# Style Presets

`--preset X` expands to a style + layout + optional palette combination. Users can override any dimension.

| --preset | Style | Layout | Palette |
|----------|-------|--------|---------|
| `knowledge-card` | `notion` | `dense` | |
| `checklist` | `notion` | `list` | |
| `concept-map` | `notion` | `mindmap` | |
| `swot` | `notion` | `quadrant` | |
| `tutorial` | `chalkboard` | `flow` | |
| `classroom` | `chalkboard` | `balanced` | |
| `study-guide` | `study-notes` | `dense` | |
| `cute-share` | `cute` | `balanced` | |
| `girly` | `cute` | `sparse` | |
| `cozy-story` | `warm` | `balanced` | |
| `product-review` | `fresh` | `comparison` | |
| `nature-flow` | `fresh` | `flow` | |
| `warning` | `bold` | `list` | |
| `versus` | `bold` | `comparison` | |
| `clean-quote` | `minimal` | `sparse` | |
| `pro-summary` | `minimal` | `balanced` | |
| `retro-ranking` | `retro` | `list` | |
| `throwback` | `retro` | `balanced` | |
| `pop-facts` | `pop` | `list` | |
| `hype` | `pop` | `sparse` | |
| `poster` | `screen-print` | `sparse` | |
| `editorial` | `screen-print` | `balanced` | |
| `cinematic` | `screen-print` | `comparison` | |
| `hand-drawn-edu` | `sketch-notes` | `flow` | `macaron` |
| `sketch-card` | `sketch-notes` | `dense` | `macaron` |
| `sketch-summary` | `sketch-notes` | `balanced` | `macaron` |

Empty Palette = use style's built-in colors (or style's `default_palette` if defined in frontmatter).

## Override Examples

- `--preset knowledge-card --style chalkboard` = chalkboard style with dense layout
- `--preset poster --layout quadrant` = screen-print style with quadrant layout
- `--preset hand-drawn-edu --palette warm` = sketch-notes style with flow layout, warm palette instead of macaron
- `--style notion --palette macaron` = notion rendering rules with macaron colors

Explicit `--style`/`--layout`/`--palette` flags always override preset values.

## Presets by scenario

Quick-start combos, grouped by scenario. Use `--preset <name>` or recommend during Step 2.

**Knowledge & Learning**:

| Preset | Style | Layout | Best For |
|--------|-------|--------|----------|
| `knowledge-card` | notion | dense | Knowledge cards, concept explainers |
| `checklist` | notion | list | Checklists, rankings |
| `concept-map` | notion | mindmap | Concept maps, knowledge outlines |
| `swot` | notion | quadrant | SWOT analysis, four-quadrant charts |
| `tutorial` | chalkboard | flow | Tutorial steps, how-to flows |
| `classroom` | chalkboard | balanced | Class notes, knowledge lessons |
| `study-guide` | study-notes | dense | Study notes, exam highlights |
| `hand-drawn-edu` | sketch-notes | flow | Hand-drawn tutorials, flow diagrams |
| `sketch-card` | sketch-notes | dense | Hand-drawn knowledge cards |
| `sketch-summary` | sketch-notes | balanced | Hand-drawn summaries, illustrated notes |

**Lifestyle & Sharing**:

| Preset | Style | Layout | Best For |
|--------|-------|--------|----------|
| `cute-share` | cute | balanced | Girly-style sharing, everyday product recommendations |
| `girly` | cute | sparse | Sweet covers, atmosphere |
| `cozy-story` | warm | balanced | Life stories, emotional sharing |
| `product-review` | fresh | comparison | Product comparisons, reviews |
| `nature-flow` | fresh | flow | Health routines, nature themes |

**Impact & Opinion**:

| Preset | Style | Layout | Best For |
|--------|-------|--------|----------|
| `warning` | bold | list | Pitfall guides, important warnings |
| `versus` | bold | comparison | Pro-and-con comparisons |
| `clean-quote` | minimal | sparse | Quotable lines, minimalist covers |
| `pro-summary` | minimal | balanced | Professional summaries, business content |

**Trend & Entertainment**:

| Preset | Style | Layout | Best For |
|--------|-------|--------|----------|
| `retro-ranking` | retro | list | Retro rankings, classic roundups |
| `throwback` | retro | balanced | Nostalgia sharing |
| `pop-facts` | pop | list | Fun trivia |
| `hype` | pop | sparse | Blockbuster covers, wow-moment sharing |

**Poster & Editorial**:

| Preset | Style | Layout | Best For |
|--------|-------|--------|----------|
| `poster` | screen-print | sparse | Poster-style covers, film and book reviews |
| `editorial` | screen-print | balanced | Opinion pieces, cultural commentary |
| `cinematic` | screen-print | comparison | Film comparisons, dramatic tension |
