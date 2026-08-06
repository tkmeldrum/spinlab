# spinlab website

Website for the spinlab research group at William & Mary. Built with [Hugo](https://gohugo.io) using the [Hugo Blox](https://hugoblox.com) "Research Group" theme.

## Local development

```sh
hugo server -D
```

Requires the Hugo **extended** edition (see `.github/workflows/publish.yaml` for the pinned version). Hugo Modules will fetch the theme automatically on first run.

## Content

- `content/post/` — news items, one folder per post (`YY_MM_DD_slug`)
- `content/publications/` — publications, one folder per entry
- `content/authors/` and `content/people/` — group member profiles
- `content/research/` — research area pages shown on the homepage
- `content/_index.md` — homepage layout (which sections appear, in what order)

Content can be edited directly as Markdown, or through the Decap CMS at `/admin`.

### Adding a news post

1. Copy an existing folder in `content/post/` (naming convention: `YY_MM_DD_short-slug/`) or run `hugo new post/YY_MM_DD_short-slug`.
2. Edit `index.md`'s front matter (`title`, `date`, `authors`) and write the post body below the `---`.
3. Add a `featured.jpg`/`featured.png` to the same folder for the post's thumbnail (keep it under ~1MB — Hugo will still resize it for display, but a smaller source avoids bloating the git repo and the build).
4. The homepage "Latest News" section (`content/_index.md`, `id: news`) shows the 3 most recent posts automatically; older posts are listed at `/post/`.

### Adding a publication

1. Copy `content/publications/example-publication/` to a new folder, e.g. `content/publications/2026-your-paper-slug/`, and fill in the front matter (title, authors, date, DOI, journal, links to PDF/code/etc. — see the comments in that file for the full field list).
2. Delete the `draft: true` line so the entry is no longer a template. It will publish automatically the next time the site builds.
3. The homepage Publications section (`content/_index.md`, `id: publications`) lists every non-draft entry, most recent first.

### Adding/updating a group member

1. Copy an existing folder in `content/authors/`, or run `hugo new authors/first-last/_index.md`.
2. Set `user_groups` in the front matter to control where they appear: `Principal Investigator`, `Researchers`, `Graduate Students`, `Undergraduate Students`, `Administration`, `Visitors`, or `Alumni`. A person can belong to more than one group.
3. The homepage only shows `Principal Investigator`, `Researchers`, `Graduate Students`, and `Undergraduate Students` (see the `user_groups` list under `id: people` in `content/_index.md`) — move someone to `Alumni` there to retire them from the homepage roster without deleting their profile. The full roster at `/people/` (currently served at the URL `/people/people/` — a pre-existing quirk, not something introduced recently) lists every group, including alumni.

### Editing the homepage layout

`content/_index.md` defines the homepage as an ordered list of `sections` (hero, research, publications, group photo, people, news, …). Reordering, hiding, or retitling a section is usually just a matter of editing that file — no template changes needed.

Two custom overrides support the current homepage design and aren't part of the stock theme, so don't be surprised to find them when tracing behavior:
- `layouts/partials/views/showcase.html` — a local override of the theme's research-card layout (controls image size and the left/right "hug the centerline" alignment of the alternating research blocks).
- `assets/scss/custom.scss` — site-specific CSS (navbar logo sizing, hero/showcase image sizing and alignment, the research intro's centered 50%-width paragraph).

## Deployment

The live site is built and deployed to **GitHub Pages** on every push to `main` via `.github/workflows/publish.yaml`, and served at the custom domain `meldrumlab.org` (`baseURL` in `config/_default/hugo.yaml`; the domain itself is configured in the repo's GitHub Pages settings, not in this repo's files).

There's no separate staging environment — to preview a change before it goes live, run it locally first:

```sh
hugo server -D
```

then push to `main` once it looks right. The GitHub Actions build usually finishes in a couple of minutes; check the **Actions** tab on GitHub if a change doesn't show up on the live site shortly after pushing.

`netlify.toml` is *not* the deploy path for the live site, but it is still needed: the `/admin` CMS uses Decap's `git-gateway` backend, which authenticates through **Netlify Identity** on the linked Netlify project. Don't remove the Netlify project or `netlify.toml` without first replacing the CMS auth method, or `/admin` login will break.
