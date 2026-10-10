# SabatKu publications

Berita, artikel, editorial, dan feature dari sumber terverifikasi, dengan provenance dan format sumber yang jelas.

Status: executable repository foundation; no approved content included. Android/Web integration and `.skpack` generation remain future work.

## Commands

```sh
npm ci
npm run validate
npm test
npm run build:content
```

Sources are under `content/`; examples under `examples/` never enter public output. Canonical schemas/taxonomy are owned by `sabatku-contracts`; vendored snapshots have SHA-256 pins in `contracts/lock.json`. Deliberate contract upgrades must update snapshots and pins together.

## Publishing

GitHub Actions validates content/tests then builds an artifact. Push to main deploys only `public/` to GitHub Pages using GitHub Actions. Enable Pages → Source: GitHub Actions. Draft files are never served by Pages, but this public Git repository exposes committed source files; private editorial files must stay elsewhere.

Published revision files are immutable. Reuse of a revision ID for changed content is rejected when existing output is present; retain previous publication artifacts when releasing revisions. Catalog is generated last. Online chapters use Markdown; hashes and byte counts accompany files. No complete offline book claim is made until client installation and packaging exist.

## Architecture

See [library blueprint](https://github.com/AiWerek-Tech/sabatku-docs/blob/main/architecture/digital-library-blueprint.md) and [taxonomy/publications](https://github.com/AiWerek-Tech/sabatku-docs/blob/main/architecture/library-taxonomy-and-publications.md).
