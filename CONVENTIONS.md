# Conventions for editing this site

For anyone changing the DePasquale Lab website, by hand or with Claude or another AI assistant. [README.md](README.md) explains how the site works. This file explains how we want it edited.

## Finding photos and details about what happened in the lab

If you are using Claude (or another assistant) to build the site, **search the `#food-drinks-fun` Slack channel**. It is where lab photos get posted, and it usually explains what was going on.

- **Photos come with dates.** Slack strips a photo's original capture date, so the day it was posted is the best date available. The messages around a post often say what the event was (a dinner, a celebration, the BBQ) and who organized it.
- **Search by file name** (for example `IMG_1234`) to find where and when a photo was posted, or read the channel around a date.
- **Use only what you need.** Do not copy chat content onto the site: phone numbers, logistics, jokes at someone's expense, or private conversations.
- **Ask Brian for the caption.** The channel tells you when and what, not what to say. Do not invent anecdotes, and do not name people in a photo from their faces. Ask.
- **Be careful with who appears.** Ask before publishing photos of children or of anyone who may not want to be on a public page.
- Photos downloaded from Slack have no metadata. Resize them anyway (about 1000 px, JPEG) and save without metadata, so no location data is ever published.

## What goes on the site

Public, confirmed information only: published papers, public preprints, awards, talks, and appointments that are already public.

Never publish: pending or unfunded grants, funding amounts, papers under review or in revision without a preprint, internal reviews or evaluations, advising counts, committee rosters, or private chat details.

- **Teaching** (courses, enrollments) stays off Happenings.
- **Spell names as the person does** (LinkedIn is the usual check). When two sources disagree, ask.
- Say what you could verify and what you inferred. A date inferred from a URL or a post is fine, but note it in the PR.

## Happenings page

- Collapsible years, each split into collapsible seasons (Fall, Summer, Spring, Winter). December to February is Winter, March to May Spring, June to August Summer, September to November Fall.
- Newest first. Items with a known month start with it ("May: ..."). Items with only a season sit in that season without a month prefix.
- Link lab members to `https://depasquale-lab.github.io/members/<file-name>.html`.
- Images go in `images/` and are referenced from this page as `../images/<file>`, so they work in PR previews too.
- Dated sources are better than memory: BU news pages, announcement pages, and the publisher's page.

## Member pages

- Role decides the section: `pi`, `phd`, `undergrad`, `alumni`, `collaborator`, or `mascot`.
- Photo: a square JPEG, about 400 px, in `images/`.
- Bios are first person. Build them from the person's own site or LinkedIn and keep them short.
- Publications and presentations lists include only public work. Bold the page owner's name.

## Working in the repo

- `main` is protected. Make a branch, open a PR, and check the preview link on the PR. Brian merges.
- Do not force-push `main` or rewrite history unless Brian asks. If something sensitive was published, tell Brian. It takes more than deleting a file (GitHub keeps copies of merged pull requests).
- After a deploy, browsers can show the old version for up to 10 minutes. Hard-refresh before concluding a change did not work.
- With the GitHub CLI, always pass `--repo depasquale-lab/depasquale-lab.github.io`. Without it, `gh` can point at the upstream template.
- The citation bot sometimes pushes an "Update citations" commit to a PR branch. Run `git pull --rebase` before pushing again.
- Keep files small. Compress images and video rather than committing originals.
