# danielbujok.com

A collection of interactive toys and games built for a kid who likes dinosaurs, buttons, and making things explode.

**Live site:** [danielbujok.com](https://danielbujok.com)

## What's Inside

| Page | What It Does |
|------|-------------|
| **Sprinkle Button** | A giant candy-colored button covered in sprinkles. Hover makes it wiggle, clicking launches confetti and emoji everywhere. Includes a click counter with escalating hype messages. |
| **Hatch a Dino** | A green dino egg that shakes and cracks the faster you tap. Fill the pressure bar before it drains and the egg explodes into shell fragments, revealing a baby dinosaur. |
| **Pop a Balloon** | A balloon that physically inflates with each tap, developing stretch marks and shifting color as it strains. Push it past the limit and it bursts with a satisfying pop. |

Both inflate-to-pop toys share the same mechanic: tapping adds pressure, but pressure constantly decays, so you have to tap fast enough to outpace it.

## Running Locally

No build step. Open `index.html` in a browser or serve with any static file server:

```bash
# Python
python3 -m http.server 8000

# Node
npx serve .
```

## Deployment

The site is deployed via [Cloudflare Pages](https://pages.cloudflare.com) connected to this repo.

**Cloudflare Pages settings:**
- Framework preset: None
- Build command: *(leave empty)*
- Build output directory: `/`

Pushes to `main` trigger automatic deploys.

## Adding New Pages

1. Create a new `.html` file in the root
2. Keep everything self-contained (inline CSS and JS)
3. Add a card linking to it on the homepage (`index.html`)
4. Push to `main`

See `CLAUDE.md` for detailed conventions and design guidelines.

## Tech

Plain HTML, CSS, and JavaScript. No frameworks, no build tools, no dependencies. Google Fonts are the only external resource.

## License

This is a personal project. The code is public for transparency but not licensed for redistribution.
