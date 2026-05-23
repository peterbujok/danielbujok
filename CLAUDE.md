# Daniel's Fun Zone - danielbujok.com

## Project Overview

A static HTML site of interactive toys, games, and fun experiments built for a young child (Daniel Bujok). The site is a growing collection of standalone HTML pages, each containing a self-contained interactive experience. No build tools, no frameworks, no dependencies beyond what's loaded via CDN in each page.

## Deployment

- **Hosting:** Cloudflare Pages
- **Repo:** Public GitHub repository
- **Build:** None. Cloudflare Pages serves the root directory as-is.
- **Domain:** danielbujok.com

## Tech Stack

- Vanilla HTML, CSS, JavaScript
- Google Fonts loaded via CDN (Lilita One, Bubblegum Sans are the primary typefaces)
- No build step, no bundler, no package.json
- Each page is fully self-contained (styles and scripts inline)

## File Structure

```
/
  index.html              # Homepage with card grid linking to all activities
  toy-button.html         # Sprinkle button with confetti explosion
  inflate-and-pop.html    # Dino egg hatch + balloon pop (both on one page)
  CLAUDE.md               # This file
  README.md               # GitHub readme
```

## Design Principles

This site is built for a child with developing motor skills. Every design decision should prioritize:

1. **Large touch targets.** Buttons and interactive elements should be oversized. Minimum 44px tap targets, but aim for much larger (full-card links, big buttons). No tiny icons or close-together links.

2. **Forgiving interactions.** Hover states should be generous. Click/tap zones should extend beyond the visible element where possible. Missed taps should still feel fun (background ripples, etc.).

3. **Immediate visual feedback.** Every interaction needs an instant, obvious response. Confetti, shakes, scale changes, color shifts. Never leave a tap feeling like nothing happened.

4. **Playful, bright, warm aesthetic.** Bright gradients, rounded corners, chunky borders, big emoji, storybook vibes. No dark/scary themes. No small text.

5. **Self-contained pages.** Each HTML file should work completely on its own with zero external dependencies beyond CDN font links. All CSS and JS inline. No shared stylesheets or script files.

6. **No reading required.** Icons and emoji should communicate what things do. Text labels are supplementary, not primary navigation cues.

## Adding a New Page

1. Create a new `.html` file in the root directory.
2. Keep all styles and scripts inline within the file.
3. Use Google Fonts `Lilita One` (headings) and `Bubblegum Sans` (body) for consistency.
4. Add a card entry to `index.html` inside the `.card-grid` div, following the existing card pattern:
   - Pick a color theme (unique from existing cards)
   - Use a big emoji as the `.card-icon`
   - Write a short `.card-title` and `.card-desc`
   - Link to the new file via `href`
   - Include 4 `.card-sparkle` spans
5. Update the `animation-delay` on the new card to stagger after existing cards (increment by 0.2s).

## Content Guidelines

- No ads, no tracking, no analytics, no cookies
- No external API calls or data collection
- No content that requires reading ability to enjoy
- Everything should work offline after initial page load (fonts are the only external resource)
- Keep file sizes reasonable (each page should be under 50KB)
