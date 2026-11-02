---
description: How to write and preview these docs. Every component is plain Markdown.
---

# Writing docs

These pages use the [Sumi](https://sumi.mkdocs-ng.org/) theme for [MkDocs NG](https://mkdocs-ng.org/). Everything is plain Markdown, so the files read well on GitHub too.

## Preview locally

```sh
pip install -r requirements.txt
mkdocs serve                  # http://127.0.0.1:8000/, Chinese under zh/
mkdocs serve --language zh    # only Chinese, faster
```

## Where things live

```filetree
docs/                 # English pages
├── index.md          # home page (data in front matter)
├── guide/
├── reference/
├── releases.md       # release page, filled from releases.yml
├── releases.yml
└── blog/
    ├── .authors.yml
    └── posts/        # one file per post, named YYYY-MM-DD-slug.md
docs-zh/              # Chinese pages, same layout
mkdocs.yml            # settings for both languages
```

## Components

| You write | You get |
| --- | --- |
| `> [!NOTE]` | A callout. Also `TIP`, `IMPORTANT`, `WARNING`, `CAUTION`. |
| A numbered list + `{.steps}` | A procedure with numbered steps. Indent step content by 4 spaces. |
| A list of links + `{.cards}` | A grid of cards. |
| Code fences with `{tab="…"}` | Tabs. |
| A table + `{.fields}` | A parameter reference. |
| ```` ```mermaid ```` | A diagram. |
| ```` ```filetree ```` | A file tree. |
| `$E = mc^2$` | Math. |
| `++Ctrl+K++` | Keys. |
{.wide}

See the [Sumi component guide](https://sumi.mkdocs-ng.org/docs/write/) for all of them.

## Before you open a pull request

```sh
mkdocs build --strict
```

`--strict` turns broken links and missing pages into errors. CI runs the same command.
