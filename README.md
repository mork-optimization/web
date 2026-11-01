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
- `styles.css`: Atlas visual design and responsive layouts.
- `assets/`: project logo, TSP documentation dashboard screenshot, and 1200×630 social preview.
- `CNAME`: existing canonical hostname; preserve when deploying through GitHub Pages.
- `robots.txt` and `sitemap.xml`: crawler discovery.

Feature copy is based on the main Mork repository's docs for algorithm components, autoconfig, AutoLLM, reference comparisons, instance selection, timing traces, and serialization. The dashboard screenshot comes from `docs/examples/TSP/img/dashboard.png`; it is an example from the documentation, not a current live campaign.

Publish the repository root using the repository's GitHub Pages configuration. The homepage does not configure DNS or redirect the apex domain; verify that `mork-optimization.com` redirects to the existing `www` canonical hostname when deploying. Update absolute canonical, Open Graph, robots, and sitemap URLs together if that hostname changes.

## Review notes

The deployed docs currently return 404 for the AutoLLM and timing-trace pages. Their homepage links use the repository and docs landing page until those documentation pages are published. Replace with feature deep links after deployment. The research DOI resolves to a publisher that blocks automated checks (HTTP 403). Browser visual QA remains required before publication.
