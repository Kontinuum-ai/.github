# Kontinuum &middot; `.github`

The GitHub organisation profile for [Kontinuum](https://kontinuum.audio).

- **[`profile/README.md`](profile/README.md)** — the page shown at
  [github.com/Kontinuum-ai](https://github.com/Kontinuum-ai). GitHub only
  renders it from this exact path in this exact repo.
- **[`assets/logo.svg`](assets/logo.svg)** / **[`logo-dark.svg`](assets/logo-dark.svg)** —
  the full lockup: the lemniscate of dots plus the wordmark and tagline.
  Light and dark differ only in the background rect.
- **[`assets/mark.svg`](assets/mark.svg)** — the lemniscate alone, generated
  from `logo-dark.svg` by dropping the two `<text>` nodes and the background
  and tightening the viewBox. This is what the banner uses, so the wordmark is
  not drawn twice.
- **[`assets/logo.png`](assets/logo.png)** — 1024&times;1024 for the
  organisation avatar, which has to be uploaded through the GitHub web UI
  (there is no REST API for it). `logo-2048.png` is the larger raster.
- **[`assets/org-banner.png`](assets/org-banner.png)** — the banner at the top
  of the profile, rendered at 2x from `tools/org-banner.html`.

The banner sets no webfont on purpose: the site uses the
`ui-monospace, "SF Mono", Menlo` stack, so Chrome resolves the same faces here
that a visitor resolves on kontinuum.audio.

Images in the profile README are referenced by absolute `raw.githubusercontent`
URL, because relative paths do not resolve for viewers of the org page.

```bash
./tools/render.sh    # regenerate the banner and the avatar (needs Chrome)
```
