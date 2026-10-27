# Motion Prompt Lab

A static site that builds a ready-to-paste Claude prompt for an animated video.
The visitor picks a style, adds a topic or script, chooses voiceover or not, and copies the prompt.

## Files

- `index.html`: the whole site (gallery, filters, modal, prompt builder)
- `styles/`: one reference HTML file per style (add these later)

## Put it on GitHub Pages

1. Create a new repository and upload these files.
2. Go to Settings, then Pages.
3. Under "Build and deployment", choose "Deploy from a branch", branch `main`, folder `/ (root)`.
4. Your site appears at `https://<username>.github.io/<repo>/`.

## Add a new style

1. Make a working reference animation (one HTML file) and save it as `styles/<id>.html`.
2. In `index.html`, copy a block inside `STYLES` and change `id`, `name`, `family`, `blurb`, `reference` and the `card` text.
3. Replace the CSS thumbnail with a real preview image or video when you have one.

If a reference file is missing, the prompt shows a "paste reference here" marker instead.

## Edit the prompt

The prompt text lives in `TEMPLATE` near the top of the script. Placeholders look like `{{CONTENT}}`.

## Test locally

Opening the file directly works, but loading `styles/*.html` needs a server:

    python3 -m http.server 8000
