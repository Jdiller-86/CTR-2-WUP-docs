# CTR2WUP public documentation

This repository contains generated documentation only. Application source remains
in the private CTR2WUP repository. No ROMs, keys, saves, game assets, translated
game code, SDK or application build binaries belong here.

Website: https://jdiller-86.github.io/CTR-2-WUP-docs/
Source commit: `068149c223d48e42c44f907845086b1f64b1fa4a` · project version `0.23.0`.
CTR2WUP is in early development: the Windows GUI and playable commercial-game
WUP conversion remain unfinished. See the maintained progress and acceptance pages.

## Free publishing

1. Create/use the public repository `Jdiller-86/CTR-2-WUP-docs` without changing
   the private application repository's visibility.
2. Extract this bundle into its root and push the generated files to `main`.
3. In Settings → Pages, choose **GitHub Actions** as the source. Initial setup may
   require the repository owner; no premium plan is needed for public Pages.
4. The included native workflow publishes only `site/`. If setup or access is
   denied, retain the generated files and report the actual GitHub error.

## Read without a website

Open `site/CTR2WUP-Documentation-0.23.0.html` in any modern browser. Reading, navigation and search work
offline with no server or downloads. Printing includes all articles even if a
search filter is active. External source/issue links require internet and may need
repository access.

## Update from the authorized source checkout

```sh
python3 -m venv artifacts/docs-venv
artifacts/docs-venv/bin/python -m pip install -r docs-requirements.txt
artifacts/docs-venv/bin/python tools/build-docs-site.py
python3 tools/package-docs-site.py --output artifacts/docs-publication-NEW
```

Copy the new generated `site/`, this README and provenance/checksum files here;
preserve repository settings and the Pages workflow. Do not edit the published
articles independently: maintain the original Markdown and regenerate. If the
public repository name changes, pass `--public-repository OWNER/NAME` when packaging.

Project/runtime and site-engine licenses are preserved inside the site. The public
bundle excludes application source and the raw ARM startup assembly/linker files;
the maintained notice links back to their original source provenance. Generated
Material JavaScript/CSS remains part of the documentation site, not game code.
