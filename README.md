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
Brand direction A · Pole (Josh's pick, 2026-11-15): the Pool Position mark (`img/mark-pool-position.svg`) by the nav name and the
page lockups, the shipped A app icons (`icon-prosim.png`, `icon-scorebook.png`, touch icons) as favicons. Headings stay HTML text
(no wordmark image until licensed lettering exists).
Shots refreshed 2026-11-15 from Release simulator builds of pool-position-ios main 24d81934: ProSim as on main (phone Home, Who's
in, the rank moment, a regular's page, Fran's position lesson; Apple TV first: Home, a rack in play, the rank moment, Fran's page)
and the Scorebook 1.3 (70) shots from 11-13/14. **Phone shots carry the simulator's own iPhone bezel** (DeviceKit chrome + screen
mask + Dynamic Island, baked in by the hub's `skills/marketing-shots/frame.swift`); `.phone` only clips the outer corner
(border-radius 16.7%/8%). Halls are clean Apple TV frames (`-tvNoHUD -cam`) cropped so no signs, screens, bottles or drinks show.
No crowd or patrons, hall TVs dark, sample names only (Jordan, Casey, Riley, Sam; the regulars are characters).
Each shot and its launch flags are listed in the shot archive (LIST.md, kept off the site). Still to add: the Scorebook's Duo laptop picture (`<!-- SB-DUO -->` section).
Contact on every page is support@33degrees.studio (no personal email). Every page has a small footer link to 33degrees.studio.
Refresh the shots when the halls or controls change.
