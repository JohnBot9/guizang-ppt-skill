<p align="center">
  <img src="https://img.shields.io/github/stars/JohnBot9/guizang-ppt-skill?style=flat-square" alt="stars">
  <img src="https://img.shields.io/github/license/JohnBot9/guizang-ppt-skill?style=flat-square" alt="license">
  <img src="https://img.shields.io/badge/Skill-Agent-111111?style=flat-square" alt="skill">
  <img src="https://img.shields.io/badge/HTML-Deck-0A7CFF?style=flat-square" alt="html">
  <img src="https://img.shields.io/badge/Codex-Supported-222222?style=flat-square" alt="codex">
</p>

# Guizang PPT Skill

> Forked from [op7418/guizang-ppt-skill](https://github.com/op7418/guizang-ppt-skill) / 14k+ stars

An AI agent skill for Codex & Claude Code that generates single-file HTML horizontal-swipe decks, deck visuals, and social covers.

Fork maintained by [JohnBot9](https://github.com/JohnBot9). Original by [Guizang](https://x.com/op7418).

## Quick Start

`ash
npx skills add https://github.com/JohnBot9/guizang-ppt-skill --skill guizang-ppt-skill
`

Tell your AI agent:

`
Install guizang-ppt-skill. Clone https://github.com/JohnBot9/guizang-ppt-skill into ~/.claude/skills/guizang-ppt-skill, verify SKILL.md, assets/, references/ exist.
`

Then use it:

`
Create a Swiss-style deck from this article, ~7 slides, 2-3 generated visuals.
Turn this Markdown into a magazine-style presentation.
Generate a 21:9 cover image from this deck core idea.
`

## Two Visual Systems

**Style A: Editorial Magazine x Electronic Ink**
Monocle-like layouts with code textures. Best for narratives, opinions, salons, personal voice.

**Style B: Swiss International Typographic Style**
Grid-first, single anchor color, sharp rectangles, hairline rules, extreme type contrast. Best for facts, products, analysis, frameworks.

![Style A preview](https://github.com/user-attachments/assets/5dc316a2-401c-4e37-9123-ea081b6ae470)
![Style B preview](https://github.com/user-attachments/assets/8960e78c-69bb-4b7e-aa95-6fad64b70314)

## Features

- Two visual systems: editorial storytelling (Style A) + factual Swiss structure (Style B)
- Horizontal swipe: arrows / scroll wheel / touch / dots / ESC index
- Style A: 10 layouts (cover, divider, big numbers, image/text, grid, pipeline, comparison)
- Style B: 22 locked layouts (Cover, Statement, KPI Tower, Loop Diagram, Duo Compare, Image Hero, Closing Manifesto)
- 9 curated theme presets (5 electronic-ink + 4 Swiss anchor-color)
- Optional image generation via GPT-Image 2.0 / GPT-M 2.0
- Social covers: 21:9, 1:1, 3:4, video thumbnails
- Press B for low-power static mode
- Single HTML file, no build, no server

## Directory

`
guizang-ppt-skill/
  SKILL.md                     Main skill file
  README.md                    This file
  README.en.md                 English README (from upstream)
  CONTRIBUTING.md              Contribution guide
  LICENSE                      AGPL-3.0
  assets/
    template.html              Style A editorial template
    template-swiss.html        Style B Swiss template
    motion.min.js              Motion library
    screenshot-backgrounds/    Bundled WebP backgrounds (5+4)
  scripts/
    validate-swiss-deck.mjs    Swiss layout validator
  references/
    checklist.md               Quality checklist (P0-P3)
    components.md              Component catalog
    layouts.md                 Style A 10 layout skeletons
    layouts-swiss.md           Style B 22 locked layouts
    swiss-layout-lock.md       Swiss fidelity hard rules
    themes.md                  Style A 5 theme presets
    themes-swiss.md            Style B 4 anchor-color themes
    image-prompts.md           Image generation guide
    screenshot-framing.md      Screenshot styling semantics
    swiss-map-component.md     Swiss map component
  .github/
    ISSUE_TEMPLATE/            Issue templates
    pull_request_template.md
`

## Theme Presets

Pick from references/themes.md. Custom hex values are NOT allowed.

### Style A (Electronic Ink)

| Theme | Colors | Best For |
|-------|--------|----------|
| Ink Classic | #0a0a0b / #f1efea | General, commercial launches |
| Indigo Porcelain | #0a1f3d / #f1f3f5 | Tech, research, AI |
| Forest Ink | #1a2e1f / #f5f1e8 | Nature, sustainability, non-fiction |
| Kraft Paper | #2a1e13 / #eedfc7 | Nostalgic, humanist, indie |
| Dune | #1f1a14 / #f0e6d2 | Art, design, gallery |

### Style B (Swiss)

| Theme | Anchor Color | Best For |
|-------|-------------|----------|
| International Klein Blue | #002FA7 | Default, commercial, AI products |
| Lemon Yellow | #FFD500 | Youth, sports, retail |
| Lemon Green | #C5E803 | Ecology, sustainability, Gen Z |
| Safety Orange | #FF6B35 | Alerts, news, industrial |

Default for Swiss: International Klein Blue.

## Design Principles

1. Restraint over flash - WebGL only bleeds on hero pages
2. Structure over decoration - hierarchy via type scale + grid, not shadows
3. Images are first-class - align to body, stable ratios, crop from bottom only
4. Generated visuals are assets - no titles/footers inside images
5. Rhythm on hero pages - hero/non-hero alternation
6. Dynamic effects must be optional - B toggles static mode
7. Consistent terminology - Skills is Skills
8. Swiss layouts stay locked - reuse the 22-page system

## Contributing

Bugs, layouts, new ideas welcome! Priorities:

- Add classes to template.html first, do not let layouts.md reference undefined classes
- When changing template-swiss.html, update layouts-swiss.md and swiss-layout-lock.md together
- New Swiss rules update validate-swiss-deck.mjs
- Log pitfalls in checklist.md at P0/P1/P2/P3 tiers
- New themes go in themes.md with a use case

## License

AGPL-3.0 (c) 2026 [op7418](https://github.com/op7418). Fork maintained by [JohnBot9](https://github.com/JohnBot9).