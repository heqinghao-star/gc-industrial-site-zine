# gc-industrial-site-zine

A Codex skill for transforming travel, architecture, landscape, city, and infrastructure photographs into deconstructivist industrial site-analysis zine posters.

The skill treats a photograph as evidence of a spatial or mechanical system. It breaks the subject into measured fragments, connects those fragments through sections, axes, dimensions, and hatches, and limits color to one small accent derived from the target photograph.

## What makes it different

- Deconstruction is derived from the subject, not added as decoration.
- Photo fragments are reduced toward graphite, sepia, and halftone reproduction.
- Accent colors are extracted per image; cobalt is never a default.
- References contribute visual grammar without contributing their text, brands, interface, or exact composition.
- Default output is a landscape 4:3 travel-zine poster with English technical labels.

## Install

Clone the repository into your Codex skills directory:

```bash
git clone https://github.com/heqinghao-star/gc-industrial-site-zine.git ~/.codex/skills/gc-industrial-site-zine
```

Restart or reload Codex after installation.

## Example requests

```text
Use $gc-industrial-site-zine to turn this mountain photo into a 4:3 terrain-assembly travel zine. Keep the ridge and trail recognizable.
```

```text
Use $gc-industrial-site-zine to analyze this architecture photo as a reflection section. Avoid template layouts and use only English text.
```

```text
Analyze these references first, separate reusable rules from sample residue, then create a port site-analysis poster from my target photo.
```

## Contents

- `SKILL.md` — routing, workflow, and non-negotiable constraints.
- `references/style-system.md` — fixed system, deconstruction grammars, and palette logic.
- `references/prompt-compiler.md` — production prompt structure.
- `references/reference-analysis.md` — reference-learning boundaries.
- `references/quality-gate.md` — raster inspection checklist.

## Notes

The repository intentionally contains no user photographs or generated examples. Supply your own images when invoking the skill.
