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
Brand direction A · Pole (Josh's pick, 2026-11-15): the full logos, as outlined SVGs (no web font): `img/logo-pool-position-nav.svg`
in the nav on every page, `img/logo-pool-position.svg` above the home hero heading, `img/logo-prosim.svg` and `img/logo-scorebook.svg`
on their pages' heroes. Wordmark set in Archivo Italic (OFL), 2026-11-15; may be replaced by hand-drawn lettering later. The
sources and the build are in thirtythree-degrees-studio `brand/pool-position-2026-11/` (`A-pole/svg/*-clear.svg`, `*-nav.svg`);
copy them from there, never retype. The mark (`img/mark-pool-position.svg`) stays the favicon; the shipped A app icons stay the
touch icons and the home page's app cards.
Footer copyright on every page: "© 2026 Thirty-Three Degrees Studio LLC" (Josh, 2026-11-15: "Go ahead and use © 2026 Thirty-Three
Degrees Studio LLC now").
Scorebook page hero: the app's own Table screen on an open iPhone Duo (`img/sb-duo.jpg`), never a ProSim render (Josh, 2026-11-15:
"on the scorebook page the top image shouldn't be an image from ProSim game"). Duo shots (`.pair.duos`) are capped at 80% of the
viewport height and wrap, so each is fully visible on a portrait phone; side by side only when both fit (Josh, 2026-11-15: "Only see
half of each screenshot without scrolling on a portrait screen").
Shots refreshed 2026-11-15 from Release simulator builds of pool-position-ios main 24d81934: ProSim as on main (phone Home, Who's
in, the rank moment, a regular's page, Fran's position lesson; Apple TV first: Home, a rack in play, the rank moment, Fran's page)
and the Scorebook 1.3 (70) shots from 11-13/14. **Phone shots carry the simulator's own iPhone bezel** (DeviceKit chrome + screen
mask + Dynamic Island, baked in by the hub's `skills/marketing-shots/frame.swift`); `.phone` only clips the outer corner
(border-radius 16.7%/8%). Halls are clean Apple TV frames (`-tvNoHUD -cam`) cropped so no signs, screens, bottles or drinks show.
No crowd or patrons, hall TVs dark, sample names only (Jordan, Casey, Riley, Sam; the regulars are characters).
Each shot and its launch flags are listed in the shot archive (LIST.md, kept off the site). The Scorebook Duo section (`<!-- SB-DUO -->`) uses Josh's real iPhone Duo screenshots (open, 1812x2576, 2026-11-15; sample players Jack and Jill), framed in the Duo inner-screen shape from the simulator's mask; the status bar was rebuilt with time and Wi-Fi only (a sports team logo and another app's icon removed).
Contact on every page is support@33degrees.studio (no personal email). Every page has a small footer link to 33degrees.studio.
Refresh the shots when the halls or controls change.
