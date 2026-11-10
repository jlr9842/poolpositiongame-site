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
Shots refreshed again 2026-11-10 (Josh's notes) from Release simulator builds of pool-position-ios main 0056a223 (ProSim as
shipped in 0.1 (21), 8e90d952; Scorebook as shipped in 1.3 (67), 5ccec686): iPhone 18 Pro Max, iPad Pro 13, iPhone Duo (folded,
open flat, book, laptop; landscape heroes and hall pictures are `-stills` from the open Duo) and the Apple TV. **Every ProSim shot
is taken with `-noCrowd`** (Josh: no stand-in people). Three halls: Palmer's, the Home Lounge and Pub 85 (blue and red tables).
Pub 85's sign wall and back bar stay out of frame (no readable signs, no bottles). Scorebook shots show the tapped sets
(`-liveEight`, `-livePoints`, `-liveRace8`) and the Table's scene row. Sample names only (Jordan vs Casey; the House's regulars
Grace and Manny are characters). Palmer's drink signs are cropped out and the halls' TVs are dark (`-lightLab notv`).
Each shot and its launch flags are listed in the shot archive (LIST.md, kept off the site).
Contact on every page is support@33degrees.studio (no personal email). poolposition.app doesn't link to 33degrees.studio.
Refresh the shots when the halls or controls change.
