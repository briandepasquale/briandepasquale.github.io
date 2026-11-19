# Conventions for editing this site

For anyone changing Brian DePasquale's personal website, by hand or with Claude or another AI assistant. [README.md](README.md) explains how the site works. This file explains how we want it edited. The lab site, [depasquale-lab.github.io](https://depasquale-lab.github.io), uses the same rules.

## What goes on the site

Public, confirmed information only: published papers, public preprints, awards, talks, and appointments that are already public.

Never publish: pending or unfunded grants, funding amounts, papers under review or in revision without a preprint, internal reviews or evaluations, advising counts, committee rosters, private chat details, recommendation letters, applications, transcripts, or anything from tenure or review documents.

- **Spell names as the person does.** When two sources disagree, ask.
- Use they/them for anyone whose pronouns are not stated.
- Say what you could verify and what you inferred. A date inferred from a URL or a post is fine, but note it in the PR.
- Prefer official dated sources (the publisher, DOI, arXiv or bioRxiv, a BU or conference page) over memory.
- Do not put phone numbers, personal email addresses, or home details on the site.

## Page and content conventions

This site is built from the academicpages Jekyll template. Content lives in:

- `_pages/`: the main pages (about, cv, publications, talks, teaching, news).
- `_publications/`, `_talks/`, `_teaching/`, `_posts/`, `_portfolio/`: one Markdown file per entry, with front matter.
- `files/`: PDFs and other downloads (served at `/files/<name>`). `images/`: photos and figures.
- `_config.yml`: site-wide settings. `_data/navigation.yml`: the top menu.

Rules:
- One entry per file, named by date and slug (for example `2025-05-01-gatsby-talk.md`). Keep the template's front matter fields.
- Link to the lab site for lab members and lab news. Do not duplicate lab content here.
- Keep the template's sample entries out of the site (they are being removed).
- Keep files small: compress images, and do not commit raw video or large originals. Git keeps every version forever. PDFs of talks and CVs should be a final version only.
- Do not leave drafts or placeholders in published collections.

## Working in the repo

- `master` is protected. Make a branch, open a PR, and Brian merges. Never push to `master`, force-push, or rewrite history unless Brian asks in words. If something sensitive was published, tell Brian. It takes more than deleting a file (GitHub keeps copies of merged pull requests).
- Branch names start with an underscore and name the topic (`_gatsby-talk`). Delete the branch after its PR merges.
- With the GitHub CLI, always pass `--repo briandepasquale/briandepasquale.github.io`.
- Every PR gets a live preview. A comment on the PR links to `/preview/pr-N/`. Check it before merging. After a merge, the live site can take about 10 minutes to update and browsers may cache for 10 minutes, so hard-refresh before concluding a change did not work.
- `gh-pages` is written only by the workflows. Never edit it by hand.
- Keep notes about private sources in files ending `.local.md`. They are git-ignored through `.git/info/exclude`. Check `git status` before every commit and stage named paths, not whole folders.
- Local-only notes, PDFs from private folders, and anything marked confidential never go in the repo.
