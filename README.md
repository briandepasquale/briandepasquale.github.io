# [Brian DePasquale](https://briandepasquale.github.io)

Source for the personal website of Brian DePasquale, Assistant Professor of Biomedical Engineering at Boston University: **https://briandepasquale.github.io**

For the lab, see the [DePasquale Lab website](https://depasquale-lab.github.io).

It is a [Jekyll](https://jekyllrb.com) site built from the [academicpages](https://github.com/academicpages/academicpages.github.io) template (itself based on the [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/) theme, MIT license, see `LICENSE`) and hosted on GitHub Pages. Almost everything is a Markdown file.

**Last updated:** November 19, 2026 (repository organization). For the latest change, check the [commit history](https://github.com/briandepasquale/briandepasquale.github.io/commits/master). If you make a substantial content update, please bump this date.

## How changes get to the site

1. `master` is protected. Nothing is pushed to it directly. Every change goes through a pull request (PR). No approval is required, so you can merge your own PR once the preview looks right.
2. Make a branch from `master`, edit files, push the branch, and open a PR.
3. GitHub builds a **live preview** of your branch. A comment on the PR links to it, at `https://briandepasquale.github.io/preview/pr-<number>/`. Check it before merging. The preview is removed when the PR closes.
4. When the PR is merged, the `deploy` workflow rebuilds the site and publishes it to the `gh-pages` branch, which GitHub Pages serves. The live site usually updates within 10 minutes.

See [CONVENTIONS.md](CONVENTIONS.md) for what may be published and how we edit. `CLAUDE.md` points AI assistants at it.

## What's inside

| Path | What it is |
|---|---|
| `_pages/` | The main pages: about, CV, publications, talks, teaching, news. |
| `_publications/`, `_talks/`, `_teaching/`, `_posts/`, `_portfolio/` | One Markdown file per entry. |
| `files/` | PDFs and other downloads, served at `/files/<name>`. |
| `images/` | Photos and figures. |
| `_config.yml` | Site title, author profile, social links and Jekyll settings. |
| `_data/` | Navigation menu and UI text. |
| `_includes/`, `_layouts/`, `_sass/`, `assets/` | The template's building blocks. You normally do not touch these. |
| `markdown_generator/`, `talkmap*` | Optional template tools for generating entries from a spreadsheet and mapping talks. |
| `.github/workflows/` | `preview.yml` builds PR previews, `deploy.yml` publishes the live site to `gh-pages`. |
| `CONVENTIONS.md`, `CLAUDE.md` | How we want the site edited. |
| `CHANGELOG.md`, `CONTRIBUTING.md` | Left over from the template. They are about the upstream project, not this site. |

## Previewing on your own computer (optional)

Most people can skip this and use the PR preview.

1. Install Ruby and Bundler.
2. Run `bundle install`. If you get errors, delete `Gemfile.lock` and try again.
3. Run `bundle exec jekyll serve` and open http://localhost:4000.

## Good to know

- `_config.yml` has `future: true`, so entries dated in the future are published. Remove stale placeholder entries rather than leaving them in the collections.
- `README.md`, `CONVENTIONS.md` and `CLAUDE.md` are excluded from the website.

## Credits

Built with the [academicpages](https://github.com/academicpages/academicpages.github.io) template, by Stuart Geiger and contributors, forked from Minimal Mistakes, copyright 2016 Michael Rose, MIT license.
