# poolposition.app

The public site for the Pool Position brand: Pool Position: ProSim (the game) and Pool Position: Scorebook.
Static pages on GitHub Pages, custom domain `poolposition.app` (DNS at GoDaddy; .app is HSTS-preloaded, HTTPS only).
`poolpositiongame.com` forwards to `https://poolposition.app/prosim/` and `poolpositionapp.com` to `https://poolposition.app/`
(GoDaddy domain forwarding, 301, not from this repo). Only the pages and images
live here; screenshots use sample data only.

| Path | What |
|---|---|
| `/` | Brand landing, both apps |
| `/prosim/`, `/prosim/privacy/`, `/prosim/support/` | ProSim |
| `/scorebook/`, `/scorebook/privacy/`, `/scorebook/support/` | Scorebook |
| `/t/<code>` | ProSim table invites (universal link / App Clip). No file per code: `404.html` shows the invite page for `/t/...` |
| `/.well-known/apple-app-site-association` | applinks (`/t/*` → `com.joshramey.prosim`) and appclips (`com.joshramey.prosim.Clip`), team R344K83LVM. `.nojekyll` keeps `.well-known` published |

**Removing the Scorebook:** delete `scorebook/` and every block between `<!-- SCOREBOOK -->` and
`<!-- /SCOREBOOK -->` (`grep -rn SCOREBOOK .`).

**When the Scorebook is live:** replace the "Coming soon" pill in `scorebook/index.html` with its App Store link
(the comment there has the markup).

**When ProSim has an App Store ID:** uncomment the `apple-itunes-app` meta in `404.html` and `t/index.html`.

## Look and screenshots

Style A, "Night at the table" (Josh's pick, 2026-11-04): dark felt, Liquid Glass panels, gold accents (`style.css`).
Shots refreshed 2026-11-10 from Release simulator builds of pool-position-ios main 0056a223 (ProSim as shipped in 0.1 (21),
8e90d952, no ProSim changes since; Scorebook as shipped in 1.3 (67), 5ccec686): iPhone 18 Pro Max, iPad Pro 13, iPhone Duo
(folded, open flat, book, laptop; the landscape heroes are `-stills` from the open Duo) and the Apple TV. Sample names only
(Jordan vs Casey; the House's regulars Grace and Manny are characters). Palmer's appears framed as a hall in the app, not a
partner; its drink signs are cropped out of the hero and the halls' TVs are dark (`-lightLab notv`), so no race loop shows.
Each shot and its launch flags are listed in the shot archive (LIST.md, kept off the site).
Refresh the shots when the halls or controls change.
