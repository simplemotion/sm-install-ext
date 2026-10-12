<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/simplemotion/.github/main/assets/banners/SM-White.svg">
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/simplemotion/.github/main/assets/banners/SM-Black.svg">
    <img alt="SimpleMotion" src="https://raw.githubusercontent.com/simplemotion/.github/main/assets/banners/SM-Black.svg" width="800">
  </picture>
</p>

<p align="center">
  <em>Engineered for Architecture, Entertainment, Industry and Manufacturing.</em>
</p>

# SECURE — simplemotion/sm-install-ext

> Security posture for the external installer site, `install.simplemotion.com`.

## What this repo serves

The `gh-pages` branch holds the external copy of the SimpleMotion installers. The source and the threat model are in [simplemotion/sm-install-int](https://github.com/simplemotion/sm-install-int/blob/main/SECURE.md).

## Who can write the site

- Only the `deploy-ext` job of `sm-install-int` writes `gh-pages`. It uses a `sm-binary-bridge` App token scoped to this repo.
- `main` holds policy files only. The organisation ruleset protects it.

## Reporting issues

Email **security@simplemotion.com** for a vulnerability in this repo or in the site that it serves. Do not open a public issue.
