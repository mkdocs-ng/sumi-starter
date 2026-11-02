# AGENTS.md

This repository is a documentation site built with MkDocs NG and the Sumi theme.

## Commands

```sh
pip install -r requirements.txt
mkdocs serve                                          # preview English at http://127.0.0.1:8000/
mkdocs serve -f mkdocs.zh.yml                         # preview Chinese
mkdocs build --strict && mkdocs build --strict -f mkdocs.zh.yml   # what CI runs; must pass
```

Always run the strict builds before you finish. Broken links, missing nav entries and unknown config keys fail them.

## Layout

- `mkdocs.yml` — English site settings and `nav`. Every new page must be added to `nav`.
- `mkdocs.zh.yml` — Chinese site. `INHERIT`s `mkdocs.yml`; overrides `docs_dir`, `site_dir`, `theme.locale`, `nav` and `extra.alternate`.
- `docs/` — English pages. `docs-zh/` — Chinese pages, same paths. Not every page needs a translation.
- `docs/index.md` — the home page. Its content is YAML front matter (`hero`, `sections`) for Sumi's `landing.html` template, not Markdown body text.
- `docs/releases.yml` — release data, newest first, shared by both languages. `docs/releases.md` only holds the intro.
- `docs/blog/posts/YYYY-MM-DD-slug.md` — blog posts with `date`, `authors`, `tags`, `description` front matter. Authors are in `docs/blog/.authors.yml`.

## Writing rules

- Plain Markdown. Do not use MDX, shortcodes or raw HTML when a component below exists.
- Links between pages point at `.md` files with relative paths (`../guide/install.md`), never at built URLs.
- Every page starts with `description:` front matter (one sentence) and one `# Title`.
- Keep the source readable on GitHub: components are lists, tables, blockquotes or fences with one `{…}` attribute line.

## Sumi components

| Write | Renders as |
| --- | --- |
| `> [!NOTE]` / `[!TIP]` / `[!IMPORTANT]` / `[!WARNING]` / `[!CAUTION]` | Callout. `> [!TIP]- Title` is collapsible. |
| Ordered list, then a line `{.steps}` | Numbered procedure. Indent step content by 4 spaces. |
| Bullet list of links with a description line, then `{.cards}` | Card grid. Start an item with `:lucide-icon-name:` for an icon. |
| Adjacent fences with `{tab="Label"}` | Tabs. Same labels sync across pages. |
| ```` ```py title="app.py" ```` | Code block with a file name. |
| Table, then `{.fields}` | Parameter reference (first column = name). |
| Table, then `{caption="…"}` / `{.wide}` | Captioned or full-width table. |
| `![alt](img.png)` then `{caption="…"}` | Figure. |
| ```` ```mermaid ```` | Diagram. |
| ```` ```filetree ```` | File tree; `# comment` after an entry. |
| `$…$`, `$$…$$` | Math. |
| `++Ctrl+K++`, `:lucide-rocket:` | Keys, inline icon. |

Full reference: https://mkdocs-ng.github.io/mkdocs-sumi/docs/write/ (each page there has a Markdown copy at the same path with `.md`).
