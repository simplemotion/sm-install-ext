# CLAUDE.md

## What this repo is

`simplemotion/sm-install-ext` is the GitHub Pages site for `install.simplemotion.com`, the external installer site. It is public and holds no source.

GitHub Pages gives each repo one custom domain. The two installer domains therefore need two repos (Greg, 2026-10-12):

| Domain | Copy | Repo |
|---|---|---|
| `install.simplemotion.dev` | Internal: executive and employees, every channel | `simplemotion/sm-install-int` (source and site) |
| `install.simplemotion.com` | External: freelance and customers, `release` and `preview` only | `simplemotion/sm-install-ext` (this, site only) |

## Working rules

- Make every installer change in `sm-install-int`. Its build writes both copies from one source.
- Do not edit the `gh-pages` branch. The `deploy-ext` job of `sm-install-int` replaces it on each deploy, with a `sm-binary-bridge` App token.
- Pages builds from the `gh-pages` branch. The branch carries `CNAME` and `.nojekyll`, which the `sm-install-int` build writes.
- DNS: `install.simplemotion.com` is a CNAME to `simplemotion.github.io` in the Azure DNS zone `simplemotion.com` (resource group `sm-dns`).
- `main` holds the policy files only: README.md, CLAUDE.md, CHANGE.md, ASSIGN.md and SECURE.md.
- **No "Co-Authored-By" trailers** in commits.
- **All IP assigned to SimpleMotion.Design Pty Ltd (ACN 611 618 770)** per `ASSIGN.md`.
