# Mork homepage

Static homepage for https://www.mork-optimization.com/. No build step, runtime dependencies, or JavaScript required.

## Preview

From this directory:

```sh
python3 -m http.server 8765 --bind 127.0.0.1
```

Open http://127.0.0.1:8765. Review at desktop and narrow mobile widths before publishing, including keyboard navigation and the skip link.

## Files

- `index.html`: content, navigation, and search/social metadata.
- `styles.css`: Mork color and type tokens, components, and responsive layouts.
- `BRAND.md`: shared visual identity, writing rules, and guidance for the generator and documentation.
- `assets/`: project logo, TSP dashboard and route screenshots, and 1200×630 social preview.
- `CNAME`: existing canonical hostname; preserve when deploying through GitHub Pages.
- `robots.txt` and `sitemap.xml`: crawler discovery.

Feature copy is based on the main Mork repository's docs for algorithm components, autoconfig, AutoLLM, reference comparisons, instance selection, timing traces, and serialization. The current dashboard and route screenshots mirror `docs/examples/TSP/img/dashboard.png` and `docs/examples/TSP/img/route.png`. They were captured from a real Berlin52 LocalSearchExperiment (seed 1234, 10 repetitions, 2 workers, benchmark and warmup disabled). See `example-tsp/frontend/README.md` for reproduction; refresh both documentation and homepage copies together.

Publish the repository root using the repository's GitHub Pages configuration. The homepage does not configure DNS or redirect the apex domain; verify that `mork-optimization.com` redirects to the existing `www` canonical hostname when deploying. Update absolute canonical, Open Graph, robots, and sitemap URLs together if that hostname changes.

## Review notes

The deployed docs currently return 404 for the AutoLLM and timing-trace pages. Their homepage links use the repository and docs landing page until those documentation pages are published. Replace with feature deep links after deployment. The research DOI resolves to a publisher that blocks automated checks (HTTP 403). Browser visual QA remains required before publication.

## Identity and responsive review

Use [BRAND.md](BRAND.md) when editing the homepage or another Mork site. The generator has its own local
stylesheet in `css/styles.css`; the documentation maps the same palette to Material in
`docs/assets/stylesheets/brand.css` in the main Mork repository. Serve each site independently.

Review at 1440, 1024, 850, 768, 390, and 320px widths. Check the hero's deliberate two-line title, natural
wrapping in other headings, the step columns, screenshot captions, and keyboard focus. The primary slogan
is retained; the feature descriptions name concrete actions. Screenshot captions describe the actual
experiment; detailed provenance and chart interpretation belong here and in the TSP tutorial.
