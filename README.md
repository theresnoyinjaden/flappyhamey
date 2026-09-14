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

The bird image is baked directly into `index.html` as a base64 data URI, so
the game always shows the real sprite no matter how the file is copied,
downloaded, or hosted — no separate `assets/` folder required.

`assets/bird.png` in this repo is kept as the editable source image. To swap
in a new sprite:

1. Replace `assets/bird.png` with your own image (roughly square works best).
2. Re-embed it into `index.html`:
   ```sh
   python3 -c "
   import base64
   b64 = base64.b64encode(open('assets/bird.png','rb').read()).decode()
   print(len(b64), 'chars')
   " # then paste the base64 into BIRD_IMAGE_SRC in index.html
   ```
   or run any base64 encoder and replace the `data:image/png;base64,...`
   string assigned to `BIRD_IMAGE_SRC` near the top of the `<script>` block.
