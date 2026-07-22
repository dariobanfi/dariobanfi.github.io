# dariobanfi.com

A deliberately minimal blog. Posts are hand-written HTML. GitHub Pages builds
the site with Jekyll on every push — there's nothing to install or run locally.

## Add a new post

1. Copy `_template.html` into `_posts/` and rename it with a date + slug:
    
   ```
   _posts/2026-08-01-my-post.html
   ```

   The date orders the post; the slug becomes the URL: `/posts/my-post/`.

2. Edit the header (between the `---` lines) and write the HTML body.
   Drop images in `img/` and link them: `<img src="/img/x.jpg" alt="...">`.

3. Commit and push. That's it — the home page and the post's pretty URL are

## How it fits together

- `_config.yml` — site settings + the `/posts/:title/` pretty-URL rule
- `_layouts/default.html` — the page shell (header, footer, `<head>`)
- `_layouts/post.html` — wraps a post's HTML with its title + date
- `index.html` — home page; loops over `_posts/` automatically
- `about.html` — about page (served at `/about/`)
- `_posts/` — one HTML file per post
- `style.css` — all styling; monochrome, dark-mode aware
- `_template.html` — starting point for a new post (not published)
- `img/` — images

## Preview locally (optional)

You don't need this — pushing shows it live. But if you want a local preview
you'd need Ruby + Jekyll installed, then run `jekyll serve`. Most of the time
it's easier to just push and look at the live site.
