# Mork visual and writing guide

Use this small identity guide for the homepage, project generator, and documentation. The homepage is
the visual reference. Keep its warm colors, serif display headings, and simple line illustrations;
adapt the density and background to each task.

## Name and logo

Write **Mork** in prose and product names: **Mork project generator**, **Mork documentation**.
Use **MORK** only for the wordmark. Preserve the existing logo's proportions and colors; use the white
variant on dark backgrounds. Leave at least one quarter of the logo's width clear around it. Do not
add shadows, redraw the mark, or use an unrelated icon as the product logo.

The homepage assets are `assets/logo.svg`; documentation uses `docs/assets/logo.svg` and
`docs/assets/logo_white.svg`. Keep the favicon recognizable at small sizes.

## Color roles

| Role | Color | Application |
| --- | --- | --- |
| Paper | `#f4eddf` | Homepage background; optional generator shell |
| Surface | `#ffffff` | Documentation, forms, screenshots |
| Panel | `#eaddc6` | Supporting illustrations and grouped content |
| Ink | `#392c24` | Main text, dark navigation, button hover |
| Muted | `#675548` | Secondary text on light backgrounds |
| Accent | `#9c3e28` | Primary action, links, short labels |
| On accent | `#fff8ed` | Text on accent and ink backgrounds |
| Divider | `#cfc0aa` | Decorative separators; not text or input boundaries |
| Success | `#276443` | Completed operation, accompanied by a label or icon |
| Warning | `#805600` | Recoverable issue, accompanied by explanatory text |
| Error | `#a52a2a` | Invalid input or failed operation, accompanied by text |

Use a muted-color border for form inputs so their boundaries remain visible. Reserve green for success;
the generator's primary action uses the same terracotta accent as the homepage. Do not recolor data series
or documentation admonitions simply to match the brand.

Dark documentation uses background `#241f1c`, paper-colored text, divider-colored secondary text, and
light terracotta links `#f0aa8d`. Keep the dark header and check code blocks, search, and navigation in
both themes. Do not apply the light theme's dark link color to dark surfaces.

## Typography and layout

- Display headings and wordmark: `Georgia, "Times New Roman", serif`, regular weight except the wordmark.
- Body, navigation, forms, and dense documentation headings: `Arial, Helvetica, sans-serif`.
- Code and short technical labels: `ui-monospace, SFMono-Regular, Consolas, monospace`.
- No downloaded fonts are required. Body copy starts at 16px with roughly 1.6 line height.
- Keep long prose near 60–75 characters per line. Use a spacing scale of 4, 8, 12, 16, 24, 32, and 48px;
  larger section spacing is appropriate on the homepage.
- Use thin borders and square or subtly rounded controls. The rotated illustration belongs to the
  homepage; do not rotate forms, screenshots, or documentation panels.
- Balance short headings and use pretty wrapping for paragraphs as progressive enhancements. Ordinary
  wrapping must remain usable. Keep manual line breaks only where intentional, such as the main slogan.
- Resolve isolated last words by shortening copy or adjusting available width before reducing font size.
  Do not apply `white-space: nowrap` to whole paragraphs or headings.

## Controls and navigation

Primary buttons use accent fill and on-accent text; secondary buttons use an accent border. Use verb-led
labels such as **Generate a project**. Keep focus visible, labels attached to inputs, and errors beside
the field they explain. Aim for 44px control height. A disabled or busy button must explain its state.

Use the same destinations and names across sites: **Home**, **Documentation**, **Generator**, **GitHub**.
Link to `https://www.mork-optimization.com/`, `https://docs.mork-optimization.com/`,
`https://generator.mork-optimization.com/`, and `https://github.com/mork-optimization/mork`.
The active destination can be omitted or marked with `aria-current="page"`. Keep visible text beside
navigation icons. Use simple 18–24px line icons with a consistent stroke; retain recognizable service logos.

## Application examples

| Surface | Application |
| --- | --- |
| Homepage | Cream background, serif headlines, terracotta actions, spacious sections, real screenshots |
| Generator | Same logo, navigation, and primary action; compact serif title; white form surface; sans-serif labels; monospace logs |
| Documentation | White reading surface, ink-colored header, terracotta links, serif page title, sans-serif section headings; retain Material navigation and theme switching |

The generator should read **Generate a project**, followed by a short instruction to enter a name and
choose a version. Explain the actual accepted name format beside the field. Label output **Generation
log**, show completion or failure in text, and preserve the generator's validation and download behavior.

## Writing and screenshots

Keep **Hard problems. Easier to solve.** as the main slogan. Elsewhere, name the action or capability:
**Compare against reference results**, **Export results and solutions**, **Inspect experiment results**.
Prefer short sentences and specific verbs. Explain what a feature does before implementation details.
Avoid repeated abstract promises about ideas, evidence, progress, or “the rest.”

Label diagrams by purpose: **How AutoLLM works**. Caption screenshots with their problem and experiment,
for example **Berlin52 results: five algorithms, ten runs each.** A static screenshot can show a real run;
do not describe it as “not a live run.” Document provenance and reproduction commands in the README.
Keep chart interpretation and retention details in the tutorial rather than the homepage caption.

## Maintenance and review

`web/styles.css` contains the homepage tokens. `docs/assets/stylesheets/brand.css` maps the same values
to Material's theme variables. Keep these small adapters aligned with this guide when changing the palette.
The generator uses its own `css/styles.css` with matching tokens. Each site serves its own styles without fetching CSS from another Mork deployment.

Review at 1440, 1024, 768, 390, and 320px widths, including intermediate layouts. Check headings and final
paragraph lines visually, horizontal overflow, image aspect ratios, keyboard focus, and navigation wrapping.
Check documentation in light and dark mode. Preserve body text contrast of at least 4.5:1 and visible
control boundaries. Do not use brand styling to obscure data or interface states.
