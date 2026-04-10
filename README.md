# CS 440 Reading Blog — Template

Your running reading blog for **CS 440: Advanced Networking** (Fall 2026, Northwestern).

## Setup (5 minutes)

1. **Fork this repository** (or click "Use this template" on GitHub).
2. Rename your copy to `cs440-blog` (or any name you like).
3. Go to **Settings > Pages** and set the source to `main` branch.
4. Edit `_config.yml` — change `author` to your name.
5. **Add the instructor as a collaborator:**
   Settings > Collaborators > Add `fabianeb` (or the handle provided in class).
6. Your blog will be live at `https://<your-username>.github.io/cs440-blog/`.

If you prefer to keep your repo **private**, that's fine — GitHub Pages works with
private repos on free student accounts (via [GitHub Education](https://education.github.com/)).
The instructor will still be able to read it as a collaborator.

## Writing a new post

1. Copy `TEMPLATE.md` into the `_posts/` folder.
2. Rename it using the format: `YYYY-MM-DD-short-title.md`
   (e.g., `2026-09-24-internet-invariants.md`).
3. Fill in the front matter (title, authors, venue, week number).
4. Write your critique following the section prompts.
5. Commit and push. GitHub Pages rebuilds automatically.

**Due by 9:00 PM the evening before class.**

## The Connections section

Each post includes a **Connections** section. Use it to link back to your
earlier posts when you see recurring themes, contradictions, or ideas that
build on each other. This is the most valuable part of a running blog — by
Week 9, you will have built a personal map of the research landscape.

## Structure

```
_posts/
  2026-09-24-internet-invariants.md    <- example post (included)
  2026-09-29-partial-reachability.md   <- you write these
  ...
_layouts/
  post.html                            <- post layout
_config.yml                            <- site configuration
index.md                               <- home page (auto-generated list)
TEMPLATE.md                            <- copy this for each new post
```

## Local preview (optional)

```bash
gem install bundler jekyll
bundle install
bundle exec jekyll serve
# Open http://localhost:4000
```
