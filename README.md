# Sumi Starter

A ready-to-publish documentation site for your project, built with [MkDocs NG](https://mkdocs-ng.org/) and the [Sumi](https://sumi.mkdocs-ng.org/) theme. It has a home page, a guide, a configuration reference, release notes with downloads, a blog, and an English and a Chinese edition. Every page is plain Markdown.

**[Use this template](https://github.com/new?template_name=sumi-starter&template_owner=mkdocs-ng)** · [Sumi docs](https://sumi.mkdocs-ng.org/) · [Components](https://sumi.mkdocs-ng.org/docs/write/)

## Try it locally

```sh
git clone https://github.com/<you>/<your-repo>.git
cd <your-repo>
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
mkdocs serve
```

Open <http://127.0.0.1:8000/>. Switch to the Chinese edition with the language menu in the header. Add `--language zh` to build only one language while you work on it.

## Make it yours

Change things in this order, and check the preview after each step:

1. **Identity** — in `mkdocs.yml`: `site_name`, `site_description`, `site_url`, `repo_url`, `copyright`. Do the same under `languages.zh`.
2. **Home page** — the front matter of `docs/index.md`: the hero text, buttons, install command and feature cards.
3. **Content** — replace the pages in `docs/guide/` and `docs/reference/`, and update `nav` in `mkdocs.yml`.
4. **Releases** — edit `docs/releases.yml`, newest first.
5. **Blog** — edit `docs/blog/.authors.yml` and the first post, or delete `docs/blog/` and its `nav` entry.
6. **Languages** — listed under `languages` in `mkdocs.yml`. Translate the pages in `docs-zh/` (untranslated ones are shown in English with a note), add a language the same way, or delete `docs-zh/` and the `languages` block for an English-only site.
7. **Brand** — set `theme.accent` and `theme.logo`.

## Publish on GitHub Pages

1. In your repository, open **Settings → Pages** and set **Source** to **GitHub Actions**.
2. Push to `main`. The `docs` workflow builds both languages with `mkdocs build --strict` and deploys them. The English site is at the root and the Chinese one at `/zh/`.

Pull requests are built too, so a broken link fails the check before it is merged.

## Work with an AI agent

[AGENTS.md](AGENTS.md) tells Claude Code, Codex and similar tools how this site is built and which Markdown components exist. A good first prompt: *"Replace the sample content with docs for my project, based on its README."*

## License

The template is released under [CC0 1.0](LICENSE): use it for anything, no attribution needed.
