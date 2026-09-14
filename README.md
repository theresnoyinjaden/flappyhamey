# Flappy Hamey

A single-file, dependency-free Flappy Bird-style game built with HTML5 Canvas.
Guide Hamey through pipes styled after the Israeli flag, past themed zones
(farms, classroom, parliament, desert, home, ocean, the strait), all the way
home.

## Play locally

Just open `index.html` in a browser — no build step, no server required.

Controls: tap / click / space / enter to flap. Click **START** on the title
screen to begin.

## Deploy to Netlify

This repo is a static site, so Netlify needs no build command:

1. Push this repo to GitHub (already done if you're reading this from the repo).
2. In Netlify, click **Add new site → Import an existing project** and pick
   this repository.
3. Build settings are already defined in `netlify.toml`:
   - Build command: *(none)*
   - Publish directory: `.`
4. Deploy — Netlify will serve `index.html` directly.

Alternatively, drag-and-drop the project folder onto
[app.netlify.com/drop](https://app.netlify.com/drop) for an instant deploy.

## Custom bird sprite

Drop a transparent PNG at `assets/bird.png` (roughly square, ~64x64px) and
it will automatically replace the placeholder bird box — no code changes
needed.
