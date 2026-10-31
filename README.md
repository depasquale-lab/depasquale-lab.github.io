# [DePasquale Lab website](https://depasquale-lab.github.io)

Source for the website of the Artificial and Biological Intelligence Laboratory at Boston University: **https://depasquale-lab.github.io**

It is a [Jekyll](https://jekyllrb.com) site built from the [Greene Lab website template](https://github.com/greenelab/lab-website-template) ([template docs](https://greene-lab.gitbook.io/lab-website-template-docs)) and hosted on GitHub Pages. You do not need to know Jekyll to edit it. Almost everything is a Markdown file.

**Last updated:** October 31, 2026 (research page, happenings through fall 2026, undergraduate and alumni pages). For the latest change, check the [commit history](https://github.com/depasquale-lab/depasquale-lab.github.io/commits/main). If you make a substantial content update, please bump this date.

## How changes get to the site

1. `main` is protected. Nothing is pushed to it directly. Every change goes through a pull request (PR). No approval is required, so you can merge your own PR once the preview looks right.
2. Make a branch from `main`, edit files, push the branch, and open a PR.
3. GitHub builds a **live preview** of your branch. A comment on the PR links to it, at `https://depasquale-lab.github.io/preview/pr-<number>/`. Check it before merging. The preview is removed when the PR closes.
4. When the PR is merged, the `on-push` workflow rebuilds the site and publishes it. The live site usually updates within 10 to 20 minutes.

## What's inside

| Path | What it is |
|---|---|
| `index.md` | **Research** page (the home page). The lab description, the feature blocks with figures, and the publications list. |
| `team/index.md` | **People** page. Lists members by role, and the "interested in joining?" text. |
| `_members/` | One Markdown file per person or collaborating lab. Each becomes a profile page. |
| `happenings/index.md` | **Happenings** page (news, awards, talks, arrivals and lab events), newest year first. The old `/news/` address redirects here. |
| `images/` | Photos, figures and icons. |
| `videos/` | Hosted videos (keep these small). |
| `CONVENTIONS.md` | How we want the site edited: what may be published, page conventions, and where to find lab photos and dates (the `#food-drinks-fun` Slack channel). `CLAUDE.md` points AI assistants at it. |
| `_config.yaml` | Site title, description, social links and Jekyll settings. |
| `_data/` | Data files, including `types.yaml`, which defines member roles and link icons. |
| `_includes/`, `_layouts/`, `_styles/`, `_scripts/`, `_plugins/` | The template's building blocks. You normally do not touch these. |
| `.github/workflows/` | The automation that builds previews and deploys the site. |
| `.docker/` | Optional local preview environment. |
| `blog/`, `projects/`, `research/`, `contact/` | Template starter pages. They are not linked in the menu. |

## Common edits

### Add yourself (or someone else) to the People page

1. Copy an existing file in [`_members/`](_members) and name it `first-last.md`.
2. Fill in the front matter and write your bio below it:

   ```yaml
   ---
   name: First Last
   image: images/first-last.jpg
   role: phd          # pi, phd, undergrad, alumni or collaborator
   description: One line shown under your photo
   aliases:
   links:
     email: you@bu.edu
     linkedin: your-linkedin-handle
     google-scholar: YourScholarId&hl=en
     github: your-github-name
   ---
   ```

3. Add a square photo (about 400×400 pixels, JPEG) to `images/`.
4. The `role` decides which section of the People page you appear in. Link types (`email`, `linkedin`, `orcid`, `home-page`, `website`, and so on) are defined in `_data/types.yaml`.
5. To move someone to Alumni, change `role` to `alumni` and update the description.

Collaborating labs are members with `role: collaborator`, plus a `home-page` link.

### Add a happening

Edit `happenings/index.md`. The page is a set of collapsible years, each split into collapsible seasons (Fall, Summer, Spring, Winter, and "Throughout the year" for items with no month). Add a bullet inside the right season, newest first. Months are optional: Dec to Feb is Winter, Mar to May is Spring, Jun to Aug is Summer and Sep to Nov is Fall. To start a new year, copy a whole `<details class="year">` block and change its `<summary>`:

```markdown
* September: [Paper title](https://doi.org/...) is published in a journal. Congratulations!
```

Link lab members to their pages with `https://depasquale-lab.github.io/members/<file-name>.html`.

### Add or change a research block

Blocks live in `index.md`. Each one captures text, then calls `feature.html`:

```markdown
{% capture text %}
A short description.

Relevant preprint: [_Title_](https://...) \\
Authors (year) \\
Venue
{:.center}
{% endcapture %}

{%
  include feature.html
  image="images/figure.jpg"
  caption="Short caption"
  title="Small title shown above the figure"
  text=text
%}
```

Use `title=` for the heading above a figure. The template ignores `headline=`. Members' names can be links to their pages (`members/<file-name>.html`).

### Add images and video

- Put files in `images/` or `videos/` and reference them without a leading slash from top-level pages (`images/zeno.jpg`). This works on the live site and in PR previews. Pages in subfolders, such as the Happenings page, need `../` in front.
- Keep files small. Resize photos, save figures as compressed JPEGs, and re-encode videos (for example with `ffmpeg`) rather than committing raw recordings. Git keeps every version forever.
- Only post photos, videos and details that the person is happy to have public.

## What belongs on the site

Public, confirmed information only: published papers, preprints, awards, talks and appointments that are already public. Do not post unfunded or pending grants, papers still under review, funding amounts, internal reviews or other private material.

## Previewing on your own computer (optional)

- With Docker: run `bash .docker/run.sh`, then open http://localhost:4000.
- Without Docker: install Ruby and run `bundle install` and `bundle exec jekyll serve`.

Most people can skip this and use the PR preview instead.

## Good to know

- Pages end in `.html` (for example `members/ryan-senne.html`).
- A bot sometimes pushes an "Update citations" commit to a PR branch. If a push is rejected, run `git pull --rebase` and push again.
- The workflows run on `ubuntu-24.04` on purpose, because the newer GitHub runner image does not provide the Ruby version the site uses (3.1).
- The template includes citation tooling (`_cite/`, `_data/sources.yaml`), but the publications on the Research page are written by hand in `index.md`.
- The `README.md` file itself is excluded from the website.

## Credits

Built with the [Greene Lab lab-website-template](https://github.com/greenelab/lab-website-template) (see `LICENSE.md` and `CITATION.cff`).
