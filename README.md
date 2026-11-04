# poolpositiongame.com

The public site for the Pool Position brand: Pool Position: ProSim (the game) and Pool Position: Scorebook.
Static pages on GitHub Pages, custom domain `poolpositiongame.com` (DNS at GoDaddy). Only the pages and images
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
