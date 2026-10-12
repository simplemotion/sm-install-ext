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

# simplemotion/sm-install-ext

This repo serves the **external** SimpleMotion installer site at
**<https://install.simplemotion.com>**. The site is for the freelance and
customers cohorts. Its installers accept the `release` and `preview` channels only.

This repo holds no source. The installer source is in
[simplemotion/sm-install-int](https://github.com/simplemotion/sm-install-int),
which also serves the internal site at <https://install.simplemotion.dev>.
For the install commands, read the
[sm-install-int README](https://github.com/simplemotion/sm-install-int#readme).

## How the site gets here

1. A change merges to `main` of `sm-install-int`.
2. Its `sm-pages.yml` workflow builds the external copy.
3. The `deploy-ext` job replaces the `gh-pages` branch of this repo with that copy, as one commit.
4. GitHub Pages builds the site from `gh-pages`.

Do not edit the `gh-pages` branch. The next deploy replaces it.
