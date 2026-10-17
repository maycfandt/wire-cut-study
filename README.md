# Wire Cut Study

[![Netlify Status](https://api.netlify.com/api/v1/badges/b12fbcab-bf88-401c-8208-1aff4190b15d/deploy-status)](https://app.netlify.com/projects/splendid-churros-27f7e2/deploys)

**A drawing made only by cutting.** Drag a wire across a square plate and the pieces come
loose and slowly drift away.

**Live:** [cheesewireisyourfriend.com](https://cheesewireisyourfriend.com)

![A pale square parted by straight cuts, its pieces drifting apart on a dark ground](site/og.png)

## The idea

Nothing on screen is ever drawn directly. There is one square, and every mark you see is a
gap left behind by a straight cut. Keep cutting and the plate breaks into smaller and
smaller pieces that wander off. Press Gather and they all ease back to where they started,
so the original square reassembles with every cut showing as a hairline.

It is a small, calm toy rather than a game: no score, no goal, no sign-up.

## How to play

| Action | Mouse or touch | Key |
| --- | --- | --- |
| Cut | Drag from bare ground across the plate | |
| Move a piece | Drag the piece | |
| Nudge loose pieces | Tap bare ground | |
| Cut tool | | C |
| Hold tool (move only, no cutting) | | H |
| Drift, Fall, Still | | 1, 2, 3 |
| Random colours | | X |
| Gather the pieces home | | G |
| New plate | | N |
| Close the panel | | Escape |

The pill at the bottom of the screen opens the options: colour palettes (including a custom
picker and a random "Chance" pair), the wire tool and the motion style.

## Privacy

- **No cookies, no tracking, no analytics, no sign-up.**
- **Nothing loads from any other website.** Fonts are hosted alongside the page rather than
  fetched from Google Fonts, so no visitor's IP address is shared with a third party.
- A Content Security Policy (in `netlify.toml`) enforces this, so a stray third-party
  script or font would be blocked rather than quietly loaded.

## Accessibility

- Follows the device's light or dark setting by default.
- Respects "reduce motion": the interface stops fading and Gather snaps instead of
  animating.
- Every control can be reached and used from the keyboard.

## Project structure

```
site/               Everything that is published, and nothing else
  index.html        The whole toy: markup, styles and script in one file
  og.png            1200x630 link preview image
  fonts/            Self-hosted Archivo and DM Mono (woff2) with their licences
netlify.toml        Hosting config: publish folder, security and cache headers
LICENSE             MIT licence for the code
README.md           This file
```

No build step, no package manager, no framework, no dependencies.

## Running it locally

Serve the `site` folder with any static server, for example:

    python3 -m http.server 8000 --directory site

Then visit http://localhost:8000

Opening `site/index.html` directly also works, though some browsers block local font files
that way.

## Deploying

Hosted on [Netlify](https://www.netlify.com), deploying from the `main` branch on GitHub.
The domain is registered with Namecheap, with its DNS pointing at Netlify.

- **Every push to `main` goes live** within a minute or so.
- Pull requests get their own preview link from Netlify, so changes can be checked before
  they are merged.
- `netlify.toml` is the source of truth for hosting settings and overrides anything set in
  the Netlify dashboard.

## Ideas for later

1. A way to keep an image: export the current plate as a PNG.
2. Reproducible random palettes, so a colour pair you like can be recovered.
3. A freehand cutting mode alongside the straight wire.

## Credits

- [Archivo](https://github.com/Omnibus-Type/Archivo) by Omnibus-Type, and
  [DM Mono](https://github.com/googlefonts/dm-mono) by Colophon Foundry, both under the
  SIL Open Font License 1.1. Licence texts are in `site/fonts/`.

## Licence

The code is released under the [MIT Licence](LICENSE), so you are free to use, change and
share it as long as the copyright notice comes along. The fonts keep their own SIL Open
Font License, which is included in `site/fonts/`.
