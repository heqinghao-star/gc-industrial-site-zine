---
name: gc-industrial-site-zine
description: Transform travel, architecture, city, landscape, and infrastructure photographs into deconstructivist industrial site-analysis zine posters with measured photo fragments, technical drawing relations, paper-print texture, and a source-derived accent color. Use for final poster generation, style analysis, or production-ready prompts; do not use for ordinary photo enhancement or generic scrapbook collages.
---

# Industrial Site Zine

Turn a photograph or visual brief into a restrained 4:3 field-study poster where the subject is dismantled into meaningful components and reassembled through industrial drawing logic.

Unless the user explicitly asks for analysis or prompt-only output, return both the generated raster image and the final generation prompt.

## Route the request

- **Generate — default:** photograph, place, object, or theme → structural reading → source-aware palette → poster → inspection.
- **Photo edit:** preserve the supplied subject while changing crop, reproduction, fragmentation, and analytical drawing treatment.
- **Analyze + generate:** learn a visual system from supplied references, separate reusable rules from sample residue, then make a new poster.
- **Reference analysis:** analyze and systematize references without generating unless requested.
- **Prompt-only:** use only when explicitly requested.

Read [references/style-system.md](references/style-system.md) for every mode. Read [references/prompt-compiler.md](references/prompt-compiler.md) before generation or prompt-only work. Read [references/reference-analysis.md](references/reference-analysis.md) when references are supplied for style learning. Read [references/quality-gate.md](references/quality-gate.md) before returning generated work.

## Image roles and preservation

Assign every supplied image one role before prompting:

- **Edit target:** its recognizable subject must appear in the result.
- **Style reference:** learn only visual grammar; do not copy subject, wording, interface, brand, exact fragments, accent shape, or composition.
- **Supporting insert:** preserve only the specified object or fragment inside a new composition.

Use high preservation for identity-sensitive people, products, artworks, pets, and characters. Use medium preservation for places, architecture, landscapes, and infrastructure unless the user asks to lock the exact view. For medium preservation, list the visible spatial relationships that must survive.

Always pass every relevant image into the image-generation call. When local paths are available, use them directly. Inspect each image before describing it.

## Core design decision

Do not treat this style as “photo plus technical annotations.” First infer a real system inside the subject, then deconstruct that system.

Examples of valid systems:

- port: gantry span, load path, crane joint, container module;
- architecture: facade mass, structural void, window module, water datum, reflection section;
- mountain: ridge mass, geological face, tree belt, trail cut;
- city: wheel axis, horizon datum, sun position, tower edge;
- street: circulation line, facade rhythm, threshold, elevation change.

Fragments, axes, dimensions, hatches, and labels must explain that chosen system. Remove any mark that has no analytical role.

## Generation workflow

1. Inspect source dimensions, ratio, subject, material colors, key geometry, spatial order, visible text, brands, and sensitive identity traits.
2. Record preservation invariants for every edit target.
3. Choose one structural thesis, such as “the port is a load-transfer machine” or “the reflection is a folded section.”
4. Choose a deconstruction grammar that fits the thesis: exploded fragments, folded section, interrupted elevation, displaced detail, sectional wedge, or radial mechanism.
5. Extract a palette from the target photograph. Select one accent because it relates to a material, light condition, or structural role. Never default to cobalt or inherit a reference accent automatically.
6. Compile the prompt using [references/prompt-compiler.md](references/prompt-compiler.md).
7. Generate a flat 4:3 paper poster using the actual input image.
8. Inspect against [references/quality-gate.md](references/quality-gate.md). Regenerate once if the image remains a colorful photograph with decorative overlays, copies a reference composition, loses the target subject, introduces unrequested language, or uses an unrelated accent.

## Non-negotiable boundaries

- Default canvas is landscape 4:3 unless the user requests another ratio.
- Use one coherent analytical event rather than unrelated collage pieces.
- Preserve generous paper field and asymmetric balance.
- Reduce photo fragments toward charcoal, graphite, sepia, chalk white, or subdued source neutrals.
- Keep one source-derived accent small and structural; do not spread it across the whole photograph.
- Keep labels sparse, concrete, and related to visible geometry.
- Default to concise English Latin-alphabet text. Use another language only when explicitly requested.
- Do not copy reference text, brands, watermarks, interface chrome, exact dates, exact locations, signatures, accent shapes, or exact layouts.
- Avoid tourism icons, map pins, passports, compass roses, airplanes, generic pictograms, tidy card grids, commercial headlines, glossy mockups, cinematic depth, 3D rendering, neon palettes, and dense scrapbook styling.

## Output

For generation, return:

- the generated image and saved path;
- the final prompt;
- the selected structural thesis and deconstruction grammar;
- image roles and preservation level;
- the chosen accent color and the source relationship that justified it;
- a short note about any regeneration or remaining limitation.
