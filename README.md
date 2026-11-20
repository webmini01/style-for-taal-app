# Styles for the Taal app

The Taal app's Style Store reads this repo straight from GitHub (raw files):

- `catalog.json` – the list the app shows (made by the build tool, do not edit by hand)
- `categories.json` – the categories, in order
- `styles/<id>.json` – one file per style
- `thumbs/<id>.jpg` – a real frame of each style (made by the build tool)

## Adding a style

1. Add `styles/<id>.json` (copy one that is close and change it). `id` must match the file name,
   `category` must be one of `categories.json`.
2. In the app's repo run `node engine/tools/store-build.mjs <path to this repo>` – it renders the
   thumbnails and writes `catalog.json`.
3. Commit and push. The app sees the new style within about 5 minutes. fonts and animations that are inside the app can be used; anything unknown falls back to a
safe default in the app.
