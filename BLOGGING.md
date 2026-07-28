# How to publish a blog post

Posts live in `_posts/` and are written in Markdown. Publishing is just adding
one file and pushing to GitHub — GitHub Pages rebuilds the site automatically.

## 1. Create the file

Name it `YYYY-MM-DD-short-title.md` (the date and slug become the URL), e.g.:

```
_posts/2026-08-01-my-new-post.md
```

## 2. Add front matter and write

```markdown
---
title: "My New Post"
description: "One or two sentences shown in search results and previews."
date: 2026-08-01 10:00:00 +0900
categories: tech            # optional — becomes part of the URL
tags: [ai, samsung, seoul]  # optional
image: /images/my-post.jpg  # optional — social share image for this post
---

Write your post here in **Markdown**.

## Headings make sections

- Lists work
- `code` works

![Alt text for an image](/images/my-photo.jpg)
```

Layout (`post`) and author (`Ayush Patel`) are applied automatically from
`_config.yml` — you don't need to repeat them.

## 3. Preview locally (optional)

```bash
docker run --rm -v "$PWD":/site -w /site -p 4000:4000 ruby:3.3 \
  bash -c "bundle install && bundle exec jekyll serve --host 0.0.0.0"
# open http://localhost:4000
```

## 4. Publish

```bash
git add _posts/2026-08-01-my-new-post.md
git commit -s -m "Add post: My New Post"
git push
```

The post appears on `/blog/`, the homepage "Latest from the blog" section,
`feed.xml` (RSS) and `sitemap.xml` within a couple of minutes.

## Tips

- **description** is the most important SEO field — write it like a search
  snippet.
- Put images in `images/` and always include descriptive alt text.
- Drafts: keep unfinished posts in a `_drafts/` folder (no date in filename);
  they won't be published until moved to `_posts/` with a date.
