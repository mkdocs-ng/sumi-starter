# Sumi Starter

A ready-to-publish documentation site for your project, built with [MkDocs NG](https://mkdocs-ng.github.io/mkdocs/) and the [Sumi](https://mkdocs-ng.github.io/mkdocs-sumi/) theme. It has a home page, a guide, a configuration reference, release notes with downloads, a blog, and an English and a Chinese edition. Every page is plain Markdown.

**[Use this template](https://github.com/new?template_name=sumi-starter&template_owner=mkdocs-ng)** · [Sumi docs](https://mkdocs-ng.github.io/mkdocs-sumi/) · [Components](https://mkdocs-ng.github.io/mkdocs-sumi/docs/write/)

## Try it locally

```sh
git clone https://github.com/<you>/<your-repo>.git
cd <your-repo>
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
mkdocs serve
```

Open <http://127.0.0.1:8000/>. The Chinese edition runs with `mkdocs serve -f mkdocs.zh.yml`.

## Make it yours

Change things in this order, and check the preview after each step:

1. **Identity** — in `mkdocs.yml`: `site_name`, `site_description`, `site_url`, `repo_url`, `copyright`. Do the same in `mkdocs.zh.yml`.
2. **Home page** — the front matter of `docs/index.md`: the hero text, buttons, install command and feature cards.
3. **Content** — replace the pages in `docs/guide/` and `docs/reference/`, and update `nav` in `mkdocs.yml`.
4. **Releases** — edit `docs/releases.yml`, newest first.
5. **Blog** — edit `docs/blog/.authors.yml` and the first post, or delete `docs/blog/` and its `nav` entry.
6. **Languages** — keep `docs-zh/` and `mkdocs.zh.yml`, translate them, or delete both and the `extra.alternate` block.
7. **Brand** — set `theme.accent` and `theme.logo`.

## Publish on GitHub Pages

1. In your repository, open **Settings → Pages** and set **Source** to **GitHub Actions**.
2. Push to `main`. The `docs` workflow builds both editions with `--strict` and deploys them. The English site is at the root and the Chinese one at `/zh/`.

Pull requests are built too, so a broken link fails the check before it is merged.

## Work with an AI agent

[AGENTS.md](AGENTS.md) tells Claude Code, Codex and similar tools how this site is built and which Markdown components exist. A good first prompt: *"Replace the sample content with docs for my project, based on its README."*

## License

The template is released under [CC0 1.0](LICENSE): use it for anything, no attribution needed.
