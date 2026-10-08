# Swords & Wizardry: Birthright

Campaign rules published from Markdown using MkDocs Material and Netlify.

## Update the rules from Obsidian

The website source is `docs/index.md`. Copy the contents of your Obsidian rules note into that file and commit/push to `main`. Netlify rebuilds the website automatically after the repository is connected.

You can also open a local clone of this repository as an Obsidian vault and edit `docs/index.md` directly. Saving in Obsidian does not push to GitHub: commit and push with GitHub Desktop or Git afterwards.

Use standard Markdown links and relative image paths for published content. Put images in `docs/assets/`. Obsidian-only plugins and embeds need separate conversion.

## Connect Netlify

Import the `bagfullofdice/Rules` GitHub repository into Netlify, select the `main` branch, and deploy. The root `netlify.toml` supplies:

- Build command: `python -m pip install -r requirements.txt && python -m mkdocs build --strict`
- Publish directory: `site`
- Base directory: leave empty
- Python version: `3.12`

## Preview locally

```sh
python -m pip install -r requirements.txt
python -m mkdocs serve
```

Open the address shown by MkDocs. To verify a production build:

```sh
python -m mkdocs build --strict
```
