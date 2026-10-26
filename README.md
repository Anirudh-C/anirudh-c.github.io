# Homepage

Personal homepage built with Jekyll and the
[no-style-please](https://github.com/riggraz/no-style-please) theme.

## Editing

- **Name and one-line description**: `title`, `author` and `description` in `_config.yml`
  (keep `author` identical to how your name appears in author lists so it gets bolded).
- **Homepage list**: `_data/menu.yml`. Each entry links to a page; `post_list` on the
  publications entry controls how many papers are previewed there.
- **Papers**: one Markdown file per paper in `publications/_posts/`, named
  `YYYY-MM-DD-short-name.md`. The front matter holds `title`, `authors`, `venue` and
  optionally `preprint`, `pdf`, `arxiv`, `code`, `note`; the body is the blog post about
  the paper. Each paper is listed on `publications.md` and gets its own page.
- **Journal papers**: `_data/journals.yml`, listed at the bottom of the publications
  page without a blog post.
- **Other pages**: `about.md` is a plain Markdown list. To add a page, copy it, change
  its `title`, and add it to `_data/menu.yml`.

## Local preview

```sh
bundle config set --local path vendor/bundle
bundle install
bundle exec jekyll serve
```

Then open http://localhost:4000.

## Deploying to GitHub Pages

1. Create a public repo named `USERNAME.github.io` on GitHub.
2. Replace `USERNAME` in `_config.yml`.
3. Push this folder to the repo's `main` branch.
4. In the repo, go to **Settings → Pages** and set *Source* to *Deploy from a branch*,
   branch `main`, folder `/ (root)`.

The site will be live at https://USERNAME.github.io after a minute or two.
